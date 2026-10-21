# AI-Leveraged Business Models for a Solo Founder With an Agent Team: What Actually Makes Money (October 2026)

**Profile assessed:** one human, no employees, a small team of AI agents (Claude/ChatGPT/other models), ~$0–5k capital, Mac mini + MacBooks. Goal: $1M net worth. Current org profile says "autonomous trading."

**Method:** ~35 web searches (standard + extended) and primary-source fetches between 21 Oct 2026 and the writing of this document. Where a number comes from a vendor blog, a self-reported X post, or an aggregator, it is labelled as such. Where I could reach a primary source (academic paper, platform report, verified-revenue page), I cite it directly. Overall evidence quality for this topic is **low-to-medium**: the strongest data are (a) the academic trading literature, (b) platform-published newsletter/SaaS data, and (c) Stripe-verified revenue pages. Almost everything about "AI agencies" is self-reported or sold by people selling courses.

---

## 0. Bottom line up front

1. **Autonomous trading should not be the primary revenue engine.** Every large-sample study of retail day/active trading finds that only ~1–3% of persistent participants earn meaningful money, and the newest LLM-trading literature (2025–2026) shows that reported "alpha" from LLM agents mostly disappears after costs and look-ahead contamination. Live LLM trading competitions in late 2025 lost money for 4 of 6 frontier models. With $0–5k of capital, even a genuinely positive edge cannot compound to $1M on any reasonable timeline. (Section 4.)

2. **The models actually producing documented solo revenue in 2025–2026 are, in order of evidence quality:** (i) micro-SaaS/AI products run by an audience-holding founder (Marc Lou ~$3.26M lifetime verified across 20 products; Tony Dinh's TypingMind; Levels' Photo AI), (ii) productized recurring services (DesignJoy at $1M+/yr solo; many $5k–40k MRR AI-service retainers, self-reported), (iii) courses/digital products sold to an existing audience (CodeFast $834k verified). The generic "AI automation agency" has the **fastest time to first dollar (weeks) but the worst operating economics** (scoping, maintenance, sub-$2k client budgets) according to the only honest practitioner post-mortem I found. (Section 3.)

3. **Base rates are brutal everywhere:** ~70% of micro-SaaS earn <$1k MRR; median Gumroad creator ~$72/month; ~half of paid Substacks earn <$500/yr; median solo-founder income ~$3k/month. The power law is the constant. What separates the 2–3% that cross $1M ARR is **distribution (an audience or a repeatable outbound motion) plus shipping volume**, not the AI tooling. (Section 2, 5.)

4. **Ranked recommendation for this profile** (Section 6):
   - **#1 — A niche productized AI service with recurring retainers for one SMB vertical** (speed-to-lead / missed-call capture + follow-up + review/GEO visibility for, e.g., home-services or dental), delivered mostly by agents, sold by the human. Fastest cash, ~$0 capital, 70–90% gross margin, converts into a sellable vertical SaaS later.
   - **#2 — Vertical micro-SaaS built from #1's delivery system** (the "service-to-software ladder"). Higher ceiling, sellable asset (sub-$1M-ARR SaaS trades at roughly 2.5–4x revenue on marketplaces), but slower and lower hit rate.
   - **#3 — Build-in-public audience + digital products** as the distribution engine for #1 and #2, not as the primary business.
   - Trading: at most a capped (≤10% of surplus cash) R&D side-bet with live, cost-inclusive validation; never the income plan.

5. **90-day path to first $1k–10k MRR for #1** is in Section 7. Realistic expectation, based on the practitioner consensus: 1–2 retainers ($1.5–3k/mo each) by day 60–90; $10k MRR is a 6–12 month outcome for most, not 90 days.

---

## 1. The context nobody selling you a course mentions: base rates

