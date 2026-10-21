# Where AI Creates a Temporary Labor-Price Arbitrage for a One-Person Operator (October 2026)

Prepared 2026-10-21. Method: ~40 web searches and primary-source fetches; every number below carries its source. Figures from vendor blogs are flagged as such. Economic framing throughout: an arbitrage exists where (a) the market price is still anchored to human hours, (b) a frontier-model agent team can deliver the output at near-zero marginal cost, (c) the buyer has money and switching inertia, and (d) incumbents are slow to reprice. The "gap" is the time until buyers reprice or incumbents adopt.

---

## 0. The control group: what a closed gap looks like

Before choosing where to go, it helps to see what happens when the gap closes. Two markets have already repriced:

- **Translation.** The ELIS 2026 survey reports language companies seeing falling sales prices and buy-in rates, with more than half of respondents seeing the number of language companies in their market shrink ([ELIS 2026](https://elis-survey.org/wp-content/uploads/2026/03/ELIS-2026-Report.pdf)). A UK Society of Authors survey found 36% of translators had lost work to generative AI and 43% had lower income ([Bloodinthemachine summary](https://www.bloodinthemachine.com/p/ai-killed-my-job-translators)). Post-editing rates are reported at $0.03–$0.06/word, roughly half of prior full-translation rates ([biztoolkit](https://www.biztoolkit.co/post/translation-localization-rates-in-2026-per-word-per-hour-per-project)). Slator's 2026 report (second-hand) has 57% of translation companies reporting revenue declines.
- **Freelance writing.** Hui, Reshef & Zhou (Organization Science 2024) find a 2% drop in jobs and 5% drop in monthly earnings for AI-exposed Upwork freelancers after ChatGPT ([WashU summary](https://olin.washu.edu/about/news-and-media/news/2023/08/study-ai-tools-cause-a-decline-in-freelance-work-and-incomeat-least-in-the-short-run.php)). Demirci, Hannane & Zhu (Management Science 2025) find a 21% relative decline in automation-prone job posts, with writing posts down 30% within eight months ([CESifo WP 11276](https://ideas.repec.org/p/ces/ceswps/_11276.html)).

**Lesson:** gaps close fastest where (1) the buyer is a sophisticated, price-sensitive procurer (agencies, platforms), (2) the output is a commodity file, and (3) nothing regulatory or relational sits between the buyer and the tool. The open gaps in 2026 are the mirror image: unsophisticated or time-starved buyers, outputs embedded in a workflow with liability, and a relationship or credential wrapper around the AI.

The Anthropic Economic Index (May 2026 period) is consistent with this: the top matched work tasks are information search, advising on products and financial matters, editing material prepared by others, writing/editing copy for clients, developing training materials, and "review files, records and other documents to obtain information to respond to requests" ([Anthropic Economic Index](https://www.anthropic.com/economic-index)). Those are precisely the task bundles in denial appeals, bid writing, bookkeeping review, and compliance documentation. (Observed usage only; not evidence of displacement.)

---

## 1. Professional services still priced at human rates

### 1a. Grant writing and RFP / government bid responses

**Price today (human-anchored).** Freelance grant writers: $30–$150/hr; foundation proposal $1,500–$5,000 flat; federal applications $5,000–$15,000+; retainers $2,000–$6,000/mo ([Grantable](https://grantable.co/how-much-does-a-grant-writer-cost), [GrantSmarts](https://grantsmarts.com/grant-writer-cost-guide/), [AGA](https://americangrantassociation.org/how-do-grant-writers-get-paid-salary-fees-pricing-models-income-explained-2026/)). Government proposals: $3,000–$25,000 per bid; The Bid Lab publishes $245/hr with a 10-hour minimum; a contingency shop charges 10% of awarded value; compliance-only reviews are $497–$997 ([SLED AI pricing](https://www.sledai.com/blog/procurement-service-pricing-2026/), [BidBionic](https://bidbionic.com/blog/how-much-does-proposal-writing-cost)). Industry rule of thumb: proposal cost is 1–4% of contract value ([SLED AI stats](https://www.sledai.com/blog/government-contracting-statistics/)).

**Demand / under-bid evidence.**
- SLED AI's proprietary analysis of 370,000+ state and local solicitations: average 4.5 bids per solicitation and **40% of solicitations receive fewer than 3 bids** ([SLED AI](https://www.sledai.com/blog/government-contracting-statistics/)). Vendor data, unverified.
- SAMradar's FY2024 FPDS pull claims **81% of new federal contracts had a single offer** (their "zero competition" definition), up from 36% "one offer + not reported" in 2019 ([SAMradar](https://www.samradar.com/post/fy-2024-federal-spending-report-historic-91-5-offers-71-zero-competition-1-32-on-sam-gov)). Vendor marketing; the definition conflates single-offer with no-competition, so treat the level as unreliable but the direction (thin competition) as plausible. GAO reports civilian agency "competition rate" of 89% vs Defense ~52% on $793B FY2025 spend ([FedWeek](https://www.fedweek.com/federal-managers-daily-report/contract-spending-increased-some-18-billion-to-793-billion-in-2025-gao-says/)). I could not find a GAO figure specifically for set-asides with 0–1 bids; the honest answer is that no primary source publishes it and FPDS "number of offers received" would need to be queried directly.
- Only ~14% of SAM-registered entities (~85k of ~612k) win anything in a year; first-time bidders have a reported 3% win rate ([SLED AI](https://www.sledai.com/blog/government-contracting-statistics/)). Deltek: SLED bid counts fell 4.2% YoY in Q1 2026 while dollars per solicitation rose ([Deltek](https://www.deltek.com/resources/articles/state-local-contractors-q1-2026/)).
- Rural capacity gap is well documented: in FEMA BRIC, only 3% of winning counties were low-capacity by Headwaters' Rural Capacity Index; high-capacity counties won 83% of the time ([Daily Yonder](https://dailyyonder.com/study-rural-communities-still-at-disadvantage-when-competing-for-govt-grants/2023/10/16/)). The Lincoln Institute finds "millions, possibly billions" of federal grant money unspent yearly due partly to local capacity ([Lincoln Institute](https://www.lincolninst.edu/es/publications/working-papers/challenge-unspent-federal-grants/)). 16,000+ US municipalities have under 5,000 residents ([Spectrum GovTech](https://www.spectrumgovtech.com/blog/ai-small-municipalities)).
- Nonprofit side: SSIR (Spring 2026) says most nonprofits have minimal or no dedicated grant staff ([SSIR](https://ssir.org/articles/entry/grant-writing-infrastructure)); State of Nonprofits 2026: ~75% of CEOs report rising demand, ~60% say foundation grants got harder, ~30% cut staff ([Innovation Observer](https://innovationobserver.com/2026/06/10/when-grant-writing-isnt-the-problem/)). Only 24.6% of nonprofits use AI for grant writing; 60% are interested ([TechSoup/Tapp via Virtuous](https://virtuous.org/blog/ai-for-nonprofits/)).

**How much AI can do.** Opportunity filtering, go/no-go scoring, compliance matrices, first and second drafts, past-performance narratives, pricing worksheets, formatting: 80–90% of hours. The human remains on: the capture call with the client, final compliance check, and signature.

**Regulatory / ethics.** Percentage-of-grant pricing violates GPA and AFP ethics codes and is rejected by most funders, so grants must be flat-fee or retainer ([AGA](https://americangrantassociation.org/how-do-grant-writers-get-paid-salary-fees-pricing-models-income-explained-2026/)). Contingency on *contracts* (not grants) is common and legal. NIH NOT-OD-25-132 treats applications "substantially developed by AI" as not original ([Virtuous summary](https://virtuous.org/blog/ai-for-nonprofits/)), so federal research grants are excluded from the AI-heavy play. No license is required to write bids or grants.

**Gap closure speed.** Medium (3–5 years). AI drafting tools are cheap ($20–$179/mo: Grantable, GrantBoost, Instrumentl per [FundRobin](https://www.fundrobin.com/articles/how-to-guide/ai-tools-for-nonprofits/ai-grant-writing-software-comparison/)), but the buyer (a town clerk, a church administrator, a $3M contractor) does not want a tool; they want the proposal to be done. Price erosion will come from other AI-equipped freelancers, not from buyer tool adoption.

### 1b. Bookkeeping and tax prep for small businesses

**Price today.** Human bookkeeping $600–$1,800/mo for 200–500 transactions; solo/side businesses $200–$400/mo ([getholdings](https://getholdings.com/resources/blog/bookkeeper-cost-2026)). Managed AI+human services: Zeni $494–$719/mo ([layernext](https://www.layernext.ai/post/best-ai-bookkeeping-tools-for-2026)). Firm-side wholesale AI ledgers: Digits ~$35/client ([layer3labs](https://www.layer3labs.io/guides/ai-bookkeeping-for-small-business)). Tax prep: Schedule C averages $490–$640 at CPA firms, up to $760 ([bpa.tax](https://bpa.tax/average-tax-preparation-cost-for-small-businesses-2026-data/), [SK Financial](https://www.skfinancial.com/blog/average-cost-of-tax-preparation-by-cpa)); NSA survey add-on for Schedule C ~$192 ([TaxDome](https://taxdome.com/blog/tax-preparation-cost-fees)).

**Demand evidence (supply shortage).** 300,000+ accountants and auditors left the profession 2019–2022 (17% from peak); CPA exam candidates fell from 49,597 (2016) to 28,082 (2024); accounting degrees at a 20-year low of 55,152 in 2023–24 ([ACCWire](https://www.accwire.com/accountant-shortage/), [Ramp](https://ramp.com/blog/accountant-shortage)). Capital is voting: Thrive Holdings' $1B AI accounting roll-up (Current, ex-Crete, ~50 practices; OpenAI took a stake) ([Forbes](https://www.forbes.com/sites/annatong/2026/06/02/thrive-holdings-to-bet-1-billion-on-ai-powered-accounting-roll-up/)); Modus $85M (Lightspeed) buying majority stakes in firms ([crossing.one](https://crossing.one/blog/modus-ai-accounting-firm-85m-raise-small-firms-2026)); Accrual $75M (General Catalyst, Feb 2026) ([BusinessWire](https://www.businesswire.com/news/home/20260205968515/en/Accrual-Launches-with-$75-Million-to-Bring-AI-Native-Automation-to-Accounting)); Juno $12M (Apr 2026) ([CPA Practice Advisor](https://www.cpapracticeadvisor.com/2026/04/13/juno-raises-12m-seed-to-scale-ai-tax-preparation-platform-that-automates-90-of-busy-work/181502/)); Synthetic, a bookkeeping firm "without human bookkeepers," $10M seed from Khosla ([CPA Trendlines](https://cpatrendlines.com/2026/10/20/the-42-ai-tech-firms-with-1-23-billion-in-new-2026-funding/)). PE has put $50B+ into CPA firms in six years ([Jupid](https://jupid.com/blog/who-is-buying-accounting-firms-2026)).

**Licensing.** Bookkeeping: none. Paid tax prep: a PTIN ($0 credential barrier beyond IRS registration); the Annual Filing Season Program is voluntary, 18 CE hours ([IRS PTIN](https://www.irs.gov/ptin), [IRS AFSP FAQ](https://www.irs.gov/tax-professionals/frequently-asked-questions-annual-filing-season-program)). Representation before the IRS needs EA/CPA. Some states (CA, OR, MD, NY) register preparers.

**AI-operable share.** Categorization, reconciliation, AP/AR, monthly close, management reports, tax organizer prep, draft returns: ~80%. Human: client onboarding, judgment calls, sign-off, and the yearly tax conversation.

**Gap closure.** Slow-to-medium. The roll-ups are explicitly buying *relationships*, which tells you the moat is the client relationship, not the ledger. A solo operator can underprice the $600–$1,800 incumbent at $350–$700 with better responsiveness and still run 85%+ gross margin. The risk is a race to $65/mo self-serve tools (Digits), but adoption of self-serve among owners is low; the US Chamber (May 2026) found only 6% of small-business workers had automated a workflow with minimal human involvement ([Hivergent summary](https://hivergentai.com/blog/ai-readiness-assessment-cost-small-business/)).

**Adjacent wedge: HOA financial-only management.** Small communities face minimum contracts of $1,500–$3,000/mo for full management, but "financial-only" is $199–$500/mo ([APM HOA](https://www.apmhoa.com/blog/how-much-does-hoa-management-cost-2026), [Edison](https://edisonassociationmanagement.com/blog/hoa-management-fees)). That is bookkeeping with a board as the buyer, and boards are slow adopters with mandatory budgets.

### 1c. Legal document / contract review for SMBs

Human-led flat fee review: $250–$1,000 per contract (Forbes, March 2026, via [aiunpacker](https://aiunpacker.com/blog/10-contract-review-ai-systems-that-spot-problems-human-lawyers-miss)); one firm's menu is $250 simple / $500 standard / $1,000 negotiation / $2,000 drafting. Consumer AI tools are $10–$149/mo ([Justee](https://justee.ai/blog/ai-contract-review-guide)). **Regulatory:** advising on the legal effect of a contract is practice of law in every state; the working model is attorney-of-record approving AI-prepared output (ABA Formal Op. 512). A non-lawyer operator must either partner with a licensed attorney (fee-split restrictions apply, except in Arizona ABS and Utah sandbox) or sell "contract summaries / issue spotting, not advice," which is a thin line. Gap closes fast because Spellbook-type tools at $99–$199/seat are already inside law firms. **Verdict: viable only as a sub-service inside a compliance or bookkeeping relationship, not a standalone.**

### 1d. Medical / dental billing, claim appeals, denial management

**Price today.** Outsourced billing 4–10% of collections; solo providers commonly 6.5–8.5%; specialty 8–12% ([Neolytix](https://neolytix.com/articles/what-is-the-going-rate-for-medical-billing-services/), [getpracticehelp](https://www.getpracticehelp.com/medical-billing-rcm/medical-billing-cost-guide/)). Denial/underpayment recovery on **pure contingency: 20–35% of recovered dollars**, no upfront; denial-queue-only 15–25% with a monthly minimum; old-AR 25–35% ([MD Clarity](https://www.mdclarity.com/comparison/best-denial-recovery-services), [rcrhub](https://rcrhub.com/hubbub/25-questions-ask-before-hiring-denial-management-company), [EliteMed](https://elitemedfinancials.com/outsource-mental-health-billing/)). MGMA cost-to-collect benchmark ~13.7% of collections.

**Demand evidence.** Initial denial rates 7–12% depending on source; MGMA: 41% of providers report denial rates above 10% ([MedicalBillersAndCoders](https://www.medicalbillersandcoders.com/article/claim-denial-rate-in-2026.html), [bilnow](https://bilnow.com/medical-billing-statistics/)). AHA: **80.7% of appealed Medicare Advantage prior-auth denials were overturned in 2024, but only 11.5% were appealed** ([bilnow citing AHA](https://bilnow.com/medical-billing-statistics/)). AMA 2026 survey: ~40 prior auths per physician per week, ~13 staff hours/week, 40% of physicians employ staff solely for PA, 32% say requests are often/always denied ([AMA](https://www.ama-assn.org/press-center/ama-press-releases/ama-survey-prior-authorization-reform-pledge-falls-short-physicians), [RCM Today](https://www.rcm.today/news/ama-2026-prior-authorization-survey)). 42.2% of physicians were still in private practice in 2024 (AMA Benchmark), the buyer segment that cannot afford Cloudmed/R1 ([AMA](https://www.ama-assn.org/about/ama-research/physician-practice-benchmark-survey)). Only 15% of healthcare organizations using revenue-cycle AI report positive ROI, i.e., incumbents have not solved it ([bilnow](https://bilnow.com/medical-billing-statistics/)).

**Documented AI operators.** Claimable: $39.95 per patient appeal, self-reported 75–85% win rate ([GlobeNewswire](https://www.globenewswire.com/news-release/2024/10/02/2956879/0/en/Claimable-Launches-First-Ever-AI-Powered-Appeals-Platform-to-Fight-Unjust-Healthcare-Denials.html), [WABE](https://www.wabe.org/ai-powered-tool-claimable-helps-patients-fight-insurance-claim-denials/)). Counterforce Health (free, nonprofit, Durham NC): claims >50% approval vs 40% baseline ([NBC](https://www.nbcnews.com/news/us-news/ai-helping-patients-fight-insurance-company-denials-wild-rcna219008)). Both are consumer-facing; the **practice-side contingency model is where the money is**, and it is still served by human-labor RCM shops.

**AI-operable share.** Denial triage, root-cause coding, payer-policy retrieval, appeal letter drafting with clinical citations, status tracking, resubmission: ~75–85%. Human: BAA/HIPAA setup, payer portal credentials, phone escalations (AI voice is legally fine for B2B/informational calls with identification, see TCPA notes below), and clinician sign-off on medical-necessity language.

**Regulatory.** No license for billing/denial work in most states; HIPAA business-associate agreement is mandatory; use a HIPAA-eligible model deployment (Claude via AWS Bedrock/GCP Vertex with BAA, or Anthropic enterprise BAA). Do not touch clinical decisions.

**Gap closure.** Medium-slow (3–5 years). Payers are deploying AI denials faster than small practices deploy AI appeals; the asymmetry *widens* the gap in the near term. Large RCM vendors will eventually bundle it, but they ignore sub-$5M practices.

### 1e. Immigration / visa paperwork (non-legal)

Federal regulation defines practice of immigration law to include *selecting and preparing forms and advising on answers*; only attorneys and DOJ-accredited representatives may do it ([CLINIC](https://www.cliniclegal.org/upil), [USCIS](https://www.uscis.gov/scams-fraud-and-misconduct/avoid-scams/become-an-authorized-provider)). JustiGuide (47k users) is registering as a law firm to stay on the right side of this ([TechCrunch](https://techcrunch.com/2025/11/26/justiguide-wants-to-use-ai-to-help-people-navigate-the-u-s-immigration-system)). **Verdict: UPIL exposure is severe (criminal in many states); avoid unless you are an attorney or build as back-office for immigration firms (Docketwise already does this). Score low.**

### 1f. HR compliance and employee handbooks

Consultant handbook $1,500–$5,000; multi-state attorney-drafted $5,000–$25,000; ongoing compliance support $500–$2,000/mo; handbook software $49–$200/mo ([DocBird](https://docbird.io/employee-handbook-cost), [Rulewize](https://rulewize.com/blog/employee-handbook-cost), [Blissbook](https://blissbook.com/blog/how-much-does-it-cost-to-create-an-employee-handbook/)). Only 36% of SMB owners have written AI-use policies (Nationwide 2026) and that itself is a new SKU. AI-operable share is the highest on this list (~90%): state-by-state law tracking, drafting, redlining, annual updates. No license; HR consulting is unregulated. Gap closes medium-fast because SHRM templates and $49/mo software exist, but buyers at 10–100 employees keep paying consultants because they want someone to blame. Productize as a $199–$499/mo "compliance desk" with handbook included.

### 1g. SOC 2 / compliance readiness

Readiness assessments $3,000–$17,000; fixed-fee readiness $4,000–$5,500 (Axipro) to $15k (Control & Function); vCISO retainers $3,000–$20,000/mo, mid-market $5–12k ([trycomp.ai](https://www.trycomp.ai/hub/soc-2-cost-breakdown), [soc2auditors.org](https://soc2auditors.org/insights/vciso-cost/), [zipsec](https://www.zipsec.com/blog/vciso-pricing)). Vanta and Drata both run referral/reseller/MSP partner tracks with recurring pay for services partners ([xamplify Vanta](https://xamplify.com/partner-programs/vanta/), [Drata](https://xamplify.com/partner-programs/drata/)); Vanta's MSP program has a multi-tenant console ([Cyberfort](https://cyberfortgroup.com/cyberfort-joins-vantas-managed-service-provider-partner-program/)). AI-operable: policy authoring, control mapping, evidence collection scripts, vendor reviews, risk registers: ~80%. Human: scoping call, auditor liaison. No license. The inbound channel (Vanta/Drata partner directories, where startups look for a readiness firm) lowers cold-selling burden. Gap closes medium: platforms keep automating, but every new B2B SaaS seed company needs SOC 2 before its first enterprise deal, so demand regenerates.

### 1h. Translation / localization

See Section 0: gap already closed. MTPE $0.03–$0.06/word. Avoid except high-liability legal/medical with a certified translator wrapper.

### 1i. Resume and career services

Executive resumes $400–$2,000 (most $700–$900); boutique C-suite $1,900–$12,000; AI resume builders $15–$50/mo ([Resumeble](https://www.resumeble.com/career-advice/resume-services-cost), [Empire Resume](https://www.empireresume.com/blog/executive-resume-writing-services/)). Consumer buyer, one-off, price-shopping, AI tools already ubiquitous. Gap closing fast. Low ticket. Score low except as an upsell.

### 1j. Academic editing

Editage from $0.06/word (~$300 per 5,000 words), premium $0.13/word ([Editage](https://www.editage.com/services/english-editing/standard-editing-plan)). Price is already AI-adjacent and buyers (grad students, non-native researchers) are among the heaviest ChatGPT users. Gap closed. Avoid.

---

## 2. Intermediation / brokerage models

| Model | Pay per deal | Licensing | Cycle | AI share | Notes |
|---|---|---|---|---|---|
| Business brokerage (<$1M) | 10–12% of price; median BizBuySell sale $350k => ~$35k/deal; minimums $10–50k ([Clearly Acquired](https://www.clearlyacquired.com/blog/how-much-do-business-broker-fees-actually-cost-in-2026), [BizBuySell Q3 2026](https://investors.costargroup.com/news-releases/news-release-details/bizbuysell-releases-q3-2026-insight-report)) | RE license in ~16–17 states (CA, FL among them); asset-only sales unlicensed in TX, NY, OH, PA, NC ([midwest-brokers](https://www.midwest-brokers.com/business-broker-licensing-requirements-by-state-the-2026-reference-guide/)) | 6–12 months | ~50% (CIM drafting, valuation, buyer outreach, data room) | 2,132 closings/quarter on BizBuySell alone, down 7% YoY; buyer/seller confidence 49/47 |
| Equipment finance referral | 2–5% of funded (4–6% on $25–100k deals); lender programs up to low-teens points ([sendstrike](https://sendstrike.ai/blog/heavy-equipment-financing-broker), [EFN](https://equipmentfinancenews.com/news/lender-operations/equipment-finance-brokers-last-wild-west-of-business/)) | Commercial loan broker license in CA (CFL), a few other states; mostly unlicensed | 2–6 weeks | ~60% | "Last Wild West" per trade press |
| SBA 7(a) referral | Capped ~1% or $3,000 (introduction only); packaging 1–3% paid by borrower; Form 159 disclosure ([commercialfinancereferrals](https://commercialfinancereferrals.com/sba-loan-referral-fees), [Starfield & Smith](https://starfieldsmith.com/2026/07/best-practices-working-with-referral-agents/)) | None, but SBA disclosure | 60–90 days | ~70% for packaging | Low per-deal, regulated fee |
| Trades recruiting (direct hire) | 15–25% of first-year pay => $9,750–$16,250 on a $65k journeyman ([Blue Collar Recruiter](https://thebluecollarrecruiter.com/skilled-trades-hiring-costs-comparison-what-it-costs-to-hire-a-skilled-trades-worker-in-2026-recruit/)); qualified applicant cost $9–$14 via paid social ([Boostpoint](https://boostpoint.com/industries-skilled-trades/what-it-costs-to-recruit-skilled-trades-workers-2026/)) | None in most states | 2–6 weeks | ~65% (sourcing, screening, scheduling, AI voice screens) | Buyer is the $1–10M contractor who cannot hire |
| Insurance lead gen | Exclusive Medicare web leads $25–$120; live transfers $55–$120; AEP +20–40% ([insifter](https://insifter.com/guide-lead-costs.html), [enzodialer](https://enzodialer.com/resources/insurance/medicare-leads)) | Lead gen unlicensed; selling policies licensed; TCPA/CMS marketing rules for Medicare are strict | Days | ~70% | Commodity, ad-spend heavy |
| CRE lead gen / referral | 25% of commission convention, but paying an **unlicensed** finder is illegal in most states (NJ, NC); CA finder exception only ([tremgroup](https://www.tremgroup.com/real-estate-referral-fees-state-by-state-guide/), [Justia NJ](https://answers.justia.com/question/2025/03/26/can-i-pay-a-referral-fee-to-a-non-licens-1054648)) | RE license needed to be paid a split | Months | ~60% | Get licensed or sell marketing services at flat fee |
| Freight brokerage | Gross margin ~$189/load vs ~$205 cost to move; 43% of brokers saw margin fall H1 2026 ([Truckstop/BI](https://truckstop.com/blog/freight-broker-outlook-1h26/), [usetenfold](https://www.usetenfold.ai/blog/ai-agents-in-freight-brokerage-whats-actually-changing-in-2026)) | FMCSA authority + $75k BMC-84 bond | Continuous | ~70% | Unit economics negative for sub-scale entrants. Avoid. |
| AI tool affiliates | HubSpot 30% recurring 12 mo; Writesonic 30–40% lifetime; Systeme.io 60% lifetime; Thinkific 30% lifetime; ElevenLabs 22%/12 mo ([eesel](https://www.eesel.ai/blog/ai-affiliate-programs), [layer3labs](https://www.layer3labs.io/guides/best-ai-affiliate-programs)) | None | 6–18 months to build audience | ~80% content, ~0% audience trust | Needs an audience first; not a starting point |

**Highest pay per deal with least licensing:** business brokerage in an unlicensed state (TX/NY/OH/PA/NC, asset-only) at ~$35k/deal median, then trades recruiting (~$10–16k/placement, no license), then equipment finance (~$2–5k on a $100k ticket). SBA referral caps at $3k and is not worth building around.

---

## 3. Selling to the AI boom

- **Expert data labeling.** Mercor average advertised rate $109/hr (Aug 2026; down from $141 in June), $60–$250 range; physicians $130–$170/hr; lawyers $110–$130/hr; Surge $50–$200/hr for vetted frontier experts; Outlier ceilings $90–$150/hr ([herohunt Mercor](https://www.herohunt.ai/blog/mercor-2026-how-it-works-pay-alternatives/), [aitraining.jobs](https://aitraining.jobs/research/what-ai-labs-pay-for-human-data)). After platform cut and unpaid time, generalist take-home ~ $22/hr. **Economics:** income is strictly hours × rate, no leverage, you cannot delegate to agents (ToS and the whole point), and rates are already falling. Good **cash-flow bridge** for a credentialed person during months 1–6; not a business.
- **Claude skills / GPT Store / MCP marketplaces.** As of mid-2026 there is **no native billing rail** for Claude Skills or Codex plugins; monetization is off-platform; only hosted MCP registries (Smithery-type) have a billing path ([Totalum](https://www.totalum.app/blog/agent-skills-marketplaces-2026), [agent37](https://www.agent37.com/blog/how-to-monetize-claude-skills)). Third-party catalogs list skills at ~$29 ([KissMySkills](https://kissmyskills.com/blogs/news/best-claude-skills-marketplaces-2026)). **Hype flag:** every "sell Claude skills" article is written by a skills-marketplace vendor. Treat as a lead magnet for services, not revenue.
- **Vertical AI implementation (ServiceTitan / Jobber / Dentrix).** ServiceTitan Sept 2026 survey (n=1,017): active AI engagement 52% (up from 46% Dec 2025); 64% of users report productivity gains; top barriers "unclear use cases," "software integration," "accuracy concerns" ([ServiceTitan](https://www.servicetitan.com/press/servicetitan-report-finds-74-of-residential-contractors-see-ai-as-key)). Jobber 2026: 52% of blue-collar owners use AI day-to-day for estimates, invoices, follow-ups ([smallbizelevate](https://www.smallbizelevate.com/blog/ai-for-home-service-businesses)). US Chamber May 2026: only 6% of small businesses have automated a workflow ([Hivergent](https://hivergentai.com/blog/ai-readiness-assessment-cost-small-business/)). The gap is between "I use ChatGPT for emails" and "my dispatch, follow-up and review-response run themselves."
- **AI workshops / training.** Half-day team workshop $3,000–$12,000 (10–25 people); consultants $8,000–$15,000 for 15–30; per-seat $199–$499 ([Pertama](https://www.pertamapartners.com/insights/cost-per-employee-ai-training-budgeting), [NEU](https://www.neumediagroup.com/ai-training-cost)). Association keynotes: $7,500–$25,000 mid-tier; most associations buy in the $10–35k band ([ConsultClarity](https://www.consultclarity.org/post/keynote-speakers-association-conferences-usa), [Speakers Associates](https://www.speakersassociates.com/how-to-choose-ai-keynote-speaker-2026/)). Good as a **customer-acquisition channel** for the implementation retainer, weak as a standalone (non-recurring, speaker-saturated).
- **AI readiness audits.** $2,000–$8,000 small business; $5,000–$15,000 mid-market; $15–50k enterprise ([Aries](https://ariesconsultinggroup.com/blog/ai-readiness-audit-cost/), [cabinco](https://cabinco.com/ai-readiness-assessment-cost/)). **Hype flag:** heavily commoditizing; dozens of identical vendor pages. Useful only as a paid discovery step before implementation.

---

## 4. Underserved buyers with money

- **Seniors / Medicare.** 35M+ in Medicare Advantage (55% of eligibles), +1.1M YoY; SNPs 8.2M ([KFF 2026](https://www.kff.org/medicare/medicare-advantage-in-2026-enrollment-update-and-key-trends/)). Fee-only Medicare consulting exists at $1,800–$3,500 deposits per transition ([Healthcare Navigation](https://www.healthcarenavigation.com/how-we-help/medicare-consulting-service/)) but plan *selection* advice for compensation runs into state insurance-producer licensing and CMS marketing rules. Senior move management $50–$150/hr ([seniormoveguide](https://www.seniormoveguide.com/how-much-does-a-senior-move-manager-cost/)) is physical labor; AI share low. **Estate paperwork** via registered Legal Document Assistants (CA) / Certified Legal Document Preparers (AZ): $975 trust package, $500 will package ([AZ Statewide Paralegal](https://azstatewideparalegal.com/document-preparation-rates/)) vs attorney median $2,475 revocable trust ([LegalTemplates study, 909 firms](https://legaltemplates.net/resources/estate-planning/cost-of-estate-planning/)). The LDA/CLDP registration is a real, achievable wrapper in AZ and CA; elsewhere it is UPL. Medium opportunity, geographically limited.
- **Small landlords.** 80% of individually owned rentals are self-managed; mom-and-pops hold >1/3 of units ([Baselane](https://www.baselane.com/resources/landlord-statistics), [Urban Institute](https://www.urban.org/projects/exploring-mom-and-pop-landlord-rentals)). But property management for a fee requires a real-estate license in most states. Sell them bookkeeping/tax (Schedule E) and lease-compliance docs instead; fold into 1b.
- **HOAs.** See 1b: financial-only management at $199–$500/mo is an AI bookkeeping product with a captive, slow-moving, budget-holding buyer.
- **Churches / nonprofits.** See 1a. Flat-fee grants only.
- **Independent medical practices.** 42.2% of physicians; see 1d. The single best "has money, bleeds money, slow to adopt" buyer on the list.
- **Trades contractors $1–10M.** See Section 3 and recruiting. Two acute pains: can't hire, can't follow up on leads. 52% "engage with AI," 6% automated anything.
- **Local governments.** 16,000+ municipalities under 5,000 people; 55.7% of governments use AI but only 42.9% have a policy ([Granicus via Kok](https://terencekok.com/blog/ai-governance-formalisation-local-government-adoption-gap/)); 63% of (Canadian) municipalities cite lack of in-house expertise as the top barrier ([municiPal AI](https://municipalai.ai/canadian-municipalities-are-all-in-on-ai/)). Buy via sole-source under small-purchase thresholds (often $25–50k), which avoids the RFP for your own engagement. Grant writing is the wedge; AI policy + records-request automation is the upsell.

---

## 5. Content / attention arbitrage in 2026

- **Local newsletters.** Naptown Scoop: ~$200k revenue in 2023 on 18k subs (~$11/sub/yr), targeting $350k in 2024, almost entirely local ad sales ([Creator Spotlight](https://www.creatorspotlight.com/p/ryan-sneddon-naptown-scoop), [SparkLoop](https://sparkloop.app/blog/friday-feature-naptown-scoop)). 6AM City (~$25–27M est. revenue, 30+ markets) is replacing reporters with AI workflows in markets it can't staff and says a new city costs $250–300k in year one ([Adweek](https://www.adweek.com/media/6am-city-layoffs-artificial-intelligence/), [newsmachines](https://newsmachines.beehiiv.com/p/6am-city-ai-workflows)). **The arbitrage is real but slow:** AI cuts the content cost to near zero, but revenue is local ad sales (human, outbound) and it took Sneddon three years to $200k.
- **Faceless YouTube / TikTok.** YouTube's July 2025 "inauthentic content" rule is tool-agnostic; mass-produced templated output is demonetized; AI use per se is not ([Outlierkit](https://outlierkit.com/blog/youtube-ai-crackdown), [milx](https://milx.app/en/trends/does-ai-impact-youtube-monetization-what-youtube-has-to-say)). Claims of "thousands of channels suspended" come from a single blog. **Hype flag:** every "$10k/month faceless channel" page sells a course. Not an arbitrage; a lottery with platform risk.
- **Programmatic SEO.** Ahrefs: 58% CTR drop on #1 result when AI Overviews appear (Feb 2026); Chartbeat: small publishers down ~60% in referral traffic over two years ([SEJ](https://www.searchenginejournal.com/impact-of-ai-overviews-how-publishers-need-to-adapt/556843/), [Press Gazette](https://pressgazette.co.uk/publishers/search-isnt-dead-its-fragmenting-how-to-manage-google-traffic-decline/)). Google's scaled-content-abuse policy was in scope of the June and September 2026 spam updates ([digitalapplied](https://www.digitalapplied.com/blog/programmatic-seo-after-march-2026-surviving-scaled-content-ban)). Only pSEO backed by unique data survives. Closed for generic plays.
- **Being the cited source in AI answers (GEO).** AI-referred visitors convert far better than organic in every study (Opollo: 14.2% vs 2.8%, n=312 B2B tech firms; Siege Media median 1.26x across 78 sites; Knotch ~2x across 13,770 domains) but volume is 47–190x smaller than Google and ChatGPT's citation click rate is ~0.7% ([CiteProof](https://citeproof.co/blog/llm-traffic-conversion-rate), [Opollo](https://opollo.com/blog/the-2026-ai-search-benchmark-report/)). **Verdict:** valuable as a *service* sold to the SMB verticals above (be the HVAC company ChatGPT names in your metro), weak as an owned-media play.

---

## 6. Scoring

Scale 1–5. Capital: 5 = under $2k needed. Speed: 5 = $10k/month plausible inside 90 days. $1M/7yr: 5 = clear path to $1M cumulative profit (or $1M revenue run-rate) by 2033. AI share: 5 = 90%+ of delivery hours agent-operable. Cold-selling: 5 = mostly inbound; 1 = relentless outbound. Evidence: 5 = primary data; 1 = vendor blogs only.

| # | Opportunity | Capital | Speed to $10k/mo | Path to $1M/7yr | AI-operable | Cold-sell burden (5=low) | Evidence | Total |
|---|---|---|---|---|---|---|---|---|
| 1 | Denial management / appeals for independent practices (contingency) | 5 | 3 | 5 | 4 | 2 | 4 | 23 |
| 2 | Bid & grant writing for low-capacity buyers (SLED, rural towns, small nonprofits, set-aside contractors) | 5 | 4 | 4 | 4 | 2 | 3 | 22 |
| 3 | AI-native bookkeeping + tax + HOA financials (subscription) | 5 | 2 | 5 | 4 | 2 | 4 | 22 |
| 4 | SOC 2 / compliance readiness + fractional compliance desk | 5 | 3 | 4 | 4 | 3 | 3 | 22 |
| 5 | Trades recruiting (direct-hire placement) | 5 | 3 | 4 | 3 | 2 | 3 | 20 |
| 6 | HR compliance desk / handbooks (subscription) | 5 | 3 | 3 | 5 | 2 | 3 | 21 |
| 7 | Vertical AI implementation + workshops for contractors (ServiceTitan/Jobber) | 5 | 4 | 3 | 3 | 2 | 3 | 20 |
| 8 | Business brokerage, sub-$1M, unlicensed states | 4 | 1 | 4 | 3 | 1 | 4 | 17 |
| 9 | Equipment-finance referral brokering | 5 | 3 | 3 | 3 | 1 | 2 | 17 |
| 10 | Local newsletter (one metro) | 4 | 1 | 3 | 4 | 2 | 4 | 18 |
| — | Estate-doc preparation (AZ/CA LDA) | 4 | 2 | 3 | 4 | 3 | 3 | 19 (geo-limited) |
| — | Expert data labeling (Mercor/Surge) | 5 | 5 | 1 | 1 | 5 | 4 | 21 (no leverage; bridge only) |
| — | AI affiliate programs | 5 | 1 | 2 | 4 | 4 | 3 | 19 (needs audience) |
| — | Insurance lead gen | 3 | 3 | 3 | 4 | 3 | 3 | 19 (ad-spend, TCPA) |
| — | Contract review (non-lawyer) | 5 | 2 | 2 | 4 | 2 | 3 | 18 (UPL) |
| — | Immigration paperwork | 5 | 2 | 1 | 4 | 3 | 3 | 18 (UPIL; avoid) |
| — | Translation, academic editing, resumes | 5 | 2 | 1 | 5 | 3 | 4 | gap closed |
| — | Faceless video, generic pSEO | 4 | 1 | 1 | 5 | 4 | 3 | platform risk |
| — | Freight brokerage | 2 | 1 | 2 | 4 | 1 | 4 | negative unit economics |

Note on totals: raw sums reward the data-labeling bridge because it scores 5 on capital, speed and cold-sell despite zero leverage. The ranking below weights $1M-path and AI-operable share double, which is the correct weighting for a one-person agent-leveraged operator.

**Ranked top 10 (weighted):** 1 Denial management; 2 Bid/grant writing; 3 Bookkeeping/tax/HOA; 4 SOC 2 readiness; 5 HR compliance desk; 6 Trades recruiting; 7 Vertical AI implementation for contractors; 8 Business brokerage (unlicensed state); 9 Local newsletter; 10 Equipment-finance referral.

**Portfolio note.** Items 1–3 share one buyer type (owner-operated practices and firms with $1–10M revenue, a bookkeeper, and no CFO) and one sales motion (local, referral-driven, outbound to a named list). Items 4–5 share the "every new startup needs this before its first enterprise deal" motion. A solo operator should run **one of 1–3 as the core and 5 or 7 as the acquisition wedge**, not five things.

---

## 7. The top three, defended, with first 90 days

### #1 Denial management and appeals for independent practices (contingency)

**Why it wins on the economics.** The price is set by human labor (RCM shops staffing billers at $20–30/hr and charging 20–35% of recovery), the output is a letter plus a resubmission (pure language work with retrieval), the buyer has money that is literally sitting in denied claims, the buyer is demonstrably slow (11.5% appeal rate against an 80.7% overturn rate is the cleanest "money on the table" statistic in this report), and the counterparty (payers) is *increasing* denials with AI, which grows the inventory. Contingency pricing means zero price objection: "we only get paid when you get paid." A single mid-size practice with $3M collections and a 9% denial rate has ~$270k/year in denials; recovering half at a 25% fee is ~$34k/year from one client. Ten clients is a $340k business; forty is $1M+.

**Risks and how the gap closes.** HIPAA (sign BAAs, use a HIPAA-eligible model endpoint, no PHI in consumer chat tools). Payer-portal access and phone work are the slow parts; AI voice for informational B2B calls to payers is permissible with identification under the FCC's 2024 ruling, but check counsel ([econsent summary](https://econsent.org/posts/ai-voice-agents-tcpa-rules-october-2026/)). Gap closes when EHR vendors (athena, eCW) bundle AI appeals, likely 2028–2030 for the small-practice tier. Lock in 2–3 year contracts with auto-renew and a prevention report that keeps you valuable as denials fall.

**First 90 days.**
- Days 1–15: Pick one specialty with high denial complexity and lots of independents (behavioral health, PT, dermatology, or dental; dental has its own payer world and is underserved). Build the agent stack: denial ingestion (835/EOB parsing), payer-policy retrieval (medical policy PDFs per payer), appeal-letter generator with citation to policy and clinical notes, tracker. Draft BAA, service agreement (20–30% contingency, 12-month term, denial-queue-only scope so you do not displace their biller). Obtain a HIPAA-eligible model deployment.
- Days 16–45: Run a free "denial audit" offer to 50 practices in one metro: they export 90 days of denials, you return a one-page recovery estimate. Outbound by the practice manager's name (agents build the list from NPI registry + state licensing boards + Google Maps). Target 5 audits, 2 signed.
- Days 46–90: Work the first two queues end to end; publish anonymized before/after (appeal rate, overturn rate, dollars). Add AI voice follow-up for claim status. Ask each client for one referral to another independent. Target: 4 clients, $8–15k/month run-rate by day 90, scaling as recoveries land (expect a 45–90 day cash lag; this is why data-labeling hours at $85–130/hr are a sensible bridge).

### #2 Bid and grant writing for low-capacity buyers

**Why it wins.** It is the fastest to first revenue on this list (per-proposal fees of $3–25k, no license, no HIPAA, flat fees acceptable), the under-bid evidence is strong directionally (40% of SLED solicitations draw fewer than 3 bids; thin federal competition; 83% of FEMA BRIC awards go to high-capacity counties), and the buyers (small contractors chasing set-asides, towns under 5,000 people, churches and small nonprofits) do not want software. The agent team does the expensive part: monitoring SAM.gov/state portals daily, go/no-go scoring, compliance matrices, drafts, pricing templates. One operator can carry 6–10 live bids a month where a human writer carries 2–3.

**Risks.** Contingency is forbidden for grants (use flat fee/retainer); NIH/federal research grants exclude AI-heavy drafting; win rates for first-time bidders are 3%, so sell *capacity and pipeline*, not wins, and price per submission. Gap closes as GovDash-style tools get adopted by mid-size contractors (2027–2029); the sub-$10M contractor and the small town will be last.

**First 90 days.**
- Days 1–15: Choose two lanes: (a) a NAICS cluster you can learn (janitorial, landscaping, IT staffing, construction trades) for SLED and federal set-asides, and (b) rural municipalities in one or two states for infrastructure/resilience grants. Build the pipeline agent (daily SAM.gov + state portal scrape, scoring rubric, auto-generated one-page bid briefs). Build the proposal factory (compliance matrix generator, past-performance library, pricing sheet, style guide).
- Days 16–45: Offer 10 contractors a free weekly "bids you qualify for" brief (this is the lead magnet; it costs you nothing). Convert 3 to a $1,500–$2,500/mo retainer plus $2,500–$7,500 per submission. For towns, approach the clerk/administrator of 30 municipalities with a specific open grant they qualify for and a fixed $4,000–$8,000 application fee under their small-purchase threshold.
- Days 46–90: Submit 8–12 proposals. Publish a compliance scorecard of your own submissions. Join the state APEX Accelerator (ex-PTAC) and SBDC referral lists; they refer small businesses to proposal help for free. Target: $10–20k/month by day 90 (this is the one where $10k in 90 days is realistic).

### #3 AI-native bookkeeping, tax, and HOA financials (subscription)

**Why it wins on the long game.** Recurring revenue, lowest churn of any item here, a documented supply shortage (300k accountants gone, CPA candidates down 43%), and sophisticated capital (Thrive/OpenAI, Lightspeed, General Catalyst, Khosla) paying up for exactly this thesis. Pricing power is intact: incumbents charge $600–$1,800/mo while AI-native delivery costs under $100/mo in tools. 120 clients at $700/mo is $1M ARR, with no license needed beyond a PTIN for tax. HOA financial-only ($199–$500/mo) and small-landlord Schedule E work are low-competition entry wedges.

**Risks.** Slowest to $10k/month because switching bookkeepers happens at year-end and trust is earned. Self-serve AI ledgers ($65/mo) could compress the low end; stay above it by owning tax plus advisory. Gap closes slowest of the three (roll-ups are paying for relationships, which is a signal the relationship is the moat).

**First 90 days.**
- Days 1–20: Stand up the stack (QBO/Xero ProAdvisor accounts, bank-feed automation, an agent for categorization + monthly close + management report narrative, a client portal). Get a PTIN; enroll in AFSP CE (18 hours) so you can be in the IRS directory for the 2027 season. Decide the niche: trades contractors, therapists, or HOAs under 50 units.
- Days 21–60: Offer a free "90-day clean-up and tax-readiness review" to 40 owners in the niche (agents pull the list; you do the 20-minute call). Price: $350–$700/mo including year-end return. Partner with two independent CPAs who are turning away small clients; take their overflow on a referral fee.
- Days 61–90: 10–15 clients onboarded; publish monthly on-time close rate. Add HOA financial-only packages via board outreach (boards meet monthly; agents find meeting notices). Target: $5–8k MRR by day 90, $10k by month 5–6, with the January–April tax season as the step-up.

---

## 8. Hype flags (things that look like arbitrage and are not)

1. **"Sell Claude skills / GPTs / MCP connectors."** No native billing; every article is from a marketplace vendor.
2. **Faceless AI video at "$10k/month."** Course-seller content; YouTube's inauthentic-content rule plus zero moat.
3. **Generic programmatic SEO.** 58% CTR loss under AI Overviews; scaled-content-abuse enforcement in June and September 2026.
4. **AI readiness audits as a business.** Commoditized to $750–$2,500; use only as a paid discovery step.
5. **"One-person $1B company."** Walked back by its own author; documented solo outcomes are $1–3.5M ARR (Levels, Lou, Dinh) and they are product, not services, businesses ([Taskade roundup](https://www.taskade.com/blog/one-person-companies)).
6. **Vendor-reported overturn and ROI rates** (Claimable 75–85%, "30–40% denial reductions"): plausible direction, unaudited level.
7. **Freight brokerage AI.** Agents cut cost, but a new entrant's gross margin per load is below cost to serve.
8. **Expert data labeling as a career.** Rates fell from $141 to $109 average in 10 weeks on Mercor; it is a bridge, not a destination.

---

## 9. Source index (primary and key secondary)

- Anthropic Economic Index, May 2026 period: https://www.anthropic.com/economic-index
- GAO / FedWeek on FY2025 contract spending and competition rates: https://www.fedweek.com/federal-managers-daily-report/contract-spending-increased-some-18-billion-to-793-billion-in-2025-gao-says/
- SAMradar FY2024 FPDS analysis (vendor): https://www.samradar.com/post/fy-2024-federal-spending-report-historic-91-5-offers-71-zero-competition-1-32-on-sam-gov
- SLED AI 2026 statistics (vendor, 370k solicitations): https://www.sledai.com/blog/government-contracting-statistics/
- Deltek Q1 2026 SLED snapshot: https://www.deltek.com/resources/articles/state-local-contractors-q1-2026/
- Headwaters / Daily Yonder on BRIC awards by capacity: https://dailyyonder.com/study-rural-communities-still-at-disadvantage-when-competing-for-govt-grants/2023/10/16/
- Lincoln Institute, unspent federal grants: https://www.lincolninst.edu/es/publications/working-papers/challenge-unspent-federal-grants/
- SSIR, grant writing infrastructure (Spring 2026): https://ssir.org/articles/entry/grant-writing-infrastructure
- Grant writer pricing: https://grantable.co/how-much-does-a-grant-writer-cost ; https://americangrantassociation.org/how-do-grant-writers-get-paid-salary-fees-pricing-models-income-explained-2026/
- Proposal pricing: https://www.sledai.com/blog/procurement-service-pricing-2026/ ; https://bidbionic.com/blog/how-much-does-proposal-writing-cost
- Bookkeeping pricing: https://getholdings.com/resources/blog/bookkeeper-cost-2026 ; https://www.layernext.ai/post/best-ai-bookkeeping-tools-for-2026
- Accountant shortage: https://www.accwire.com/accountant-shortage/ ; https://ramp.com/blog/accountant-shortage
- AI accounting roll-ups: https://www.forbes.com/sites/annatong/2026/06/02/thrive-holdings-to-bet-1-billion-on-ai-powered-accounting-roll-up/ ; https://www.businesswire.com/news/home/20260205968515/en/Accrual-Launches-with-$75-Million-to-Bring-AI-Native-Automation-to-Accounting ; https://cpatrendlines.com/2026/10/20/the-42-ai-tech-firms-with-1-23-billion-in-new-2026-funding/
- IRS PTIN / AFSP: https://www.irs.gov/ptin ; https://www.irs.gov/tax-professionals/frequently-asked-questions-annual-filing-season-program
- Tax prep fees: https://bpa.tax/average-tax-preparation-cost-for-small-businesses-2026-data/ ; https://taxdome.com/blog/tax-preparation-cost-fees
- Medical billing pricing: https://neolytix.com/articles/what-is-the-going-rate-for-medical-billing-services/ ; https://www.getpracticehelp.com/medical-billing-rcm/medical-billing-cost-guide/
- Denial recovery contingency: https://www.mdclarity.com/comparison/best-denial-recovery-services ; https://rcrhub.com/hubbub/25-questions-ask-before-hiring-denial-management-company
- Denial / appeal statistics (AHA, MGMA via bilnow): https://bilnow.com/medical-billing-statistics/
- AMA 2026 prior authorization survey: https://www.ama-assn.org/press-center/ama-press-releases/ama-survey-prior-authorization-reform-pledge-falls-short-physicians
- AMA Physician Practice Benchmark (42.2% private practice, 2024): https://www.ama-assn.org/about/ama-research/physician-practice-benchmark-survey
- Claimable: https://www.globenewswire.com/news-release/2024/10/02/2956879/0/en/Claimable-Launches-First-Ever-AI-Powered-Appeals-Platform-to-Fight-Unjust-Healthcare-Denials.html ; Counterforce Health: https://www.nbcnews.com/news/us-news/ai-helping-patients-fight-insurance-company-denials-wild-rcna219008
- Immigration UPIL: https://www.cliniclegal.org/upil ; https://www.uscis.gov/scams-fraud-and-misconduct/avoid-scams/become-an-authorized-provider ; https://techcrunch.com/2025/11/26/justiguide-wants-to-use-ai-to-help-people-navigate-the-u-s-immigration-system
- Handbook / HR pricing: https://docbird.io/employee-handbook-cost ; https://rulewize.com/blog/employee-handbook-cost
- SOC 2 / vCISO pricing: https://www.trycomp.ai/hub/soc-2-cost-breakdown ; https://soc2auditors.org/insights/vciso-cost/ ; Vanta MSP program: https://cyberfortgroup.com/cyberfort-joins-vantas-managed-service-provider-partner-program/
- Translation: https://elis-survey.org/wp-content/uploads/2026/03/ELIS-2026-Report.pdf ; https://www.bloodinthemachine.com/p/ai-killed-my-job-translators
- Freelance labor-market studies: https://olin.washu.edu/about/news-and-media/news/2023/08/study-ai-tools-cause-a-decline-in-freelance-work-and-incomeat-least-in-the-short-run.php ; https://ideas.repec.org/p/ces/ceswps/_11276.html
- Resume pricing: https://www.resumeble.com/career-advice/resume-services-cost ; Editage: https://www.editage.com/services/english-editing/standard-editing-plan
- BizBuySell Q3 2026: https://investors.costargroup.com/news-releases/news-release-details/bizbuysell-releases-q3-2026-insight-report ; broker fees: https://www.clearlyacquired.com/blog/how-much-do-business-broker-fees-actually-cost-in-2026 ; licensing: https://www.midwest-brokers.com/business-broker-licensing-requirements-by-state-the-2026-reference-guide/
- SBA referral fees: https://commercialfinancereferrals.com/sba-loan-referral-fees ; https://starfieldsmith.com/2026/07/best-practices-working-with-referral-agents/
- Equipment finance commissions: https://sendstrike.ai/blog/heavy-equipment-financing-broker ; https://equipmentfinancenews.com/news/lender-operations/equipment-finance-brokers-last-wild-west-of-business/
- Trades recruiting: https://thebluecollarrecruiter.com/skilled-trades-hiring-costs-comparison-what-it-costs-to-hire-a-skilled-trades-worker-in-2026-recruit/ ; https://boostpoint.com/industries-skilled-trades/what-it-costs-to-recruit-skilled-trades-workers-2026/
- Freight: https://truckstop.com/blog/freight-broker-outlook-1h26/ ; https://www.usetenfold.ai/blog/ai-agents-in-freight-brokerage-whats-actually-changing-in-2026
- Insurance leads: https://insifter.com/guide-lead-costs.html ; CRE referral legality: https://www.tremgroup.com/real-estate-referral-fees-state-by-state-guide/
- AI affiliates: https://www.eesel.ai/blog/ai-affiliate-programs ; https://www.layer3labs.io/guides/best-ai-affiliate-programs
- Expert labeling pay: https://www.herohunt.ai/blog/mercor-2026-how-it-works-pay-alternatives/ ; https://aitraining.jobs/research/what-ai-labs-pay-for-human-data
- Skills marketplaces: https://www.totalum.app/blog/agent-skills-marketplaces-2026
- ServiceTitan 2026 AI survey: https://www.servicetitan.com/press/servicetitan-report-finds-74-of-residential-contractors-see-ai-as-key ; HousingWire: https://www.housingwire.com/articles/ai-adoption-residential-contracting/
- Workshop / keynote pricing: https://www.pertamapartners.com/insights/cost-per-employee-ai-training-budgeting ; https://www.consultclarity.org/post/keynote-speakers-association-conferences-usa
- AI readiness audit pricing: https://ariesconsultinggroup.com/blog/ai-readiness-audit-cost/
- KFF Medicare Advantage 2026: https://www.kff.org/medicare/medicare-advantage-in-2026-enrollment-update-and-key-trends/
- Estate docs: https://legaltemplates.net/resources/estate-planning/cost-of-estate-planning/ ; https://azstatewideparalegal.com/document-preparation-rates/
- Landlords / HOAs: https://www.baselane.com/resources/landlord-statistics ; https://www.apmhoa.com/blog/how-much-does-hoa-management-cost-2026
- Local gov AI: https://terencekok.com/blog/ai-governance-formalisation-local-government-adoption-gap/ ; https://www.spectrumgovtech.com/blog/ai-small-municipalities
- Newsletters: https://www.creatorspotlight.com/p/ryan-sneddon-naptown-scoop ; https://www.adweek.com/media/6am-city-layoffs-artificial-intelligence/
- YouTube policy: https://outlierkit.com/blog/youtube-ai-crackdown
- AI Overviews / pSEO: https://www.searchenginejournal.com/impact-of-ai-overviews-how-publishers-need-to-adapt/556843/ ; https://www.digitalapplied.com/blog/programmatic-seo-after-march-2026-surviving-scaled-content-ban
- AI referral conversion: https://citeproof.co/blog/llm-traffic-conversion-rate ; https://opollo.com/blog/the-2026-ai-search-benchmark-report/
- TCPA / AI voice: https://econsent.org/posts/ai-voice-agents-tcpa-rules-october-2026/
- Solo-founder cases: https://www.taskade.com/blog/one-person-companies
