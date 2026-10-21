# Deep-Stack Business Ideas: ten businesses the connected stack can run from day one

Prepared 2026-10-21 for the Owner by the AI CEO. Constraints assumed: $0–10k capital, no audience, no appetite for cold calling, a Mac mini running 24/7, and the connectors and the small-business skill pack already wired into Claude.

## How to read this

Each idea is scored 1–5 on six axes (5 is always better):

| Axis | Meaning |
|---|---|
| Capital | 5 = needs under $1k |
| Speed | 5 = first $10k month plausible inside 4 months |
| $1M prob. | 5 = ≥40% chance of a $1M revenue year within 7 years |
| AI-operable | 5 = ≥90% of recurring work runs on scheduled tasks and skills |
| Cold-selling | 5 = customers arrive inbound or through marketplaces, no outbound calling |
| Evidence | 5 = pricing and demand verified from primary or multiple independent sources |

Probability estimates are judgment calls anchored on three things: the size of the customer pool (cited), the verified price per customer (cited), and the number of customers that price implies for $1M/year, discounted for churn and the Owner's constraints. They are not survival-rate statistics.

Two stack caveats that affect several ideas and that the Owner should settle first:

1. **Twilio.** The connected Twilio connector is described as "SMS/voice search and retrieval". Sending SMS at scale may require the Twilio Messaging API via the `build-connector` skill (Zapier) or a small Agent SDK worker on the Mac mini. Any US SMS program also needs A2P 10DLC brand and campaign registration, which carriers have enforced on 100% of unregistered traffic since February 2025; fees are small ($4–4.50 brand, $15 vetting, $1.50–10/campaign/month) but approval can take 1–4 weeks and every client's program must be registered separately ([Twilio](https://pages.twilio.com/10DLC-HelpArticles-WW), [Conduit](https://conduit.ai/blog/a2p-10dlc-registration-step-by-step-for-2026)).
2. **Per-client authorization.** Every "we read the customer's QuickBooks/HubSpot/Shopify/Square" idea requires the customer to authorize access. The clean way is to run each client as a separate connector authorization (QuickBooks supports accountant/firm access to many client files; HubSpot partner access; Shopify collaborator accounts; Square OAuth). Build this once as an onboarding skill (`smb-onboard` already exists) and it becomes the moat: the competitors charge SaaS prices to give the owner a dashboard, we charge for the outcome because we act on the data.

---

## Ranked list

| Rank | Idea | Capital | Speed | $1M prob. | AI-operable | Cold-selling | Evidence | Total /30 |
|---|---|---|---|---|---|---|---|---|
| 1 | Grant Studio for sub-$1M nonprofits | 5 | 4 | 3 | 4 | 4 | 4 | 24 |
| 2 | Get-Paid: AR recovery for QuickBooks businesses | 5 | 4 | 3 | 5 | 3 | 4 | 24 |
| 3 | CFO-in-a-Box: monthly finance pulse with industry benchmarks | 5 | 3 | 3 | 4 | 3 | 4 | 22 |
| 4 | Bid Desk: SAM.gov triage and proposal writing for small contractors | 5 | 3 | 3 | 4 | 3 | 3 | 21 |
| 5 | Never-Miss-a-Lead: SMS speed-to-lead and booking for home services | 4 | 3 | 3 | 4 | 2 | 4 | 20 |
| 6 | Close Pack: white-label month-end packet for bookkeeping firms | 5 | 2 | 3 | 5 | 3 | 3 | 21 |
| 7 | Answer-Engine Visibility subscription for local and SMB brands | 5 | 3 | 2 | 4 | 4 | 3 | 21 |
| 8 | Win-Back: dormant-customer reactivation for Square/Shopify merchants | 4 | 3 | 2 | 4 | 2 | 3 | 18 |
| 9 | Illness-Signal marketing triggers (PopHIVE) | 5 | 2 | 1 | 5 | 4 | 2 | 19 |
| 10 | Template Foundry: Canva-to-Shopify digital product studio | 5 | 2 | 1 | 5 | 5 | 3 | 21 |

Ranking is by $1M probability first, then cold-selling burden and evidence quality, then total score. Ideas 6, 7 and 10 have decent totals but rank lower because their ceiling or their defensibility is weaker. Ideas 1–3 share the same inbound engine (content on HubSpot blog + landing pages, marketplace profiles, referral partners), so the recommended plan is to launch 1 and 2 together, add 3 as an upsell, and keep 10 running on autopilot as the lead magnet.

---

## 1. Grant Studio: productized grant writing for sub-$1M nonprofits

