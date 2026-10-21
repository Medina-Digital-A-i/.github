# Evidence-Weighted Paths to $1M Net Worth in Under 7 Years
## For a US individual with $0–10k, no audience, and a 24/7 AI agent team

**Prepared:** October 2026
**Framing:** This is a research memo, not a plan. Every probability below is the author's calibrated judgment, built from the cited base rates and labeled with the quality of the evidence behind it. Where evidence is thin (most of the "AI-augmented" claims, almost all vendor-blog numbers), it says so.

---

## 0. Executive summary (the short version)

1. **The base rate is brutal.** Only ~5% of US millionaires in the largest survey of them (Ramsey, n≈10,000) got there in 10 years or less; the median took 25–30 years ([Ramsey Solutions](https://www.ramseysolutions.com/retirement/how-to-become-a-millionaire)). Reaching $1M in under 7 years from ~$0 is a right-tail event for *any* path. The question is which paths have the fattest right tail per dollar of capital and per hour of human time, and which the AI team actually shifts.

2. **The academic literature is unambiguous that self-employment in general does not pay** (Hamilton 2000; Moskowitz & Vissing-Jørgensen 2002; Hurst & Pugsley 2011), **but equally unambiguous that a specific subgroup pays very well**: incorporated owners of employer firms in skill-intensive industries, selected on cognitive ability, prior industry experience, and willingness to work more hours (Levine & Rubinstein 2017; Smith, Yagan, Zidar & Zwick 2019; Azoulay et al. 2020). The returns are in the tail, and the tail is predictable from observable traits.

3. **Three structural facts dominate the ranking:**
   - **Owner-operator businesses are the only asset class where someone with $0 can own a $1M+ asset in a few years**, because (a) the SBA 7(a) program lends ~80–90% of purchase price with 10% equity injection, and (b) small-business cash flow trades at only ~2.6x (BizBuySell 2025) while the owner's labor earns the whole cash flow.
   - **Services businesses are what the AI team can run.** The Anthropic Economic Index shows the fastest-growing fully automated API workflows are business sales/outreach and document/code production; the human bottleneck that remains is trust-based selling and relationship holding.
   - **Intermediation (commissions on others' transactions) has the highest income-to-capital ratio in the economy**, but every intermediation market (recruiting, insurance, business brokerage, real estate, freight) shows a steep, slow ramp and a median earner who is poor. The AI team compresses the ramp; it does not remove the selling.

4. **Ranked top 5 (author's probability of $1M net worth within 7 years, conditional on sustained full-time effort by a capable person):**
   1. Niche, productized B2B service firm run by AI agents, built explicitly to (a) throw off $150–400k/yr SDE and (b) fund an SBA acquisition in years 2–4 ("service-to-acquire stack"): **~12–18%**
   2. Self-funded search / SBA 7(a) acquisition of a $300k–$700k SDE business, once ~$50–100k cash exists: **~10–15% unconditional from $0; ~35–45% conditional on closing a sound deal**
   3. Contingency recruiting / specialized staffing firm with AI-run sourcing: **~8–12%**
   4. Commercial-lines insurance brokerage (build a book, sell at 2–3x commissions): **~7–10%**
   5. Federal/state government contracting in services (subcontract → prime, set-asides): **~5–8%**

   Everything else (micro-SaaS, enterprise sales W-2, startup employee, VC-backed startup, real estate agent, e-commerce, creator) scores lower on probability, evidence, or both; details in Section 5.

---

## 1. What the academic literature says about returns to entrepreneurship

### 1.1 The median entrepreneur earns less (the "puzzle")

**Hamilton (2000, *JPE*)**, using SIPP panel data, found that most self-employed people earn less than they would in paid employment, with the earnings gap growing over time: the median self-employed worker's earnings after ten years in business trail those of a comparable employee by roughly a third, and initial earnings and earnings growth are both lower. Only the upper quartile of the self-employed distribution out-earns paid employment. Hamilton's interpretation is that nonpecuniary benefits ("being your own boss") compensate for the gap ([WashU profile](https://profiles.wustl.edu/en/publications/does-entrepreneurship-pay-an-empirical-analysis-of-the-returns-to/); [paper PDF](https://www.edegan.com/pdfs/Hamilton%20(2000)%20-%20Does%20Entrepreneurship%20Pay%20An%20Empirical%20Analysis%20Of%20The%20Returns%20To%20Self%20Employment.pdf)). Evidence quality: **high** (peer-reviewed, panel data, widely replicated internationally).

**Moskowitz & Vissing-Jørgensen (2002, *AER*)** showed that despite entrepreneurial households holding more than 70% of their private-equity wealth in a single actively-managed firm, and despite roughly two-thirds of such firms failing within a decade, the aggregate return to private equity is *no higher* than public equity. Given the undiversified risk, a rational investor would demand at least ~10 percentage points per year more. The candidate explanations are nonpecuniary benefits, preference for skewness, and overestimated survival odds ([AER](https://www.aeaweb.org/articles?id=10.1257%2F00028280260344452); [NBER w8876](https://www.nber.org/papers/w8876)). Evidence quality: **high**, though the data are 1989–1998 SCF.

**Hurst & Pugsley (2011, *Brookings Papers*)** documented why: most small businesses are not trying to grow. Over 50% of new owners cite nonpecuniary reasons as the primary motive; only 34% cite income; most have no intention to add employees or innovate, and are concentrated in a handful of local-service industries (skilled trades, restaurants, real estate, professional practices) where the owner is essentially selling their own labor ([NBER w17041](https://www.nber.org/system/files/working_papers/w17041/w17041.pdf); [Brookings](https://www.brookings.edu/wp-content/uploads/2011/09/2011b_bpea_hurst.pdf)). Evidence quality: **high**.

**Scott Shane, *The Illusions of Entrepreneurship* (2008)** synthesized the survey evidence: the typical US startup is undercapitalized (most start with well under $100k; firms started with >$100k have materially better survival), is in a low-growth retail or personal-service industry, and the typical founder of a ten-year-old firm earns about 65% of what they would have earned as an employee ([SSRN](https://www.ssrn.com/abstract=1081323); [Shane 2008 slides](https://www.researchgate.net/profile/Silburn-Clarke/post/I_am_studying_the_role_of_Business_Advisory_Centres_in_the_retention_of_micro_small_businesses_in_Ghana_Pls_suggestions_of_works_to_consult/attachment/59d6278579197b8077985ce8/AS%3A326127366230016%401454766231063/download/Shane+ppt+The+illusion+of+entrepreneurship+-+lessons+from+US+public+policy.pdf)). Evidence quality: **medium-high** (synthesis of government surveys; some figures now dated).

**Åstebro (2003, *Economic Journal*)** on independent inventors is the cleanest demonstration of skewness: the distribution of returns to independent invention has a negative median but positive mean, with a tiny fraction of projects generating almost all of the aggregate return — consistent with "skewness-loving" rather than rational expected-value investing ([Åstebro bibliography](https://ideas.repec.org/a/eee/jbvent/v29y2014i1p88-105.html)). Åstebro, Chen & Thompson's "Stars and Misfits" (*Management Science*, 2011) found self-employment entry concentrated at both ends of the ability distribution — the very able (stars) and those poorly matched to wage work (misfits) ([FIU](https://digitalcommons.fiu.edu/economics_wps/24/)). Evidence quality: **high** for the shape of the distribution.

**Survival base rates.** BLS Business Employment Dynamics data: roughly 80% of new employer establishments survive 1 year, ~50% survive 5 years, ~35% survive 10 years; the spread by industry is modest (5-year survival ranges from ~45% in information to ~62% in agriculture) ([Census BDS StatBrief](https://www.census.gov/content/dam/Census/library/publications/2010/ADRM/CES/BDS_StatBrief4_Exit_Survival.pdf); [BLS summaries](https://workspace369.com/research/small-business-survival-rate-statistics/)). Note: "exit" ≠ "failure"; a meaningful share of exits are sales. Evidence quality: **high** for the numbers; **low** for inferring financial failure.

### 1.2 The incorporated subgroup earns substantially more — and is predictable

**Levine & Rubinstein (2017, *QJE*, "Smart and Illicit")** is the pivotal paper. Splitting the self-employed by legal form in NLSY79 and CPS data:

- The median **incorporated** self-employed person earns about **50% more per hour and works about 25% more hours** than the median salaried worker; median hourly earnings of the incorporated are ~80% above the unincorporated and ~35% above salaried employees (CPS tabulations, Table I: median hourly earnings $24.6 incorporated vs $18.0 salaried vs $13.8 unincorporated; annual hours 2,331 vs 1,976 vs 1,936).
- The median **unincorporated** self-employed earns ~15% *less* per hour than a salaried worker.
- Earnings **rise at every decile** of the distribution when an individual transitions into incorporated self-employment — this is not just a tail effect.
- Who becomes incorporated: higher AFQT (cognitive) scores, more education (46% college grads vs 33% of salaried), higher adolescent self-esteem, *and* higher adolescent "illicit" risk-taking index. The combination of "smart and illicit" predicts both entry and the earnings premium.
- Occupational content: incorporated owners do nonroutine cognitive work (managers, professionals); unincorporated owners do manual work (carpenters 9.2%, truck drivers 4.6%, mechanics 3.5%).
- Importantly, 85% of those who end up incorporated started their self-employment spell *unincorporated* — i.e., successful owners usually begin informally and incorporate as they grow.

([QJE](https://econpapers.repec.org/RePEc:oup:qjecon:v:132:y:2017:i:2:p:963-1018.); [NBER w19276](https://www.nber.org/system/files/working_papers/w19276/w19276.pdf); figures extracted from the published PDF.) Evidence quality: **high**.

**Smith, Yagan, Zidar & Zwick (2019, *QJE*, "Capitalists in the Twenty-First Century")** used the universe of US tax returns. In 2014, 69% of the top 1% and 84% of the top 0.1% of income earners received pass-through business income. Roughly three-quarters of top pass-through profit is a return to the owner's *human capital* (it collapses when the owner dies or retires), not to financial capital. The typical top-1% business owner is a working-age, undiversified owner of a mid-market firm in a skill-intensive industry — the paper's examples include regional auto dealers, beverage distributors, law/consulting/medical practices and specialty contractors; there are over 1.1 million pass-through owners with fiscal income above $390k ([NBER w25442](https://www.nber.org/system/files/working_papers/w25442/w25442.pdf); [BFI brief](https://bfi.uchicago.edu/wp-content/uploads/BFI_RB_Zwick_201926.pdf); [QJE](https://academic.oup.com/qje/article-abstract/134/4/1675/5542244)). Evidence quality: **very high** (administrative data).

**Azoulay, Jones, Kim & Miranda (2020, *AER: Insights*)**: using Census/IRS administrative data on all US founders, the mean age at founding for the fastest-growing 0.1% of new firms is **45.0**; founders in their 20s are *less* likely to succeed; and **prior experience in the specific industry** is one of the strongest predictors of high growth ([SSRN](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=3158929); [AER: Insights](https://pubs.aeaweb.org/doi/pdfplus/10.1257/aeri.20180582)). Evidence quality: **very high**.

**Guzman & Stern (2015, *Science*)**: observable characteristics at registration (Delaware incorporation, trademark/patent filing, non-eponymous name, corporate rather than LLC form) predict growth outcomes well — 76% of all IPO/major-acquisition outcomes fall within the top 5% of predicted "entrepreneurial quality" — but even in the top 1% of quality, only ~5% achieve a growth outcome ([Science](https://www.science.org/doi/abs/10.1126/science.aaa0201); [MIT News](https://news.mit.edu/2015/which-high-tech-firms-thrive-0205)). Evidence quality: **high**.

### 1.3 What actually predicts high returns (synthesis)

| Predictor | Direction | Strength of evidence | Source |
|---|---|---|---|
| Incorporation / employer firm (vs solo unincorporated) | Strongly positive; ~50% hourly premium at median | Very strong | Levine & Rubinstein 2017 |
| Nonroutine cognitive content of the business (vs manual) | Strongly positive | Very strong | Levine & Rubinstein; Smith et al. |
| Cognitive ability (AFQT), education | Positive, mediated through incorporation | Strong | Levine & Rubinstein |
| Risk tolerance / rule-breaking disposition | Positive | Strong (NLSY) | Levine & Rubinstein |
| Prior wage level / prior experience in the same industry | Positive; one of strongest predictors of top-growth firms | Very strong | Azoulay et al. 2020 |
| Age (mid-career, ~40s) | Positive for high-growth outcomes | Very strong | Azoulay et al. |
| Hours worked | Positive (incorporated owners work ~25% more hours) | Strong | Levine & Rubinstein; Hamilton |
| Industry: skill-intensive B2B/professional services, distribution, specialty contracting | Positive for top-1% income | Very strong | Smith et al. 2019 |
| Industry: retail, restaurants, personal services | Negative (low margins, no growth intent) | Strong | Hurst & Pugsley; Shane |
| Starting capital > ~$100k | Positive for survival | Medium | Shane 2008; Kauffman Firm Survey |
| Growth intent at founding | Positive | Strong | Hurst & Pugsley |
| Formal registration signals (Delaware C-corp, IP) | Positive for venture-scale outcomes | Strong | Guzman & Stern |

**Bottom line for this question:** The literature says *do not become a self-employed laborer*; *do become an incorporated owner of a skill-intensive business with employees (or agents), in an industry you know, working hard*. The $1M outcome is in the tail, but the tail is ~5–10x more likely for people with these traits than for the average entrant.

---

## 2. Who gets to $1M fast? Occupations and business types with fat right tails at low capital

### 2.1 Surveys of millionaires

- **Ramsey Solutions National Study of Millionaires (2017–18, n≈10,167)**: top occupations are engineer, accountant, teacher, management/sales, attorney; 79% received no inheritance; only 31% averaged $100k/yr over their careers; **only 5% reached $1M in ≤10 years**, and the typical path took 25–30 years to age ~50 ([Ramsey](https://www.ramseysolutions.com/retirement/the-national-study-of-millionaires-research); [Ramsey "how to become a millionaire"](https://www.ramseysolutions.com/retirement/how-to-become-a-millionaire)). **Caveat:** non-random, self-selected sample from a personal-finance audience, skewed toward 401(k) savers; it under-samples business owners and over-samples salaried savers. Evidence quality: **medium-low** for population inference, but it is the largest sample on *time-to-$1M*, and the 5% figure is the key base rate.
- **Stanley & Danko, *The Millionaire Next Door* (1996)**: the self-employed are <20% of workers but about two-thirds of millionaires (figure varies by edition/definition; a later tabulation gives 33%), concentrated in "dull-normal" businesses — welding contractors, pest control, paving, dry cleaning ([Spokesman-Review 1998](https://www.spokesman.com/stories/1998/jun/28/meet-the-millionaire-next-door-one-surprising/)). Evidence quality: **medium** (dated, proprietary survey).
- **Wealth-X (2016–2019)**: ~68% of the global ultra-wealthy and 62% of US billionaires are self-made; finance/investing produced ~20% of self-made US billionaires, with technology close behind ([CNBC](https://www.cnbc.com/2019/09/26/majority-of-the-worlds-richest-people-are-self-made-says-new-report.html); [Entrepreneur](https://www.entrepreneur.com/leadership/62-percent-of-american-billionaires-are-self-made/269593)). Evidence quality: **medium** (proprietary), and irrelevant to the $1M question except to confirm the industries with the fattest tails.
- **Fed SCF 2022**: 20% of families own a business (record high); business equity is highly concentrated at the top of the wealth distribution; the median nonemployer business is worth $0 while the median business with >5 employees is worth $400k ([Federal Reserve](https://www.federalreserve.gov/publications/october-2023-changes-in-us-family-finances-from-2019-to-2022.htm)). Evidence quality: **very high**.

### 2.2 IRS top-income mobility

Auten, Gee & Turner's IRS panel work shows ~40% of people in the top 1% in a given year are out of it the next year, and ~60% are out within a decade; Splinter & Larrimore (2026) show two-decade mobility reduces measured top-0.1% shares by >20% ([Splinter summary](https://davidsplinter.com/TopMobility.html); [Fed FEDS 2026-015](https://www.federalreserve.gov/econres/feds/files/2026015pap.pdf)). The relevant point: **entry into the top 1% ($400k+ income) is common and often transient**, driven disproportionately by business sales and lumpy pass-through income — exactly the $1M-net-worth-generating event. Evidence quality: **high**.

### 2.3 Occupation-level right tails (for a person with no capital)

| Occupation / business | Median | Right tail | Ramp to right tail | Evidence quality |
|---|---|---|---|---|
| Enterprise SaaS AE (W-2) | Median OTE ~$280k; only ~39% hit quota | Top performers $670k+ | 2–4 yrs from SDR; requires getting hired | Medium ([RepVue](https://www.repvue.com/salaries/enterprise-account-executive)) |
| Realtor | Gross $59k; **62% of agents with ≤2 yrs earned <$10k**; net $37k | 33% gross >$100k; 16+ yr agents $88.5k median | 5–10 yrs | High ([NAR 2026 Member Profile](https://www.nar.realtor/news/economists-outlook/the-feature-sheet-2026-member-profile)) |
| Independent P&C insurance agent | $60–80k | $300k+ with a renewing book; book sells at 1.5–3x commissions | 3–5 yrs | Low-medium (vendor data) ([Renegade](https://renegadeinsurance.com/insurance-agency-valuation/)) |
| Contingency recruiter | Unknown; high attrition | Solo recruiters doing 10+ placements/yr at 20–25% of salary earn $200–400k | 1–3 yrs | Low (vendor blogs; SHRM fee benchmarks) |
| Business broker | ~20–30% of listings sell; "5–10 deals/yr → $100–200k" | Top brokers on $1–5M deals earn $500k+ | 2–4 yrs | Low-medium ([IBBA guide](https://www.ibba.org/wp-content/uploads/2021/01/ibba-guide-business-brokerage-profession.pdf)) |
| Freight agent | $30–60k yr 1 | $150k+ on a $2M book | 3+ yrs | Low |
| Early startup employee (hire #1–10) | Hire #1 median 1.49% FD equity, falling to ~0.3% by hire #5 | Need a $300M+ exit and survive dilution for a $1M outcome | 5–8 yrs | Medium ([Carta](https://carta.com/data/equity-report-2024/)) |
| Search fund CEO (traditional) | — | Median equity earned per exited CEO **$2.25M**; mean $5.7M | 2 yr search + 5–7 yr hold | High ([Stanford 2024](https://cdn.prod.website-files.com/6455268783d6938b9451ea80/669fbcb3e5f07cc9a6093751_StanfordGSB_Study_2024.pdf)) |
| VC-backed founder | ~75% of founders exit with $0 equity (Hall & Woodward 2010, *AER*) | Mean payoff ~$5.8M, median ~$0 | 7–10 yrs | High |

The pattern is consistent across every commission/intermediation occupation: **a poor median, a fat tail, a multi-year ramp, and attrition that removes most entrants before the ramp pays off.** The right question for an AI-augmented operator is whether the agents can compress the ramp (sourcing, outreach, documentation, follow-up) — the evidence says yes for the *work* and no for the *trust*.

---

## 3. Entrepreneurship Through Acquisition (ETA)

### 3.1 Traditional search funds (Stanford data)

Primary source: Stanford GSB *2024 Search Fund Study* (data through Dec 2023, 681 funds) and *2026 Study* (through Dec 2025, 862 funds).

- **Aggregate IRR 35.1%, ROI 4.5x** (2024); **33.9% IRR, 4.75x** (2026). Excluding the top 5 funds, IRR ~33% and ROI ~3.2x. Exited funds: 42.9% IRR.
- **Only 63% of concluded searches acquire anything** (57% for recent cohorts; ~48% for 2021–24 cohorts per secondary reports). Of those that acquire: **31% lose money** (66% of those partial, 34% total), 27% return 1–2x, 36% 2–5x, 25% 5–10x, **11% >10x**.
- **Median deal: $14.4M purchase price, 7.0x EBITDA, 27% EBITDA margin, 25% growth, 34 employees.** Searchers are 79% ≤35 years old; mean search salary $139k; median first-year CEO salary $190k.
- **Searcher economics:** mean equity earned per *exited* CEO $5.7M, **median $2.25M**; for still-operating CEOs mean $6.09M, median $1.98M.
- Partnered searches: 40.5% IRR vs solo ~lower, but 5 of 6 recent 10x+ outcomes were solo searchers.

([Stanford 2024 Study PDF](https://cdn.prod.website-files.com/6455268783d6938b9451ea80/669fbcb3e5f07cc9a6093751_StanfordGSB_Study_2024.pdf); [Stanford GSB insights](https://www.gsb.stanford.edu/insights/search-funds-show-strong-performance-acquisitions-returns); [Stanford 2026 Primer](https://cdn.prod.website-files.com/6455268783d6938b9451ea80/6a0c69fbc5155d301022362d_2026%20A%20Primer%20for%20Search%20Funds_vFinal.pdf))

**Counter-evidence:** Yale SOM (Oct 2025, 1,192 deal-level observations) found **58% of deal-level MOICs fall in 0–1.99x and only 2% exceed 10x**, with weighted-average MOIC ~2.5–2.8x — i.e., the Stanford aggregate is heavily driven by a few outliers and by survivorship/self-reporting ([Yale SOM case](https://som.yale.edu/sites/default/files/2025-10/How%20are%20Search%20Fund%20Investors%20Really%20Faring.pdf)). Evidence quality: **medium-high** (self-reported but long-running, with a credible critical replication).

**Implication for the searcher (not the investor):** combining the 63% close rate with the 69% gain-conditional-on-close rate, roughly **43% of people who launch a traditional search end up with a gain, and the median gain among exits is $2.25M of equity**. The searcher's personal downside is ~2 years of a $139k salary (paid by investors) — this is the single best-documented low-capital path to a seven-figure outcome in the entire literature, with the obvious caveat that the gate is credential-based (investors back MBAs from a short list of schools) and the timeline is 7–10 years, not 7.

### 3.2 Self-funded search / SBA 7(a) acquisitions (the version open to someone with $0–10k)

**Market facts (quality: medium; primary SBA data exist but most tabulations are third-party):**
- SBA approved ~78,000 7(a) loans worth $37.3B in FY2025, of which roughly **7,000 loans / $8.3B were change-of-ownership (acquisition) loans, average ~$1.18M, up ~35% YoY** ([CT Acquisitions tabulation of SBA data](https://ctacquisitions.com/guides/sba-7a-acquisition-lender-rankings-2024-2026/); [SOP 50 10 8 summary](https://www.whitefordlaw.com/news-events/client-alert-sba-issues-sop-50-10-8-key-changes-impacting-sba-7a-lending)).
- Since **June 1, 2025 (SOP 50 10 8)**, the SBA reinstated a **10% minimum equity injection** on total project cost; a seller note on **full standby** can count for up to half of it, so the buyer's true minimum cash is ~5% of project cost. 2025 survey data: ~45% of deals include a seller note, but only ~9% of seller notes are full-standby ([angelinvestorsnetwork](https://angelinvestorsnetwork.com/capital-raising/sba-7a-acquisition-financing-zero-down-myth-2026); [commerciallendingx](https://www.commerciallendingx.com/blog/seller-note-full-standby-what-buyers-need-to-know)). **"Zero down" is effectively dead**; a $1M deal needs ~$50–100k of buyer cash (or investor equity, which is permitted).
- **Multiples:** BizBuySell 2025 full-year: median sold price $350k, median cash flow $158,950, median revenue $703k, **average cash-flow multiple 2.61x**; services businesses had the strongest demand ([BizBuySell 2025 recap](https://www.bizbuysell.com/blog/2025-year-in-review/)). Insurance agencies trade at 1.5–3x commissions; HVAC/plumbing owner-operators at 2–3.5x SDE while PE platforms pay 9–13x EBITDA (the arbitrage behind roll-ups) ([beancount guide](https://beancount.io/blog/2026/07/11/hvac-plumbing-private-equity-roll-up-guide)).
- **Default rates:** acquisition loans default *less* than other 7(a) uses. Yale (2025): 1.22%/yr for acquisition vs 1.64% other (2019–23); GoSBA tabulation of 2020–25 loans: 0.71% change-of-ownership vs 1.99% startups; lifetime charge-off for 2018–19 acquisition cohorts ~6.9% by count vs 9.8% for all other 7(a). Program-wide trailing-12-month default hit 4.8% in March 2026, the highest since 2013 — the cycle is turning ([Yale SOM case](https://som.yale.edu/sites/default/files/2025-04/Exploring%20and%20Understanding%20the%20U.S.%20Small%20Business%20Administration%207(a)%20Loan%20Program.pdf); [GoSBA](https://gosbaloans.com/guide/sba-loan-default-rates-by-loan-use/); [Lumos](https://www.lumosdata.com/blog/sba-default-rates-small-business-credit-risk-2026)). Evidence quality: **medium-high** (SBA data, several independent tabulations agree on direction).
- **Self-funded searcher returns:** the only dataset is the Search Investment Group's self-funded study (investor-reported, no independent audit): median investor IRR 25–30%, 5% capital-loss rate, searchers retaining 60–80%+ of common equity in most deals; traditional search excludes self-funded deals from its series ([smash.vc](https://smash.vc/search-fund-statistics/); [Peony](https://www.peony.ink/blog/search-fund-guide)). Evidence quality: **low** (small, selected, vendor-adjacent).
- **Silver tsunami:** estimates of Boomer-owned businesses range 2.3–3M (Project Equity) to 12M including micro-firms; McKinsey (Apr 2026) projects ~6M SMB transitions by 2035 with >1M viable for sale; 58% of Boomer owners say they want to sell by 2030, and only 30–54% have a succession plan ([Forbes](https://www.forbes.com/sites/alisoncoleman/2026/01/14/the-silver-tsunami-is-reshaping-small-business-why-exit-planning-cant-wait/); [Teamshares](https://www.teamshares.com/resources/silver-tsunami/)). Evidence quality: **medium** (projections; direction robust, magnitudes soft). Supply is real but the SBA-financeable segment ($300k–$2M SDE) is also where buyer competition and PE roll-ups are most intense.

### 3.3 Can an AI-augmented operator buy a $300k–$1M SDE business with little money down?

**Arithmetic (illustrative, $400k SDE business at 2.75x = $1.1M price, ~$1.2M project cost):**
- SBA 7(a): ~$960k at ~10% (prime + 2.75%, 10-yr amortization) → ~$152k/yr debt service.
- Seller note (full standby, counts toward injection): $60k.
- Buyer cash injection: $60k (5%) — plus working capital and ~$30–50k of closing costs/SBA guarantee fee. **Realistic cash need: $90–130k.**
- Post-close: $400k SDE − $152k debt service − $80k replacement manager/owner salary buffer = ~$170k free cash before taxes, if SDE holds.
- Equity build: principal paydown ~$60–80k/yr + retained cash + any SDE growth. If the business grows SDE 10%/yr and is resold at 3x in year 5, equity ≈ $1.1–1.5M. If SDE falls 20%, the DSCR drops below 1.25 and the owner is in a workout.

**Why "little money down" is still the binding constraint:** the 10% injection on a $1.2M project is $120k; a half-standby seller note cuts the cash to $60k only if the seller agrees to a 10-year full-standby note, which ~91% do not. The realistic answer is that someone starting at $0 must first generate ~$75–150k (Section 5's #1 path exists for this reason) or raise it from self-funded-search investors, who typically take 10–30% of common equity plus a preferred return.

**What AI agents change:** deal sourcing (scraping listings, proprietary outreach to the ~2.3M+ Boomer owners), financial-statement normalization/QoE-lite, LOI drafting, lender packaging, SOP drafting, and post-close back-office (bookkeeping, scheduling, invoicing, marketing). Evidence that this changes *outcomes* is **anecdotal only** as of 2026. The deal still requires an SBA lender to underwrite the *person* (credit score, relevant experience, personal guarantee), and the 2025 SOP tightening (10% injection; lending on trailing not projected numbers) shows the regulator is moving *against* thin-equity, inexperienced buyers ([mmcg](https://www.mmcginvest.com/post/sba-stopped-lending-on-projections-sop-50-10-8-1-closes-acquisition-loans-on-last-year-s-numbers)).

**Verdict:** The acquisition route is the best-evidenced low-capital path to a seven-figure equity position — but it is a *second* step. From $0–10k it is not financeable in year 1. The probability of a sound close for a well-prepared self-funded searcher is perhaps 35–50% within 18 months of starting a search (the traditional-search 57–63% close rate is a ceiling; self-funded searchers have no salary and often quit), and conditional on close, ~65–70% end with a gain (Stanford) with median searcher equity in the low seven figures at a 5–7-year exit.

---

## 4. High income-to-capital activities an AI team can substantially run in 2026

**What the usage data show.** The Anthropic Economic Index reports that augmentation (~52%) now edges automation (~45%) in consumer usage, but that *API* workflows are far more directive/automated and that the fastest-growing fully automated API categories between Nov 2025 and Feb 2026 were **business sales/outreach automation** and **trading/market operations**, each roughly doubling; the highest task-exposure occupations are programmers, customer-service reps, data-entry, medical-records and market-research analysts ([Anthropic Economic Index](https://www.anthropic.com/news/the-anthropic-economic-index); [Anthropic labor-market measure](https://www.anthropic.com/research/labor-market-impacts); [secondary summary](https://agentmarketcap.ai/blog/2026/04/09/anthropic-economic-index-2026-ai-agent-occupation-substitution)). Evidence quality: **medium-high** for *what AI is used for*; **none** for *business outcomes of AI-run firms*. Every "one-person $1M ARR with agents" claim found (Levels, Polsia, Medvi, Base44) is a founder's self-report, several contradicted by other reports (Base44 had ~8 employees at sale) ([taskade](https://www.taskade.com/blog/one-person-companies); [agentmarketcap](https://agentmarketcap.ai/blog/2026/04/09/solo-founder-ai-agent-stack-1m-arr)). Treat as **anecdote**.

**The screening rule:** the AI team is most valuable where the *deliverable* is text/code/analysis, the *buyer* is a business that pays on value not hours, and the *scarce input* was previously skilled labor. It is least valuable where the scarce input is a license, a relationship, physical presence, or regulated advice.

| Activity | Income/capital ratio | Share AI can run | Human bottleneck | Evidence on economics |
|---|---|---|---|---|
| **Productized B2B services** (compliance docs, SOC2/ISO readiness, grant/RFP writing, outbound lead-gen for a vertical, bookkeeping/CFO-lite, technical writing, localization, data pipelines) | Very high (capital = laptop + subscriptions) | 70–90% of delivery; 50–80% of marketing | Closing, QA, accountability | Medium: MBO Partners 2025: 5.6M independents earn >$100k (≈8% of all independents; up 19% YoY) ([MBO 2025](https://info.mbopartners.com/rs/mbo/images/MBO_2025_State_of_Independence_Research_Report.pdf)); agencies sell at 2–4x SDE |
| **Government contracting (services)** | High; set-asides and SBIR give price protection | 60–80% (capture research, proposal drafting, compliance matrices, past-performance writeups) | Registrations, teaming relationships, contracting-officer trust | Medium: $178B to small business FY23, but **only 1.4% of dollars to first-time primes**; new small entrants down ~60% in a decade; small-contractor margins ~8% vs 20–24% for large; SBIR Phase I ~16–17% award rate ([SBA](https://www.sba.gov/article/2024/04/29/biden-harris-administration-awards-record-breaking-178-billion-federal-procurement-opportunities); [Third Way](https://www.thirdway.org/report/12-solutions-for-small-business-success-in-federal-contracting); [Deltek](https://www.deltek.com/en/government-contracting/guide/pricing/profit-margin-government-contracts)) |
| **Compliance / regulatory work** (SOC2, HIPAA, CMMC, state licensing, privacy) | High | 60–80% | Auditor relationships, liability; some work is licensed (CPA, attorney) | Low-medium (no distributional data; strong demand signals from CMMC 2.0 and state privacy laws) |
| **Contingency recruiting / staffing** | Very high (fees 15–25% of first-year salary; retained 25–35%) | 70–85% (sourcing, screening, scheduling, follow-up) | Candidate trust, client trust, negotiation | Medium for fees ([SHRM via Manatal](https://www.manatal.com/blog/recruitment-fees)); **low** for income distribution |
| **Insurance brokerage (commercial lines)** | Very high; recurring 10–15% commissions, book sells at 1.5–3x | 50–70% (quoting, servicing, renewals, marketing) | Licensing (easy), carrier appointments (hard without a book), relationship sales | Low-medium (vendor data) |
| **Business brokerage / M&A advisory** | Very high (8–12% of sale price on <$1M; Lehman above) | 60–80% (valuation, CIM writing, buyer outreach, data room) | Seller trust, licensing in some states, 20–30% of listings actually sell | Low-medium ([IBBA](https://www.ibba.org/wp-content/uploads/2021/01/ibba-guide-business-brokerage-profession.pdf)) |
| **Lead generation / pay-per-lead** | High | 70–90% | Ad platform policy risk, buyer churn | **Low** (no credible data found; vendor-driven) |
| **Micro-SaaS** | High; sells at ~3.9x profit (Acquire.com Jan 2026) with 71% margins | 80–95% of build; 40–60% of distribution | Distribution, churn | Medium ([Acquire.com](https://blog.acquire.com/acquire-com-biannual-acquisition-multiples-report-jan-2026/)); sub-$100k deals trade at only 1.7–2.2x on Flippa |
| **Freight brokerage** | Moderate (13–15% gross margin, 35–70% splits) | 60–80% | Carrier/shipper relationships; thin margins | Low |
| **Real estate brokerage** | Moderate | 40–60% | Licensing, local presence, showings | High (NAR); poor median |

**Where the AI team moves the needle most:** the first three rows. These are businesses whose cost structure was 60–80% skilled labor, whose pricing is value-based, and whose customers are B2B. Reducing labor cost to near zero turns a 20–30% margin consultancy into a 60–80% margin one with the same price point; that margin is what funds the acquisition in Section 3.

---

## 5. Scored table, ranking, and defense of the top 3

### 5.1 Scoring (1 = worst, 5 = best; P = author's probability of ≥$1M net worth within 7 years, conditional on a capable person's full-time, sustained effort starting from $0–10k)

| # | Path | Capital needed (5=least) | Time to $10k/mo (5=fastest) | P($1M in 7 yrs) | AI share (5=most) | Cold selling needed (5=least) | Evidence quality (5=best) | Composite |
|---|---|---|---|---|---|---|---|---|
| 1 | **Niche productized B2B service firm → fund SBA acquisition ("service-to-acquire stack")** | 5 | 4 (6–12 mo) | **12–18%** | 4 | 2 | 3 | 18 |
| 2 | **Self-funded search / SBA 7(a) acquisition, $300k–700k SDE** (requires ~$75–150k first) | 2 | 3 (at close; 12–24 mo) | **10–15% uncond.; 35–45% cond. on sound close** | 3 | 3 | 4 | 15 |
| 3 | **Contingency recruiting / niche staffing** | 5 | 4 (3–9 mo for first placements) | **8–12%** | 4 | 1 | 2 | 16 |
| 4 | **Commercial-lines insurance brokerage** (build book, sell at 2–3x) | 4 | 2 (18–36 mo) | **7–10%** | 3 | 1 | 2 | 12 |
| 5 | **GovCon services (sub → prime, set-asides, SBIR)** | 4 | 2 (12–30 mo) | **5–8%** | 4 | 3 | 3 | 16 |
| 6 | **Enterprise SaaS sales (W-2) + aggressive saving + side acquisition** | 5 | 3 (OTE ramp 12–24 mo) | **5–8%** | 2 | 2 | 4 | 16 |
| 7 | **Micro-SaaS portfolio built by agents, sold at 3–4x** | 5 | 2 | **4–6%** | 5 | 3 | 3 | 18 (but low P) |
| 8 | **Business brokerage / Main-Street M&A advisory** | 5 | 2 | **4–6%** | 4 | 1 | 2 | 14 |
| 9 | **Pay-per-lead / local lead-gen for home services** | 4 | 3 | **3–5%** | 5 | 2 | 1 | 15 |
| 10 | **Real estate agent (residential)** | 4 | 1 | **3–4%** | 2 | 1 | 5 | 13 |
| 11 | **E-commerce / Amazon FBA brand** | 2 | 2 | **2–4%** | 3 | 4 | 3 | 14 |
| 12 | **Early employee (#1–10) at a VC-backed startup** | 5 | 3 (salary) | **2–3%** | 1 | 4 | 3 | 16 |
| 13 | **Creator / affiliate / SEO content** | 5 | 1 | **1–3%** | 4 | 4 | 1 | 15 |
| 14 | **VC-backed startup founder** | 3 | 1 | **1–3%** (but fattest tail) | 4 | 2 | 5 | 15 |
| 15 | **Freight brokerage / independent agent** | 4 | 2 | **1–2%** | 3 | 1 | 1 | 11 |

Composite is additive and purely indicative; the ranking below weights probability and evidence quality much more than the composite does.

**Calibration notes on the probabilities.** The population base rate for anyone to reach $1M in ≤7 years from ~$0 is well under 1% (5% of millionaires did it in ≤10 years, and millionaires are ~12% of households). Conditioning on a capable, full-time, incorporated operator with strong cognitive skills and an AI team raises every estimate roughly an order of magnitude; the top rows are meant to be ~10–20x the population base rate, not 50x. The spread between the top path and the median path (~3–5%) is smaller than most people assume; the spread in *evidence quality* is larger.

### 5.2 Ranking

1. **Service-to-acquire stack** (productized B2B service → SBA acquisition)
2. **Self-funded search / SBA acquisition** (as a stand-alone, for someone who can raise the injection)
3. **Contingency recruiting / niche staffing**
4. Commercial insurance brokerage
5. GovCon services
6. Enterprise sales W-2 ladder
7. Micro-SaaS portfolio
8–15. The rest, in the order of the table.

### 5.3 Defense of the top 3

#### Rank 1 — Niche productized B2B service firm, built to fund an acquisition

**Why it ranks first.** It is the only path that (a) needs no capital, (b) matches the Levine-Rubinstein/Smith et al. profile exactly (incorporated, skill-intensive, nonroutine cognitive, B2B, owner working long hours), (c) is the business type whose cost structure AI agents collapse most completely, and (d) produces the two things the acquisition path needs — ~$100k of cash and a track record of running a P&L — within 12–24 months. It also has a sellable terminal value on its own: agencies and productized services trade at ~2–4x SDE, and Acquire.com data show 3.9x profit for the SaaS-like end of the spectrum.

**Evidence for the income claim.** MBO Partners: 5.6M independents earned >$100k in 2025 (up 19% in a year; 5.8M in 2026) — roughly 8% of all independents, higher among full-time business-service providers ([MBO 2025](https://info.mbopartners.com/rs/mbo/images/MBO_2025_State_of_Independence_Research_Report.pdf); [Forbes](https://www.forbes.com/sites/elainepofeldt/2025/10/29/six-figure-self-employment-surges-report-finds/)). Smith et al.: professional/consulting services are among the most common top-1% pass-through businesses. IRS SOI: professional, scientific and technical services is the largest sole-proprietor profit sector (~25% of all Schedule C profit) ([IRS SOI](https://www.irs.gov/statistics/soi-tax-stats-nonfarm-sole-proprietorship-statistics)). Evidence that AI *specifically* lifts the odds: **anecdotal**; the strongest support is indirect (Anthropic index showing outreach and document production are the most automated API workloads).

**Why not higher than 12–18%.** The median consultant still earns less than a comparable employee (Hamilton); AI deflates prices for exactly the work it makes cheap, so the margin advantage decays within 2–4 years; cold outbound is now AI-saturated and reply rates are falling; and the owner must convert a $200–400k/yr cash machine into a $1M *asset*, which means either selling it (buyers discount owner-dependent firms heavily) or using it to buy something else (Section 3 risks). The honest path to $1M here is: $150–400k/yr SDE for 3–5 years + a $300–800k sale or an acquisition — not the service firm alone.

**Design rules (from the evidence):**
- Pick a vertical you have prior experience in (Azoulay et al.: industry experience is the top predictor) and a deliverable that is text/analysis/code with a compliance or revenue deadline (so the buyer pays for outcome, not hours).
- Incorporate from day one (S-corp or LLC taxed as S); Levine-Rubinstein's 85% of successful owners who "started unincorporated" is a selection artifact you do not need to replicate.
- Price per outcome with retainers; target 70%+ gross margin with agents doing delivery; hire your first human only for QA/account management.
- Bank the SBA injection: set a hard rule that 50% of net profit goes to an acquisition fund.

**First 90 days.**
- *Days 1–10:* Agents compile a list of 30 candidate niches scored on (i) your experience, (ii) regulatory/revenue deadline pressure, (iii) deliverable automatability, (iv) buyer density on LinkedIn/SAM.gov/state registries. You pick one. Form the entity, bank account, basic contracts (agents draft; you have a lawyer review once).
- *Days 10–25:* Build the "productized" offer: one scope, one price, one SLA, one sample deliverable produced end-to-end by agents and QA'd by you. Build a 300-contact target list with agents; write three outreach sequences; set up CRM.
- *Days 25–60:* Outbound at scale (agents send/follow up; you take every call). Target: 40 conversations, 8 proposals, 3 paying clients at $2–5k/mo. Offer a steep founding-client discount in exchange for a case study and referrals. Do the delivery with agents; log every hour of human time.
- *Days 60–90:* Raise price for new clients by 30–50%. Systematize delivery into agent runbooks. Open the acquisition fund account. Begin a weekly 2-hour "deal flow" ritual: agents scrape BizBuySell/BizQuest/broker sites and send direct letters to owners in your vertical; you read every teaser. Target by day 90: $10k+ MRR booked, 5+ case-study-eligible deliverables, and a lender pre-qualification conversation with two SBA preferred lenders so you know your injection and experience gaps.

#### Rank 2 — Self-funded search / SBA 7(a) acquisition of a $300k–$700k SDE business

**Why it ranks second rather than first.** On the evidence it is the *best-documented* path to seven-figure equity for an individual (Stanford: median searcher equity at exit $2.25M; 69% of closed deals end in a gain; acquisition loans default less than other 7(a) uses). It ranks second only because it is not reachable from $0 — it needs ~$75–150k of injection, closing costs and working capital, plus a story an SBA lender will underwrite. Conditional on being at that starting line, it is the highest-probability path in this memo.

**Evidence quality** is the best in the set for the *traditional* model (Stanford/IESE series since 1996; Yale's critical replication) and **weak** for the self-funded model (one investor-reported survey). The SBA default data are real but tabulated by vendors.

**What kills the deal:** (1) searcher attrition — 37–42% of traditional searchers never close, and self-funded searchers have no salary; (2) overpaying — 2025 BizBuySell average 2.61x cash flow means a 3.5x deal has no cushion against a 20% SDE decline under 10% interest; (3) owner dependence — the seller *was* the sales function; (4) the 2025 SOP shift to trailing-twelve-month underwriting eliminates growth-story financing.

**Where the AI team helps most:** proprietary sourcing (direct outreach to thousands of owners rather than brokered listings, where 20–30% of listings sell and the best deals are competed), fast financial normalization, lender packages, and post-close back office (which is where a first-time owner's 60-hour weeks go). Where it does not help: the lender's view of *you*, and the seller's willingness to trust you with their life's work and a seller note.

**Target profile (from the multiples and default evidence):** B2B services or specialty contracting with recurring revenue (insurance agency, commercial cleaning/landscaping with contracts, managed IT, testing/inspection, medical billing, niche distribution), $300–700k SDE, 10+ years of operation, owner retiring, 2.5–3.0x SDE, seller note ≥10% with ≥24-month standby, DSCR ≥1.5x on trailing numbers.

**First 90 days (assumes ~$100k available, e.g., from Path 1 or an investor).**
- *Days 1–15:* Agents build a thesis memo on 3 verticals you have experience in, with multiples, owner-age demographics (state licensing boards, Secretary of State registries), and a lender list. Get pre-qualified with two SBA preferred lenders; get a personal financial statement, resume, and "experience narrative" lender-ready. Line up a QoE-lite accountant and an SBA-experienced attorney on hourly terms.
- *Days 15–45:* Agents scrape every listing in the vertical daily and run a direct-mail/email campaign to 1,500+ owner-operators; you take every reply call. Build a one-page buyer profile to send to 50 brokers. Target: 60 teasers reviewed, 15 management calls, 5 IOIs.
- *Days 45–90:* Pick 2–3 targets for LOI. Agents build a normalized three-statement model with DSCR sensitivity (SDE −20%, rates +2%), customer-concentration analysis, and a 100-day post-close plan. Negotiate structure before price: seller note, standby, transition period, working-capital peg. Sign one LOI by day 90 (Stanford: searchers who sign an LOI within six months close at 74% vs 40% for the slowest), and open diligence. Expect close at month 5–7.

#### Rank 3 — Contingency recruiting / niche staffing firm

**Why it ranks third.** It is the purest intermediation business accessible with $0: fees of 15–25% of first-year salary (SHRM benchmark ~20%), no license, no inventory, no capital, and the two most labor-intensive activities — sourcing candidates and running outreach to hiring managers — are precisely the "business sales and outreach automation" workloads the Anthropic index shows doubling. Ten placements at $120k salaries at 20% = $240k/yr on near-zero cost. A staffing firm with repeatable placements sells at ~0.5–1x revenue or 3–5x EBITDA, and a contract-staffing book (temp/contract) converts the lumpy fee into recurring margin — this is how recruiting firms become seven-figure assets.

**Evidence quality is low** for income distribution (no government or academic dataset on solo recruiter earnings; only vendor blogs), **medium** for fee structure (SHRM, SIA: $189B industry), and the right tail is well attested by the existence of thousands of two-to-five-person firms clearing $500k+. The ramp risk is the same as every intermediation business: candidates and clients ghost, placements fall through, fees are paid 60–90 days after a start date, and the first six months can be zero.

**Design rules.** Pick a niche where you have domain credibility and where salaries are $100k+ (so one placement ≥$20k); run split-fee deals with established firms to get early inventory; charge retained or "engaged" fees (partial upfront) as soon as you can; move toward contract staffing (margin recurs weekly) by year 2. Keep the agents' sourcing proprietary (your own enrichment and screening pipeline is the moat; LinkedIn automation is a terms-of-service risk, so prefer email/phone and public data).

**First 90 days.**
- *Days 1–14:* Entity, E&O insurance quote, fee agreement template, split-fee network membership. Agents build a candidate database in the niche (public profiles, GitHub/portfolios, licensing boards, conference speaker lists) and a 500-company list with hiring signals (job postings older than 30 days = pain).
- *Days 14–45:* Two parallel motions: (a) agents run outbound to hiring managers with a "we have 3 vetted candidates for your open role" hook — you take every call and get job orders; (b) agents pre-screen candidates by email/form, you do 15-minute calls. Target: 10 job orders, 30 candidate submittals, 5 interviews scheduled.
- *Days 45–90:* First 1–2 placements (fees arrive ~day 100–120, so bridge with Path 1 cash or a part-time contract). Convert the best client into an engaged-search retainer. Build the "job order → submittal within 72 hours" agent runbook. Target by day 90: 2 placements closed ($30–50k in receivables), 6 active job orders, a 1,500-candidate proprietary database.

### 5.4 Why the others rank lower (briefly, with the decisive evidence)

- **Commercial insurance brokerage (#4):** best recurring economics and a well-established 1.5–3x book multiple, but carrier appointments without a book are hard, the ramp is 3–5 years, and income data are vendor-only. Strong candidate as the *acquisition target* for Path 2 rather than a greenfield start.
- **GovCon (#5):** real money and real set-asides, but only 1.4% of federal dollars go to first-time primes, new small entrants have fallen ~60% in a decade, small-contractor margins are ~8%, and sales cycles are 12–30 months. The realistic entry is subcontracting and SBIR; the AI team's capture/proposal work is genuinely valuable here, which is why it stays in the top 5.
- **Enterprise sales W-2 (#6):** the best *evidence* of any high-income path (RepVue, n>13,000: median OTE $280k, top performers $670k+) and no capital, but only ~39% of reps hit quota, you must get hired, and $1M in 7 years requires saving ~$120k+/yr after tax for 6+ years — a top-decile outcome. Excellent as the *day job that funds Path 2*.
- **Micro-SaaS (#7):** the AI team can build almost all of it, and Acquire.com shows 3.9x profit multiples at 71% margins; but sub-$100k businesses trade at 1.7–2.2x, distribution is the whole game, and the market is flooded with agent-built products. Many small bets, low per-bet odds.
- **Business brokerage (#8):** rides the silver tsunami with 8–12% commissions, but 70–80% of listings never sell, income is lumpy, and the best deal flow goes to established brokerages.
- **Real estate agent (#10):** the best data and the worst median — 62% of agents with ≤2 years' experience earned under $10k gross in 2025.
- **Startup employee (#12) / founder (#14):** the highest ceiling and lowest probability. Hall & Woodward found ~75% of VC-backed founders exit with nothing; Guzman-Stern show <5% growth outcomes even in the top 1% of predicted quality; an employee #5 at 0.3% needs a $300M+ exit after dilution for $1M. Rational only as a lottery ticket layered on a cash-flowing base.
- **E-commerce / creator / freight:** capital-intensive, platform-dependent, or thin-margin, with the weakest evidence; not competitive on probability-weighted speed.

---

## 6. What would change this ranking

- **Evidence that AI-run service firms sell at normal multiples.** If buyers (or PE roll-ups) start paying 3x+ SDE for agent-operated service firms with documented runbooks, Path 1's terminal value rises and it becomes a stand-alone $1M path rather than a feeder.
- **SBA policy.** A further tightening of equity injection, seller-note standby rules, or a return to 2008-style default rates (program-wide defaults are already at a 13-year high) would push Path 2 down and raise the cash needed.
- **Price deflation in AI-automatable services.** If per-deliverable prices for compliance docs, proposals, and outbound fall 50%+ over 2–3 years (plausible), Path 1 margins compress toward the Hamilton median and the window to bank an injection narrows. Speed matters.
- **A real dataset on self-funded search outcomes.** Today it is one investor-reported survey. If an independent study showed 30%+ loss rates for SBA-financed first-time buyers, Path 2's conditional probability would need to drop.

## 7. Source list (primary and key secondary)

**Academic / administrative**
- Hamilton, B. (2000). *Does Entrepreneurship Pay?* JPE 108(3). https://profiles.wustl.edu/en/publications/does-entrepreneurship-pay-an-empirical-analysis-of-the-returns-to/
- Moskowitz, T. & Vissing-Jørgensen, A. (2002). AER 92(4). https://www.aeaweb.org/articles?id=10.1257%2F00028280260344452 ; NBER w8876 https://www.nber.org/papers/w8876
- Hurst, E. & Pugsley, B. (2011). *What Do Small Businesses Do?* BPEA; NBER w17041. https://www.nber.org/system/files/working_papers/w17041/w17041.pdf
- Levine, R. & Rubinstein, Y. (2017). *Smart and Illicit.* QJE 132(2). https://econpapers.repec.org/RePEc:oup:qjecon:v:132:y:2017:i:2:p:963-1018. ; NBER w19276 https://www.nber.org/system/files/working_papers/w19276/w19276.pdf
- Smith, Yagan, Zidar & Zwick (2019). *Capitalists in the Twenty-First Century.* QJE 134(4). https://www.nber.org/system/files/working_papers/w25442/w25442.pdf
- Azoulay, Jones, Kim & Miranda (2020). *Age and High-Growth Entrepreneurship.* AER: Insights 2(1). https://pubs.aeaweb.org/doi/pdfplus/10.1257/aeri.20180582
- Guzman, J. & Stern, S. (2015). *Where is Silicon Valley?* Science. https://www.science.org/doi/abs/10.1126/science.aaa0201
- Åstebro, T. (2003). *The return to independent invention.* Economic Journal 113. ; Åstebro, Chen & Thompson (2011). *Stars and Misfits.* Management Science 57(11). https://digitalcommons.fiu.edu/economics_wps/24/
- Shane, S. (2008). *The Illusions of Entrepreneurship.* Yale UP. https://www.ssrn.com/abstract=1081323
- Hall, R. & Woodward, S. (2010). *The Burden of the Nondiversifiable Risk of Entrepreneurship.* AER 100(3).
- Auten, Gee & Turner (2013); Splinter & Larrimore (2026). Top-1% mobility. https://davidsplinter.com/TopMobility.html ; https://www.federalreserve.gov/econres/feds/files/2026015pap.pdf
- Federal Reserve (2023). *Changes in U.S. Family Finances 2019–2022 (SCF).* https://www.federalreserve.gov/publications/october-2023-changes-in-us-family-finances-from-2019-to-2022.htm
- Census BDS survival brief. https://www.census.gov/content/dam/Census/library/publications/2010/ADRM/CES/BDS_StatBrief4_Exit_Survival.pdf
- IRS SOI nonfarm sole proprietorship statistics. https://www.irs.gov/statistics/soi-tax-stats-nonfarm-sole-proprietorship-statistics
- Kauffman Firm Survey. https://www.researchgate.net/publication/228217166_The_Kauffman_Firm_Survey_Results_from_the_Baseline_and_First_Follow-Up_Surveys

**ETA / SBA**
- Stanford GSB 2024 Search Fund Study. https://cdn.prod.website-files.com/6455268783d6938b9451ea80/669fbcb3e5f07cc9a6093751_StanfordGSB_Study_2024.pdf
- Stanford GSB 2026 Primer. https://cdn.prod.website-files.com/6455268783d6938b9451ea80/6a0c69fbc5155d301022362d_2026%20A%20Primer%20for%20Search%20Funds_vFinal.pdf
- Yale SOM (2025). *How are Search Fund Investors Really Faring?* https://som.yale.edu/sites/default/files/2025-10/How%20are%20Search%20Fund%20Investors%20Really%20Faring.pdf
- Yale SOM (2025). *Exploring the SBA 7(a) Loan Program.* https://som.yale.edu/sites/default/files/2025-04/Exploring%20and%20Understanding%20the%20U.S.%20Small%20Business%20Administration%207(a)%20Loan%20Program.pdf
- IESE International Search Funds 2026. https://www.iese.edu/media/research/pdfs/ST-0689-E
- BizBuySell 2025 Year in Review. https://www.bizbuysell.com/blog/2025-year-in-review/
- SOP 50 10 8 summary (Whiteford). https://www.whitefordlaw.com/news-events/client-alert-sba-issues-sop-50-10-8-key-changes-impacting-sba-7a-lending
- SBA default tabulations: GoSBA https://gosbaloans.com/guide/sba-loan-default-rates-by-loan-use/ ; Lumos https://www.lumosdata.com/blog/sba-default-rates-small-business-credit-risk-2026 ; CT Acquisitions https://ctacquisitions.com/guides/sba-financing-statistics-2026/
- Self-funded search (vendor/secondary): https://smash.vc/search-fund-statistics/ ; https://www.peony.ink/blog/search-fund-guide
- Silver tsunami: https://www.forbes.com/sites/alisoncoleman/2026/01/14/the-silver-tsunami-is-reshaping-small-business-why-exit-planning-cant-wait/ ; https://www.teamshares.com/resources/silver-tsunami/

**Occupations / markets**
- Ramsey National Study of Millionaires. https://www.ramseysolutions.com/retirement/the-national-study-of-millionaires-research ; https://www.ramseysolutions.com/retirement/how-to-become-a-millionaire
- NAR 2026 Member Profile. https://www.nar.realtor/news/economists-outlook/the-feature-sheet-2026-member-profile
- RepVue Enterprise AE. https://www.repvue.com/salaries/enterprise-account-executive
- Carta Equity Report 2024. https://carta.com/data/equity-report-2024/
- MBO Partners 2025 State of Independence. https://info.mbopartners.com/rs/mbo/images/MBO_2025_State_of_Independence_Research_Report.pdf
- Acquire.com multiples Jan 2026. https://blog.acquire.com/acquire-com-biannual-acquisition-multiples-report-jan-2026/
- IBBA brokerage guide. https://www.ibba.org/wp-content/uploads/2021/01/ibba-guide-business-brokerage-profession.pdf
- Insurance agency valuation (vendor). https://renegadeinsurance.com/insurance-agency-valuation/
- SBA $178B small-business contracting. https://www.sba.gov/article/2024/04/29/biden-harris-administration-awards-record-breaking-178-billion-federal-procurement-opportunities ; Third Way new-entrant data https://www.thirdway.org/report/12-solutions-for-small-business-success-in-federal-contracting ; Deltek margins https://www.deltek.com/en/government-contracting/guide/pricing/profit-margin-government-contracts
- Anthropic Economic Index. https://www.anthropic.com/news/the-anthropic-economic-index ; https://www.anthropic.com/research/labor-market-impacts
- Wealth-X self-made data. https://www.cnbc.com/2019/09/26/majority-of-the-worlds-richest-people-are-self-made-says-new-report.html
- Stanley & Danko. https://www.spokesman.com/stories/1998/jun/28/meet-the-millionaire-next-door-one-surprising/
