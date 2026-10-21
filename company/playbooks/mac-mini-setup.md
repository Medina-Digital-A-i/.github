# Playbook: Mac mini as the Always-On Worker

Goal: the Mac mini runs the CEO on a schedule, reads and writes the same repo memory as the cloud,
and never needs a human at the keyboard. Owner: Builder. Steps the Owner performs once.

## 1. Install
```bash
# Claude Code
curl -fsSL https://claude.ai/install.sh | bash
claude --version
claude            # run once, then /login with the claude.ai account that owns the company

# Git and the repo
mkdir -p ~/medina && cd ~/medina
git clone git@github.com:medina-digital-a-i/.github.git company && cd company
```
Set up a GitHub SSH key or token on the Mac so `git push` works unattended.

## 2. Keep the Mac awake and headless
- System Settings > Energy: prevent sleep when the display is off, start up after a power failure.
- Enable Screen Sharing or SSH so you can reach it from a MacBook.
- `sudo pmset -a sleep 0 disksleep 0`

## 3. The daily run script
Save as `~/medina/run-brief.sh` and `chmod +x` it:
```bash
#!/bin/zsh
set -e
cd ~/medina/company
git pull --rebase origin main
claude -p "Run /brief. Then have the Chief of Staff update company/memory/state.md and commit with message 'brief $(date +%F)'." \
  --permission-mode acceptEdits \
  --permission-prompts none \
  --max-budget-usd 3 \
  --output-format text >> ~/medina/logs/brief-$(date +%F).log 2>&1
git push origin main || true
```
Create `~/medina/logs` first. `--max-budget-usd` is the cost ceiling per run. Start low.

## 4. Schedule it with launchd
Save as `~/Library/LaunchAgents/ai.medina.brief.plist`:
```xml
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version="1.0"><dict>
  <key>Label</key><string>ai.medina.brief</string>
  <key>ProgramArguments</key><array><string>/Users/YOURNAME/medina/run-brief.sh</string></array>
  <key>StartCalendarInterval</key><dict><key>Hour</key><integer>7</integer><key>Minute</key><integer>0</integer></dict>
  <key>StandardOutPath</key><string>/Users/YOURNAME/medina/logs/launchd.out</string>
  <key>StandardErrorPath</key><string>/Users/YOURNAME/medina/logs/launchd.err</string>
  <key>EnvironmentVariables</key><dict><key>PATH</key><string>/usr/local/bin:/opt/homebrew/bin:/usr/bin:/bin</string></dict>
</dict></plist>
```
Then: `launchctl load ~/Library/LaunchAgents/ai.medina.brief.plist`. Test with
`launchctl start ai.medina.brief` and read the log.

Add a second plist for `/weekly` on Sunday 20:00 and a third for `/upgrade` on Saturday 10:00.

## 5. Alternative with zero Mac upkeep
Cloud scheduled tasks at claude.ai/code/routines run the same `/brief`, `/weekly` and `/upgrade`
in the cloud, with connectors, on paid plans, minimum hourly. Output lands on a `claude/` branch
and needs the merge step in `memory-sync.md`. Use this if the Mac is unreliable, or use both.

## 6. Local models (optional, later)
Install Ollama or LM Studio and pull a small open model for cheap bulk jobs (classification,
first-pass drafts, summarizing scraped pages). The Scout keeps the recommended model in
`company/playbooks/multi-model-stack.md`. Claude stays the brain.

## 7. Safety
- The script has a dollar cap per run and a log. Read the log weekly.
- The Mac never holds customer payment data. Secrets live in the macOS Keychain or env vars.
- If a run misbehaves: `launchctl unload` the plist. That is the kill switch.