**Customer and what they pay for.** Small nonprofits (588,665 US nonprofits report under $1M revenue, roughly a third of 1.56M tax-exempt organizations per IRS-based figures compiled by [Blackbaud](https://webfiles.blackbaud.com/files/50-fascinating-philanthropy-stats/sector-impact.html)) that have no development staff. They pay for: a qualified prospect list, a go/no-go on each opportunity, a drafted and submitted proposal, and tracked deadlines and reporting obligations after award.

**Price and evidence.** Foundation proposals $1,500–5,000 each; federal applications $5,000–15,000+; retainers $2,000–6,000/month for 1–3 proposals plus strategy ([Grantable rate guide 2026](https://grantable.co/how-much-does-a-grant-writer-cost), [Funding for Good](https://fundingforgood.org/how-to-determine-grant-writing-fees/), [goLance rate guide](https://golance.com/hiring/best-freelance-grant-writers-hourly-rate)). Software-only comparables: Instrumentl at $299–999/month billed annually ([aitoolsbakery, read from instrumentl.com Aug 2026](https://aitoolsbakery.com/?p=16274)). Proposed pricing: **$1,250/month retainer** (one foundation proposal per month plus prospecting and deadline tracking) or **$1,800 per proposal** à la carte. That undercuts human freelancers while charging 3–4x software, which the nonprofit accepts because we deliver the submission, not a database. Contingency/percentage fees are unethical under GPA and AFP codes, so do not offer them ([Grantable](https://grantable.co/how-much-does-a-grant-writer-cost)).

**How customers are found (inbound/marketplaces).** (a) Upwork, where grant postings draw 20–50 proposals and pay $34–60/hour, which signals steady demand ([Upwork listing](https://www.upwork.com/freelance-jobs/apply/Experienced-U.S.-Grant-Researcher-Grant-Writer-Proven-Grant-Funding-Success-Required_~022065866241620016897/)); (b) a HubSpot landing page plus blog series ("grants for [state] [cause] nonprofits under $1M", refreshed weekly by scheduled task) which doubles as AEO content; (c) a free "grant readiness score" form on Netlify that feeds HubSpot; (d) referrals from bookkeepers who serve nonprofits (overlaps with idea 6). No cold calling: the free tool and Upwork do the intake.

**Tools and skills that run it.** `grant-rfp-writer` (finds opportunities, go/no-go, drafts, tracks deadlines), `proposal-builder`, Google Drive (past submissions, program data), Google Calendar (deadline and reporting calendar), Gmail (`inbox-manager` for funder correspondence), DocuSign (one-click; board sign-offs and engagement letters), HubSpot (pipeline, landing pages, blog), Canva (one-page program summaries and budget graphics), QuickBooks (recurring invoices via `qbo_sales_create_recurring_invoice`, `invoice-chase`), scheduled tasks (weekly opportunity scan per client, daily deadline check).

**What the Owner must do personally.** 30-minute intake call per client (video, not cold), final read of every submission before it goes out, sign engagement letters, and hold the relationship when a funder calls. About 2–3 hours per client per month at steady state.

**Capital.** Under $1,000: HubSpot Starter or free, Netlify free, Canva Pro, Upwork fees. Claude usage is the main variable cost.

**Time to first $10k month.** 4–6 months. Eight retainer clients at $1,250, or a mix with per-proposal work. Upwork gives the first 2–3 clients within 60 days if the profile shows two sample proposals.

**Path to $1M in 7 years and probability.** 67 retainer clients at $1,250/month = $1.0M/year. With 588k eligible organizations that is 0.01% penetration. Churn is the problem: a nonprofit that wins drops to maintenance, one that loses twice leaves. Plan for 40% annual churn, so reaching 67 active clients needs ~45 new clients/year by year 4, which inbound plus Upwork can supply. **Probability 25–30%.** Basis: verified willingness to pay in the $1,500–5,000 band, a very large pool, and AI already doing the bulk of drafting; discounted for churn and for the reputational risk of early losses.

**Risks.** Win-rate reputation (mitigate with a hard go/no-go so you only write what you can win); AI-generated proposals becoming a commodity (Grantable and others sell the software directly), which pushes the value to prospecting, compliance and post-award tracking; nonprofit payment slowness (use `invoice-chase`).

**Scores.** Capital 5, Speed 4, $1M prob. 3, AI-operable 4, Cold-selling 4, Evidence 4.

---

## 2. Get-Paid: accounts-receivable recovery for QuickBooks businesses

**Customer and what they pay for.** US small businesses on QuickBooks Online that are owed money. Intuit's 2025 report: 56% of US small businesses are owed money on unpaid invoices, averaging **$17,500** each; 47% have invoices more than 30 days overdue; businesses with many late invoices report cash-flow problems at 50% vs 34% ([QuickBooks 2025 Late Payments Report, 2,487 US respondents](https://quickbooks.intuit.com/r/small-business-data/small-business-late-payments-report-2025/)). They pay for a polite, relentless, multi-channel chase that they do not have to run themselves: email sequences, SMS nudges, payment links, escalation drafts, and a weekly "who still owes you" summary.

**Price and evidence.** Software comparables: Chaser from $259/month flat ([Capterra](https://www.capterra.com/p/157101/CHASER/pricing/), [Software Advice](https://softwareadvice.com/debt-collection/chaser-profile/)). Outsourced AR runs 1–5% of receivables; traditional collection agencies take 25–50% of recoveries; AI success-fee platforms quote 5–15% ([Boostly](https://invoice.boostly.com/blog/accounts-receivable-outsourcing), [InsideARM](https://one-to-one-sellers.insidearm.com/news/00024207-collection-agencies-that-charge-a-flat-fe)). Proposed pricing: **$199/month flat** for the always-on chase (all invoices under 60 days) **plus 8% of anything recovered that was over 60 days when we took it on**. The flat fee is below Chaser; the success fee is well below agencies and only touches money the customer had written off.

**How customers are found.** (a) Content and AEO: "how to collect unpaid invoices", state-by-state late-fee rules, template demand letters, each page ending in a free "AR health check" (customer authorizes QuickBooks read access, we return an aging analysis in minutes; `qbo_accounting_get_ar_aging_summary` makes this a 1-minute demo); (b) Intuit's Find-a-ProAdvisor directory once the Owner passes the free ProAdvisor certification; (c) bookkeepers and fractional CFOs as referral partners (they hate chasing and do not get paid to); (d) Upwork and Fiverr "accounts receivable" gigs for the first ten clients. Cold-selling 3 because referral partners need a few warm conversations.

**Tools and skills.** QuickBooks (AR aging, `qbo_sales_send_invoice_reminder`, `qbo_sales_create_payment_link`, `qbo_sales_send_payment_link`), `invoice-chase`, Gmail (sequences, `inbox-manager` for replies and disputes), Twilio (SMS nudge; see caveat 1), HubSpot (one deal per overdue invoice, saved reports), Google Calendar (promise-to-pay follow-ups), `cash-flow-snapshot` (the weekly summary), scheduled tasks (daily aging pull, cadence sends, Friday report), Canva (branded statements).

**What the Owner must do personally.** Approve escalation past "firm reminder" (legal letters, agency handoff), handle the rare angry debtor call, and do the ProAdvisor certification (about a day). Under an hour per client per month.

**Capital.** Under $1,000.

**Time to first $10k month.** 4–6 months: 35 clients at $199 plus success fees, or 25 clients if success fees average $100/month each.

**Path to $1M and probability.** 300 clients at $199 = $717k; success fees on average recovered balances ($17.5k owed per business, if we recover 30% of the >60-day slice at 8%, roughly $400/client/year) take it to ~$840k; add the CFO-in-a-Box upsell (idea 3) for the rest. **Probability 25%.** Basis: the pain is quantified by Intuit on a large sample, price points are verified in market, the service is almost entirely automatable, and the pool (millions of QBO subscribers) is enormous. Discounted because Intuit itself keeps shipping reminder and payment features and because Chaser-style tools may add AI agents.

**Risks.** Fair Debt Collection Practices Act and state collection-agency licensing: as long as we act as the business's agent on its own first-party receivables using its own name, FDCPA generally does not apply, but some states license third-party collectors; the Owner should get a one-hour legal review before taking the success fee on >60-day balances. Twilio 10DLC per client. Intuit adding native "AI chase" features.

**Scores.** Capital 5, Speed 4, $1M prob. 3, AI-operable 5, Cold-selling 3, Evidence 4.

---

## 3. CFO-in-a-Box: monthly finance pulse with industry benchmarks

**Customer and what they pay for.** Owner-run businesses with $1–5M revenue on QuickBooks who cannot justify a fractional CFO. They pay for a monthly packet: closed books narrative, 30/60/90-day cash forecast with confidence bands, industry benchmark comparison (the QuickBooks connector exposes `benchmarking_against_industry` and `industry_benchmark_widget`, which is data a human fractional CFO does not have), a lending-readiness read (`qbo_lending_get_approval_factors`, `qbo_lending_shop_loans`), and a 30-minute call.

**Price and evidence.** Fractional CFOs charge $1,500–3,000/month under $1M revenue and $2,500–5,000/month at $1–5M ([Taxstra](https://taxstra.com/resources/fractional-cfo-cost/), [Acuity](https://acuity.co/fractional-cfo/)); hourly $175–500 ([NSKT](https://nsktglobal.com/usa/blog/fractional%20cfo%20engagement%20models%20for%20every%20business%20stage)). QuickBooks Live Full-Service is $300–700/month and explicitly excludes advisory, AR/AP and forecasting ([Fit Small Business](https://fitsmallbusiness.com/quickbooks-live-bookkeeping-review/), [Beancount review](https://beancount.io/blog/2026/04/20/quickbooks-live-bookkeeping-review)). Proposed: **$750/month** for the packet and call; **$1,500/month** with AR chase (idea 2) and AP staging included.

**How customers are found.** Same inbound engine as idea 2 (free AR check and free "benchmark your business against your industry" report are strong lead magnets because the benchmark data is not freely available elsewhere), ProAdvisor directory, bookkeeper referrals (we do not do bookkeeping, so we are not a competitor to them), SBA lender and loan-broker referrals (we produce lender-ready packets).

**Tools and skills.** QuickBooks (P&L, balance sheet, AR/AP aging, benchmarking, cash-flow generator, lending tools), `close-month`, `month-end-prep`, `cash-flow-snapshot`, `business-pulse`, `report-builder`, `report-pack`, `monday-brief`, Google Drive (packet archive), Google Calendar (monthly call), Canva (packet design), HubSpot (client CRM), scheduled tasks (monthly close chain, weekly pulse).

**What the Owner must do personally.** The 30-minute monthly client call (this is where the price comes from; the AI can prepare every word but owners pay to talk to a person), and judgment on the three recommendations. The Owner does not need to be a CPA; the packet is management information, not attestation. If a client wants a credentialed signature, subcontract a fractional CFO reviewer at $175/hour for an hour per packet.

**Capital.** Under $1,000.

**Time to first $10k month.** 6–9 months (13 clients at $750). Slower than idea 2 because the ticket is higher and trust takes a cycle.

**Path to $1M and probability.** 110 clients at $750 = $990k. That is 110 monthly calls, which is 55 hours/month for the Owner, within reach. **Probability 25%.** Basis: a verified price gap between $300–700 bookkeeping and $2,500+ fractional CFO; unique benchmark data; low churn once a client depends on the packet. Discounted because Intuit is likely to productize exactly this inside QuickBooks, and because selling at $750 without credentials takes referrals.

**Risks.** Intuit shipping it natively; liability if a client acts on a forecast (use plain disclaimers and confidence bands, already in `cash-flow-snapshot`); Owner time scaling linearly with calls.

**Scores.** Capital 5, Speed 3, $1M prob. 3, AI-operable 4, Cold-selling 3, Evidence 4.

---

## 4. Bid Desk: SAM.gov triage and proposal writing for small government contractors

**Customer and what they pay for.** Small businesses with a set-aside status (SDVOSB, WOSB, 8(a), HUBZone) or simply "small" who cannot read 24,000 notices a month. SAM.gov carries 261,000+ active solicitations and roughly 60% of opportunities carry a small-business set-aside designation ([Gov Contract Finder, Feb 2026](https://govcontractfinder.com/small-business-contracting/compete-small-business-set-asides-fy2026)); FY2026 set-aside obligations were $11.42B across 155,756 contracts through May ([GovChime](https://www.govchime.com/analytics/set-aside/SBA)). They pay for (a) a daily filtered feed with a go/no-go per solicitation, and (b) a compliant, drafted response when they bid.

**Price and evidence.** Government/federal proposal writing commands $3,000–10,000 per submission ([Funding for Good](https://fundingforgood.org/how-to-determine-grant-writing-fees/), [Grantable](https://grantable.co/how-much-does-a-grant-writer-cost)); firms sell full bid management with a writer and a compliance reviewer ([The Bid Lab](https://thebidlab.com/rfp/), [RFP Writer](https://www.parse.gl/brands/rfpwriter-net)). Published per-response prices are scarce (searches found none), so evidence is 3. Proposed: **$400/month** for the triage feed and go/no-go memos, **$3,500 per response** for simplified acquisitions and $7,500 for full technical volumes.

**How customers are found.** APEX Accelerator (formerly PTAC) workshops and their counselor referrals, GovCon LinkedIn and Reddit communities, SBA district office events, Upwork and Contra (RFP writers list there with free consults: [Contra](https://contra.com/community/0LdvxESI-48-72-hour-rfp-proposal-expertise-book)), inbound content ("set-aside opportunities for [NAICS] this week" pages refreshed daily by scheduled task).

**Tools and skills.** `grant-rfp-writer` (explicitly filters SAM.gov and DIBBS feeds), `proposal-builder`, `contract-review` (reading the solicitation terms), Google Drive (past performance library), Calendar (Q&A and due dates), DocuSign (reps and certs), HubSpot (bid pipeline), Canva (graphics and cover pages), Claude in Chrome (SAM.gov portal actions that have no API), scheduled tasks (daily feed per client NAICS set).

**What the Owner must do personally.** Register the company in SAM.gov, sit on the go/no-go call for big bids, and never submit without the client's sign-off. Pricing volumes stay with the client.

**Capital.** Under $1,000.

**Time to first $10k month.** 5–8 months: 10 triage subscribers plus 2 responses a month.

**Path to $1M and probability.** 40 triage clients ($192k) plus 110 responses a year at an average $5,000 ($550k) plus a few retained "capture" clients at $2,500/month ($300k). **Probability 20%.** Basis: high ticket and a clearly underserved pool; discounted because win rates drive referrals, procurement cycles are long, and the Owner will need a credible GovCon reviewer early.

**Risks.** Federal budget and shutdown cycles; FAR compliance mistakes; competitors (Loopio, Responsive, GovTribe, SamSearch) adding AI drafting, which pushes value to capture strategy and compliance.

**Scores.** Capital 5, Speed 3, $1M prob. 3, AI-operable 4, Cold-selling 3, Evidence 3.

---

## 5. Never-Miss-a-Lead: SMS speed-to-lead and booking for home-service businesses

**Customer and what they pay for.** HVAC, plumbing, roofing, cleaning, landscaping, med-spa and dental practices that lose leads because nobody answers. Only 3% of marketers respond to a lead within 5 minutes and 59% respond late or inconsistently (Feb 2026 survey of 500 marketers, via [Regie.ai](https://regie.ai/blog/10-speed-to-lead-statistics-that-boost-sales-performance)); the HBR finding that contact within an hour is 7x more likely to reach the decision maker is widely cited ([Calldrip](https://calldrip.com/blog/speed-to-lead-statistics)). They pay for: every web form, missed call and marketplace inquiry answered by text inside 60 seconds, qualified, booked onto the calendar, logged in the CRM, and reminded.

**Price and evidence.** Podium lists $399/month Core and $599/month Pro on annual contracts ([PricingSaaS](https://pricingsaas.com/companies/podium), [CostBench](https://costbench.com/software/review-management/podium/)); Birdeye runs $299–449 per location per month plus $500–1,500 onboarding ([CostBench](https://costbench.com/software/review-management/birdeye)). Proposed: **$297/month per location**, month-to-month, no onboarding fee, with a 14-day "we answer your leads, you watch" trial.

**How customers are found.** Cold-selling burden is the highest in this list (2). Inbound options: a missed-call demo page ("text this number, see what your customers would see"), Thumbtack/Angi/Nextdoor contractor communities, HubSpot Solutions Directory listing ([HubSpot KB](https://knowledge.hubspot.com/marketplace/use-the-hubspot-solutions-directory)), partnerships with local lead-gen agencies who need a fulfillment partner, and referrals from the first three clients (home-service owners talk to each other at supply houses).

**Tools and skills.** Twilio (inbound SMS/voice capture; outbound send via build-connector if needed), `speed-to-lead`, `lead-triage`, `call-list`, Google Calendar (`suggest_time`, `create_event`), HubSpot (contact and deal creation, `crm-autopilot`), Gmail (form notifications), `review-reputation` (post-job review request by SMS), `reactivate` (seasonal win-back), Supermetrics (ad-source attribution), scheduled tasks (minute-level poll of inboxes and Twilio, nightly no-show re-engagement).

**What the Owner must do personally.** 10DLC registration per client, a 20-minute onboarding call, and setting the escalation rules (what the AI may promise, what it must hand to the client). After that, nothing per lead.

**Capital.** $1,000–2,500 (Twilio numbers and messaging, a Zapier plan if the send path needs it).

**Time to first $10k month.** 5–8 months: 34 locations at $297.

**Path to $1M and probability.** 280 locations at $297 = $1.0M. **Probability 20%.** Basis: a huge pool and prices verified at $300–600/month with vendors who are far less capable than an agent that actually books the job; discounted for the outbound burden, Podium/Birdeye/Hatch moving to AI agents, and the per-client messaging compliance load.

**Risks.** TCPA and state mini-TCPA exposure if consent is sloppy (require web-form consent language, honor STOP); carrier filtering; the Owner's dislike of selling makes this the slowest to start unless an agency partner fills the funnel.

**Scores.** Capital 4, Speed 3, $1M prob. 3, AI-operable 4, Cold-selling 2, Evidence 4.

---

## 6. Close Pack: white-label month-end packet for bookkeeping firms

**Customer and what they pay for.** Bookkeeping and small accounting firms (IBISWorld counts about 324,000 US payroll and bookkeeping businesses in 2025, [IBISWorld](https://www.ibisworld.com/united-states/number-of-businesses/payroll-bookkeeping-services/1397)). They pay per client-file per month for a packet they can forward under their own brand: reconciliation flags, P&L narrative, cash forecast and benchmark page, produced the morning after they close. The firm keeps the client relationship; we are invisible infrastructure.

**Price and evidence.** Keeper (now Double) charges firms $10/$25/$50 per connected client per month ([yespress directory](https://yespress.io/products/keeper.md)); Intuit's Books Close add-on is $8 per client per month after beta ([Beancount guide](https://beancount.io/blog/2026/10/10/quickbooks-books-close-pricing-small-bookkeeping-practice-guide)). Those tools give checklists; we deliver finished narrative and forecast. Proposed: **$35 per client-file per month**, minimum 10 files. Evidence 3 because the per-file price is anchored on software, not on a service comparable.

**How customers are found.** ProAdvisor Facebook groups and forums, Intuit Connect and Scaling New Heights conference rooms (the Owner attends one, which is not cold calling), a free "close packet for your hardest client" offer via a Netlify form, Upwork postings for "bookkeeping overflow", and referral from ideas 2 and 3 clients' bookkeepers.

**Tools and skills.** QuickBooks (accountant access to each client file), `close-month`, `month-end-prep`, `cash-flow-snapshot`, `report-builder`, `report-pack`, `brand-style` (apply each firm's brand to the packet), Canva (brand templates), Google Drive (delivery folder per firm), scheduled tasks (run on the firm's close date), Slack (firm channel for exceptions).

**What the Owner must do personally.** Demo calls with firm owners (30 minutes each), a quarterly check-in. Almost no per-packet work.

**Capital.** Under $1,000.

**Time to first $10k month.** 8–12 months (about 290 client-files across 15–20 firms). Slow because each firm starts with a handful of files.

**Path to $1M and probability.** 2,400 files at $35 = $1.0M, i.e. roughly 80 firms averaging 30 files. **Probability 20%.** Basis: a known buyer who already pays per-client software fees and is short of staff; discounted because Keeper/Double and Intuit will add narrative and forecast features and because per-file pricing invites comparison.

**Risks.** Platform risk (Intuit), data-access terms for third-party processors, firms worrying about a competitor reading their clients' books (mitigate with a contract: we never contact end clients).

**Scores.** Capital 5, Speed 2, $1M prob. 3, AI-operable 5, Cold-selling 3, Evidence 3.

---

## 7. Answer-Engine Visibility subscription for local and SMB brands

**Customer and what they pay for.** SMBs and local brands that want to appear in ChatGPT, Gemini, Perplexity and Google AI answers. AI referral traffic is small but growing fast: ChatGPT referrals rose ~206% year over year and the number of domains receiving ChatGPT referrals rose from 71k to up to 260k ([SE Ranking summary of Semrush/Datos](https://seranking.com/blog/ai-traffic-research-study/)); AI referrals are 0.1–2.8% of traffic depending on industry ([Rise at Seven](https://riseatseven.com/blog/aeo-ai-search-statistics/)). They pay for a monthly prompt-tracking report, a prioritized fix list, and the content and page changes made for them.

**Price and evidence.** Tools: Otterly $29, Peec $95–495, AthenaHQ ~$295, Profound Growth $399 (the self-serve tiers may have been pulled) ([UD.hk pricing roundup](https://ud.hk/en/blogs/insight/article/ai-visibility-tool-pricing-2026-09-14), [Rework comparison](https://resources.rework.com/tools/aeo-ai-visibility/profound-vs-peec-ai)). Proposed: **$349/month** done-for-you (tracking plus 4 content/page changes a month), **$149/month** report-only.

**How customers are found.** The service is its own proof: the Owner's own site must rank in AI answers for "AI visibility service for [industry]". HubSpot's AEO tools (`get_aeo_metrics`, `manage_aeo_prompts`, `manage_aeo_recommendations`) make a free "see what ChatGPT says about your business" report a 5-minute lead magnet. HubSpot Solutions Directory listing. Cold-selling 4.

**Tools and skills.** HubSpot AEO tools, blog, landing and website pages, `seo-ai-visibility`, `content-strategy`, `social-content-engine`, Canva, Netlify (client microsites), Supermetrics (Google Search Console and GA4 dashboards), Ahrefs (one-click), scheduled tasks (weekly prompt runs and monthly report).

**What the Owner must do personally.** Approve content calendars; nothing else recurring.

**Capital.** Under $1,000 (tool subscriptions if HubSpot's AEO data proves thin).

**Time to first $10k month.** 5–7 months (29 clients at $349).

**Path to $1M and probability.** 240 clients at $349. **Probability 15%.** Basis: fast-growing demand and verified $95–499 price points; heavily discounted because the category is young, tool prices are falling, and proving ROI is hard when AI referrals are under 1% of traffic.

**Risks.** Commoditization; "AEO" becoming a feature of every SEO tool; HubSpot's AEO tools requiring paid tiers.

**Scores.** Capital 5, Speed 3, $1M prob. 2, AI-operable 4, Cold-selling 4, Evidence 3.

---

## 8. Win-Back: dormant-customer reactivation for Square and Shopify merchants on performance pricing

**Customer and what they pay for.** Square and Shopify merchants with a customer list and no marketing staff. Over 4.5 million sellers used Square in 2025 ([Block FY2025 10-K](https://www.sec.gov/Archives/edgar/data/1512673/000162828026012254/xyz-20251231.htm)). They pay for monthly reactivation campaigns to customers who have not bought in 60–180 days: segment, offer, send by SMS and email, track redemption with a unique discount code, report revenue recovered.

**Price and evidence.** SMS marketing ROI claims range from $21–41 per $1 (Sakari) to $71 per $1 (Attentive via Forbes); automated flows are 7.6% of sends but 45% of SMS revenue ([Sakari](https://sakari.io/blog/sms-marketing-statistics-data-backed-insights-for-2025-2026), [Revenue Memo](https://www.revenuememo.com/p/sms-marketing-statistics)). These are vendor figures, so evidence is 3. Proposed: **$99/month plus 10% of revenue redeemed on our codes**; flat **$249/month** alternative for merchants who dislike percentages.

**How customers are found.** Square and Shopify merchant communities, local chamber and Main Street programs, a "how many of your customers went quiet?" calculator (merchant connects Square read-only; `list-customers`/`list-orders` answer in seconds), referrals from POS resellers. Cold-selling 2: most merchants still need a conversation.

**Tools and skills.** Square (customers, orders, catalog, discounts), Shopify (`list-customers`, `list-orders`, `create-discount`, `run-analytics-query`), `reactivate`, `social-content-engine`, Canva (offer creatives), Twilio (SMS; caveat 1), HubSpot or Mailchimp/Klaviyo (email), Supermetrics (attribution), scheduled tasks (monthly segment refresh and send).

**What the Owner must do personally.** Approve each month's offer (margin guardrails), 10DLC per merchant.

**Capital.** $1,000–2,500.

**Time to first $10k month.** 5–8 months (40 merchants at $99 plus performance fees).

**Path to $1M and probability.** 330 merchants at an average $250/month blended. **Probability 15%.** Basis: a giant pool and strong channel economics; discounted for Square Marketing, Shopify Email and Klaviyo doing this natively and for the outbound burden.

**Risks.** Attribution disputes on the percentage; SMS consent (reactivation of old lists is exactly where TCPA claims come from, so email-first with SMS only for opted-in contacts).

**Scores.** Capital 4, Speed 3, $1M prob. 2, AI-operable 4, Cold-selling 2, Evidence 3.

---

## 9. Illness-Signal: PopHIVE-driven marketing triggers for health-adjacent local businesses

**Customer and what they pay for.** Independent pharmacies, urgent cares, pediatric practices, HVAC and indoor-air-quality installers, cleaning companies and daycare operators whose demand moves with RSV, flu and COVID. They pay for a county-level weekly signal and for campaigns that fire automatically when a threshold is crossed ("RSV ED visits in your county up 40% in two weeks: here is this week's post, email and ad budget suggestion").

**Price and evidence.** Precedent: Kinsa sold illness-driven demand forecasts to pharmacy chains and symptom-relief brands and claimed 12–20 week city-level flu forecasts ([MIT News](https://news.mit.edu/2020/kinsa-health-0821), [Kinsa Insights release](https://business.dptribune.com/dptribune/news/read/42823054/kinsa_insights_announces_new_a.i.)); the CDC has long noted OTC sales as an early community-illness indicator ([CDC MMWR](https://www.cdc.gov/Mmwr/preview/mmwrhtml/su5301a47.htm)). No published SMB-tier price exists, so evidence is 2. Proposed: **$79/month** signal-only, **$199/month** with campaign execution; a free weekly county illness email as the lead magnet.

**How customers are found.** Entirely inbound: the free weekly county newsletter (SEO/AEO content generated by scheduled task from PopHIVE), pharmacy and urgent-care association newsletters, HVAC forums during allergy and flu seasons.

**Tools and skills.** PopHIVE (`get_trend`, `get_map`, `compare`, `get_data`), HubSpot (segments, campaigns, blog), Canva (creatives), `social-content-engine`, `canva-creator`, `ad-manager`, Supermetrics (results), Netlify (public county pages), scheduled tasks (weekly pull, threshold check, campaign fire).

**What the Owner must do personally.** Nothing recurring; a disclaimer review with a lawyer (the data is public and aggregate, and we are not giving medical advice).

**Capital.** Under $500.

**Time to first $10k month.** 9–14 months.

**Path to $1M and probability.** 420 subscribers at a $199 blend, or a data-licensing deal with a CPG or pharmacy chain (the Kinsa route). **Probability 10%.** Basis: the underlying data is free and public, so the moat is activation and audience; small-business willingness to pay for a signal is unproven.

**Risks.** Seasonality (revenue concentrates in October–March), PopHIVE data lag or coverage changes, perception of profiting from illness (keep the tone public-health, not fear).

**Scores.** Capital 5, Speed 2, $1M prob. 1, AI-operable 5, Cold-selling 4, Evidence 2.

---

## 10. Template Foundry: Canva-to-Shopify digital product studio (and the lead magnet for everything above)

**Customer and what they pay for.** Small-business owners and nonprofits buying ready-made operating documents: contractor estimate and change-order packs, grant-ready document kits (budget templates, logic models, board resolutions), bookkeeping-client onboarding kits, late-payment letter sets, AI-adoption playbooks by occupation (sourced from the Anthropic Economic Index on which tasks conversations are matched to, cited to https://www.anthropic.com/economic-index). Sold on Shopify (native free Digital Products app, [Shopify App Store](https://apps.shopify.com/delivery)) and mirrored on Etsy via Claude in Chrome.

**Price and evidence.** Etsy digital-download shops: $50–200/month new, $500–5,000+/month established; top 10% of digital sellers £8,000–30,000/month; margins 90–95%; 4.5M digital listings so planners and wall art are saturated ([Biztoolkit](https://www.biztoolkit.co/post/how-much-do-etsy-sellers-make-in-2026-average-revenue-by-category), [ListifyAI](https://www.listifyai.net/blog/how-much-do-etsy-sellers-make-2026)); printable planners average ~$4.93 ([LitCommerce](https://litcommerce.com/blog/?p=34874)). Canva Creators royalties are small and the template program is in beta ([Krea](https://www.krea.ai/blog/can-you-make-money-with-canva-creators-program-and-etsy-templates-in-2026)). Proposed: packs at **$19–49**, bundles **$97–197**; business documents, not planners, to avoid the saturated categories.

**How customers are found.** Etsy and Pinterest search, the Owner's own blog and AEO pages, and as the free or paid "tripwire" at the bottom of every lead magnet in ideas 1–8. Cold-selling 5.

**Tools and skills.** Canva (`generate-design`, brand templates, `export-design`), Shopify (`create-digital-product`, `upload-digital-product-file`, `create-collection`, `create-discount`, `run-analytics-query`, `generate-business-names`, `generate-domain-names`), Netlify (landing pages), HubSpot (email list), `content-strategy`, `social-content-engine`, scheduled tasks (weekly new product, monthly pricing review), Anthropic Economic Index (content source).

**What the Owner must do personally.** Approve the first five products and the brand. Then nothing.

**Capital.** Under $500 (Shopify Basic, Canva Pro).

**Time to first $10k month.** 12–24 months, and only with a catalog of 150+ products and an email list.

**Path to $1M and probability.** $1M/year from digital templates alone is top-0.1% territory. **Probability 5%.** Its real job is to feed ideas 1–3 with buyers who already paid us something.

**Risks.** Saturation and AI-generated competition; Etsy policy on AI content; refund and IP disputes.

**Scores.** Capital 5, Speed 2, $1M prob. 1, AI-operable 5, Cold-selling 5, Evidence 3.

---

## Five tools or connectors not yet connected that unlock the most value

1. **Twilio Messaging send path (Twilio Messaging API via `build-connector`/Zapier, or a small Agent SDK worker on the Mac mini) plus a Campaign Registry account.** The current Twilio connector is search and retrieval. Without an outbound send and per-client 10DLC registration, ideas 2, 5 and 8 cannot deliver the SMS leg that justifies their price ([Twilio 10DLC overview](https://pages.twilio.com/10DLC-HelpArticles-WW)).
2. **DocuSign (one click).** Engagement letters, grant board sign-offs, reps and certs, and client authorization forms for QuickBooks/Square access. Ideas 1, 3, 4 and 6 all stall at "please sign this" without it; `contract-review`, `grant-rfp-writer` and `hiring-screener` already call for it.
3. **SAM.gov Opportunities API, Grants.gov and Candid/Foundation Directory feeds (via `build-connector`).** Idea 1 and idea 4 are only as good as their opportunity feed. SAM.gov's API is free and filters by set-aside code and NAICS; Grants.gov is free; Candid's directory is the standard foundation prospect source. Wiring them turns `grant-rfp-writer` from "paste in a URL" into a daily scheduled triage.
4. **Stripe (or Square subscriptions used as our own billing).** Every idea is a recurring subscription or a success fee; QuickBooks recurring invoices work but card-on-file, metered success fees and dunning are what keep churn low. Square is connected and can do subscriptions and invoices, so this may be a configuration task rather than a new connector, but a Stripe connector would also unlock Stripe-based merchants for idea 8.
5. **Ahrefs (one click) and Google Search Console/GA4 through Supermetrics (already connected, needs authorization).** The inbound engine for ideas 1, 2, 3, 7 and 10 depends on content that ranks in both Google and AI answers. Ahrefs gives keyword demand and competitor gaps; Search Console gives the proof. Without them the `seo-ai-visibility` and `content-strategy` skills are guessing.

Honorable mentions: **Zapier via `build-connector` to Jobber/Housecall Pro/ServiceTitan** (idea 5 lives inside those tools, not HubSpot); **Google Business Profile API** (reviews and messaging for ideas 5 and 7); **Gusto** (only if payroll services are added to idea 3); **Mailchimp or Klaviyo** (email volume beyond HubSpot free limits for idea 8).

---

## Recommended sequencing

1. **Month 0–1:** Fix the Twilio send path and billing (Square subscriptions). Ship the free lead magnets: AR health check (idea 2), benchmark report (idea 3), grant readiness score (idea 1). Open Upwork profiles for grant writing and AR. Start Template Foundry (idea 10) on autopilot as the tripwire.
2. **Month 1–6:** Sell ideas 1 and 2. Target 8 grant retainers and 35 AR clients. Begin ProAdvisor certification.
3. **Month 6–12:** Upsell AR clients to CFO-in-a-Box (idea 3). Pilot Close Pack (idea 6) with the two bookkeepers who referred the most AR clients. Pilot Bid Desk (idea 4) with one contractor who arrives through content.
4. **Year 2+:** Decide between the finance stack (2, 3, 6) and the proposal stack (1, 4) as the core; keep the other as a product line. Ideas 5, 7, 8 and 9 are options to exercise only if an inbound channel proves itself.

## Evidence quality notes

Pricing for Chaser, Podium, Birdeye, Instrumentl, Keeper/Double, Peec and Profound comes from third-party pricing trackers and comparison sites, which is the normal state for vendors that gate pricing behind sales calls; the figures agreed across at least two sources in each case. The strongest primary sources used are Intuit's 2025 Late Payments Report (n=2,487 US), Block's FY2025 10-K, IBISWorld's business count, and IRS-derived nonprofit counts via Blackbaud. Speed-to-lead and SMS ROI statistics are vendor-circulated and dated; they are used for direction, not magnitude. No published per-response price was found for government proposal writing, so idea 4's pricing is inferred from grant-writer federal rates and should be validated with three quotes.