| Population | Finding | Source |
|---|---|---|
| Micro-SaaS (1,000+ businesses, 15 countries) | ~70% earn under $1,000 MRR; 18% in $1k–5k; ~1–2% over $50k/mo | [RockingWeb 2025 analysis](https://www.rockingweb.com.au/micro-saas-revenue-analysis-2025/) (methodology thin; combines MicroConf, YC, Stripe Atlas data) |
| Indie SaaS (MicroConf survey, ~469–700 responses) | 28% below $1k MRR; 65% have 1–10 paying customers; 50.7% solo; ~30% flat or shrinking | [MicroConf State of Independent SaaS 2024](https://microconf.com/saas-this-year); [Startups for the Rest of Us ep. 721](https://www.startupsfortherestofus.com/episodes/episode-721-7-key-takeaways-from-the-2024-state-of-independent-saas-report) |
| Stripe-verified Indie Hackers products (n≈30) | Median 8 months, mean 9 months to $1k MRR | [Indie Hackers analysis](https://www.indiehackers.com/post/it-takes-5-months-to-reach-1k-in-mrr-491742f806) |
| Solo founders (Indie Hackers data as cited by Taskade) | Median income ~$3,000/mo; ~2–3% reach $1M+ ARR | [Taskade, One-Person Companies](https://www.taskade.com/blog/one-person-companies) (vendor blog; distribution not traced to primary) |
| Gumroad creators (146k active products, estimated) | Median creator ~$72/mo; 44% of products earned $0; top 1% capture the large majority of revenue | [InsightRaider State of Gumroad 2026](https://insightraider.com/en/state-of-gumroad-2026) (third-party estimate); [profitable.app](https://profitable.app/gumroad/stats) |
| Substack writers with paid tiers | Median ~$4,000/yr; nearly 50% earned <$500 in 2025; top 10% capture 62% of payments; ~90% of newsletters never turn on paid | [bestwriting.com Substack stats](https://bestwriting.com/substack-statistics) (secondary; could not locate Substack primary) |
| beehiiv paid newsletters (platform data) | Median free-to-paid conversion 0.62%; median price $10/mo; median LTV per paid sub $83 (Community) to $230 (Investing); monthly churn 5% (Food) to 16.7% (Money) | [beehiiv, State of Paid Newsletters 2026](https://www.beehiiv.com/blog/the-state-of-paid-newsletters-2026) (primary) |
| TrustMRR marketplace listings (Stripe-verified) | Of 20 visible sale listings, 55% had <$1k revenue; median ≈ $818 | [TrustMRR](https://trustmrr.com/) |

Takeaway: **in every category the median outcome is a hobby income.** The question is not "which model has the best median" (all are poor) but "which model lets *this* profile get to the top decile fastest with the least capital and the most agent leverage."

---

## 2. Model-by-model assessment

Scoring key for the summary table: capital = cash needed to start; TTFR = typical time to first revenue; ceiling = realistic solo ceiling with evidence; defensibility; sales/trust = how much human selling and relationship trust is required; agent-runnable = share of ongoing work agents can do today.

| Model | Capital | TTFR | Solo ceiling (documented) | Defensibility | Human sales/trust needed | Agent-runnable |
|---|---|---|---|---|---|---|
| Generic AI automation agency (SMB) | ~$0–500 | 2–12 weeks | $5k–40k MRR (self-reported) | Low | High | Delivery 60–80%; sales/scoping ~0% |
| Productized AI service, one vertical (receptionist / speed-to-lead / content ops) | ~$0–1k | 2–8 weeks | $10k–100k+ MRR (DesignJoy $1M+/yr) | Low–Med (process + reputation) | High at start, medium later | 70–90% |
| GEO/AEO "get found by AI" service | ~$0–500 | 4–12 weeks | $1.5–5k/mo per SMB client (agency list prices) | Low; results hard to prove | High (and claims risk) | 80% |
| Micro-SaaS / vertical AI tool | $0–2k | 3–9 months to $1k MRR | $10k–180k MRR (Levels, Dinh, Lou) | Med (data, integrations, brand) | Low per unit, but distribution is the whole game | Build 70%+, support 50%, marketing 30% |
| Newsletter / audience business | ~$0 | 6–18 months | Most <$500/yr; top-decile $50k–500k+/yr | Med–High once built (owned list) | Medium (voice/credibility) | Research/drafting 60%; voice must stay human |
| B2B lead-gen agency | $200–1k/mo tooling | 4–8 weeks | $5k–30k MRR typical | Low; deliverability decaying | High | 60–80% |
| Consulting / fractional AI / "done-with-you" training | $0 | 2–6 weeks | $100–300/hr; $600–1,200/day; $5–30k/mo retainers | Med (personal reputation) | Very high | 30–40% |
| Digital products / courses | $0 | Days to launch, months to sell | Median ~$72/mo; CodeFast $834k lifetime (with 100k+ audience) | Low | Audience is the prerequisite | Production 60%; marketing requires a persona |
| Done-for-you agent builds (n8n/Make/Claude) | $0–200 | 2–6 weeks | $1.5–10k per project; $500–2.5k/mo retainers | Low | High | 70% |
| White-label SaaS reseller (GoHighLevel "SaaS mode") | $497/mo platform | 4–12 weeks | $199–297/client/mo; one verified-ish 64-subscriber example | Low (platform owns the product) | High | 60% |

### 2.1 AI automation / "AI agency" for local & SMB businesses

**What the evidence says**
- *Best self-reported solo datapoint:* an X thread (June 2026) claiming **$40k MRR from 14 clients** (4 × $5k, 6 × $2.5k, 4 × $1.25k), ~$750/mo opex, run with a model-routing pipeline (intake 10 min human → agent production → 15–20 min human QA). All figures unverified; the post is also partly a vendor promo for a specific model. [YouMind reproduction of @DeRonin_ thread](https://youmind.com/landing/x-viral-articles/solo-ai-agency-40k-mrr)
- *Best honest post-mortem:* Nadia Privalikhina, 10-yr developer, two years running an AI automation agency: **~half of inbound leads had budgets under $2,000**; one $500 automation netted <$10/hr; custom integration is really ongoing consulting; APIs and model deprecations silently break deployed automations; she recommends only taking $10–20k+ projects, specializing in one industry/one automation type, or moving to "done-with-you" training. [LinkedIn: "Why I think this business model is broken"](https://www.linkedin.com/pulse/what-i-learned-building-ai-automation-agency-why-nadia-privalikhina-atk0f)
- *Reddit consensus (secondhand, vendor summary):* first 1–2 retainers in the "low four figures/month" within a few months; year-one run rate "mid-four to low-five figures/month"; the most-upvoted threads are teardowns of "$30k/month" claims that turn out to be course revenue. [Ciela summary of r/AI_Agents & r/Entrepreneur](https://ciela.ai/blogs/ai-automation-agency-realistic-income-reddit)
- *Pricing receipts collected by ProvenStartups:* $999 assessments converting 50–60% to implementation; $1,200–2,000/mo retainers (5 clients → $8k MRR); $7,500 install + $500/mo "installer ladder"; $2–3k/mo per client; one agency citing 5-yr-9-mo retainers. [ProvenStartups, AI agency revenue](https://provenstartups.com/blog/ai-agencies/ai-agency-revenue)
- *Failure rate:* no credible agency-specific failure statistic exists. Enterprise proxies: S&P Global found 42% of companies abandoned most AI initiatives in 2025; Gartner forecasts >40% of agentic AI projects cancelled by 2027. [AllAble](https://www.allable.ai/blog/ai-automation-agency/); [thedataexperts](https://thedataexperts.us/writing/why-ai-projects-continue-to-fail-reality-check-2025.html)

**Assessment:** Capital ~$0. TTFR 2–12 weeks if you do outbound daily. Ceiling $20–40k MRR solo before delivery capacity breaks (the "Couplepreneurs" example hit a ceiling at $40k/mo). Defensibility low. The *generic* version fails on scoping and small budgets; the *specialized, productized, retainer* version is what every survivor describes. Agents can run most delivery and QA; **they cannot do discovery calls, scoping, or trust-building with a plumber.**

### 2.2 Productized AI services (AI receptionist, speed-to-lead, content ops)

**Pricing evidence (2026)**
- AI receptionist retail price points: $49–65/mo budget tier (Rosie, Goodcall, My AI Front Desk); $99–299/mo mainstream; $199/mo flat unlimited; Retell base $0.07/min + LLM $0.006–0.06/min. [CloudTalk](https://www.cloudtalk.io/blog/how-much-does-voice-ai-cost/); [NextPhone](https://www.getnextphone.com/blog/ai-receptionist-cost); [AgentZap](https://agentzap.ai/blog/ai-receptionist-pricing-complete-cost-guide-2025)
- Agency/done-for-you layer on top: $497–997/mo entry; voice-agent service $500–1,500/mo per client (creator pricing framework, not receipts). [AgentZap](https://agentzap.ai/blog/ai-receptionist-pricing-complete-cost-guide-2025); [ProvenStartups](https://provenstartups.com/blog/ai-agencies/ai-agency-revenue)
- Vertical retainers claimed by agency guides: home services $2–4k/mo; dental $2–5k/mo (one guide) vs $300–1,500/mo (another) — wide disagreement. [DataStaq](https://datastaqai.com/blog/ai-automation-agency-niches-small-business); [Buldrr](https://buldrr.com/7-ai-agents-businesses-are-paying-for-in-2026/)
- Vendor outcome claims (unverified): Sydney dental clinic paid $400/mo, booked 23 extra appointments in 30 days; an HVAC company handled 423 calls, booked 51 appointments worth $26k+. [Builts.ai](https://builts.ai/blog/home-services-dispatch-and-voice-ai-agent-case-study/)
- Demand signal: CallRail reports a 14% missed-call rate in home services; Invoca (July 2026) finds only 52% of calls answered by a person. The widely quoted "62% of calls go unanswered" traces to an unlocatable "411 Locals" study — do not cite it to clients. [StealthAgents roundup](https://stealthagents.com/research/home-services-missed-call-revenue-statistics-2026)
- SMB AI adoption: Intuit's 2026 report (34k+ owners) finds 77% of US SMBs use AI regularly, 43% say it increased revenue — but "use" includes free tools. [Intuit AI Impact Report 2026](https://www.intuit.com/blog/global-stories/ai-impact-report/)

**Non-AI proof that the productized model works solo:** DesignJoy (Brett Williams) — $5k/mo unlimited-design subscriptions, Trello intake, no meetings, ~$176/mo costs, reported $1.3M–2M/yr single-handed (figures from 2020–2023 secondary sources; no 2025–26 update found). [Indie Hackers](https://www.indiehackers.com/post/how-designjoy-got-from-0-to-120k-month-with-no-paid-advertising-a31375fce0); [AI Trav](https://aitrav.beehiiv.com/p/design-joy-one-man-business-earning-13-million-per-year)

**Content-ops variant:** LinkedIn ghostwriting with AI assist — consistent $2–5k/mo per executive client; one self-reported $15k/mo solo at 6–7 clients; no churn data anywhere. [ecommercefastlane](https://ecommercefastlane.com/how-chatgpt-scaled-my-ghostwriting-side-hustle/); [aibusiness.vc](https://aibusiness.vc/solo/ai-linkedin-ghostwriter)

**Assessment:** This is the strongest fit for the profile. Capital ~$0–1k (telephony + a voice platform's per-minute costs are pass-through). TTFR 2–8 weeks. Gross margin 70–90% claimed (plausible given per-minute costs; nobody publishes net). Agents can run intake, build, QA, monitoring, reporting and monthly client updates; the human sells, scopes and handles escalations. Defensibility comes from vertical process knowledge, case studies and reputation — not technology. Risk: platform vendors (Rosie, Goodcall, CloudTalk) sell direct at $49–299/mo, so the solo operator must sell *outcomes and integration* (CRM, booking, follow-up, reviews), not "an AI receptionist."

### 2.3 GEO/AEO "get found by ChatGPT" services

- List prices: WebFX $1,500–5,000/mo for small business; First Page Sage "Starter" $1,800–4,200/mo with 3-month minimum; Skill Mammoth (home services) $750/$1,500/$3,000 tiers. All from agencies selling the service; "none rests on an independent market study." [WebFX](https://www.webfx.com/blog/ai/generative-engine-optimization-cost/); [First Page Sage](https://firstpagesage.com/seo-blog/geo-aeo-pricing-statistics/); [Skill Mammoth](https://skillmammoth.com/blog/best-generative-engine-optimization-agencies)
- Reality check on demand: AI referrals are ~0.1–2.8% of website traffic depending on industry (~1% average); only 6.8% of US ChatGPT answers contain an external link (Similarweb, May 2026); referral mix swung from 25% to 60% homepage landings in three weeks after one ChatGPT update. ChatGPT's share of gen-AI visits fell from ~76% (Jun 2025) to ~53% (May 2026) as Gemini rose. **No credible local-business lead data from AI search exists.** [Similarweb AI search stats](https://aisearch.similarweb.com/blog/gen-ai-stats/); [SEJ on Similarweb](https://searchenginejournal.com/ai-search-isnt-replacing-google-its-layering-on-top-similarweb-data/583378/)
- Meanwhile AI Overviews cut top-result CTR by ~58% (1.76%→0.61%) on a 300k-keyword set — i.e., the *fear* that sells GEO is real even if GEO's measurable payoff is not. [Lishchuk playbook](https://lishchuk.com/blog/solo-founder-marketing-playbook-2026.html)

**Assessment:** Sellable as an **add-on line item** (schema, entity consistency, review velocity, citations) inside a visibility retainer; risky as a standalone promise because results are small, volatile and hard to attribute. Agents can execute nearly all of it. Expect refund/churn pressure when clients ask "how many leads came from ChatGPT?"

### 2.4 Micro-SaaS and vertical AI tools

**Verified or near-verified solo numbers**
- Marc Lou: TrustMRR founder page shows **20 startups, $3,256,469 total verified revenue, $55,767 current MRR**; ShipFast $1.3M lifetime, CodeFast $834k lifetime, DataFast ~$29k MRR, TrustMRR ~$25k MRR. 2025 revenue ~$1.03M, zero employees. [TrustMRR founder page](https://trustmrr.com/founder/marclou); [yespress profile](https://yespress.io/marc-lou.md)
- Tony Dinh: TypingMind reported at $130–160k/mo (Mar 2026, single secondary source); earlier self-reported $45k/mo across TypingMind/DevUtils/Xnapper, mostly one-time purchases. [Nomadpreneur](https://nomadpreneur.beehiiv.com/p/solo-founder-who-turned-100-into-1-500-000-no-team-no-investors); [Indie Hackers](https://www.indiehackers.com/post/my-solopreneur-story-zero-to-45k-mo-in-2-years-1b858f47af)
- Pieter Levels: Photo AI ~$105–138k MRR (self-reported, 2025–26); portfolio ~$3M+/yr; ~70 failed projects before the hits. [ppc.land](https://ppc.land/how-one-photo-ai-app-generates-132k-monthly-after-70-failed-startups/); [aiidelist](https://aiidelist.com/indie-developers/pieter-levels)
- Base44 (Maor Shlomo): sold to Wix for $80M cash after six months — but he had 8 employees by the sale, and this is a 1-in-a-million outlier, not a model. [TechCrunch](https://techcrunch.com/2025/06/18/six-month-old-solo-owned-vibe-coder-base44-sells-to-wix-for-80m-cash)
- Counter-example of inflation: the "$3.6M ARR solo" HeadshotPro claim is unsupported; Latka lists $96k (2023) and the founder says he hired a team. [Latka](https://getlatka.com/companies/headshotpro); [Unite.AI interview](https://www.unite.ai/tr/danny-postma-founder-of-headshotpro-interview-series/)

**Vertical niches:** no verified solo dental/legal/construction/real-estate tool at $10k MRR surfaced; guides claim 6–18 months to $10k MRR for focused full-time founders, 24–36 months part-time. [SoftwareSeni](https://www.softwareseni.com/solo-founder-saas-metrics-from-0-to-10k-mrr-in-6-months-with-realistic-timelines/); [editorialge](https://editorialge.com/ai-saas-niches-where-founders-hit-10k-mrr/)

**Exit value:** sub-$1M-ARR SaaS listed at roughly 2.5–4x revenue / 4–6x SDE on marketplaces (secondary summary of Acquire.com-style data; Acquire's own 2025 report not retrievable); MicroConf: 20% of bootstrapped exits happen at $1–3M ARR. [Beancount guide](https://beancount.io/blog/2026/07/11/bootstrapped-saas-valuation-multiples-2026-acquire-com-indie-founders-guide); [MicroConf](https://microconf.com/saas-this-year)

**Assessment:** Highest ceiling and the only model here that creates a **sellable asset at a revenue multiple**. But 70% never pass $1k MRR, median 8 months to $1k MRR, and every $1M+ solo example had either a large audience (Levels, Lou, Dinh) or a timing-lucky consumer AI product. Capital $0–2k. Agents can write most of the code and support; **they cannot manufacture distribution.**

### 2.5 Newsletters / audience businesses

- beehiiv primary data (above): 0.62% median free→paid; a 1,000-subscriber list at median numbers earns ~$62/month; 1,000 *paying* subs at $10 = $120k/yr; Investing newsletters monetize 3x better than Travel/Community. [beehiiv](https://www.beehiiv.com/blog/the-state-of-paid-newsletters-2026)
- Substack: median ~$4k/yr among paid-tier writers; half earn <$500. [bestwriting](https://bestwriting.com/substack-statistics)

**Assessment:** As a *primary* business: slow, median-poor, and the AI/Money verticals have the worst churn (13–17%/mo). As the **distribution layer** for a service or product: essential — every $1M+ solo founder found runs on an owned audience. Agents can research and draft; the voice and the public "operator shipping in the open" persona must be human.

### 2.6 B2B lead-gen agency

- Average cold-email reply rate ~3.4% (Woodpecker-derived), down from 6–7% two years ago; small, targeted sends (≤50) reply at 5.8% vs 2.1% for 500+; deliverability is now the binding constraint. [Lemlist](https://www.lemlist.com/blog/cold-email-response-rate); [Leadriver](https://www.leadriver.io/blog/cold-email-reply-rate-benchmarks-2026); [Martal](https://martal.ca/b2b-cold-email-statistics-lb/)
- No solo lead-gen agency revenue data found.

**Assessment:** Commoditized, decaying channel, high churn, and the AI tooling (Clay, Instantly, Apollo) that made it easy also made it crowded. Useful as a *skill* for your own acquisition, not as the product.

### 2.7 Consulting / fractional AI / "done-with-you" training

- Independent rates: $80–400/hr (cluster $100–300); $600–1,200/day; retainers $5–30k/mo; $999 "AI tools assessment" converting 50–60% into implementation. [Groovyweb](https://www.groovyweb.co/blog/ai-consulting-rates-2026); [Pertama Partners](https://www.pertamapartners.com/insights/ai-consulting-pricing-guide); [ProvenStartups](https://provenstartups.com/blog/ai-agencies/ai-agency-revenue)
- Demand signal: Upwork 2026 In-Demand Skills: AI-related earnings up 109% YoY; AI integration +178%; AI chatbot dev +71%; "fix the AI output" work +70%. Fiverr: AI-agent searches +18,347% (interest, not earnings). [selfemployed.com on Upwork](https://www.selfemployed.com/news/ai-freelance-skills-demand-2026/)
- Privalikhina's pivot is exactly here: demand for *training* grew; she now asks every discovery call about it. [LinkedIn](https://www.linkedin.com/pulse/what-i-learned-building-ai-automation-agency-why-nadia-privalikhina-atk0f)

**Assessment:** Fastest path to $5–10k/month for a credible technical person; terrible leverage (sells hours; agents can do ≤40%); not an asset. Good **wedge** (a paid $500–999 assessment) that de-risks the sale of a retainer.

### 2.8 Digital products / courses

- CodeFast made $92k in two days at launch and $834k lifetime — to an audience of 100k+ built over years. [Indie Hackers](https://www.indiehackers.com/post/marc-lou-launches-coding-course-codefast-makes-92k-in-two-days-0bmnoYSUCBPO5xjJpk88); [TrustMRR](https://trustmrr.com/founder/marclou)
- Everyone else: median $72/mo. [InsightRaider](https://insightraider.com/en/state-of-gumroad-2026)

**Assessment:** Pure function of audience size. Zero capital, high margin, zero defensibility. Sequence it *after* you have proof and followers.

### 2.9 Done-for-you agent builds (n8n / Make / Claude SDK)

- Freelance n8n rates $40–100/hr (Upwork), projects $1–1.5k (simple) to $1.5–5k (5–15 workflows) up to $2–15k; single-workflow "AI agent" $3–8k; retainers $500–2.5k/mo; budget 15–25% of build cost/yr for upkeep. [Ciphernutz](https://ciphernutz.com/blog/hire-n8n-expert-cost-pricing-guide); [AFFStudio](https://affstudio.org/2026/08/20/how-to-start-an-n8n-automation-agency-in-2026-services-pricing-and-first-clients/); [betonai](https://betonai.net/how-to-build-a-10k-month-ai-automation-agency-in-2026-n8n-vs-make-vs-zapier-complete-pricing-client-acquisition-and-revenue-playbook/)

**Assessment:** Same economics as 2.1 with a lower ticket and heavier maintenance tail. Only worth it inside a productized, retainer-based offer.

### 2.10 White-label SaaS reseller (GoHighLevel "SaaS mode")

- Platform $497/mo; resell at ~$297/client/mo (or $99–299); break-even 2–3 clients; one 64-subscriber × $199/mo example collected by ProvenStartups; local-agency claims of $10–12k/mo are promotional. [Pintox](https://pintox.com/blog/gohighlevel/ghl-saas-mode/); [ProvenStartups](https://provenstartups.com/blog/ai-agencies/ai-agency-revenue)

**Assessment:** A legitimate, boring way to add a recurring software line to a local-services offer; the platform owns the product and the churn risk is yours. Fits as a component of #1, not as the business.

---

## 3. Where the hype is thickest (and what to discount)

- "$30k–50k/month in 90 days" AI-agency claims: the most-upvoted Reddit threads say this is **course revenue relabelled**. [Ciela](https://ciela.ai/blogs/ai-automation-agency-realistic-income-reddit)
- "70–90% margins": plausible gross; **nobody publishes net** after inference, telephony, onboarding, monitoring, refunds and the founder's unpaid hours. [ProvenStartups](https://provenstartups.com/blog/ai-agencies/ai-agency-revenue)
- "Solo founder $3.6M ARR" (HeadshotPro): unsupported; the founder hired. [Latka](https://getlatka.com/companies/headshotpro)
- "One-person unicorn": no instance exists; Base44 had eight employees at sale. [TechCrunch](https://techcrunch.com/2025/06/18/six-month-old-solo-owned-vibe-coder-base44-sells-to-wix-for-80m-cash)
- GEO ROI numbers ("30–40% higher AI referrals"): no methodology; AI referrals are ~1% of traffic. [Similarweb](https://aisearch.similarweb.com/blog/gen-ai-stats/)
- "Clients never fire an automation agency because removing it breaks their business" vs "clients churn once the automation becomes invisible": two agency blogs, opposite claims, neither with data. [RankSquire](https://ranksquire.com/2026/01/21/automation-agency-model/); [AllAble](https://www.allable.ai/blog/ai-automation-agency/)

---

## 4. Trading as a wealth path: the evidence, and whether "autonomous trading" should be the engine

### 4.1 Retail discretionary/day trading (large-sample academic studies)

| Study | Sample | Finding |
|---|---|---|
| Chague, De-Losso & Giovannetti, *Day Trading for a Living?* (FGV/USP, 2019–20) | **All** 19,646 individuals who began day-trading Brazilian mini-Ibovespa futures 2013–15 | Of those who persisted 300+ days, **97% lost money**; only ~1.1% earned more than the Brazilian minimum wage; ~0.4–0.5% earned more than a bank teller's starting salary; the top earner made ~US$310/day with high risk. | [SSRN 3423101](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=3423101); [FGV repository](https://repositorio.fgv.br/items/e87d04fc-4b4c-4a56-ab5a-1c84c1afde1b/full); [CXO Advisory summary](https://www.cxoadvisory.com/investing-expertise/day-trading-a-bust/) |
| Barber, Lee, Liu & Odean, *Do Day Traders Rationally Learn About Their Ability?* | Complete Taiwan Stock Exchange transaction data, 1992–2006 | "the aggregate performance of day traders is negative... the vast majority of day traders are unprofitable, and many persist despite an extensive experience of losses"; >75% quit within two years; the fraction of profitable (experienced) day traders is "consistently about 5%"; the companion paper finds **<1% of the day-trading population predictably earns profits.** | [Berkeley Haas PDF](https://faculty.haas.berkeley.edu/odean/papers/Day%20Traders/Day%20Trading%20and%20Learning%20110217.pdf) (text extracted directly) |
| Barber & Odean, US brokerage households | 66k households | Most-active traders underperform the market by ~6.5 pp/yr. | [curvedtrading summary](https://curvedtrading.com/articles/en/trading/average-day-trader-income/) |
| ESMA / FCA CFD disclosures | EU/UK retail CFD accounts | **74–89% of retail CFD accounts lose money** (ESMA 2018 analysis); broker-published 2025 figures: Plus500 76–79%, IG ~68–71%, eToro 46–77% depending on region/period. | [ESMA](https://www.esma.europa.eu/pl/node/84933); [Good Money Guide](https://goodmoneyguide.com/trading/risk-warning-loss-percentages/); [Investors Centre UK](https://www.theinvestorscentre.co.uk/trading/statistics/day-trading/) |

### 4.2 Crypto and prediction markets

- No exchange publishes user P&L. Survey/secondary estimates: 70–84% of retail crypto day traders lose in year one; consistent profitability "10–20%" at best (vendor estimates). [Gate wiki](https://web3.gate.com/crypto-wiki/article/what-percentage-of-crypto-traders-make-money-20260116); [Fortraders](https://fortraders.com/blog/is-crypto-day-trading-worth-it)
- Polymarket on-chain: only 0.51% of wallets (of 95M transactions, Apr 2024–Dec 2025) made >$1,000 profit; a separate LayerHub count found ~13.6% of users profitable at all and ~1% above $1k. Galaxy: 69% of retail Polymarket traders finish in the red. [Phemex summary](https://phemex.com/news/article/polymarket-analysis-unveils-six-key-profit-strategies-for-2025-49430); [Decrypt](https://decrypt.co/290625/most-polymarket-traders-have-lost-money); [Yahoo/Galaxy](https://finance.yahoo.com/markets/crypto/articles/69-retail-polymarket-traders-finish-045227939.html)
- Retail bots: the only "study" ("3% of 500 retail bot strategies beat buy-and-hold after fees") is untraceable; platform-reported median bot returns (~12%/yr) are self-reported and survivorship-biased. [BotVerdict](https://botverdict.com/articles/are-crypto-trading-bots-profitable-in-2026-an-honest-analysis-of-real-returns/)

### 4.3 LLM / agentic trading specifically (the part relevant to "autonomous trading")

- **Alpha Arena Season 1 (nof1, Oct–Nov 2025):** six frontier LLMs each given $10k to trade crypto perps live on Hyperliquid. **Four of six lost money**; Claude Sonnet 4.5 ended around $5.8k (≈–42%), GPT-5 lost >60%; Qwen3-Max +22% and DeepSeek +5% were the only winners; the winner in the next season (Grok) was the only model still profitable a month later. Models over-traded (1,418 trades vs 158 for the best performer). [Forklog](https://forklog.com/en/four-out-of-six-ai-models-suffer-losses-in-trading-tournament/); [Forklog S1.5](https://forklog.com/en/ai-model-grok-4-2-triumphs-in-trading-tournament/)
- **"The Alpha Illusion" (arXiv 2605.16895, May 2026):** reported alpha from end-to-end LLM trading agents "should not be treated as deployment evidence." Three confounders: temporal contamination (training data overlaps the backtest), unmodeled frictions (spreads, slippage, API/latency costs), and short-window uncertainty (Sharpe standard error as large as the Sharpe). Reproduction on a 2025–26 window: *TradingAgents* Sharpe fell from 0.43 to 0.22 after costs and underperformed buy-and-hold on 4 of 5 stocks; *QuantAgent* went from –0.96 to –1.15. [alphaxiv 2605.16895](https://www.alphaxiv.org/abs/2605.16895)
- **AI-Trader live benchmark (arXiv 2512.10971):** "general model intelligence does not automatically translate into trading skill; most agents show weak returns and poor risk management." **AlphaCrafter (arXiv 2605.05580):** ML/LSTM models that look strong in backtests "degrade sharply live." **LiveTradeBench (arXiv 2511.03628):** offline backtests leak information. [econpapers](https://econpapers.repec.org/paper/arxpapers/2512.10971.htm); [arXiv 2605.05580](https://arxiv.org/pdf/2605.05580); [arXiv 2511.03628](https://www.arxiv.org/pdf/2511.03628)

### 4.4 The arithmetic, independent of edge

With $5,000 of capital, even a world-class 30%/yr net return (top-decile hedge-fund territory) produces $1,500 in year one. Reaching $1M from $5k at 30%/yr takes ~20 years; at 100%/yr (which no audited retail track record sustains) it takes ~7.6 years with zero drawdown. The binding constraint is **capital, not alpha** — and the only way to get capital is a cash-flowing business.

### 4.5 Verdict

**Autonomous trading should not be the primary revenue engine.** It is the single worst-evidenced path on this list: (a) 95–99% of persistent participants fail in every large sample, (b) the specific technology in the org profile (LLM agents) has, as of 2026, no credible live out-of-sample edge in the peer-reviewed or competition record, and (c) the capital base makes the payoff irrelevant even if (a) and (b) were wrong. If the trading agents are kept at all, treat them as **R&D and content** (a public, honest "my agents trade $1k live" log is a legitimate audience magnet) with a hard cap (≤10% of surplus cash, never borrowed), live paper-then-micro-live validation ≥6 months, cost-inclusive accounting, and a pre-committed kill rule.

---

## 5. What successful solo founders actually do day to day, and what distribution works now

**Day-to-day patterns (from the people with verified or near-verified $1M+/yr):**
- **Ship volume, kill fast.** Levels: ~70 failed projects before Nomad List/Photo AI; launch within ~2 weeks; validate by getting users to pay; cron jobs/scripts (now agents) run operations. [Lex Fridman recap](https://keshavatearth.substack.com/p/pieter-levels-interview-with-lex); [techleap profile](https://finder.techleap.nl/news/note/the-internet-s-solitary-millionaire-pieter-levels-journey)
- **Portfolio, not one bet.** Lou: 20 products, ~$3.26M verified lifetime; most earn ~nothing, two or three carry everything. [TrustMRR](https://trustmrr.com/founder/marclou)
- **AI writes most of the code; the founder does distribution.** Lou reports ~90% of code via Cursor; Levels streams coding sessions; the founder's job is "audience building and distribution." [Demand Curve, The Solo Founder Era](https://www.demandcurve.com/newsletters/growth-newsletter-328)
- **Productized, async, no meetings** (DesignJoy: Trello queue, 4–5 hrs/day, 20 clients). [Memberstack showcase](https://memberstack.io/showcase/how-i-built-designjoy)
- **Pipeline runs as a system** (the $40k MRR agency: 10-min intake → agent production → 15–20 min QA → automated handoff; reusable "skills" per task type). [YouMind](https://youmind.com/landing/x-viral-articles/solo-ai-agency-40k-mrr)
- **Public revenue transparency is the marketing** (Levels, Lou, Dinh all publish numbers; the format that wins is "transparent operator shipping," not "marketer publishing tips"). [Lishchuk](https://lishchuk.com/blog/solo-founder-marketing-playbook-2026.html)

**Distribution channels in late 2026:**
- **Owned email list** — consistently the highest ROI and the only channel platforms can't throttle. [startupslab](https://startupslab.site/blog/blog-saas-marketing-playbook-2026)
- **One social platform, 3–5 posts/week, real numbers**: X for developers/B2B SaaS; LinkedIn for operators/revenue teams (and SMB owners). [Lishchuk](https://lishchuk.com/blog/solo-founder-marketing-playbook-2026.html)
- **Direct outbound to a narrow ICP** (≤50 highly targeted sends reply at ~5.8% vs 2.1% for blasts). [Leadriver](https://www.leadriver.io/blog/cold-email-reply-rate-benchmarks-2026)
- **Referrals + public case studies** — the primary engine named by every service operator above.
- **Informational SEO is dying** (AI Overviews: –58% CTR; 83% zero-click); long-tail commercial queries and being *cited* still work. [Lishchuk](https://lishchuk.com/blog/solo-founder-marketing-playbook-2026.html)
- **Marketplaces** (Upwork: AI integration +178%) as a cold-start channel for the first 2–3 paying clients. [selfemployed.com](https://www.selfemployed.com/news/ai-freelance-skills-demand-2026/)

---

## 6. Ranked recommendation for this profile

**Why these three, in this order:** the profile has near-zero capital, strong agent leverage, hardware that can run local models/automation 24/7, and (presumably) technical credibility — but no audience and no track record. The ranking optimizes for (1) time to cash, (2) agent-runnable share, (3) convertibility into a sellable asset, (4) evidence quality.

### #1 — Niche productized AI service with recurring retainers for one SMB vertical ("Never Miss a Lead" stack)
- **Offer:** for one vertical (home services — HVAC/plumbing/electrical — or dental/med-spa): AI phone/SMS answering + instant lead follow-up + booking + review requests + a monthly "AI visibility" report (GEO/schema/listings as an add-on line). Sold as outcomes: "every call answered, every lead followed up in <60s, more reviews."
- **Why:** fastest documented time-to-revenue (weeks), ~$0 capital, 70–90% gross margin, consistent $500–3,000/mo price points across sources, demand backed by real missed-call data, and a delivery pipeline that agents can run ~80% of. It directly generates the case studies and vertical process knowledge that become #2.
- **Ceiling solo:** $20–40k MRR before capacity/support limits (the documented break point); $1M net worth here comes from **cash flow saved + later sale of the book or the software layer**, not a big exit. At $15k MRR / 80% margin ≈ $144k/yr pre-tax; at $30k MRR ≈ $288k/yr. Realistic timeline to $1M net worth via this path alone: 5–8 years of saving/investing, shorter if #2 lands.
- **Weaknesses:** human selling is non-negotiable; vendors sell direct at $49–299/mo; churn risk when the automation "becomes invisible"; scope creep (Privalikhina) unless rigidly productized.

### #2 — Vertical micro-SaaS extracted from #1
- Once 5–10 clients share the same workflow, package it (own dashboard + the voice/SMS stack via Retell/Vapi/Twilio APIs, or white-label a platform first) and sell at $199–497/mo self-serve to the same vertical. Use #1's clients as design partners and references.
- **Why:** only model that creates an asset priced at a revenue multiple (~2.5–4x revenue sub-$1M ARR); a $300–400k ARR vertical tool is a plausible $1M+ exit; solo examples (Lou, Dinh, Levels) show $50–150k MRR is attainable with distribution.
- **Weaknesses:** 70% of micro-SaaS never pass $1k MRR; 8–9 months median to $1k MRR; needs the distribution engine (#3).

### #3 — Build-in-public audience + digital products (the distribution engine)
- Publish the real numbers: client count, MRR, what broke, the agent pipeline, and (if kept) the honest trading-agent log. One platform (LinkedIn for SMB/operator buyers; X if the SaaS targets builders), 3–5 posts/week, weekly email. Later: a $99–499 "how I run a one-person AI service business" product/course and templates — only once there is proof.
- **Why:** every $1M+ solo founder found runs on an owned audience; it compounds the sales motion for #1 and the launch for #2; near-zero cost.
- **Weaknesses:** 6–18 months before it pays directly; median newsletter income is trivial; must be human-voiced.

**Not recommended as primary:** autonomous trading (Section 4), generic "AI automation agency," B2B lead-gen agency, standalone GEO agency, white-label reseller as the whole business.

---

## 7. 90-day path to first $1k–10k MRR (pick #1)

**Targets (calibrated to practitioner consensus, not guru claims):** Day 30: 1 paying client (pilot or $1.5–2.5k/mo). Day 60: 3–4 clients ($5–8k MRR). Day 90: 5–7 clients ($8–12k MRR) is the *optimistic* case described by the $40k-MRR operator; the *median* case from Reddit consensus is 1–2 retainers in the low four figures. Plan for the median; structure for the optimistic.

**Days 1–10: Pick the vertical and build the demo you can sell in 15 minutes**
- Choose one vertical with (a) high-value inbound phone leads, (b) documented missed-call pain, (c) owners reachable by phone/LinkedIn: home services (HVAC/plumbing/roofing) or dental/med-spa. Pick the one where you have any personal network.
- Agents: scrape/assemble a 300-business list (Google Maps + website + current call handling), draft the ICP, write the 3-tier offer: **Starter $497/mo** (AI answering + missed-call text-back + booking link), **Core $1,497/mo** (+ CRM follow-up sequences, review requests, monthly report), **Pro $2,997/mo** (+ outbound reactivation campaigns, GEO/schema/listings, quarterly strategy call). Setup fee $500–1,500 (waive for first 3 "founding clients" in exchange for a case study).
- Build the stack on a per-minute voice platform (Retell/Vapi/Twilio) + n8n or Claude agents on the Mac mini for routing, CRM updates, reporting. Record a 3-minute demo: a real call to "their" business handled live.
- Cost: domain, a phone number, voice minutes — under $200.

**Days 11–30: Sell (human) while agents prepare everything else**
- Daily: 20 personalized touches (call + email + LinkedIn) to owners from the list; the pitch is a **free missed-call audit**: agents call the business 5 times at different hours, log answer rate/time, and produce a one-page "you missed X of 5 calls; here's what that costs" report. This is the $999-assessment wedge, given free to the first 20.
- Offer the first 3 clients a 30-day "pay-only-if-it-books" pilot or 50% off month one. Goal: 1 signed client by day 30.
- Agents: write and schedule 3–5 LinkedIn posts/week documenting the build (start #3 immediately); draft the onboarding checklist, call scripts per vertical, QA rubric, and the monthly client report template.

**Days 31–60: Deliver flawlessly, productize the delivery, ask for referrals**
- Onboard client #1 with a written success metric (calls answered %, leads texted back within 60s, appointments booked) — the one thing that prevents "the automation became invisible" churn.
- Pipeline as system: intake form → agent configures → human 15-min QA → go-live → agents monitor transcripts daily and flag escalations → weekly automated client email with numbers.
- Keep 20 touches/day; add every client's before/after as a case post. Ask each live client for 2 introductions. Target 3–4 clients by day 60.
- Add the white-label CRM/booking layer if clients lack one (GHL-style, $297/mo resold) — only if ≥3 clients need it (platform cost $497/mo).

**Days 61–90: Raise prices, lock retention, start the software ladder**
- Move new clients to Core/Pro pricing; switch founding clients to annual-discounted plans (beehiiv/SaaS data: annual billing materially cuts churn).
- Publish the first real case study with numbers (calls answered, appointments booked, revenue attributed).
- Start the #2 spec: what dashboard, settings and reports every client asks for → that is the product. Recruit 2–3 clients as design partners.
- Review at day 90 against the kill criteria: if <1 paying client after 60 days of ≥15 daily touches, the problem is the vertical or the offer, not the tech — switch vertical before switching models.

**Operating cadence for the human (approx. 5–6 hrs/day):** 2 hrs outbound/sales calls; 1 hr QA/escalations; 1 hr content (approve agent drafts, record one video/demo); 1 hr client comms; the rest, agents run.

**Capital plan:** total cash at risk in 90 days ≈ $300–1,200 (voice minutes, phone numbers, one platform seat, domain). Trading agents: paused, or capped at ≤$500 live with full public logging as content.

---

## 8. What would change this recommendation

- If the founder already has a 20k+ engaged audience in a builder niche → start at #2/#3 (Lou/Levels model) and skip services.
- If the founder has deep expertise in one vertical's software (e.g., ex-ServiceTitan, ex-dental PMS) → go straight to vertical SaaS with design-partner pre-sales (Subscribr-style $20k in pre-sold lifetime deals before writing code).
- If a verified, audited, ≥12-month live track record with cost-inclusive returns and a Sharpe >1 on ≥$50k appears → trading becomes a *capital allocation* decision for surplus cash, still not the business.
- If AI-referral share of SMB leads rises from ~1% to >10% with attributable tracking → GEO graduates from add-on to standalone line.

---

## Appendix: Source list (all accessed 21 Oct 2026)

**Base rates / indie data**
- RockingWeb, 1,000 Micro SaaS analysed — https://www.rockingweb.com.au/micro-saas-revenue-analysis-2025/
- MicroConf, State of Independent SaaS 2024 — https://microconf.com/saas-this-year
- Startups for the Rest of Us ep. 721 — https://www.startupsfortherestofus.com/episodes/episode-721-7-key-takeaways-from-the-2024-state-of-independent-saas-report
- Indie Hackers, "It takes 5 months to reach $1k MRR" — https://www.indiehackers.com/post/it-takes-5-months-to-reach-1k-in-mrr-491742f806
- Taskade, One-Person Companies — https://www.taskade.com/blog/one-person-companies
- TrustMRR — https://trustmrr.com/ ; Marc Lou founder page — https://trustmrr.com/founder/marclou
- InsightRaider, State of Gumroad 2026 — https://insightraider.com/en/state-of-gumroad-2026 ; profitable.app — https://profitable.app/gumroad/stats
- beehiiv, State of Paid Newsletters 2026 — https://www.beehiiv.com/blog/the-state-of-paid-newsletters-2026
- Substack statistics (secondary) — https://bestwriting.com/substack-statistics
- Beancount, bootstrapped SaaS multiples 2026 — https://beancount.io/blog/2026/07/11/bootstrapped-saas-valuation-multiples-2026-acquire-com-indie-founders-guide

**Agencies / productized services**
- Privalikhina, "What I learned building an AI automation agency (and why I think this business model is broken)" — https://www.linkedin.com/pulse/what-i-learned-building-ai-automation-agency-why-nadia-privalikhina-atk0f
- "How I Run an AI Agency Solo ($40k MRR)" (X thread reproduction) — https://youmind.com/landing/x-viral-articles/solo-ai-agency-40k-mrr
- Ciela, AI automation agency realistic income (Reddit summary) — https://ciela.ai/blogs/ai-automation-agency-realistic-income-reddit
- ProvenStartups, AI agency revenue receipts — https://provenstartups.com/blog/ai-agencies/ai-agency-revenue
- AllAble, AI automation agency 2026 — https://www.allable.ai/blog/ai-automation-agency/
- DesignJoy: https://www.indiehackers.com/post/how-designjoy-got-from-0-to-120k-month-with-no-paid-advertising-a31375fce0 ; https://aitrav.beehiiv.com/p/design-joy-one-man-business-earning-13-million-per-year ; https://memberstack.io/showcase/how-i-built-designjoy
- AI receptionist pricing: https://www.cloudtalk.io/blog/how-much-does-voice-ai-cost/ ; https://www.getnextphone.com/blog/ai-receptionist-cost ; https://agentzap.ai/blog/ai-receptionist-pricing-complete-cost-guide-2025
- Vertical retainer claims: https://datastaqai.com/blog/ai-automation-agency-niches-small-business ; https://buldrr.com/7-ai-agents-businesses-are-paying-for-in-2026/ ; https://builts.ai/blog/home-services-dispatch-and-voice-ai-agent-case-study/
- Missed-call benchmarks roundup — https://stealthagents.com/research/home-services-missed-call-revenue-statistics-2026
- Intuit 2026 AI Impact Report — https://www.intuit.com/blog/global-stories/ai-impact-report/
- n8n/Make pricing: https://ciphernutz.com/blog/hire-n8n-expert-cost-pricing-guide ; https://affstudio.org/2026/08/20/how-to-start-an-n8n-automation-agency-in-2026-services-pricing-and-first-clients/
- GoHighLevel SaaS mode — https://pintox.com/blog/gohighlevel/ghl-saas-mode/
- Ghostwriting: https://ecommercefastlane.com/how-chatgpt-scaled-my-ghostwriting-side-hustle/ ; https://aibusiness.vc/solo/ai-linkedin-ghostwriter
- Consulting rates: https://www.groovyweb.co/blog/ai-consulting-rates-2026 ; https://www.pertamapartners.com/insights/ai-consulting-pricing-guide
- Upwork 2026 AI demand — https://www.selfemployed.com/news/ai-freelance-skills-demand-2026/
- Cold email benchmarks: https://www.lemlist.com/blog/cold-email-response-rate ; https://www.leadriver.io/blog/cold-email-reply-rate-benchmarks-2026 ; https://martal.ca/b2b-cold-email-statistics-lb/

**GEO / distribution**
- WebFX GEO cost — https://www.webfx.com/blog/ai/generative-engine-optimization-cost/ ; First Page Sage — https://firstpagesage.com/seo-blog/geo-aeo-pricing-statistics/ ; Skill Mammoth — https://skillmammoth.com/blog/best-generative-engine-optimization-agencies
- Similarweb AI search stats — https://aisearch.similarweb.com/blog/gen-ai-stats/ ; SEJ — https://searchenginejournal.com/ai-search-isnt-replacing-google-its-layering-on-top-similarweb-data/583378/
- Solo-founder marketing playbooks: https://lishchuk.com/blog/solo-founder-marketing-playbook-2026.html ; https://startupslab.site/blog/blog-saas-marketing-playbook-2026 ; https://www.demandcurve.com/newsletters/growth-newsletter-328

**Solo founders**
- Marc Lou — https://yespress.io/marc-lou.md ; CodeFast launch — https://www.indiehackers.com/post/marc-lou-launches-coding-course-codefast-makes-92k-in-two-days-0bmnoYSUCBPO5xjJpk88
- Tony Dinh — https://nomadpreneur.beehiiv.com/p/solo-founder-who-turned-100-into-1-500-000-no-team-no-investors ; https://www.indiehackers.com/post/my-solopreneur-story-zero-to-45k-mo-in-2-years-1b858f47af
- Pieter Levels — https://ppc.land/how-one-photo-ai-app-generates-132k-monthly-after-70-failed-startups/ ; https://keshavatearth.substack.com/p/pieter-levels-interview-with-lex ; https://finder.techleap.nl/news/note/the-internet-s-solitary-millionaire-pieter-levels-journey
- Base44 — https://techcrunch.com/2025/06/18/six-month-old-solo-owned-vibe-coder-base44-sells-to-wix-for-80m-cash
- HeadshotPro reality check — https://getlatka.com/companies/headshotpro ; https://www.unite.ai/tr/danny-postma-founder-of-headshotpro-interview-series/

**Trading**
- Chague, De-Losso, Giovannetti, Day Trading for a Living? — https://papers.ssrn.com/sol3/papers.cfm?abstract_id=3423101 ; https://repositorio.fgv.br/items/e87d04fc-4b4c-4a56-ab5a-1c84c1afde1b/full ; https://www.cxoadvisory.com/investing-expertise/day-trading-a-bust/
- Barber, Lee, Liu, Odean, Do Day Traders Rationally Learn About Their Ability? — https://faculty.haas.berkeley.edu/odean/papers/Day%20Traders/Day%20Trading%20and%20Learning%20110217.pdf
- ESMA CFD measures — https://www.esma.europa.eu/pl/node/84933 ; broker loss disclosures — https://goodmoneyguide.com/trading/risk-warning-loss-percentages/ ; https://www.theinvestorscentre.co.uk/trading/statistics/day-trading/
- Polymarket: https://decrypt.co/290625/most-polymarket-traders-have-lost-money ; https://phemex.com/news/article/polymarket-analysis-unveils-six-key-profit-strategies-for-2025-49430 ; https://finance.yahoo.com/markets/crypto/articles/69-retail-polymarket-traders-finish-045227939.html
- Alpha Arena results — https://forklog.com/en/four-out-of-six-ai-models-suffer-losses-in-trading-tournament/ ; https://forklog.com/en/ai-model-grok-4-2-triumphs-in-trading-tournament/
- The Alpha Illusion (arXiv 2605.16895) — https://www.alphaxiv.org/abs/2605.16895
- AI-Trader (arXiv 2512.10971) — https://econpapers.repec.org/paper/arxpapers/2512.10971.htm ; AlphaCrafter (arXiv 2605.05580) — https://arxiv.org/pdf/2605.05580 ; LiveTradeBench (arXiv 2511.03628) — https://www.arxiv.org/pdf/2511.03628
- Crypto retail estimates (low quality): https://web3.gate.com/crypto-wiki/article/what-percentage-of-crypto-traders-make-money-20260116 ; https://botverdict.com/articles/are-crypto-trading-bots-profitable-in-2026-an-honest-analysis-of-real-returns/
