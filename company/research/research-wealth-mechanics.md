# How Wealth Actually Gets Built: Mechanics, Structure, and an Operating System for a US Solo Founder

*Research memo, October 2026. Educational research only: this is not legal, tax, or investment advice. Tax figures are for the 2026 tax year unless stated and come from IRS Rev. Proc. 2025-32, IRS Notice 2025-67, and the One Big Beautiful Bill Act (OBBBA, P.L. 119-21, signed July 4, 2025) as summarized by the sources cited. Where a number comes from a secondary source or my own arithmetic, the text says so. Verify anything you act on with a CPA or attorney.*

---

## Executive summary

1. **Millionaires are mostly made, slowly, by earned income plus boring investing.** The Federal Reserve's 2025 Survey of Consumer Finances (released October 9, 2026) puts median US family net worth at $215,900 and the mean at $1.24 million. Ramsey's 10,000-person study found 79% of millionaires received no inheritance, one-third never earned a six-figure year, and the typical path took ~28 years, crossing $1M around age 49. Thomas Stanley's data (1996) found two-thirds of millionaires were self-employed although the self-employed were under 20% of workers.
2. **Business ownership is the single biggest differentiator between the top decile and everyone else.** In the 2025 SCF, 40% of top-income-decile families own a private business versus 8% in the bottom half. Conditional on ownership, mean business equity is $1.57M against a $75,400 median: a lottery-like distribution. Tax-data research (Smith, Yagan, Zidar, Zwick) shows most top-1% earners have pass-through business income and that "the typical top earner derives most of her income from human capital, not financial capital."
3. **The "secrets" are structure, and they scale with income.** At $0-100k: Roth IRA, HSA (now available with ACA bronze plans), simple Solo 401(k), home office, bookkeeping. At $100k-500k: S-corp election, QBI planning (2026 phase-in begins at $201,750 single/$403,500 joint), maxing a $72,000 Solo 401(k), backdoor Roth, hiring children, Section 179/100% bonus depreciation. At $1M+: QSBS (now 50/75/100% exclusions at 3/4/5 years, $15M cap), cost-segregated real estate, asset location, donor-advised funds under the new 0.5%-of-AGI floor, and buy-borrow-die against a $15M estate exemption.
4. **Trading loses; indexing wins; behavior is the gap.** 79% of active large-cap funds trailed the S&P 500 in 2025 and ~90% did over 15 years (SPIVA). 97% of persistent Brazilian day traders lost money. 73-81% of retail bitcoin app users likely lost money (BIS). Morningstar estimates investors forfeit 1.2 percentage points a year to timing, about $3.8 trillion.
5. **The first million almost always comes from income, not returns.** At a 7% real return, $1,000/month takes ~28 years to reach $1M; $5,000/month takes ~11 years. The only lever that compresses the timeline by an order of magnitude is raising what you can save, which for a solo founder means owning equity in something that scales.

---

## 1. How millionaires actually get there

### 1.1 The population: who is wealthy and how wealthy

**Federal Reserve, 2025 Survey of Consumer Finances (SCF), released Oct 9, 2026.** The SCF is the gold-standard triennial survey of US household balance sheets.

| Measure (2025 dollars) | Value | Change 2022-2025 |
|---|---|---|
| Median family net worth | $215,900 | +2% |
| Mean family net worth | $1,241,500 | +7% |
| Median net worth, top income decile | $3,669,900 | +31% |
| Median net worth, top net-worth decile | $4,935,200 | +19% |
| Median net worth, age <35 | $33,000 | -23% |
| Median net worth, age 55-64 | $411,900 | +3% |
| Median net worth, 75+ | $504,900 | +37% |
| Median net worth, college degree | $505,400 | -1% |
| Median net worth, HS diploma only | $106,700 | -9% |
| Median net worth, homeowner / renter | $458,900 / $10,600 | +6% / -7% |
| Real median family income | $82,200 | +7% |

