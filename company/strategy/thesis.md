# Thesis — What Medina Digital AI Is Building and Why

_Drafted 2026-10-21 by the CEO. Status: awaiting Owner sign-off. Evidence:
`company/research/research-business-models.md` (70+ sources)._

## The one-paragraph version

We sell a result to small local businesses that lose money every day from missed calls and slow
follow-up: **every call answered, every lead followed up in under 60 seconds, more reviews.** We
deliver it with an AI stack the agent team runs, we charge a monthly retainer, and we put the
profit into index funds while we turn the delivery system into software we can sell. That is the
road from zero to seven figures. It is not fast. It is real.

## Why not trading

The org profile said "autonomous trading." The evidence says no:

| Study | Finding |
|-------|---------|
| Chague et al., all 19,646 Brazilian futures day traders 2013-15 | 97% of those who persisted 300+ days lost money; about 1% earned more than minimum wage |
| Barber, Lee, Liu, Odean, full Taiwan exchange data 1992-2006 | Under 1% predictably profitable; over 75% quit within two years |
| ESMA retail CFD disclosures | 74-89% of retail accounts lose |
| Alpha Arena live LLM trading, Oct-Nov 2025 | 4 of 6 frontier models lost money; one lost over 60% |
| "The Alpha Illusion," arXiv May 2026 | Reported LLM-agent alpha collapses after costs; underperforms buy-and-hold |

With $0-5k of capital, even a real edge cannot compound to $1M on any sane timeline. The Owner
reviewed this evidence on 2026-10-21 and removed trading from the company entirely. Surplus cash
goes to the index-fund waterfall. This section stays as the record of why.

## The business: the "Never Miss a Lead" stack

**Customer:** one vertical, chosen in week 1. Home services (HVAC, plumbing, roofing, electrical)
or dental/med-spa. High-value phone leads, documented missed-call pain (CallRail: 14% missed-call
rate in home services; Invoca: only 52% of calls answered by a person), owners reachable by phone.

**Offer:** three tiers, sold as outcomes, not as "an AI receptionist."

| Tier | Price | What they get |
|------|-------|---------------|
| Starter | $497/mo | AI phone and SMS answering, missed-call text-back, booking link |
| Core | $1,497/mo | Starter + CRM follow-up sequences, review requests, monthly report |
| Pro | $2,997/mo | Core + reactivation campaigns, AI-search visibility (GEO, schema, listings), quarterly strategy call |

Setup fee $500-1,500, waived for the first three founding clients in exchange for a case study.

**Wedge:** a free missed-call audit. The agents call the business five times at different hours,
log the answer rate, and produce a one-page "you missed X of 5 calls and here is what that costs"
report. Free to the first 20 prospects. This is the conversation starter.

**Delivery:** per-minute voice platform (Retell, Vapi or Twilio) plus Claude agents and n8n on the
Mac mini for routing, CRM updates, monitoring and reporting. The agents run roughly 80% of
delivery. The Owner sells, scopes, and handles escalations.

**Economics:** near-zero capital (under $200 to start, $300-1,200 over 90 days). Gross margin
70-90%. Solo ceiling $20-40k MRR before support capacity breaks.

## Why this one

1. Fastest documented time to first dollar of any model studied (weeks).
2. The agent team can run most of the work. The human does the part only a human can do: trust.
3. It generates the case studies, process knowledge and client base that become the software.
4. Every survivor in the research describes this exact shape: specialized, productized, recurring.
   Every failure describes the opposite: generic automation projects for sub-$2k budgets.

## The ladder: how services become an asset

- **Rung 1 (months 0-12):** retainers. Target $10k MRR by month 6-12.
- **Rung 2 (months 9-24):** when 5-10 clients share the same workflow, package it as vertical
  software at $199-497/mo self-serve, with the retainer clients as design partners. Sub-$1M ARR
  software sells at roughly 2.5-4x revenue. A $300-400k ARR tool is a plausible $1M exit.
- **Rung 3 (from day 1, pays off in 6-18 months):** build in public. Real numbers, what broke, the
  agent pipeline. One platform (LinkedIn for SMB buyers), 3-5 posts a week, a weekly email. Later
  a $99-499 product on how a one-person AI service business runs, only once there is proof.

## Base rates we are planning around

- Median solo founder earns about $3k/month. 70% of micro-SaaS never pass $1k MRR.
- Practitioner consensus: 1-2 retainers in the low four figures within a few months of daily
  outbound. $10k MRR is a 6-12 month outcome for most, not 90 days.
- Half of inbound "AI agency" leads have budgets under $2k. We filter them out with the tiers.

## The money math to $1M

Business cash flow, saved and invested, is the engine. At $15k MRR and 80% margin the business
throws off about $144k a year pre-tax. At $30k MRR, about $288k. Saved at a high rate and
invested in index funds, that is a 5-8 year road to $1M net worth on the service alone, shorter
if the software rung lands. The full wealth playbook is in `company/wealth/wealth-os.md`.

## Kill criteria

If there is fewer than one paying client after 60 days of at least 15 daily touches, the problem
is the vertical or the offer, not the technology. Switch vertical before switching tools. If the
Owner cannot or will not do daily outbound, we redesign the offer around inbound and content, and
accept a slower clock.

## What would change this thesis

- The Owner already has a large engaged audience: start with software and digital products.
- The Owner has deep insider knowledge of one vertical's software: go straight to vertical SaaS
  with pre-sold design partners.