Sources: [Federal Reserve press release](https://www.federalreserve.gov/newsevents/pressreleases/other20261009a.htm); full report *Changes in U.S. Family Finances from 2022 to 2025* ([PDF](https://www.federalreserve.gov/publications/files/scf26.pdf)), Table 2.

**Capgemini World Wealth Report 2026**: global HNWI population (investable assets of $1M+) reached a record 25.3 million in 2025, with wealth up 8.7% to $98.3 trillion, driven by "robust equity market performance and easing inflation." ([Capgemini](https://www.capgemini.com/de-de/news/pressemitteilung/world-wealth-report-2026/); [IFA Magazine](https://ifamagazine.com/capgemini-global-millionaire-population-hit-record-25-3-million-in-2025/)). Note that Capgemini's "millionaire" excludes the primary residence; the SCF includes it.

### 1.2 Where the wealth comes from: business vs. wages vs. investments vs. real estate vs. inheritance

**Business ownership (SCF 2025, Box 3 and Table 3).**
- 15.4% of all families own a privately held business, up almost 1 point from 2022.
- Ownership is steeply income-graded: **8% of families in the bottom half of income vs. 40% in the top decile.**
- Conditional on ownership, the **median business is worth $75,400 but the mean is $1,566,600.** The Fed notes the gap "reflect[s] the small fraction of privately held businesses with very high valuations." Translation: most small businesses are jobs; a minority are wealth engines.
- Real values of businesses in the bottom 90% of income fell 18-22% between 2022 and 2025; the top decile's rose ~2%.

**Rough asset mix of aggregate household wealth (my arithmetic from SCF Table 3: ownership rate x conditional mean, divided by mean net worth of $1.24M; gross values, so this overstates housing which carries mortgage debt):**

| Asset class | Share of families holding | Conditional mean | Approx. share of aggregate net worth |
|---|---|---|---|
| Primary residence (gross) | 65.6% | $534,000 | ~28% |
| Retirement accounts | 54.9% | $451,100 | ~20% |
| **Private business equity** | **15.4%** | **$1,566,600** | **~19%** |
| Pooled investment funds | 11.1% | $1,148,100 | ~10% |
| Directly held stocks | 19.0% | $524,300 | ~8% |
| Other residential real estate | 13.8% | $559,200 | ~6% |

The point: business equity is held by only one family in seven, yet it is roughly as large a slice of national household wealth as all retirement accounts combined. It is the most concentrated asset class, which is exactly why it dominates at the top.

**Top incomes are business incomes (tax data).** Smith, Yagan, Zidar and Zwick, "Capitalists in the Twenty-First Century" (QJE 2019), using IRS data, found that more than half of the top 1% and roughly 80% of the top 0.1% earn pass-through business income, that this income accrues to "working-age owners of closely held mid-market firms in skill-intensive industries," and that profits fall by three-quarters after the owner retires or dies. Their conclusion: "the typical top earner derives most of her income from human capital, not financial capital." ([NBER w25442](https://www.nber.org/papers/w25442.pdf); [Princeton](https://collaborate.princeton.edu/en/publications/capitalists-in-the-twenty-first-century/)). This is the strongest evidence that top wealth is mostly *owner-operator* wealth, not passive capital.

**Inheritance.**
- Ramsey: 79% of millionaires received no inheritance; only 3% received $1M or more; 8 in 10 came from middle- or lower-income families ([Ramsey study](https://www.ramseysolutions.com/retirement/the-national-study-of-millionaires-research)).
- Stanley & Danko, *The Millionaire Next Door*: ~80% first-generation affluent ([A Wealth of Common Sense summary](https://awealthofcommonsense.com/2025/05/7-attributes-of-the-millionaire-next-door/)).
- Fidelity Millionaire Outlook (2012, dated): 86% of millionaires describe themselves as self-made ([BenefitsPro](https://benefitspro.com/2012/07/20/fidelity-finds-86-percent-of-millionaires-are-self)).
- UBS Billionaire Ambitions Report 2025: 74% of the 924 US billionaires are self-made; 196 new self-made billionaires globally in 2025 ([UBS](https://www.ubs.com/global/en/media/display-page-ndp/en-20251204-billionaire-ambitions-report-2025.html)).
- But: Fed economists Feiveson and Sabelhaus (FEDS Notes 2018) estimate about 1.7 million inheritances per year totaling ~$290 billion, with inheritances over $1M being 2% of the count but ~40% of the dollars; recipients skew wealthier and more educated ([FEDS Note](https://www.federalreserve.gov/econres/notes/feds-notes/how-does-intergenerational-wealth-transmission-affect-wealth-concentration-20180601.htm)). Wolff and Gittleman (NBER w16840) estimate transfers at 19-29% of aggregate net worth over 1989-2007 and that roughly one-fifth of households had received one ([NBER](https://www.nber.org/papers/w16840)).

Reconciling these: inheritance is a minority story at the $1-5M level and a bigger story at the very top. For a solo founder starting from zero, the base rate is firmly on the side of "made, not born."

### 1.3 The Ramsey National Study of Millionaires (n > 10,000, fielded 2017-18)

Key findings ([Ramsey Solutions](https://www.ramseysolutions.com/retirement/the-national-study-of-millionaires-research); [original PDF](https://mms.businesswire.com/media/20190107005214/en/698578/1/National-Study-of-Millionaires.pdf?download=1)):
- **Timeline:** average of 28 years of working, saving and investing to hit $1M; most crossed at age 49. Only 5% got there in under 10 years. (Ramsey's 2026 page now says "25-30 years" and "age 50.")
- **Income:** only 31% averaged $100k+ over their careers; one-third never had a six-figure year. 15% held senior-leadership roles.
- **Top five professions:** engineer, accountant, teacher, management, attorney. Not founders, not finance.
- **Vehicle:** 8 in 10 used an employer 401(k); 3 in 4 also invested outside it; 75% credited "regular, consistent long-term investing." Zero named single-stock picking as a major factor.
- **Behavior:** 94% live on less than they earn; ~3 in 4 have never carried a credit-card balance; 93% use coupons at least sometimes.
- **Education:** 88% college graduates; 62% from public state schools; 8% from elite privates.

Caveat: this is an opt-in survey of people who are already millionaires (survivorship) and it samples the "$1-5M net worth including home" tier, which is a very different population from $10M+.

### 1.4 Thomas Stanley, *The Millionaire Next Door* (1996) and *The Millionaire Mind*

- Self-employed people were "less than 20 percent of the workers in America but account for two-thirds of the millionaires"; three-quarters of the self-employed millionaires were entrepreneurs, the rest professionals ([Money Guy summary](https://moneyguy.com/2023/07/how-normal-people-become-millionaires-real-data); [A Wealth of Common Sense](https://awealthofcommonsense.com/2025/05/7-attributes-of-the-millionaire-next-door/)).
- Stanley's "prodigious accumulators of wealth" invest roughly 15-20% of realized household income, buy used cars, live in modest neighborhoods, and have been married once. Thirty years later the SCF still shows the same pattern: the top-income decile is where business ownership (40%) and net worth ($3.67M median) both spike.

### 1.5 Savings rate is the master variable

Because investment returns are roughly fixed for everyone, the one variable you control is savings rate. My calculation of years to financial independence (portfolio = 25x annual spending) at a 5% real return, starting from zero, with spending held constant:

| Savings rate | Years to 25x expenses |
|---|---|
| 10% | ~51 |
| 20% | ~37 |
| 30% | ~28 |
| 50% | ~17 |
| 70% | ~9 |

The 28-year Ramsey timeline is exactly what a ~25-30% savings rate produces. Founders who reach $1M in under 10 years (the 5%) either saved 60%+ of a large income or sold equity. Both are income-side events, not investing-side events.

---

## 2. The "secrets" that are really just structure (2026 numbers)

A reminder of the baseline 2026 figures everything else hangs on ([Rev. Proc. 2025-32 via Kiplinger](https://www.kiplinger.com/taxes/irs-updates-capital-gains-tax-thresholds); [Clark](https://clark.com/personal-finance-credit/taxes/irs-announces-new-tax-brackets-and-other-changes-for-2026/)):
- Standard deduction: **$16,100 single / $32,200 joint**.
- Brackets 10-37%; 37% begins at $640,600 single / $768,700 joint.
- Long-term capital gains: **0% up to $49,450 single / $98,900 joint** taxable income; 15% to $545,500 / $613,700; 20% above. 3.8% NIIT above $200k/$250k MAGI (not indexed).
- Social Security wage base: **$184,500** ([Paycor](https://www.paycor.com/resource-center/articles/social-security-taxable-wage-base/)). Self-employment tax is 15.3% (12.4% SS + 2.9% Medicare) on 92.35% of net earnings, plus 0.9% additional Medicare above $200k/$250k.
- Estate and gift exemption: **$15M per person / $30M per couple**, now permanent and indexed ([Instead](https://instead.com/resources/blog/buy-borrow-die-strategy-explained-for-2026)).

### 2.1 Entity choice: sole prop / LLC vs. S-corp, and "reasonable salary"

- **A single-member LLC changes nothing for taxes**; it is a liability wrapper taxed as a sole proprietorship (Schedule C). Form one early for liability separation and professionalism, not for tax savings.
- **The S-corp election (Form 2553) is the first real structural lever.** Profit is split into W-2 salary (subject to 15.3% FICA) and distributions (no FICA). The IRS requires "reasonable compensation" for services performed; there is no safe-harbor percentage, and practitioners flag distributions above ~50% of total pay as an audit-risk heuristic, not a rule ([Uncle Kam](https://unclekam.com/tax-strategy-blog/maximizing-your-2026-s-corp-tax-savings-salary-vs-distribution-strategies/)).
- **Worked example (my arithmetic):** $150,000 net profit. As a sole prop, SE tax is roughly $150,000 x 0.9235 x 15.3% = **$21,200**. As an S-corp paying a $75,000 salary, FICA is $75,000 x 15.3% = **$11,475**, a gross saving of ~$9,700. Subtract payroll-service and extra-return costs ($1,500-3,000/yr), state franchise taxes (California charges 1.5% of S-corp net income, minimum $800), and the fact that only W-2 wages count toward your Solo 401(k) employer contribution (25% of salary, so $18,750 here, versus ~20% of the full $150,000 as a sole prop). Net benefit is real but smaller than marketing suggests, and it roughly disappears below ~$60-80k of profit.
- **Also note:** the S-corp salary must be run through payroll *during* the year; you cannot reclassify distributions as salary after December 31. Salary reduces QBI (below) but above the QBI thresholds W-2 wages are what *preserve* the deduction, so the salary level becomes an optimization problem for a CPA.

**Who it applies to:** $0-100k: usually no (sole prop/LLC). $100k-500k: yes, this is the sweet spot. $1M+: yes, but at that level you are also looking at C-corp/QSBS (2.8) and the S-corp vs. C-corp trade-off depends on whether you plan to sell.

### 2.2 Section 199A / QBI deduction (now permanent)

OBBBA made the 20% qualified business income deduction permanent and added a $400 minimum deduction. For 2026, the deduction is unrestricted below **$201,750 taxable income (single) / $403,500 (joint)**; the phase-in range was widened from $50k/$100k to **$75k/$150k**, so full phase-out for specified service trades or businesses (SSTBs: consulting, health, law, accounting, financial services, "reputation or skill" businesses) now occurs at **$276,750 / $553,500**. Above the threshold, non-SSTBs are limited to the greater of 50% of W-2 wages or 25% of wages + 2.5% of unadjusted basis of depreciable property ([Foster Swift](https://www.fosterswift.com/newsroom/publications/summary-big-beautiful-bill-tax-code-changes-businesses); [Carry](https://carry.com/learn/qbi-phaseout-sstb); [Beancount guide](https://beancount.io/blog/2026/06/01/section-199a-qbi-deduction-pass-through-owners-obbba-permanent-2026-thresholds-sstb-phase-out-w2-wages-ubia-form-8995-aggregation-guide)).

Plain English: a solo founder with $120k of profit effectively pays income tax on $96k. This is worth more than almost any other single deduction at the $100k-400k level, and the interaction with S-corp salary, retirement contributions (which *reduce* QBI), and SSTB status is where a good CPA earns their fee.

**Applies:** all tiers up to the thresholds; above ~$280k single / $555k joint, SSTBs get nothing and the planning shifts to retirement contributions that pull taxable income back under the line.

### 2.3 Solo 401(k) and SEP-IRA (2026 limits, IRS Notice 2025-67)

| | Solo 401(k) | SEP-IRA |
|---|---|---|
| Employee deferral | $24,500 (Roth or pre-tax) | none |
| Employer contribution | up to 25% of W-2 comp (S-corp) or ~20% of net SE income (sole prop) | same |
| Total cap (§415(c)) | **$72,000** | **$72,000** |
| Catch-up 50+ | +$8,000 (total $80,000) | none |
| Super catch-up 60-63 | +$11,250 (total $83,250) | none |
| Compensation cap | $360,000 | $360,000 |
| Roth option | yes | yes (SECURE 2.0, provider-dependent) |
| Mega backdoor Roth | yes if plan allows after-tax contributions + in-plan conversion | no |
| Loans | up to $50k if plan allows | no |
| Filing | Form 5500-EZ once assets > $250k | none |

Sources: [Collective](https://www.collective.com/blog/tax-tips/self-employed-retirement-plan-limits-2026); [IRA Financial](https://www.irafinancial.com/?p=7811); [Beancount Solo 401k vs SEP](https://beancount.io/blog/2026/06/01/solo-401k-vs-sep-ira-self-employed-business-owners-2026-contribution-limits-secure-2-0-super-catch-up-mega-backdoor-roth-form-5500-ez-s-corp-owner-reasonable-salary-comparison-guide).

Why the Solo 401(k) wins at modest income: on $60k of net profit, a SEP allows ~$11,150 (20%); a Solo 401(k) allows $24,500 + ~$11,150 = ~$35,650. The employee deferral layer is the difference. Sole proprietors can establish and fund a Solo 401(k) up to the tax-filing deadline for employer contributions (SECURE 2.0 loosened setup timing), but elective deferrals need to be elected by December 31.

**SECURE 2.0 wrinkle for 2026:** workers with prior-year FICA wages above ~$150,000 must make catch-up contributions as Roth. For an S-corp owner paying themselves above that, plan accordingly.

**Applies:** all tiers. At $0-100k, use it for the deferral and the Roth option. At $100k-500k, max it; the $72k is the single largest deduction available to a solo founder. At $1M+, add the mega backdoor Roth (after-tax contributions up to the $72k cap, converted to Roth) and consider a cash-balance defined-benefit plan on top (not researched here; can allow $100k-300k+/yr of deductions for owners over ~45).

### 2.4 HSA: the only triple-tax-free account

2026 limits: **$4,400 self-only / $8,750 family**, +$1,000 catch-up at 55+ ([IRA Financial](https://www.irafinancial.com/?p=174201); [NDTCO](https://knowledge.ndtco.com/2026-irs-contribution-limits)). Contributions are deductible (and, for the self-employed, avoid income tax though not SE tax unless run through an S-corp payroll), growth is untaxed, and withdrawals for medical expenses are untaxed. After 65 it behaves like a traditional IRA for non-medical withdrawals.

**New for solo founders in 2026:** OBBBA made **all ACA bronze and catastrophic marketplace plans HSA-compatible** starting January 1, 2026, regardless of whether they meet the old HDHP tests, and allowed HSA holders to use **direct primary care** arrangements (up to roughly $150/month individual, $300/month family) without losing eligibility ([IRS Notice 2026-05 via RSM](https://rsmus.com/insights/services/business-tax/irs-notice-2026-expanded-hdhp-definition-obbba-broadens-hsa.html); [IFEBP](https://blog.ifebp.org/what-employers-need-to-know-about-hsa-compatibility-expansion-in-obbba/)). Since most solo founders buy marketplace coverage, this removes the old "find an HSA-eligible plan" headache.

The "secret" use: pay medical bills out of pocket, keep receipts forever, let the HSA compound in index funds, and reimburse yourself decades later tax-free. Combined with the self-employed health insurance deduction (premiums deductible above the line), this is the highest-yield account per dollar at every income tier.

### 2.5 Roth IRA, backdoor Roth, mega backdoor

- 2026 Roth/traditional IRA limit **$7,500** (+$1,100 catch-up at 50+). Roth direct-contribution phase-out: **$153,000-$168,000 single; $242,000-$252,000 joint** ([Vision Retirement](https://www.visionretirement.com/401k-and-ira-contribution-limits)).
- **Backdoor Roth** (above the phase-out): contribute $7,500 non-deductible to a traditional IRA, convert to Roth. The pro-rata rule taxes the conversion proportionally if you hold *any* pre-tax IRA money (including SEP-IRAs and rollover IRAs), which is a specific reason solo founders often prefer a Solo 401(k) over a SEP: you can roll pre-tax IRA balances *into* the Solo 401(k) to clear the decks.
- **Mega backdoor Roth** in a Solo 401(k): after-tax contributions up to the $72,000 total, then in-plan Roth conversion. Requires a custom plan document (not the free brokerage prototype) ([IRA Financial](https://www.irafinancial.com/blog/mega-backdoor-roth-2026-limit-guide/)).
- **The Thiel example** is the extreme version of "put the asset with the highest expected growth in the Roth": ProPublica reported he placed 1.7 million PayPal founder shares valued at $0.001 each (~$1,700) into a Roth IRA in 1999; it was worth ~$5 billion by 2019 ([ProPublica](https://www.propublica.org/article/lord-of-the-roths-how-tech-mogul-peter-thiel-turned-a-retirement-account-for-the-middle-class-into-a-5-billion-dollar-tax-free-piggy-bank)). The replicable principle: Roth space is the best home for your highest-growth, least-tax-efficient assets. Holding your own startup's stock in an IRA is possible via self-directed custodians but is a prohibited-transaction minefield; most founders should not try it without specialist counsel.

**Applies:** $0-100k: direct Roth contributions, Roth deferrals in the Solo 401(k) (you are likely in a low bracket now). $100k-500k: backdoor Roth; mix of pre-tax and Roth. $1M+: mega backdoor; Roth conversions in low-income years (e.g., the year after a sale).

### 2.6 Section 179 and bonus depreciation after OBBBA

- **100% bonus depreciation is back and permanent** for qualified property (recovery period of 20 years or less) acquired and placed in service after January 19, 2025. Property acquired under the old contract rules but placed in service after 12/31/2026 can get 0%, so timing matters ([Foster Swift](https://www.fosterswift.com/newsroom/publications/summary-big-beautiful-bill-tax-code-changes-businesses); [Haynes Boone](https://www.haynesboone.com/news/alerts/significant-tax-changes-resulting-from-the-one-big-beautiful-bill.pdf)).
- **Section 179 for 2026: $2,560,000 limit, phase-out beginning at $4,090,000** of property placed in service; heavy SUVs (6,000+ lb GVWR) capped at $32,000 under 179 but eligible for bonus on the rest ([Spidell summary of Rev. Proc. 2025-32](https://spidell.com/?p=641291); [Instead](https://instead.com/resources/blog/section-179-expensing-limits-for-2026)).
- Practical difference: Section 179 is limited to business taxable income (cannot create a loss); bonus depreciation can. For a solo founder, these matter for laptops, cameras, equipment, vehicles used >50% for business, and furniture. The trap is buying things you do not need to "save on taxes"; a $1 deduction saves at most ~$0.45.

**Applies:** $0-100k: trivially (expense the laptop). $100k-500k: vehicle and equipment timing. $1M+: combine with cost segregation on real estate (2.9).

### 2.7 Augusta rule, home office, hiring family

- **Augusta rule (§280A(g)):** rent your home to your *business entity* for up to 14 days a year at a documented fair-market rate; the business deducts the rent, you exclude it from income. Exceed 14 days and you lose the exclusion on all of it. It requires a separate entity (S-corp, partnership, C-corp); a sole proprietor or disregarded LLC renting from themselves is a wash ([Adams and Reese](https://www.adamsandreese.com/insights/understanding-the-internal-revenue-codes-augusta-rule); [Beancount](https://beancount.io/blog/2026/04/25/augusta-rule-section-280a-tax-free-rental-income-business-owners)). Realistic value for a solo founder: $300-700/day x 14 days = $4-10k of tax-free income, if you actually hold documented meetings/retreats.
- **Home office:** simplified method is **$5/sq ft up to 300 sq ft = $1,500 max**; the regular method (actual expenses prorated, plus depreciation) is usually worth more for larger spaces. The space must be used regularly and exclusively for business ([IRS](https://www.irs.gov/Businesses/Small-Businesses-&-Self-Employed/Simplified-Option-for-Home-Office-Deduction)). The S-corp version is an accountable-plan reimbursement, which is cleaner.
- **Hiring your children:** a sole proprietorship or an LLC/partnership owned only by the parents can pay a child under 18 with **no Social Security or Medicare tax** (§3121(b)(3)(A)) and no FUTA under 21 (§3306(c)(5)). Wages are deductible to the business and, up to the **$16,100 standard deduction**, income-tax-free to the child, who can then fund a Roth IRA up to $7,500 or earned income ([Gusto](https://gusto.com/resources/articles/taxes/tax-benefits-hiring-children); [Mercer Advisors](https://www.merceradvisors.com/insights/taxes/tax-benefits-of-employing-your-children-in-your-business/)). An S-corp loses the FICA exemption unless wages are routed through a parent-owned family management company. Work must be real, age-appropriate, documented with timesheets and a W-2.
- **Hiring a spouse** gives you a second Solo 401(k) participant (another $72,000 of space) and, via an HRA, can make family medical costs deductible to the business. This is a well-known planning move; confirm with a CPA.

**Applies:** home office at every tier; Augusta and family payroll mostly at $100k+, because they need an entity and enough profit to matter.

### 2.8 QSBS (Section 1202) after OBBBA

For qualified small business stock **issued after July 4, 2025**:
- **Tiered exclusion: 50% after 3 years, 75% after 4 years, 100% after 5 years** (prior law: nothing before 5 years).
- **Per-issuer cap raised from $10M to $15M** (indexed after 2026), or 10x basis if greater.
- **Gross-assets test raised from $50M to $75M** (indexed).
- Stock issued before July 5, 2025 stays under the old rules ([DWT](https://dwt.com/blogs/startup-law-blog/2025/07/qsbs-big-beautiful-bill-tax-code-upgrades); [Perkins Coie](https://perkinscoie.com/insights/update/significant-changes-one-big-beautiful-bill-act-qualified-small-business-stock); [Gibson Dunn](https://www.gibsondunn.com/focus-on-qsbs-provisions-in-the-one-big-beautiful-bill-act/)).

Requirements that trip solo founders: it must be a **domestic C-corporation** (not an S-corp or LLC), stock must be acquired at original issuance, 80% of assets must be used in an active qualified business, and SSTB-type fields (health, law, consulting, financial services, "reputation or skill of employees") are excluded. The excluded gain also escapes the 3.8% NIIT.

The founder decision: if you are building something you intend to sell for $5M+, the C-corp's double-taxation cost on distributions can be worth it for a 0% federal tax on up to $15M of gain. If you are building a cash-flow business you will run for 20 years, the S-corp wins. An LLC can convert to a C-corp later; the QSBS clock starts at conversion, and the gross-assets test is applied at that moment (so convert early while assets are small). The practice of "stacking" (gifting shares to trusts for additional $15M exclusions) is an estate-planning tool for the $10M+ exit.

**Applies:** $1M+ (specifically, founders of scalable, saleable, non-SSTB businesses). Irrelevant to consultants and agencies.

### 2.9 Real estate: depreciation, cost segregation, 1031

- Residential rental property is depreciated over **27.5 years** (commercial 39), land excluded. On a $400k property with $75k land, that is ~$11,800/yr of paper loss offsetting rental income ([Uncle Kam](https://unclekam.com/tax-strategy-blog/2026-real-estate-tax-strategies/)).
- **Cost segregation** reclassifies 20-40% of a building into 5/7/15-year property; with 100% bonus depreciation permanent, a $400k property can produce an ~$80-120k first-year deduction ([Beancount](https://beancount.io/ko/blog/2026/03/20/cost-segregation-study-guide-accelerate-depreciation-save-taxes)).
- **The catch is the passive-loss rules.** Rental losses are passive and can only offset passive income unless (a) you qualify for the $25,000 active-participation allowance (phased out between $100k-150k AGI), (b) you are a **real estate professional** (750+ hours and more than half your working time in real property trades; nearly impossible for a full-time founder, but possible for a spouse), or (c) the **short-term rental** exception (average stay 7 days or less and material participation makes it non-passive). This is why "real estate pays no taxes" claims mostly apply to people whose main job *is* real estate.
- **1031 exchange:** defers gain on investment real property if replacement property is identified within **45 days** and closed within **180 days** through a qualified intermediary; real property only since 2018; deferred, not forgiven ([IRS FS-2008-18](https://www.irs.gov/pub/irs-news/fs-08-18.pdf); [IRS 2020 final regs](https://www.irs.gov/node/87786)). Depreciation is recaptured at up to 25% on sale unless you exchange until death (2.10).

**Applies:** $100k-500k as a side allocation at most; $1M+ as a deliberate tax-and-diversification strategy with a professional. For a solo founder in the growth phase, real estate's main cost is attention, not taxes.

### 2.10 Buy, borrow, die

Hold appreciated assets; borrow against them (securities-backed line of credit, typically at a spread over SOFR) instead of selling; at death heirs receive a **step-up in basis** to fair market value, which OBBBA preserved unchanged, and the loan is repaid with no capital-gains tax on lifetime appreciation ([Instead](https://instead.com/resources/blog/buy-borrow-die-strategy-explained-for-2026); [Beancount step-up guide](https://beancount.io/blog/2026/05/03/step-up-in-basis-at-death-estate-planning-eliminate-capital-gains-heirs-guide)). With a **$15M/$30M estate exemption**, this is tax-free for the overwhelming majority of estates.

Limits: SBLOCs are callable and can be margin-called in a crash; interest compounds against you; retirement accounts get no step-up; roughly a dozen states levy estate or inheritance tax at far lower thresholds. The modest version a founder can use today: never sell a low-basis asset to fund a purchase if you can borrow cheaply and the asset is diversified.

**Applies:** $1M+ (needs a sizable taxable portfolio). The $0-500k version is simply "don't sell; hold winners in taxable accounts; let the 0%/15% capital-gains brackets work."

### 2.11 Asset location

Put tax-inefficient assets (bonds, REITs, actively managed funds) in tax-deferred accounts, highest-growth assets in Roth, and broad equity index funds (low turnover, qualified dividends, deferred gains, eligible for step-up) in taxable. Vanguard's research puts the value at **5-30 basis points of after-tax return a year** for diversified investors, higher for those with large taxable accounts; their rule is bonds go first into traditional IRA/401(k), then Roth, then taxable ([Vanguard](https://corporate.vanguard.com/content/corporatesite/us/en/corp/articles/how-asset-location-can-boost-after-tax-returns.html); [Vanguard 2022 paper](https://externalcrewnet.vanguard.com/content/dam/corp/research/pdf/revisiting_conventional_wisdom_regarding_asset_location.pdf)). Also tax-loss harvesting in taxable accounts ($3,000/yr against ordinary income, unlimited against gains).

**Applies:** matters once you have both a taxable and a tax-advantaged account of meaningful size, roughly $100k-500k and up.

### 2.12 Charitable strategies under the 2026 rules

OBBBA changed charitable deductions starting in 2026 ([WealthManagement](https://www.wealthmanagement.com/philanthropy/charitable-contribution-deduction-changes-under-the-obbba); [Mercer Advisors](https://www.merceradvisors.com/taxes/how-the-one-big-beautiful-bill-changes-charitable-giving-in-2026/)):
- **Non-itemizers** can deduct **$1,000 single / $2,000 joint** of cash gifts (not to donor-advised funds).
- **Itemizers** face a new **0.5%-of-AGI floor** (first 0.5% of AGI in gifts is non-deductible) and a **35% cap** on the value of deductions for 37%-bracket taxpayers. The 60%-of-AGI limit for cash is permanent.
- Consequences: **bunching** several years of giving into one year through a **donor-advised fund** is now more valuable, and **gifting appreciated stock** (deduct FMV, never pay the gain) remains the most efficient gift. After 70.5, **qualified charitable distributions** from IRAs bypass all of this.

**Applies:** small cash gifts at every tier; DAF bunching and appreciated-stock gifts at $100k+; charitable remainder trusts and private foundations at $1M+ exits.

### 2.13 Quick map: which tools matter at which income

| Tool | $0-100k | $100k-500k | $1M+ |
|---|---|---|---|
| LLC for liability | Yes | Yes | Yes |
| S-corp election | Rarely (>~$70k profit) | **Core** | Yes unless C-corp/QSBS |
| QBI deduction | Automatic | **Core, plan around thresholds** | Mostly phased out for SSTBs |
| Solo 401(k) | Yes (Roth deferrals) | **Max $72k** | Max + mega backdoor + cash balance plan |
| HSA | **Yes** | Yes | Yes |
| Roth / backdoor Roth | Direct Roth | Backdoor | Mega backdoor, conversions |
| Home office | Yes | Yes | Yes |
| 179 / bonus | Expense equipment | Vehicles, equipment | Cost seg, large assets |
| Augusta rule | No (no entity) | Yes | Yes |
| Hire kids/spouse | Maybe | Yes | Yes |
| QSBS | Plan entity type early | Decide C vs S | **Core on exit** |
| Real estate depreciation/1031 | No | Side allocation | Yes |
| Buy-borrow-die | No | No | Yes |
| Asset location | n/a | Yes | Yes |
| DAF / appreciated stock | $1k cash deduction | Bunching | CRTs, foundations |

---

## 3. Investing fundamentals with data

### 3.1 Long-run returns

- S&P 500 total return 1928-2024: **~9.9% nominal CAGR** (Damodaran data), ~**7% real**; the arithmetic average (~11.8%) overstates what compounds ([Walnut](https://walnutinvest.com/stats/average-stock-market-return); [DQYDJ](https://dqydj.com/sp-500-annual-return-rankings/)). Dimensional notes annual returns landed within 2 points of the long-run average in only 6 of 99 years ([Dimensional](https://my.dimensional.com/chmedia/333079/source/the-bumpy-road-to-the-markets-long-term-average.pdf)). Berkshire's own letter benchmarks the S&P at **10.5% compounded 1965-2025** vs. Berkshire's 19.7% ([Coinpaper summary of the 2025 letter](https://coinpaper.com/35923/what-if-you-invested-100-with-warren-buffett-in-1964)).
- Planning assumption used below: **7% real / 10% nominal**. Many forecasters (Vanguard, Research Affiliates) expect lower US equity returns from today's valuations; 5% real is a prudent stress case.

### 3.2 Why most active managers and retail traders lose

- **SPIVA Year-End 2025:** 79% of active large-cap US funds trailed the S&P 500 in 2025, the fourth-worst year in SPIVA's 25-year history; over 15 years roughly 90% trail, and "there were no categories in which a majority of active managers outperformed" ([S&P DJI YE2025 PDF](https://www.spglobal.com/spdji/en/documents/spiva/spiva-us-year-end-2025.pdf); [InvestmentNews](https://www.investmentnews.com/equities/active-managers-stumble-again-in-2025-as-large-caps-dominate/265541); [Ritholtz on 15-year data](https://ritholtz.com/2025/05/the-data-on-active-large-cap-underperformance)). Persistence is near random: of top-half large-cap funds in 2023, 49% stayed top-half through 2025 ([Persistence Scorecard](https://www.spglobal.com/spdji/en/documents/spiva/persistence-scorecard-year-end-2025.pdf)).
- **Barber & Odean, "Trading Is Hazardous to Your Wealth" (JF 2000):** 66,465 brokerage households 1991-96; the most active quintile earned 11.4%/yr vs. 17.9% for the market; the average household 16.4% ([RePEc](https://ideas.repec.org/a/bla/jfinan/v55y2000i2p773-806.html)).
- **Day trading, Brazil (Chague, De-Losso, Giovannetti 2020):** of individuals who day-traded index futures for 300+ days, **97% lost money; only 0.4% earned more than a bank teller** (~US$54/day); no evidence of learning by doing ([RePEc abstract](https://ideas.repec.org/p/fgv/eesptd/525.html)).
- **Day trading, Taiwan (Barber, Lee, Liu, Odean):** 1992-2006 full-market data; fewer than 1% of day traders earned reliably positive net returns ([summary](https://faisalharoon.substack.com/p/day-trading-failure-rate-analysis); [CNBC](https://www.cnbc.com/2020/11/20/attention-robinhood-power-users-most-day-traders-lose-money.html)).
- **Crypto (BIS Working Paper 1049, 2022):** across 95 countries, 2015-22, **73-81% of retail bitcoin app users likely lost money**; new users enter after price rises; 40% are men under 35 ([BIS](https://www.bis.org/publ/work1049.htm); [Bloomberg](https://www.bloomberg.com/news/articles/2022-11-16/vast-majority-of-retail-investors-in-bitcoin-lost-money-bis-says)). A follow-up found the median retail investor had lost about half their investment by December 2022 ([The Block](https://www.theblock.co/post/213372/majority-of-bitcoin-retail-investors-lost-money-in-the-last-seven-years-bis)).
- **The behavior gap (Morningstar Mind the Gap 2025):** US fund investors earned **1.2 percentage points a year less** than their own funds over the decade through 2024 (8.2% fund vs. 7.0% investor), roughly **$3.8 trillion** in forgone wealth; the gap is 0.4 pts in the least-volatile funds and 2.1 pts in the most volatile, so volatility (and the panic it induces) matters more than fees ([Morningstar](https://www.morningstar.com/business/insights/research/mind-the-gap-2025); [Advisor Perspectives](https://www.advisorperspectives.com/commentaries/2026/08/21/what-advisors-can-learn-from-the-investor-return-gap?topic=etf)).

The lesson is not "markets are efficient" but "the expected value of *your* active trading is negative after costs, taxes and behavior, and the variance is high." For a founder, the opportunity cost is worse: every hour spent trading is an hour not spent on the one asset where you *do* have an edge, your business.

### 3.3 Dollar-cost averaging vs. lump sum

Vanguard (2012, updated 2023): lump-sum investing beat DCA **~68% of the time** 1976-2022, by ~2.2%/yr for all-stock portfolios, because markets rise more often than not; DCA loses less in down markets and is the right choice if the alternative is not investing at all ([Vanguard 2012 PDF](https://militarymoneymanual.com/wp-content/uploads/2021/08/Dollar-Cost-Averaging-Just-Means-Taking-Risk-Later-Vanguard.pdf); [SmartAsset on the 2023 study](https://smartasset.com/investing/lump-sum-investing-research)). For a founder with lumpy income, the practical rule: automate a fixed monthly transfer (that is DCA by default), and when a windfall arrives, invest it promptly rather than waiting for a dip.

### 3.4 Emergency fund

Bankrate's January 2026 survey: only **30%** of Americans would pay a $1,000 emergency from savings; 33% would borrow; 47% have *any* liquidity to cover it ([Bankrate](https://www.bankrate.com/press-releases/just-30-of-americans-say-they-would-pay-an-emergency-expense-of-1000-from-savings/)). For an employee the usual guidance is 3-6 months of expenses. For a solo founder whose income can go to zero with one lost client, **6-12 months of personal expenses plus 1-3 months of business operating costs** in a high-yield savings or Treasury money-market account is the floor. The reason is not just safety: a founder with runway can decline bad clients, hold out for better terms, and avoid selling investments at the bottom. The emergency fund is what makes every other strategy on this list survivable.

### 3.5 The compounding math from a $0 start

Years to reach $1,000,000 from zero, contributing monthly, with returns compounded monthly (my calculation):

| Monthly contribution | Annual savings | Years at 7% real | Years at 10% nominal |
|---|---|---|---|
| $250 | $3,000 | 45.8 | 35.6 |
| $500 | $6,000 | 36.4 | 28.9 |
| $1,000 | $12,000 | 27.6 | 22.5 |
| $2,000 | $24,000 | 19.6 | 16.5 |
| $3,000 | $36,000 | 15.5 | 13.4 |
| $5,000 | $60,000 | 11.1 | 9.9 |
| $8,000 | $96,000 | 7.9 | 7.2 |
| $10,000 | $120,000 | 6.7 | 6.2 |

Two things jump out. First, Ramsey's 28-year median is literally the $1,000/month row at 7% real: the typical millionaire is a $1k/month saver. Second, going from $1,000 to $5,000 a month cuts the timeline from 28 years to 11; going from 7% to 10% returns only cuts it from 28 to 22. **Contribution rate dominates return rate for the first million.** Return rate only dominates once the portfolio is large: at $1M, a 7% return is $70k a year, which is more than most people can save.

What $1,000/month becomes at 7% real: $173k after 10 years, $521k after 20, $1.22M after 30. The last decade produces more than the first two combined.

---

## 4. The income side: why the first million is earned, not compounded

### 4.1 The evidence

- The compounding table above: at typical savings rates, investing alone takes 25-45 years to produce $1M.
- SCF 2025: the top income decile has a median net worth of $3.67M and a 40% business-ownership rate; the bottom half has 8% ownership and a median net worth under $100k.
- Smith et al.: top-1% income is mostly pass-through business income from owner-operated firms, and it collapses when the owner leaves. This is wealth that *is* the person's work, capitalized.
- Stanley: two-thirds of millionaires were self-employed.
- Ramsey: the millionaires who got there fastest (5% in under 10 years) are the ones with the highest incomes relative to spending, not the best stock-pickers (none credited stock-picking).
- UBS 2025: 74% of US billionaires are self-made and essentially all of them made it by owning equity in an enterprise, not by salary or by investing someone else's returns.

### 4.2 "Own equity in something that scales"

Naval Ravikant's 2018 thread ("How to Get Rich Without Getting Lucky") compresses the structural insight: you will not get rich renting out your time; you need equity in a business; and the forms of leverage that do not require permission (code, media, and increasingly AI-driven products) let a single person serve thousands of customers ([summary](https://www.alexanderjarvis.com/how-to-get-rich-without-getting-lucky-by-naval-ravikant/)).

For a solo founder this translates into a ladder:

1. **Time for money** (freelancing, consulting): income capped by hours x rate. Fast to start; wealth ceiling ~$150-300k/yr; no equity value because the business *is* you (Smith et al.'s "profit falls by three-quarters after the owner leaves").
2. **Productized service / retainers**: same hours, higher margin, more predictable; still mostly non-transferable.
3. **Products** (software, courses, templates, content with ads/sponsorship, e-commerce): marginal cost near zero; income decoupled from hours; the business has a sale value (typically 2-6x annual profit for small online businesses, higher for SaaS).
4. **Equity in a scalable company** (your own C-corp with QSBS, or a stake in someone else's): the only rung where a $10M+ outcome is possible, and the rung with the highest failure rate.

The data say most people who become millionaires do so on rungs 1-2 plus a 25-30% savings rate over 25-30 years. Rungs 3-4 are what compress that to a decade. The founder's strategic question is not "how do I pick stocks" but "how do I move up one rung while keeping the cash flow from the rung below."

### 4.3 Billionaire playbooks: replicable principle vs. survivorship bias

| Person | What actually happened | Replicable principle | Survivorship / non-replicable part |
|---|---|---|---|
| **Jeff Bezos** | Left a senior job at D.E. Shaw in 1994; told his parents they would "very likely" lose the $245,573 they invested; estimated a 30% chance of success; framed the decision with the "regret minimization framework" ([Benzinga](https://benzinga.com/news/22/12/30238632/how-jeff-bezos-principle-of-regret-minimization-can-make-investors-rich); [A Wealth of Common Sense](https://awealthofcommonsense.com/2016/10/the-jeff-bezos-regret-minimization-framework/)) | Decide on the asymmetric bet early (age 30, before obligations compound); accept you will probably fail; obsess over customers and long time horizons | Had family capital, elite credentials, Wall Street network, and launched at the exact start of consumer internet. The 30% estimate was itself optimistic for most founders. |
| **Elon Musk** | Put $100M of his $180M PayPal proceeds into SpaceX, $70M into Tesla, $10M into SolarCity, and "had to borrow money for rent" ([Ritholtz/TED 2017](https://ritholtz.com/2017/05/elon-musk-ted-2017)) | Concentration in what you control; reinvest proceeds from exit #1 into exit #2 | Concentrating everything is the strategy with the highest variance; we only hear about the one who did not go to zero. Not advisable with your only $180k. |
| **Warren Buffett** | 19.7% compounded 1965-2025 vs. 10.5% S&P, mostly by owning whole businesses and insurance float | Long holding periods; buy businesses, not tickers; let compounding run for 60 years; avoid leverage that can force a sale | His edge was built in a less-efficient market decades ago with insurance float as free leverage; essentially no retail investor has replicated it. The SPIVA data are the base rate. |
| **Ray Dalio** | Founded Bridgewater in 1975 from a two-bedroom apartment; publicly called a 1982 crash that did not come, lost "just about everything," laid off nearly all staff, borrowed $4,000 from his father; rebuilt with systematic rules and diversification ([CNBC](https://www.cnbc.com/2022/06/02/ray-dalio-going-broke-was-one-of-the-best-things-to-ever-happen-to-me.html)) | Write down your decision rules; diversify so that no single forecast can end you; treat pain as a signal to reflect | Being wiped out at 33 is only a "great lesson" for those who survived; most do not get the second act. |
| **Mark Cuban** | Sold MicroSolutions for ~$6M (1990), Broadcast.com to Yahoo for ~$5.7B in stock (1999), then **hedged the Yahoo shares with a collar** before the dot-com crash, which he says saved most of his fortune ([Wikipedia](https://en.wikipedia.org/wiki/Mark_Cuban); [Entrepreneur](https://www.entrepreneur.com/article/239334)) | Sell your first company for enough to be free; **when you get illiquid concentrated stock, hedge or diversify it**; the exit is not the win until it is diversified | Broadcast.com's price was a bubble artifact; the hedge was the actually skilled move and is the most replicable lesson here. |
| **Peter Thiel** | PayPal co-founder; 1.7M founder shares in a Roth at $0.001 grew to ~$5B tax-free; early Facebook investor; *Zero to One* argues competitive markets destroy profits and founders should build monopolies ([ProPublica](https://www.propublica.org/article/lord-of-the-roths-how-tech-mogul-peter-thiel-turned-a-retirement-account-for-the-middle-class-into-a-5-billion-dollar-tax-free-piggy-bank); [Wharton](https://knowledge.wharton.upenn.edu/article/peter-thiels-notes-on-startups/)) | Pick a niche small enough to dominate, then expand; put highest-growth assets in Roth space; avoid commodity competition | The Roth move required founder shares at a nominal valuation plus a custodian willing to hold them; the IRS and Congress have scrutinized it since. Monopoly advice is easier to give than to execute. |

**The common replicable core:** (1) all of them owned equity in an enterprise they controlled; (2) all took their big risk early, when a wipeout was recoverable; (3) all reinvested the first exit into the second; (4) the ones who kept their fortunes (Cuban, Buffett, Dalio post-1982) did so through diversification and hedging, not through continued concentration.

**The survivorship bias to keep in view:** BLS data show only ~49% of new employer establishments survive five years and **34.7% of those born in 2013 were still operating in 2023** ([BLS](https://www.bls.gov/opub/ted/2024/34-7-percent-of-business-establishments-born-in-2013-were-still-operating-in-2023.htm)). Venture-scale outcomes are a tiny tail of that. The base-rate-consistent strategy is: build a cash-flowing business first (rungs 1-3), keep the personal balance sheet diversified and boring (Section 3), and take concentrated bets only with capital you can afford to lose entirely.

---

## 5. A wealth operating system for a solo founder starting from near zero

Ordered by when each item becomes worth the time. Every item is standard practice; none is a loophole.

### Month 1: foundations (cost: a few hundred dollars, ~10 hours)

1. **Separate the money.** Open a business checking account and a business credit card; never commingle. This is the prerequisite for every deduction and for liability protection.
2. **Form an LLC** in your home state (or operate as a sole prop for the first few months if cash is tight; the tax result is identical). Get an EIN (free, IRS).
3. **Bookkeeping from day one.** Cheap software or a spreadsheet; categorize monthly. The home office, equipment, software, and mileage deductions are only real if documented.
4. **Open a Roth IRA** (if under the $153k/$242k phase-outs) and set an automatic monthly transfer, even $100. The habit matters more than the amount at this stage.
5. **Start the emergency fund** in a high-yield savings account; target 1 month of expenses before anything else.
6. **Buy health insurance**; if on the ACA marketplace, choose a bronze or catastrophic plan if you are healthy, because as of 2026 those are HSA-compatible. **Open an HSA** and contribute what you can (up to $4,400/$8,750).
7. **Set the pricing floor.** Compute your real hourly cost including 15.3% SE tax, health insurance, and unpaid time; most new freelancers underprice by 30-50%.
8. **Quarterly estimated taxes.** Set aside 25-35% of every payment in a separate "tax" savings account; pay by Apr 15 / Jun 15 / Sep 15 / Jan 15.

### Month 3: systems

9. **Review the entity decision** against actual profit run-rate. If it looks like $70-80k+ of annual profit, talk to a CPA about an S-corp election (it can be made effective for the current year within 2 months and 15 days of the start of the tax year, or prospectively).
10. **Open a Solo 401(k)** at a low-cost brokerage (free prototype plans are fine for now). Elect Roth deferrals while your bracket is low.
11. **Claim the home office** (simplified $5/sq ft if under 300 sq ft; actual-expense method if larger). Document the space.
12. **Automate everything:** income account → tax reserve (30%) → emergency fund (until 6 months) → Roth IRA → Solo 401(k) → taxable brokerage, in that order, on the day money lands.
13. **Pick the investment policy once and write it down:** e.g., a total-US or global stock index fund (and, if desired, a bond fund) in every account, rebalanced annually. No individual stocks, no crypto beyond what you can lose, no trading. Revisit the written policy only once a year.
14. **Term life and disability insurance** if anyone depends on your income. Disability is the one solo founders skip and most need.

### Year 1: structure

15. **Hire a CPA for the first business return** and a one-hour planning meeting; ask specifically about S-corp timing, QBI, Solo 401(k) funding, and the self-employed health insurance deduction.
16. **Fund the Solo 401(k) employer contribution** by the filing deadline (20% of net SE income or 25% of W-2 salary).
17. **Emergency fund to 6 months** of personal expenses plus 1-3 months of business fixed costs.
18. **Build the first product-like asset** (template, course, tool, content channel, retainer package): something that earns while you are not working. This is the rung-2-to-rung-3 move and the single highest-return "investment" available.
19. **Decide the long-term entity path.** Cash-flow business you will run: S-corp. Scalable software/product you may sell: consider converting to a C-corp *early* (while assets are far below $75M) to start the QSBS 3/4/5-year clock.
20. **Annual review checklist:** net worth statement, savings rate, tax reserve adequacy, insurance, beneficiary designations, written investment policy.

### At $5k/month revenue (~$60k/yr)

- Elect **S-corp** if profit after expenses is consistently ~$70k+; otherwise stay LLC and revisit at $10k/month. Run a reasonable salary through a payroll service.
- Max the **HSA**; target **$1,000-2,000/month** total into Roth IRA + Solo 401(k).
- Raise prices or drop the bottom 20% of clients; at this level your marginal hour is worth more in sales than in delivery.
- Confirm **QBI** is being claimed (it is automatic on Form 8995 but easy for DIY software to mishandle for S-corps).

### At $10k/month revenue (~$120k/yr)

- **S-corp is almost certainly correct** now. Set salary with the CPA to balance FICA savings against Solo 401(k) space and QBI.
- **Max the Solo 401(k)** ($24,500 deferral + employer contribution) and move deferrals toward pre-tax as the bracket rises; use the **backdoor Roth** once over the phase-out.
- **Augusta rule** for the quarterly planning days you actually hold at home (requires the S-corp).
- **Hire kids** (under 18, through a parent-owned entity) or a spouse if the work is real.
- **Section 179 / bonus** on real equipment needs; do not buy a truck for the deduction.
- Open a **taxable brokerage** and apply **asset location**: bonds (if any) in the 401(k), index equities in taxable.
- Start a **donor-advised fund** if you give; bunch gifts in high-income years to clear the 0.5%-of-AGI floor and deduct above the standard deduction.
- Savings target: **30-40% of gross profit**. At $5,000/month invested, the table says ~11 years to $1M at 7% real.

### At $25k/month revenue (~$300k/yr)

- You are now inside or above the **QBI phase-in** ($201,750 single / $403,500 joint taxable income). Retirement contributions, HSA, and health premiums are the levers that pull taxable income back below the threshold; a CPA should model this every November.
- **Mega backdoor Roth** via a custom Solo 401(k) plan document; consider a **cash-balance plan** if you are 40+ and want $100k+ of additional deductions.
- If the business is a product company: finalize the **C-corp / QSBS** structure; get a 409A-style valuation when issuing stock; keep records proving the active-business and gross-assets tests.
- If the business is a service company: start building a **transferable asset** (team, systems, brand) or accept that the business is a high-income job and plan on a 30%+ savings rate into a diversified portfolio as the wealth engine.
- **Diversify ruthlessly.** This is the Cuban lesson. Keep business reinvestment to what the business needs; everything above that goes into the boring portfolio. Your human capital and business equity are already a concentrated bet.
- **Estate basics:** will, revocable trust if your state's probate is slow, updated beneficiaries, POA, and a buy-sell or continuity plan for the business.
- Consider **real estate** only if you want to manage it or qualify a spouse as a real estate professional; otherwise REIT index exposure inside the 401(k) is the low-effort version.
- At this income, with a 40% savings rate (~$120k/yr), the table gives ~**7 years to $1M**, and a business sale could compress that further. That is the "10 years, not 28" path, and it runs entirely through the income side.

---

## 6. What this research does not resolve

- The 2025 SCF does not break out net worth by self-employment status in the public summary; the two-thirds-of-millionaires-are-self-employed figure rests on Stanley's 1990s surveys and is directionally supported, not replicated, by the SCF business-ownership gradient.
- Ramsey's study is a self-selected panel and is now eight years old.
- Several 2026 tax figures (Section 179, QBI thresholds, SSTB phase-out end points) come from practitioner summaries of Rev. Proc. 2025-32; the $25 discrepancy in the single-filer SSTB cap ($276,750 vs. $276,775) between sources is unresolved here.
- The SE-tax and S-corp savings examples are my arithmetic and ignore state taxes, which can swing the answer.
- Expected future equity returns may well be below the 7% real historical figure; the compounding table should be read as a comparison of savings rates, not a forecast.

*This document is educational research compiled from public sources and is not legal, tax, or investment advice. Consult a licensed professional before acting on any of it.*
