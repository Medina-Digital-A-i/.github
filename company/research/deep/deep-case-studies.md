# Zero to $1M with AI at the Center: 30 Case Files from 2024-2026 and What They Teach

*Investigative research memo. Compiled October 21, 2026. All figures are gross revenue or run-rate unless stated. Evidence grades: **V** = verified by a third party (acquirer press release, SEC filing, Stripe-linked dashboard, Fortune/TechCrunch-reviewed records); **S** = self-reported by the founder in dated primary posts or long-form interviews; **P** = promotional or secondary (vendor case studies, aggregator sites, course marketing). "Solo/1-3" refers to headcount during the climb to $1M, not at exit.*

---

## 0. Method and what got excluded

Criteria: individual or 1-3 person team, started at or near zero in 2022-2025, reached $1M+ in revenue, run-rate, net proceeds or exit value inside 4 years, AI central to the product or the production process. Excluded: venture-backed companies with large teams at the time of the climb (Lovable, Cursor, Jenni AI, Cluely/Interview Coder, Riley Brown's Vibecode, Codeway/AppNation app studios), and founders with a large pre-2023 audience unless the audience's origin is documented. Several sub-$1M cases are kept deliberately because they show the ceiling or the failure mode of an archetype; they are labeled as such.

A note on the evidence base. Most "solo founder" revenue numbers on the internet are copies of copies. For each case I tried to get to the founder's own dated statement or a third-party record, and I grade accordingly. Aggregators (Starter Story, GetLatka, Taskade, GreyJournal, "7 solo founders..." listicles) were used only to find primary sources, never as the number of record. One skeptical fact-check site, income-reality-check.pages.dev, was useful precisely because it tries to pull apart the "non-coder with ChatGPT" framing on Blake Anderson's apps.

---

## 1. Case files

### Archetype A: Self-serve vertical AI SaaS ("wrapper with a wedge")

**A1. Chatbase — Yasser Elsaid (solo at climb)** — Grade S→V (later Stripe-linked via TrustMRR)
- **What/pays for:** "ChatGPT for your data": custom support/lead-gen chatbots trained on a company's docs. Subscriptions $9-$399+/mo; most revenue from top tier and enterprise.
- **Acquisition:** Twitter demo video (first paying customer within 30 minutes per Stripe), amplified by AI influencers including Rowan Cheung; repeated Product Hunt launches; Reddit (free chatbots for popular books/communities); Indie Hackers; AI directories; later SEO, Google Ads, Shopify integration, affiliates, warm outbound. No cold selling for the first $5M.
- **Capital:** None. Student side project (4th year of university, age 24; prior internships at Meta/Tesla/BlackBerry).
- **Timeline:** Demo tweet Feb 2-4, 2023 → ~$3k MRR end Feb → $10k MRR mid-Mar → $64k MRR mid-May → ~$1M ARR 117 days after first payment (≈June 2023) → ~$3M ARR Feb 2024 → ~$5M ARR Feb 2025 → $8M ARR Dec 2025 (team 18) → crossed $10M ARR spring 2026 (team 26); ~$19M all-time revenue by mid-2026. Turned down a ~$1M source-code buyout at month three.
- **AI vs human:** AI (OpenAI + RAG via LangChain/Pinecone) does the retrieval-and-answer. Yasser chose the wedge (customer-support bots trained on your own data), shipped two months after idea, answered every support email himself until mid-2023, and did pricing/packaging.
- **Status:** Operating, bootstrapped, ~26 people, SOC2/HIPAA, enterprise customers (IHG, Miele). Stopped publishing raw revenue after $10M ARR.
- **Lesson:** Distribution was a 60-second demo video of a product that worked the first time; the moat came later from going upmarket while the wrapper pack stayed in the consumer bucket.
- Sources: Starter Story breakdown https://www.starterstory.com/stories/chatbase-breakdown ; Supabase customer story https://supabase.com/customers/chatbase ; EO interview https://www.eomag.io/article/chatbase-yasser-elsaid ; Yasser on X (Feb 2025) https://x.com/yasser_elsaid_/status/1894801760587522417 ; ClerkChat timeline (competitor-published, TrustMRR-sourced) https://clerkchat.co/blog/how-chatbase-hit-20m-revenue-with-zero-vc ; Webtribunal https://webtribunal.net/chatbase-10-million-arr/

**A2. Formula Bot (Excel Formula Bot) — David Bressler (solo, no-code)** — Grade S
- **What/pays for:** Natural-language → Excel/Sheets formulas, later a broader AI data-analysis workspace. Freemium subscription.
- **Acquisition:** One Reddit post on r/excel (top post of the week) brought ~100k visitors overnight and a surprise ~$4-5k OpenAI bill; later r/InternetIsBeautiful; Google Ads to convert the free tool; SEO.
- **Capital:** ~$35 (Bubble $25/mo + $10 domain). Built in a weekend / six weeks on paternity leave with zero coding background, YouTube tutorials.
- **Timeline:** Launched Sept 2022 → $30k revenue in first 3 months → >$26k MRR within six months → ~$500k ARR (Indie Hackers post, ~$42k/mo) → quit Senior Director of Analytics job once Formula Bot out-earned salary → "over $1M in revenue" per podcast descriptions and Bubble/n8n case studies (1M users). Later added two developers and n8n backend because Bubble hit limits.
- **AI vs human:** GPT writes the formulas. Bressler found the pain (he lived it in analytics), wrote the Reddit post, set up paid plans fast enough to capture the spike, and later rebuilt the backend.
- **Status:** Operating; 1 founder + 2 devs.
- **Lesson:** A narrow, verifiable output (a formula that works or doesn't) plus a community where the pain is discussed daily beat any "AI for everything" positioning.
- Sources: nocode.mba case study https://www.nocode.mba/articles/nocode-case-study-formulabot ; Bubble showcase https://bubble.io/showcase/formula-bot ; n8n case study https://n8n.io/case-studies/formula-bot/ ; Indie Hackers ($500k ARR) https://www.indiehackers.com/post/tech/getting-serious-about-marketing-after-hitting-500k-arr-8XGnzrxG1neA3jy37x2D

**A3. HeadshotPro — Danny Postma (solo)** — Grade S (prior small audience; explained)
- **What/pays for:** AI professional headshots, $29/session or $69 for three; B2C with team packs.
- **Acquisition:** Twitter buzz from his earlier ProfilePicture.AI (the Dec 2022 avatar boom), then SEO: top-10 for "professional headshots", 200+ programmatic city/county pages, Product Hunt backlinks.
- **Capital:** Minimal; ~30 hours to first version on Stable Diffusion + DreamBooth, with LLaVA quality checks and Codeformer artifact cleanup.
- **Prior audience:** Postma had sold Headlime (AI copywriting) to Jasper in 2021 and had a mid-size maker following on Twitter. He is included because the audience is documented and because SEO, not Twitter, carried the business past the first month.
- **Timeline:** March 2023 launch → ~$100k ARR in 14 days → ~$300k MRR reported Sept-Dec 2024 (≈$3.6M run-rate). Early servers "often went offline".
- **AI vs human:** Diffusion models do the imaging; Postma tuned for realism beyond open-source baselines and built the programmatic SEO machine.
- **Status:** Operating; he later hired a small team. ProfilePicture.AI (the predecessor) faded with the avatar fad — a boom-bust inside the same founder's portfolio.
- **Lesson:** Ride the fad for cash, then move to the durable query people type into Google every day ("professional headshots").
- Sources: Starter Story https://www.starterstory.com/stories/headshotpro-breakdown ; profile https://startupfounderstories.com/stories/danny-postma-headshotpro-ai-headshots

**A4. TypingMind — Tony Dinh (solo + freelancers)** — Grade S (audience built 2021-22; explained)
- **What/pays for:** A better chat UI for LLM APIs (bring your own key); one-time personal licenses, then Team/B2B subscriptions which passed 50% of monthly revenue in 2025.
- **Acquisition:** Word of mouth; a $600 paid test produced 2 conversions ("I'm really bad at marketing"). His X audience (~50k by 2023, built from 2021 by sharing side projects like Black Magic, $5k/mo in 2022) seeded the launch.
- **Capital:** None; built in five days, March 2023; $22k in first week.
- **Timeline:** Mar 2023 launch → ~$30k/mo mid-2023 → $1M trailing-12-month revenue by Nov 2024 → $130-160k/mo in Oct 2025 → best month $210k+ (Dec 2025). Works ~4 h/day, lives off investments.
- **AI vs human:** The models are the product; Dinh's contribution is UX (multi-model parallel chat, RAG knowledge base) and relentless shipping.
- **Status:** Operating.
- **Lesson:** When the model vendor's own UI is mediocre, a polished front end with a BYO-key pricing hack can earn seven figures — but the B2B team plan is what made it durable.
- Sources: Oct 2025 newsletter https://news.tonydinh.com/p/oct-2025-updates-code-money-and-travel ; Starter Story https://www.starterstory.com/typingmind-breakdown ; analysis of the "solo" claim https://www.sofarbot.com/stories/tony-dinh-typingmind-45k-month-vietnam

**A5. Submagic — David Zitoun + 1 co-founder (2 at climb, 10-13 by 2025)** — Grade S
- **What/pays for:** AI captions/emoji/hook titles/"Magic Clips" for short-form video; subscriptions.
- **Acquisition:** Affiliate program launched ~30 days after first customer because there was no marketing budget; 10,000+ affiliates now drive ~20% of ARR at 30% lifetime commission (~$45k/mo payouts); Product Hunt #2 (July 3, 2023) triggered the pivot to the US market; SEO/free tools second channel. No sales team.
- **Capital:** $0 outside funding. Zitoun had edited video since age 12; co-founder spent 8 years on a website builder.
- **Timeline:** May 1, 2023 first customer → $1M ARR in 90 days (≈Aug 2023) → plateau at $5M ARR for 7-8 months → 1M users June 2024 → $8M ARR June 2025 with 13 people (~$600k revenue/employee). 15% monthly logo churn.
- **AI vs human:** Whisper-class transcription plus LLM hook generation; humans built the affiliate machine and did pricing experiments (lowered prices when stalled).
- **Status:** Operating, bootstrapped.
- **Lesson:** An affiliate program is the cold-selling substitute for creator-tool SaaS — the customers are themselves distribution.
- Sources: Superframeworks case study https://superframeworks.com/case-study/submagic ; Baremetrics Founder Chat (Nov 2025) https://baremetrics.com/founder-chats/david-zitoun ; Latka podcast https://nathanlatkathetop.libsyn.com/how-i-built-my-ai-tool-submagic-to-667kmonth-with-a-tiny-team-and-no-funding

**A6. Castmagic — Blaine Bolus, Ramon Berrios, Justin Tormey (3)** — Grade S
- **What/pays for:** Turn podcast/video audio into show notes, posts, clips; from $39/mo with usage caps.
- **Acquisition:** AppSumo lifetime deal (~$350k revenue, ~10k users at launch), paid creators and affiliates sourced by scraping Instagram hashtags, content.
- **Capital:** Self-funded; MVP in ~14 days (Elixir/Phoenix). Founders had prior venture-backed startup experience and ran DTC Pod.
- **Timeline:** March 2023 launch → $1M ARR in under 9 months → ~$2M ARR with ~10 people (Refresh Miami, 2025).
- **AI vs human:** LLM summarization/transcription; humans ran AppSumo + creator sourcing and controlled LLM cost with caps.
- **Status:** Operating, bootstrapped.
- **Lesson:** A lifetime deal is capital; it bought them a year of runway and 10k testers in one week.
- Sources: Indie Hackers post https://www.indiehackers.com/post/boostrapping-ai-startup-castmagic-to-1m-in-under-9-months-27bf7c9402 ; Refresh Miami https://refreshmiami.com/news/its-not-just-magic-its-ai-meet-the-miami-startup-turning-conversations-into-content/ ; Starter Story https://www.starterstory.com/castmagic-breakdown

**A7. Virtual Staging AI — Michael Bonacina & Mikhail Andreev (2)** — Grade V (acquirer announcement) / S (ARR)
- **What/pays for:** Adds furniture to empty-room listing photos for real-estate agents; subscriptions (>3,000-4,500 paid subscribers, >500k renders/month).
- **Acquisition:** Self-serve, SEO/word-of-mouth inside the real-estate agent community; proptech consulting partnership.
- **Capital:** Started at Harvard Innovation Labs 2023; co-founder says "bootstrapped to $1M ARR in ten months".
- **Timeline:** 2023 build → $1M ARR in ~10 months → acquired by Zillow Group, October 2024 (price undisclosed).
- **AI vs human:** Image generation/inpainting; the founders picked a vertical with a known $ per listing and an existing manual-service price anchor (human virtual staging at $25-100 per photo).
- **Status:** Inside Zillow.
- **Lesson:** "Boring" verticals with an existing service price list are where AI wrappers get acquired rather than cloned.
- Sources: GeekWire https://www.geekwire.com/2024/zillow-group-acquires-vsai-a-virtual-staging-tool-that-adds-furniture-to-real-estate-listings/ ; Crunchbase https://www.crunchbase.com/organization/virtualstagingai ; Andreev on LinkedIn https://www.linkedin.com/in/andreev-mikhail/

**A8. Undetectable AI — Christian Perry (+ co-founder, then team)** — Grade S/P (borderline on team size)
- **What/pays for:** AI-detection and "humanizer" rewriting; subscriptions.
- **Acquisition:** 100k waitlist by March 2023 (PR, SEO on the "AI detector" query wave), affiliates.
- **Capital:** Funded from revenue of a prior venture (ChatterQuant); no outside money.
- **Timeline:** Beta Mar 2023, public May 2023 → 2M users in 6 months → 11M users Nov 2024 → CEO claims $10M revenue (Sept 2025); GetLatka estimates $3.7M with 34 staff. Team grew well beyond 3 — included because the first $1M was reached by 1-3 people riding the detector query.
- **Lesson:** Query-wave products (detectors, humanizers) scale fast and attract copycats faster; the founder's own prior cash was the moat.
- Sources: PR Newswire https://www.prnewswire.com/news-releases/undetectable-ai-reaches-11-million-users-in-18-months-since-launch-302303963.html ; Sramana Mitra series https://www.sramanamitra.com/2025/10/01/best-of-bootstrapping-bootstrapped-an-ai-startup-to-10m/ ; GetLatka https://getlatka.com/companies/undetectable.ai#funding

**A9. StealthGPT — Jozef Gherman (solo)** — Grade S (inconsistent)
- Same category as A8. Launched Jan 2023; founder posted that it "hit a revenue of a million dollars" (undated, unclear if ARR or cumulative); GetLatka lists $2.2M for 2023; Starter Story snapshot shows $15.5k MRR at 14 months. Treat as "probably crossed $1M cumulative, run-rate unclear." Included to show how fuzzy "I hit $1M" claims are in this sub-niche.
- Sources: Indie Hackers https://www.indiehackers.com/product/stealthgpt ; Starter Story https://www.starterstory.com/stories/stealthgpt-breakdown ; Crunchbase https://www.crunchbase.com/organization/stealthgpt

**A10. Photo AI — Pieter Levels (solo)** — Grade S (pre-existing audience; included as the control case)
- **Why included despite the audience rule:** Levels had ~100k+ X followers before 2023 built over a decade of Nomad List/RemoteOK. He is the ceiling for what a solo wrapper can do with distribution already solved, so he anchors the top of the curve.
- **Timeline:** Launched Feb 10, 2023 (~$5.4k week one) → $28.7k/mo Apr 2023 → $61.8k/mo Jul 2023 → >$100k/mo Sept 2024 → ~$132k/mo (2025), ~$150k month at 87% margin Sept 2025; bio shows ~$100k/mo in 2026. ~2,000 subscribers at $19-$199; compute ~$12-13k/mo on Replicate. One 40,000-line PHP file, SQLite, one Hetzner server. About half of traffic from X.
- **Lesson:** Even with the best audience in indie software, the product that renews (Photo AI) outlasted the product that went viral (see C6, Fly Pieter).
- Sources: aituts case study https://aituts.com/case-study/photo-ai-pieter-levels/ ; Indie Hackers deep dive https://www.indiehackers.com/post/photo-ai-by-pieter-levels-complete-deep-dive-case-study-0-to-132k-mrr-in-18-months-3a9a2b1579

**A11. Blotato — Sabrina Ramonov (solo)** — Grade S/P
- **What/pays for:** AI social-content repurposing and auto-posting, $29-$499/mo.
- **Acquisition:** Her own short-form content (claims 0 → 200k followers in 4 months before launch, 3.5M+ by 2026, posting 100+ pieces/week with automation), DM automations, early-adopter waitlist of 50.
- **Capital:** "$0 beyond tools"; $60 Webflow template. Prior wealth from selling Qurious to Pegasystems (so not financially at zero).
- **Timeline:** Aug 1, 2024 first TikTok → Oct 20, 2024 launch → "linear" growth; blog title claims a "$1M solo AI business" but the post never states a figure; IntelPilot estimates $500k-$2M ARR. Rebuilt the Cursor-generated MVP ("terrible spaghetti code") in Next.js/Fastify/Supabase once it was making money.
- **Lesson:** Content distribution built *while* building the product is the modern substitute for an audience — but revenue claims that live only in headlines should be discounted.
- Sources: her post https://www.sabrina.dev/p/how-i-built-a-1m-solo-ai-business ; X thread on DM automation https://x.com/Sabrina_Ramonov/status/2092416741003407360 ; IntelPilot estimate https://www.intelpilot.ai/company/blotato/6a067e90a6715bdc3096572b

**A12. EasyGen — Ruben Hassid (1 → ~6-8)** — Grade S (sub-$1M; ceiling case)
- LinkedIn post generator. Hassid built ~400k LinkedIn followers from near zero in 2022-23 by posting about ChatGPT; EasyGen hit $33k MRR in 5 months and $540k ARR by end of 2024 (his own wrap-up); GetLatka estimates $880k for 2025. Never clearly crossed $1M ARR — an "audience → tool" case that stalled under $1M, which is informative.
- Sources: Starter Story https://www.starterstory.com/easy-gen-breakdown ; GetLatka https://getlatka.com/companies/easygen.io ; profile https://www.timstodz.com/p/how-ruben-hassid-used-ai-to-create

---

### Archetype B: Consumer mobile AI apps with paid-creator distribution

**B1. Cal AI — Zach Yadegari & Henry Langmack (+ Blake Anderson as funder/operator, Jake Castillo as COO)** — Grade V (TechCrunch/MyFitnessPal statement; CNBC; CBS)
- **What/pays for:** Photo-based calorie counting; weekly/annual subscriptions.
- **Acquisition:** Paid micro-creators (~$50 per TikTok post, DM 100 creators → ~10 replies → ~3 conversions), reinvested whenever 1,000 views cost less than they earned; full-time creator-marketing operator; App Store ranking flywheel (MyFitnessPal tracked it on Sensor Tower).
- **Capital:** Yadegari had sold Totally Science (a gaming site) for $100k at 16; Anderson "helped fund operating and marketing costs."
- **Timeline:** Launched May 2024 → ~$1M MRR within ~6-8 months (CNBC reported ~$1.4M/mo gross profit after store cuts) → $8M ARR claim Oct 2024 (Anderson) → 8.3M downloads July 2025 → >$30M annual revenue, 15M+ downloads, acquired by MyFitnessPal (deal closed Dec 2025, announced March 2, 2026, price undisclosed; seven employees plus contractors retained). Yadegari, 19, still runs it from college.
- **AI vs human:** A paid vision model identifies food and estimates macros (recurring API cost per photo). Humans: picked a category with existing habit (MyFitnessPal) and made the input 10x easier; ran creator ops as a daily job.
- **Status:** Acquired; independent app inside MyFitnessPal.
- **Lesson:** The app was a thin wrapper; the business was a repeatable $50-per-post creator-seeding operation run like a trading desk.
- Sources: TechCrunch https://techcrunch.com/?p=3098039 ; CNBC https://www.cnbc.com/make-it/2025/09/06/cal-ai-how-a-teenage-ceo-built-a-fast-growing-calorie-tracking-app.html ; CBS NY https://www.cbsnews.com/newyork/news/zach-yadegari-cal-ai-founder-long-island/ ; fact-check https://income-reality-check.pages.dev/a/he-made-rizzgpt-which-makes-him-1-million-a-month/

**B2. RizzGPT (now Plug AI) and Umax — Blake Anderson (+ brother on backend, co-founder)** — Grade S (self-reported; third-party totals vary from $10M to $60M)
- **What/pays for:** RizzGPT: AI replies for dating apps. Umax: facial-attractiveness rating and advice ("looksmaxxing"). Weekly subscriptions.
- **Acquisition:** Paid ~$50 per account on faceless TikTok/YouTube accounts → 200k downloads in five days, ~$80k MRR; Umax got ~half its downloads from Apple featuring.
- **Capital:** Near zero; non-technical, learned to build with ChatGPT in 2023, coded "in an attic."
- **Timeline:** RizzGPT early 2023 → ~$80k/mo peak, $2.4-2.6M lifetime. Umax 2024 → $100k month one, $200k month two, ~$500k/mo peak, best personal month $700k (Feb 2024), $4-6M lifetime; by July 2025 Umax was ~$270k/mo (his own post) — a sharp decline from peak.
- **Status:** Apps live at lower run-rates; Cal AI exit. Anderson's "I never wrote code" framing is disputed by the fact-check: he had a brother doing backend, a co-founder who had sold a company, and a full-time creator marketer.
- **Lesson:** Hit-driven. Each app rode a model-capability window (GPT-4 Vision made face-rating cheap) and a creator-seeding window; the decay after peak is the norm, so you need the next app before the current one fades.
- Sources: Scale Nuggets https://scalenuggets.beehiiv.com/p/23yearold-whos-making-11myear-ai-apps ; Tiffany Zhong on X https://x.com/tzhongg/status/2028931446317232397 ; Startup Series https://startupseries.io/how-blake-anderson-made-5-million-in-apps-using-chatgpt/ ; fact-check (above)

**B3. Wave: AI Note Taker — Josh Mohrer (solo + occasional contractors)** — Grade S (podcast interviews; Adapty case study)
- **What/pays for:** iOS/Android voice-note transcription + summaries, meeting bots, phone-call capture; weekly/monthly/annual (annual is most revenue).
- **Acquisition:** Meta ads took it from ~$1M to ~$6M ARR in four months two years ago, then stopped working for over a year; now Apple Search Ads + Google Ads deliver 800-1,000 installs/day; 4.9 stars / 11k reviews; constant paywall A/B testing via Adapty.
- **Capital:** Bootstrapped; former Uber NYC GM, math degree, basic React Native from a stint at Levels; between jobs when ChatGPT launched.
- **Timeline:** 2023 prototype built in a day → $4M ARR in 8 months → ~$7M/yr by 2025 (flat for months; ~$5M after store cuts, ~$3M kept). Cursor "home base," now Claude Code/Opus almost exclusively.
- **AI vs human:** AI writes nearly all the code and does the transcription/summaries (Whisper/AssemblyAI/Deepgram tested). Mohrer does support himself, runs ads, and admits "nothing built in the past year has mattered."
- **Status:** Operating, solo, profitable, growth-flat; competitor copied app and pricing; Apple could ship the feature natively.
- **Lesson:** A non-engineer with operating experience and the willingness to spend on ads can reach eight figures on mobile — but the plateau arrives when the paid channel saturates and the platform owner looms.
- Sources: Mixergy (Feb 2026) https://mixergy.com/interviews/the-7-million-vibe-coded-app/ ; Adapty case study https://adapty.io/case-studies/wave/ ; App Masters podcast https://podcasts.apple.com/gb/podcast/bootstrapping-an-ai-app-to-%242m-arr/id643216602?i=1000665022498

**B4. Talknotes + MakeLogo.ai — Nico Jeannen (solo)** — Grade S (own X posts) — *sub-$1M; failed-after-success case*
- **What/pays for:** Talknotes: AI voice-to-text notes app, subscriptions. MakeLogo: AI logos (fulfilled by hand with Typeform checkout before the app existed).
- **Acquisition:** Directory listings + a few Twitter sales ($700 in 10 days), Product Hunt Product of the Day (→ $1.5k MRR), then Meta ads with an onboarding-form feedback loop (MRR doubled in ~2 months). Launched MakeLogo with <600 followers.
- **Capital:** None beyond reinvested revenue ("no ads until cash flow"). Background: media buyer who managed $1M+ of Meta spend, learned to code in 2022.
- **Timeline:** Dec 2022 MakeLogo built in 48h → sold on Acquire.com for $65k three months later. Aug 2023 Talknotes MVP in a week → $7.5k MRR at 11 months → bugs after a release, signups -70%, burnout → listed and sold for $200k cash (July 2024; could have taken $300k on terms). Three exits ≈ $290k; said he was "30% away from being a millionaire." Then a year of "loss of purpose"; April 2026 launched AdKit (AI agents running ad campaigns, 500+ marketers).
- **Lesson:** Paid-ads skill is a transferable moat; but a solo founder's revenue is capped by their own nervous system — he sold at the first bug-induced dip.
- Sources: his sale thread https://x.com/nico_jeannen/status/1808130671493406761 ; Indie Hackers https://www.indiehackers.com/post/getting-acquired-for-200k-within-11-months-by-leveraging-facebook-ads-1fhPcnhMPbvMbqSWGUjS ; No-Code Exits https://nocodeexits.substack.com/p/three-exits-for-290000-then-a-year ; purpose post https://x.com/nico_jeannen/status/1957054052204007817

---

### Archetype C: Vibe-coded platforms and agent products (2025-2026)

**C1. Base44 — Maor Shlomo (solo for ~5 of 6 months; 8 staff at sale)** — Grade V (Wix press release; Wix FY2025 Form 20-F)
- **What/pays for:** Prompt-to-app builder with built-in backend/auth/db; subscriptions.
- **Acquisition:** Zero paid marketing; built in public on LinkedIn (posting the $189k May 2025 profit figure spread through founder circles); 10k users in three weeks, 250k at six months, 400k+ at sale.
- **Capital:** ~$10-20k of his own money; previously co-founded Explorium (raised ~$127M), so experienced but not rich from an exit; did reserve duty after Oct 7 before starting.
- **Timeline:** Launched ~Feb 2025 → $1M ARR three weeks after launch → $1.5M ARR at week four → ~$3.5M ARR by June → $189k profit in May 2025 (model calls were 89% of spend; moved from OpenAI to Bedrock/Vertex/Anthropic and stopped charging users for failed generations) → first employee hired ~6 weeks before deal → acquired by Wix June 18, 2025: ~$80M initial consideration incl. ~$25M retention pool, plus earn-outs through 2029; Form 20-F records $92.2M total consideration ($18.1M cash + $74.1M fair value of contingent earn-out). Calcalist reports up to ~$90M more if milestones hit, and Base44 at ~$100M ARR nine months post-deal.
- **AI vs human:** Cursor + Claude wrote the code ("I hadn't written front-end code in three months"); Shlomo did architecture, problem selection, watched user behavior, and managed unit economics. He said he felt lonely building solo.
- **Lesson:** The product that sells vibe coding to non-coders was itself vibe-coded by an expert; experience in picking what to build was the scarce input.
- Sources: Wix press release https://www.wix.com/press-room/home/post/wix-further-expands-into-vibe-coding-with-acquisition-of-base44-a-hyper-growth-startup-that-simplif ; Wix 20-F FY2025 https://www.sec.gov/Archives/edgar/data/1576789/000162828026015222/wix-20251231.htm ; Calcalist https://www.calcalistech.com/ctechnews/article/rkogikc9le ; Promptway profile https://promptway.com/blog/maor-shlomo-base44-wix-exit ; Inc. https://www.inc.com/ben-sherry/how-this-founder-sold-his-vibe-coding-startup-for-80-million-just-4-months-after-launching-it/91225024

**C2. Polsia — Ben Broca (solo, no employees; True Ventures invested after launch)** — Grade S/P (Latent Space podcast; investor blog)
- **What/pays for:** "Self-running companies": a CEO agent on Claude Opus that plans, codes, markets, does outreach, ads, email, support for the customer's business; revenue-share model mentioned; 1,100-3,000 businesses on platform; customers average ~15 messages/day with their "AI co-founder"; 20-25% use it for existing businesses.
- **Timeline:** Launched ~Jan 2026 → $1M ARR within ~30 days ($100k → $1M in two weeks) → ~$3M ARR a month later (True Ventures, March 23, 2026). Later "$250M valuation" claims are unverified.
- **Caveat:** True Ventures says it was "first to believe in Ben," i.e., VC money arrived; still a one-person company at the $1M mark, hence included.
- **Lesson:** The 2026 wedge is not "AI writes your code" but "AI runs the company"; the human's job collapses to choosing what not to build.
- Sources: True Ventures https://trueventures.com/blog/polsia-one-person-company-no-longer-a-metaphor ; Latent Space episode summary https://finance.biggo.com/podcast/289233539989e87d ; founder interview https://www.youtube.com/watch?v=6bfulpU6-Qc

**C3. Lumoo — Henrik Skagerlind Fasth & Peter Thörngren (2)** — Grade P (Lovable case study; €700k ARR, sub-$1M)
- Fashion-content platform (product imagery, virtual models, lookbooks) built in Lovable by two fashion/retail veterans with ~25 years combined industry experience, launched Feb 2025; 15+ Nordic brands (Gant, Brothers); €700k ARR in nine months (Lovable Series B post says $800k); raised SEK 6M (~€550k) from Lovable's CEO and angels. Included as the best-evidenced "domain expert + vibe coding → near-$1M in a year" case.
- Sources: Lovable one-year post https://lovable.dev/blog/one-year-of-lovable ; Lovable Series B https://lovable.dev/blog/series-b ; The Hub https://thehub.io/startups/lumoo-studio

**C4. Plinq — Sabrine Matos (solo)** — Grade P (Lovable-reported; $456k ARR, sub-$1M)
- Women's-safety background-check app (Brazil), built in Lovable by a growth marketer with no coding background after a Feb 2025 femicide case; MVP in 45 days; ~R$2.2M (~$456k) ARR three months after launch, 10k+ users; raising a ~$500k pre-seed. Mission-driven consumer product in a market where the founder understood distribution.
- Source: https://www.aieatingtheworld.com/articles/non-technical-founder-lovable-app-builder-success-story

**C5. Creator Buddy — Alex Finn (solo)** — Grade S/P ($300k ARR; audience built 2021-24; sub-$1M)
- YouTube/X content-ideation tool vibe-coded with Cursor/Claude Code/Codex ("0 lines of code written"), launched Jan 24, 2025, "$100k in 15 minutes" and ~$300k ARR at 90% margins per his posts. Finn's audience (YouTube since ~2021 on crypto, then AI) is the distribution; he also sells a Claude Code course. Included as the most prominent example of a creator converting audience into a vibe-coded tool — and as a reminder that the loud cases often top out at $300k.
- Sources: his X post https://x.com/AlexFinn/status/2059685887018192904 ; essay https://www.alexfinn.ai/p/why-vibe-coding-is-the-most-important ; profile https://yespress.io/alex-finn

**C6. fly.pieter.com — Pieter Levels (solo)** — Grade S — *failed after early success*
- Browser flight sim built by asking Cursor, ~3 hours, Feb 2025; monetized with in-game ad slots, branded blimps and a $29.99 F-16; $67k MRR by day 13, $87k MRR ("$1M ARR") by day 17 with 320k players and 74M impressions. Levels wrote at the time: "Whether the MRR is truly sustainable for a year we can only guess." His mid-2026 X bio reportedly lists it at $0/month; one outlet claims $70-90k MRR a year on, unverified. The revenue was one-time ad buys from companies chasing the attention, not renewals.
- **Lesson:** Attention revenue is not recurring revenue; viral vibe-coded products convert to zero unless there is a subscription with a reason to renew.
- Sources: Levels on X https://x.com/levelsio/status/1899596115210891751 ; Promptway https://promptway.com/blog/pieter-levels-flight-sim-to-zero ; KODiQ (contrary claim) https://kodiq.ai/article/ai-news-2026-05-19-pieter-levels-flight-sim-1m-arr-17-days/

**C7. Enrichlead — Leo (Leonel) Acevedo (solo)** — Grade S/secondary — *failure, never reached $1M*
- Lead-enrichment SaaS, publicly "100% written by Cursor, zero hand-written code," launched March 2025. Within two days: API keys exposed in the frontend, no auth, open database, no rate limiting; attackers maxed his API keys, bypassed subscriptions, wrote junk to the DB; Cursor "kept breaking other parts" when asked to fix it; shut down within a week (one source adds an unverified $14k OpenAI bill).
- **Lesson:** Vibe coding moves the failure mode from "can't build" to "can't secure"; the first $10k of revenue attracts the first attacker.
- Sources: Vibe Graveyard https://vibegraveyard.ai/story/enrichlead-vibe-coded-saas-shutdown/ ; Snyk https://snyk.io/articles/the-highs-and-lows-of-vibe-coding/ ; Bill Hartzer https://www.billhartzer.com/ai/vibe-coding-got-his-site-hacked-and-the-attackers-spent-his-api-credits-overnight/

---

### Archetype D: AI-niche media and audience businesses

**D1. The Rundown AI — Rowan Cheung (solo for year one)** — Grade V (Forbes revenue figures) / S
- **What/pays for:** Free daily AI newsletter; sponsors (Google, Salesforce, Amazon) pay for placements; Rundown University at ~$1,000/yr.
- **Acquisition:** Started Jan 2023 with zero subscribers and ~1,000 Twitter followers; AI news threads with a subscribe CTA at the end ("the first 55,000 subscribers were all organic from Twitter"); 86k subs and 100k followers by ~April 2023; 150k subs / 235k followers by May 2023; a free tool directory (Supertools) as a capture page; later paid ads reinvesting all profit; 2M subscribers by 2025.
- **Capital:** None. University dropout, self-taught via YouTube.
- **Timeline:** Jan 2023 → $3M revenue 2024 → $7M projected 2025 (Forbes, bootstrapped) → outside investment from Electrify in 2025/26. Forbes 30 Under 30 (2026).
- **AI vs human:** The newsletter was famously *not* written by AI; AI was the subject. Human did ~2 hours of research every morning plus "full-time plus overtime" writing.
- **Lesson:** In an exploding category, the fastest-to-daily-cadence curator captures the sponsor budget; speed of consistency beat quality of analysis.
- Sources: Forbes profile https://www.forbes.com/profile/rowan-cheung/ ; Creator Spotlight interview https://www.creatorspotlight.com/p/the-rundown ; Dealroom (Electrify) https://app.dealroom.co/news/feed/electrify-invests-in-the-rundown-world-s-largest-ai-newsletter-with-2m-subscribers ; EO profile https://www.eomag.io/article/the-rundown-ai-rowan-cheung

**D2. The Neuron — Pete Huang & Noah Edelman (2)** — Grade V (acquisition) / P (beehiiv case study)
- Daily AI newsletter launched Jan 2023 (Huang's LinkedIn following seeded it; Edelman was a Northwestern student); 10k in weeks, 100k in ~6 months, 500k in ~24 months; sponsorship revenue reinvested into Meta ads and the purchase of ~4 smaller AI newsletters; "low 7 figures" revenue; acquired by TechnologyAdvice January 2025 (price undisclosed), now 700k+ readers plus podcast.
- **Lesson:** Newsletters are buyable assets if the list is clean and the sponsor book is proven; they bought lists to grow, then were bought.
- Sources: beehiiv case study https://www.beehiiv.com/case-studies/the-neuron ; They Got Acquired https://theygotacquired.com/content/the-neuron-acquired-by-technologyadvice/ ; Northwestern https://www.thegarage.northwestern.edu/news/how-a-northwestern-student-built-and-sold-one-of-ais-fastest-growing-media-companies

**D3. There's An AI For That (TAAFT) — Andrei Nedelcu (solo at start; ~10 staff by 2024)** — Grade S (revenue undisclosed)
- AI-tool directory launched Dec 2022 from Bucharest after cataloguing Stable Diffusion tools; 3-4M visits/month, newsletter 1-1.7M subscribers; revenue = ~$300 listing fees, on-site ads, newsletter sponsorships at $6-8k per placement (a seven-figure run-rate is implied, not published). Nedelcu owned ~1,000 domains before — a domainer's instinct for the query.
- **Lesson:** Directories monetize the *supply side* (founders paying to be listed) — the only business model in this set where customers are other founders in the same gold rush.
- Sources: TAAFT story page https://theresanaiforthat.com/story/ ; beehiiv case study https://www.beehiiv.com/case-studies/theres-an-ai-for-that ; High Signal interview https://www.highsignal.io/how-andrei-built-theres-an-ai-for-that/

**D4. Superhuman AI — Zain & Awais Kahn (2 → 8)** — Grade S/P
- Launched early 2023; 135k subscribers in three months; 800k+ in 2024, 1.5-2M claimed 2026; ad inventory sells out; "six-figure monthly revenue" reported; Zain built a LinkedIn/X audience from near zero in 2022 by posting about ChatGPT prompts. No audited numbers.
- Sources: beehiiv spotlight https://www.beehiiv.com/blog/creator-spotlight-superhuman-by-zain-kahn ; The Tilt https://www.thetilt.com/content-entrepreneur/superhuman-ai-content-business

**D5. "Boring History" network — Adavia Davis (+ partner Eddie Eizner)** — Grade V (Fortune reviewed AdSense payouts and analytics)
- Five faceless YouTube channels (flagship: six-hour AI-narrated "fall asleep to" history documentaries); scripts and visuals via Claude, voice via ElevenLabs, orchestrated by their own TubeGen software; ~$60 and ≤6 hours per video; ~2M views/day; $40-60k/month (~$700k/yr) at 85-89% margins; ~2 hours/day of his time. He dropped out of Mississippi State in 2020. Davis himself says individual creators have until ~2027 before the window closes; YouTube began demonetizing "mass-produced" AI content in July 2025.
- **Lesson:** AI media works when the format has a reason to be long and repetitive (sleep content), where "slop" is a feature; the risk is entirely platform policy.
- Sources: Fortune (Dec 30, 2025) via Unilad https://www.uniladtech.com/social-media/youtube/youtuber-makes-700000-working-two-hours-daily-ai-303849-20260109 ; Kidelight https://www.kidelight.com/2026/10/faceless-youtube-channels-are-making.html

**D6. Aitana López — The Clueless (Rubén Cruz)** — Grade S (agency-reported) — *ceiling case, far below $1M*
- Spain's AI influencer (2023): ~€1,000 per sponsored post, ~€3,000/month average, €10k in a strong month; 300-400k followers. Shows that AI-persona influencer income is a side business, not a $1M path, despite the press.
- Sources: Entrepreneur https://www.entrepreneur.com/business-news/this-ai-fitness-model-makes-11000-a-month/465975 ; Wikipedia https://en.wikipedia.org/wiki/Aitana_L%C3%B3pez

---

### Archetype E: Build-in-public maker portfolio (products + boilerplates + courses)

**E1. Marc Lou — ShipFast, CodeFast, DataFast, TrustMRR (solo)** — Grade V (Stripe-linked TrustMRR, which he owns) / S
- **Audience origin:** Started posting Nov 2021; 8 months to 1,000 followers; ~35-40k by ShipFast launch (Aug/Sept 2023); 200k by 2025; 323k by 2026. Documented, so included.
- **What/pays for:** ShipFast ($1.27M lifetime, Stripe-verified) is a Next.js boilerplate for shipping AI SaaS fast; CodeFast a course; DataFast analytics ($15.8k MRR); TrustMRR a verified-revenue directory ($25k MRR days after launch) now with an acquisition marketplace.
- **Timeline:** ShipFast $528k in 4 months → ~$141k MRR peak April 2024 → ~$1.29M total income 2024 → $1,032,000 in 2025 (-20%), ShipFast now ~$2-3.5k/month; two 2025 launches (BioAge, ClipMarc) failed; 9 of 10 TrustMRR verticals failed.
- **AI vs human:** AI is the customer's reason to ship fast; Lou's own leverage is daily public shipping and 15 income streams. He states plainly: "An audience doesn't guarantee a successful startup."
- **Lesson:** Picks-and-shovels for the AI gold rush decays as fast as the gold rush tooling changes (Lovable/Cursor made boilerplates less necessary); diversify before the peak.
- Sources: 2025 recap https://newsletter.marclou.com/p/i-made-1-032-000-in-2025 ; TrustMRR ShipFast https://trustmrr.com/startup/shipfast ; audience origin post https://x.com/marclou/status/1958127275146399774 ; Streakr analysis https://streakr.co/playbook/marc-lou

---

### Archetype F: AI-services agency + education flywheel

**F1. Liam Ottley — Morningside AI / AAA Accelerator (solo → 65 staff)** — Grade S/P
- Taught himself Python/ML in 2022, launched YouTube Jan 3, 2023 (500k views in two months), coined the "AI Automation Agency" model, sells a Skool community; claims $7M (2024) → "$18M+" (2026) across businesses with 65+ staff; unverified. Included only as the archetype's upper bound — it stops being 1-3 people fast.
- Sources: channel https://www.youtube.com/@LiamOttley/about ; review noting unverified claims https://ippei.com/aaa-accelerator/

**F2. Nick Saraev — LeftClick / Maker School (solo-ish)** — Grade S
- Prior agency 1SecondCopy to ~$1M ARR; LeftClick (2022) is an AI-automation consultancy; YouTube to 400k+ by titling videos "Make.com"; Maker School community claims $250-330k/month on his own sites. All self-published.
- Sources: https://nicksaraev.com/biography/ ; https://leftclick.ai/faq.html

**F3. Nate Herk — TrueHorizon AI / AI Automation Society (co-founder)** — Grade S
- Left corporate Nov 2024; YouTube on n8n to ~1M subscribers; co-founded TrueHorizon AI Jan 2025 and says it passed $100k/month within a year; paid Skool at $129/mo; won Skool Games four times in 2025.
- Sources: https://www.nateherk.com/about ; review https://aifunnelinsider.com/ai-automation-society-plus-skool-review/

---

## 2. Scientific read of the set

### 2.1 Archetypes, counts, speed, the human's irreplaceable job, failure mode

| Archetype | Cases (n) | Median time to $10k/mo | What the human did that AI could not | Typical failure mode |
|---|---|---|---|---|
| **A. Self-serve vertical AI SaaS** | 12 (Chatbase, Formula Bot, HeadshotPro, TypingMind, Submagic, Castmagic, VSAI, Undetectable, StealthGPT, Photo AI, Blotato, EasyGen) | ~6-8 weeks (Chatbase ~6 wks; HeadshotPro 2 wks; TypingMind 1 wk; Submagic ~1 mo; Castmagic ~1 mo via AppSumo; Formula Bot ~2-3 mo; EasyGen ~2 mo) | Picked a narrow job with a verifiable output; wrote the one demo/post that went viral; answered support personally; priced from day one; built the affiliate/SEO engine | Feature absorbed by the model vendor or platform (ChatGPT, Apple); churn 15%/mo for prosumer tools; plateau at $5M (Submagic) or <$1M (EasyGen) when the audience-sourced channel exhausts |
| **B. Consumer mobile app + paid creator seeding** | 4 (Cal AI, RizzGPT/Umax, Wave, Talknotes) | ~2-3 months (RizzGPT weeks; Cal AI ~2 mo; Wave months; Talknotes never) | Ran creator seeding or paid ads as a daily operations job; chose a category with existing habit and 10x'd the input; paywall testing | Hit decay (Umax -50% from peak), paid channel saturation (Wave's Meta ads died), founder burnout and sale at first dip (Talknotes), platform copying |
| **C. Vibe-coded platform / agent product** | 7 (Base44, Polsia, Lumoo, Plinq, Creator Buddy, Fly Pieter, Enrichlead) | ~1 month among survivors (Base44 <3 wks; Polsia <2 wks; Plinq ~2 mo; Lumoo ~3-4 mo), but with heavy survivorship bias | Architecture and problem selection (Shlomo), domain knowledge (Lumoo, Plinq), deciding what not to build (Broca), cost management of model calls | Security collapse (Enrichlead), attention revenue not renewing (Fly Pieter), spaghetti-code rebuilds (Blotato), bigger platform absorbs the category |
| **D. AI-niche media / audience** | 6 (Rundown, Neuron, TAAFT, Superhuman, Boring History, Aitana) | ~4-6 months to first meaningful sponsor revenue (Rundown ~Q2 2023; Neuron ~6 mo; TAAFT a few months; Boring History ~years as a hobby) | Daily cadence under deadline, editorial taste, sponsor sales (warm, inbound), list buying, format invention (6-hour sleep docs) | Category saturation (dozens of AI newsletters by 2024), platform demonetization (YouTube July 2025), sponsor budgets moving to the two biggest lists, persona-influencer ceiling (~€3k/mo) |
| **E. Build-in-public maker portfolio** | 1 core (Marc Lou) + overlaps (Levels, Finn, Dinh) | ~18-24 months (Lou: Nov 2021 first tweet → Aug 2023 ShipFast) | Years of daily public shipping; packaging know-how as boilerplate/course; portfolio diversification | Product-tool decay as the underlying stack changes (ShipFast $141k → $3k MRR); failed launches (BioAge, ClipMarc); audience ≠ demand |
| **F. AI-services agency + education** | 3 (Ottley, Saraev, Herk) | ~3-6 months after the YouTube channel starts | Selling and delivering custom automation; teaching; community management | Becomes a real company with headcount (65 staff) or stays a personal-brand business with unverifiable numbers; dependency on platform (Make/n8n) keyword waves |

### 2.2 Which archetypes need the least cold selling, least capital, and produce a sellable asset?

**Least cold selling:** A (self-serve + affiliates + SEO; Chatbase did no outbound until ~$7M ARR; Submagic has no sales team at $8M), D (sponsors come inbound once you have 50k+ engaged readers; Rowan sold via a Calendly/Stripe self-serve page), and C in its platform form (Base44, Polsia grew on building-in-public posts). B replaces cold selling with *paid* selling (creator seeding, ASA/Meta ads). F is cold selling by definition, hidden behind YouTube.

**Least capital:** A and C — Formula Bot started on ~$35/month; Chatbase, TypingMind, HeadshotPro, Base44 ($10-20k) all began on personal savings plus API bills; the one recurring surprise is the API bill after a viral spike (Formula Bot $4-5k, Base44 model calls 89% of spend). D is nearly free (beehiiv + time) but needs 6+ months of unpaid daily output. B needs working capital: $500-$2k to test creator seeding, and five to six figures a month of ad spend to scale (Wave). E needs time capital (two years of audience building).

**Sellable asset:** Strongest in A (VSAI → Zillow; Chatbase turned down $1M at month three; Talknotes sold at $7.5k MRR for $200k ≈ 27x MRR), C (Base44 $80-92M; Polsia already VC-backed), D (The Neuron → TechnologyAdvice; Rundown took investment), and B at scale (Cal AI → MyFitnessPal). E and F are personal-brand businesses and are the least sellable; Marc Lou's TrustMRR marketplace shows small AI SaaS now changes hands at low multiples, while pre-revenue vibe-coded apps sell "as an asset" for hundreds to low thousands of dollars.

### 2.3 Common starting conditions

- **Skills:** 18 of 30 could code before starting (Yasser, Shlomo, Dinh, Levels, Postma, Zitoun's co-founder, Tormey, Bonacina/Andreev, Gherman, Perry, Jeannen after a 2022 bootcamp, Lou, Nedelcu, Broca, Huang's co-founder, Ramonov). The non-coders who reached seven figures (Bressler, Anderson, Mohrer, Yadegari's co-founder Langmack side, Matos, Fasth, Davis, Cheung, Edelman) all had one of: distribution skill (media buying, creator ops, LinkedIn), operating experience (Uber GM), or a domain where they were the customer (analytics, fashion, podcasting).
- **Industry knowledge:** The acquired or most durable cases were built by the customer: VSAI (real estate workflow), Lumoo (fashion), Castmagic (podcasters), Submagic (video editor since age 12), Formula Bot (analytics director), Plinq (Brazilian women's safety).
- **Hours:** Nearly all describe full-time-plus intensity in year one (Rowan "full-time plus overtime", Jeannen "15h per day", Cheung two hours of research before writing). Exceptions are post-success: Dinh 4 h/day, Davis 2 h/day, Levels' Photo AI on autopilot.
- **Location:** Irrelevant to outcome. Egypt/Canada (Elsaid), Israel (Shlomo), Vietnam (Dinh), France (Zitoun, Lou, Jeannen), Netherlands (Postma, Levels), Romania (Nedelcu), Brazil (Matos), Sweden (Lumoo), Canada (Cheung), Mississippi (Davis), US (Yadegari, Anderson, Mohrer, Bressler). US location mattered only for App Store monetization (iOS users pay far more; Android "pays far less") and sponsor pricing.
- **Capital at start:** Median ≈ $0-500; maximum ≈ $20k (Base44). The two exceptions with prior wealth (Ramonov from a $10M+ exit; Shlomo from Explorium) did not spend it.
- **Open to someone with no special background:** D (media) — Cheung and Edelman had neither code nor capital nor audience; B — Anderson had no code and started with $50 creator posts; C with 2026 tooling — Matos and Fasth built production apps in Lovable with no engineering. A still rewards builders, but Formula Bot shows the no-code path when the pain is narrow enough.

### 2.4 What changed between 2024 and late 2026

**Easier:**
1. *Code is no longer the constraint.* Lovable went from launch to $100M ARR in 8 months (July 2025) and ~$500M by June 2026; Base44 was built by one person in Cursor + Claude; Wave's founder now runs "almost exclusively" on Claude Code; Davis runs five channels on Claude + ElevenLabs. The marginal cost of a production-grade MVP dropped from a month of a developer's time to a weekend and ~$100 of tokens. (Sources: Tech.eu https://tech.eu/2025/07/23/lovable-becomes-fastest-software-company-ever-to-reach-100m-arr/ ; Mixergy; Promptway.)
2. *Agents can now run functions, not just write code.* Polsia's CEO agent on Opus 4.6 does marketing, outreach, ads and support for 3,000 businesses; Jeannen's AdKit runs ad campaigns with human approval. The solo founder's span of control went from "I can build it" to "I can operate it."
3. *Verified-revenue infrastructure exists.* TrustMRR-style Stripe-linked dashboards and Acquire.com make small AI businesses legible and tradable, so the exit path for a $5-20k MRR product is real (Talknotes, dozens of TrustMRR deals in Dec 2025).

**Saturated or closing:**
1. *Thin consumer wrappers.* Sensor Tower: ChatGPT took 63% of all in-app purchase revenue across generative-AI apps by mid-2026 and out-earned the next nine apps combined by 5x in Q1 2026; OpenAI's Sept 29, 2026 DevDay turned ChatGPT into the place apps are discovered and run. PDF-chat, chat-UI, detector and avatar categories each had one winner and a long tail at <$500k (ChatPDF ~$440k ARR, EasyGen $540k). (Sources: BigGo/Sensor Tower https://finance.biggo.com/news/38262a84-7d68-49e3-99a4-d914598fb065 ; TechCrunch https://techcrunch.com/2026/09/29/openais-latest-features-take-direct-aim-at-the-app-store-model/ )
2. *AI newsletters.* The Rundown, Superhuman, TAAFT, The Neuron each have 0.7-2M subscribers; the sponsor book consolidated around them in 2024-25, and new general-AI newsletters launched after mid-2024 have no documented path to seven figures.
3. *Creator-seeded App Store apps.* The $50-per-post TikTok arbitrage that built RizzGPT/Umax/Cal AI in 2023-24 is now a known playbook with rising creator prices and Apple featuring as the real variable; Umax fell by half, Wave's Meta ads stopped working for a year.
4. *Mass AI content.* YouTube began demonetizing mass-produced AI channels in July 2025 (Davis expects the window to shut by ~2027); Google's scaled-content enforcement removes thin AI sites, and there is no verified $1M AI-content-site case in the whole 2024-26 period. (Sources: Search Engine Land https://searchengineland.com/google-spam-update-ai-affiliate-sites-seo-experiment-470168 ; Fortune via Unilad.)
5. *Boilerplates and "ship fast" picks-and-shovels.* ShipFast's decay from $141k to ~$3k MRR tracks the arrival of Lovable/Cursor; a boilerplate is worth less when an agent writes the boilerplate.

**Opening:**
1. *Vertical agents in "boring" workflows with an existing price list* (virtual staging at $25-100/photo; fashion lookbooks; women's-safety checks). These are where exits happened (VSAI, Base44) and where incumbents buy rather than build.
2. *B2B team plans on prosumer tools.* TypingMind's B2B share passed 50% in 2025; Chatbase's enterprise closes in year three exceeded the first two years combined; Submagic's agency add-on. Upmarket is where the 2023 cohort survived 2026.
3. *Agent-run businesses and tooling for agents* (Polsia; Neon's agent-friendly database pricing; Blotato's automation). The customer is increasingly an agent or an agent-operator.
4. *Long-form, repetitive, utility media* where AI production is a feature (sleep documentaries), as opposed to AI news where it is a liability.
5. *Services delivered by one human plus agents* (AdKit, TrueHorizon's $100k/month) — a true "agency of one" with inbound from content, but still gated by selling.

### 2.5 Ranked top 5 archetypes for a US individual with $0-10k, no audience, little appetite for cold calling, and a strong AI agent team

Probabilities are my judgment of reaching $1M cumulative revenue, run-rate, or exit value within 7 years, conditional on a serious, full-time-equivalent attempt with at least three product iterations. Base rates: secondary estimates put solo SaaS founders reaching $1M ARR at roughly 2-3%; the cases above are the survivors of thousands of attempts, so I anchor low and adjust for the agent-team advantage and the 7-year horizon (which allows 3-4 sequential bets).

| Rank | Archetype | P($1M in 7 yrs) | Why this rank |
|---|---|---|---|
| 1 | **A. Vertical self-serve AI SaaS in a "boring" niche with an existing price list; SEO + directories + affiliates as distribution** | **12-18%** | Least capital, least cold selling, most sellable; 7 of the 12 cases crossed $1M ARR inside 12 months; the agent team removes the build bottleneck that previously gated non-coders. Fails when the niche is a model-vendor feature. |
| 2 | **B. Consumer mobile app with creator seeding** | **8-12%** | Fastest to cash when it hits (Cal AI $1M MRR in months) and acquirers exist; but hit-driven, needs $500-2k per test and five figures/month to scale, and the 2023-24 creator arbitrage is now priced. Multiple shots in 7 years raise the cumulative odds. |
| 3 | **D. AI-native media in a non-AI niche (not AI news)** | **6-10%** | Zero capital, inbound sponsors, sellable lists (Neuron); but requires daily output for 6-12 months before revenue, and both the AI-news and the faceless-YouTube windows are visibly closing. Best odds in a vertical where you have taste (sleep, history, a trade). |
| 4 | **C. Vibe-coded agent platform / app-builder adjacent product** | **5-8%** | Highest ceiling (Base44 $92M, Polsia $3M ARR in 60 days) but survivorship is brutal (Enrichlead, Fly Pieter), the category attracts the best-funded incumbents, and the two wins came from experienced operators. Worth one shot, not the main plan. |
| 5 | **E. Build-in-public maker portfolio** | **4-7%** | Slow (18-24 months to first hit), audience-dependent, decays with the tool stack, least sellable; but it compounds optionality and is how most of the Archetype A founders got their first 1,000 users. Run it as the *substrate* under #1, not as the business. |

Excluded from the ranking: **F (agency)** because it requires selling and converts into headcount; **AI persona influencers** (ceiling ~€3-10k/month); **AI content sites** (no verified case, active platform enforcement).

#### First 90 days — Archetype A (vertical self-serve SaaS)

*Day 1-14: pick the job, not the model.* Use the agent team to mine 20 niche communities (subreddits, trade Facebook groups, Discords, G2 reviews) for repeated, verifiable, paid-today tasks with an existing per-unit price (what VSAI found: $25-100 per staged photo; what Formula Bot found: "how do I write this formula" on r/excel daily). Shortlist five where (a) output correctness is checkable by the buyer in under a minute, (b) the buyer already pays a human or a tool, (c) ChatGPT's generic answer is clearly worse than a tuned workflow. Reject anything a model vendor would ship as a feature within a year (PDF chat, generic summarization, detectors).

*Day 15-30: ship a paid v1.* Agents build the app (Next.js/Supabase or Lovable + custom backend), Stripe from day one (every A case charged on day one), usage caps to bound API cost (Castmagic), rate limits and server-side auth from day one (Enrichlead). You write the pricing page, the 60-second demo video, and the one community post. Target: first paying stranger by day 30; Chatbase's bar was 30 minutes, Jeannen's floor was $700 in 10 days.

*Day 31-60: distribution you don't have to call anyone for.* Submit to 30+ AI directories and TAAFT ($300), launch on Product Hunt once (Submagic's pivot moment), publish 50-200 programmatic SEO pages for the niche's long-tail queries (HeadshotPro's city pages) generated and QA'd by agents, and open an affiliate program at 30% lifetime commission on FirstPromoter/Rewardful (Submagic's substitute for a sales team). Post weekly revenue screenshots on X and the niche community — the one E-archetype habit worth adopting from day one.

*Day 61-90: decide with data.* If ≥$3k MRR and <10% monthly churn: double down — add a Team plan (TypingMind's B2B inflection), hire a part-time support contractor, and start a $600-1,000 Google Ads test on the exact query. If <$1k MRR after honest distribution: kill it, keep the codebase and the SEO pages as assets, and run the next of the five shortlisted jobs. Budget for the 90 days: ~$1,500-3,000 (tokens, directory fees, domain, PH assets, ad test). Metric that predicts $1M: time from signup to first paid output under 10 minutes, and ≥50% of revenue from the top tier within six months (Chatbase, Photo AI pattern).

#### First 90 days — Archetype B (consumer mobile app with creator seeding)

*Day 1-14: category with an existing habit, input made 10x easier.* Agents scan the top-200 grossing Health & Fitness, Lifestyle, Education and Productivity apps for categories where the incumbent's input is manual and a vision/audio model collapses it (Cal AI: photo instead of search; Wave: voice instead of typing). Validate demand with three faceless TikTok/Reels accounts posting 15 clips of the concept — ~$0 beyond your time — and measure saves/comments, not views. Pick the concept with the best save rate.

*Day 15-35: ship to TestFlight with a weekly-plan paywall.* Agents build in Expo/React Native with Adapty or RevenueCat for paywalls (Wave's single biggest lever was constant paywall A/B tests); three-day trial → weekly, monthly, annual; onboarding quiz for personalization. Enroll in Apple's Small Business Program (15% instead of 30%). Submit for review by day 30; iOS first (Android users "pay far less").

*Day 36-70: creator seeding as a daily job.* Set aside $1,500-3,000. DM 100 micro-creators per day in the niche (agents draft and track; you approve); expect ~10 replies and ~3 posts at $50-150 each. Rule from Cal AI: reinvest every dollar where 1,000 views cost less than the trial-to-paid revenue they generate; stop any creator cohort that does not pay back in 14 days. Apply for Apple featuring the day you have a 4.8+ rating (Umax got half its downloads from featuring).

*Day 71-90: scale or next app.* Signal to scale: ≥$5k MRR, trial→paid ≥8%, payback <30 days. Then add Apple Search Ads on your category keywords (Wave's durable channel) and keep the creator desk running. Signal to move on: CPI payback >60 days after 30 posts — ship the next concept on the same codebase and paywall stack; Anderson's three apps in a year were the same team, same playbook. Plan for decay: every B case in this set fell 30-60% from peak within 12-18 months; the plan has to include the second app before the first peaks.

---

## 3. The five most instructive cases, in one line each

1. **Chatbase** — the template for a solo wrapper that became a $10M company: narrow job, 60-second demo, charge on day one, support it yourself, go upmarket before the vendor eats you.
2. **Base44** — vibe coding's ceiling: $0 → $92M of consideration in six months by one experienced builder who managed model costs like a CFO and built in public on LinkedIn.
3. **Cal AI** — the app was trivial; the business was a $50-per-post creator desk run daily by teenagers, which is why MyFitnessPal bought it.
4. **fly.pieter.com** — the best-known vibe-coded viral hit went from $87k MRR to (reportedly) $0 because attention revenue does not renew; its boring sibling Photo AI still prints $100k/month.
5. **Nico Jeannen / Talknotes** — paid-ads skill got a non-coder to $7.5k MRR and a $200k exit in 11 months; one bad release and burnout ended it, and the year after was empty — the human nervous system is the real capacity constraint on a one-person company.

---

## 4. Source index (primary and strongest-secondary, by case)

- Chatbase: https://www.starterstory.com/stories/chatbase-breakdown ; https://supabase.com/customers/chatbase ; https://www.eomag.io/article/chatbase-yasser-elsaid ; https://x.com/yasser_elsaid_/status/1894801760587522417 ; https://clerkchat.co/blog/how-chatbase-hit-20m-revenue-with-zero-vc
- Base44: https://www.wix.com/press-room/home/post/wix-further-expands-into-vibe-coding-with-acquisition-of-base44-a-hyper-growth-startup-that-simplif ; https://www.sec.gov/Archives/edgar/data/1576789/000162828026015222/wix-20251231.htm ; https://www.calcalistech.com/ctechnews/article/rkogikc9le ; https://promptway.com/blog/maor-shlomo-base44-wix-exit
- Cal AI: https://techcrunch.com/?p=3098039 ; https://www.cnbc.com/make-it/2025/09/06/cal-ai-how-a-teenage-ceo-built-a-fast-growing-calorie-tracking-app.html ; https://www.cbsnews.com/newyork/news/zach-yadegari-cal-ai-founder-long-island/
- Blake Anderson: https://scalenuggets.beehiiv.com/p/23yearold-whos-making-11myear-ai-apps ; https://x.com/tzhongg/status/2028931446317232397 ; https://income-reality-check.pages.dev/a/he-made-rizzgpt-which-makes-him-1-million-a-month/
- Wave AI: https://mixergy.com/interviews/the-7-million-vibe-coded-app/ ; https://adapty.io/case-studies/wave/
- Polsia: https://trueventures.com/blog/polsia-one-person-company-no-longer-a-metaphor ; https://finance.biggo.com/podcast/289233539989e87d
- Submagic: https://superframeworks.com/case-study/submagic ; https://baremetrics.com/founder-chats/david-zitoun
- Castmagic: https://www.indiehackers.com/post/boostrapping-ai-startup-castmagic-to-1m-in-under-9-months-27bf7c9402 ; https://refreshmiami.com/news/its-not-just-magic-its-ai-meet-the-miami-startup-turning-conversations-into-content/ ; https://www.starterstory.com/castmagic-breakdown
- Virtual Staging AI: https://www.geekwire.com/2024/zillow-group-acquires-vsai-a-virtual-staging-tool-that-adds-furniture-to-real-estate-listings/ ; https://www.crunchbase.com/organization/virtualstagingai
- Formula Bot: https://www.nocode.mba/articles/nocode-case-study-formulabot ; https://bubble.io/showcase/formula-bot ; https://n8n.io/case-studies/formula-bot/ ; https://www.indiehackers.com/post/tech/getting-serious-about-marketing-after-hitting-500k-arr-8XGnzrxG1neA3jy37x2D
- HeadshotPro: https://www.starterstory.com/stories/headshotpro-breakdown
- TypingMind: https://news.tonydinh.com/p/oct-2025-updates-code-money-and-travel ; https://www.starterstory.com/typingmind-breakdown
- Marc Lou: https://newsletter.marclou.com/p/i-made-1-032-000-in-2025 ; https://trustmrr.com/startup/shipfast ; https://x.com/marclou/status/1958127275146399774
- Pieter Levels: https://aituts.com/case-study/photo-ai-pieter-levels/ ; https://x.com/levelsio/status/1899596115210891751 ; https://promptway.com/blog/pieter-levels-flight-sim-to-zero
- The Rundown: https://www.forbes.com/profile/rowan-cheung/ ; https://www.creatorspotlight.com/p/the-rundown
- The Neuron: https://www.beehiiv.com/case-studies/the-neuron ; https://theygotacquired.com/content/the-neuron-acquired-by-technologyadvice/
- TAAFT: https://theresanaiforthat.com/story/ ; https://www.beehiiv.com/case-studies/theres-an-ai-for-that ; https://www.highsignal.io/how-andrei-built-theres-an-ai-for-that/
- Superhuman: https://www.beehiiv.com/blog/creator-spotlight-superhuman-by-zain-kahn ; https://www.thetilt.com/content-entrepreneur/superhuman-ai-content-business
- Boring History: https://www.uniladtech.com/social-media/youtube/youtuber-makes-700000-working-two-hours-daily-ai-303849-20260109 ; https://www.kidelight.com/2026/10/faceless-youtube-channels-are-making.html
- Undetectable AI: https://www.prnewswire.com/news-releases/undetectable-ai-reaches-11-million-users-in-18-months-since-launch-302303963.html ; https://www.sramanamitra.com/2025/10/01/best-of-bootstrapping-bootstrapped-an-ai-startup-to-10m/
- StealthGPT: https://www.indiehackers.com/product/stealthgpt ; https://www.starterstory.com/stories/stealthgpt-breakdown
- Nico Jeannen: https://x.com/nico_jeannen/status/1808130671493406761 ; https://nocodeexits.substack.com/p/three-exits-for-290000-then-a-year
- Blotato: https://www.sabrina.dev/p/how-i-built-a-1m-solo-ai-business
- EasyGen: https://www.starterstory.com/easy-gen-breakdown ; https://getlatka.com/companies/easygen.io
- Creator Buddy: https://x.com/AlexFinn/status/2059685887018192904 ; https://yespress.io/alex-finn
- Lumoo: https://lovable.dev/blog/one-year-of-lovable ; https://lovable.dev/blog/series-b
- Plinq: https://www.aieatingtheworld.com/articles/non-technical-founder-lovable-app-builder-success-story
- Enrichlead: https://vibegraveyard.ai/story/enrichlead-vibe-coded-saas-shutdown/ ; https://snyk.io/articles/the-highs-and-lows-of-vibe-coding/
- Aitana López: https://www.entrepreneur.com/business-news/this-ai-fitness-model-makes-11000-a-month/465975
- Ottley / Saraev / Herk: https://www.youtube.com/@LiamOttley/about ; https://nicksaraev.com/biography/ ; https://www.nateherk.com/about
- Market shifts: https://finance.biggo.com/news/38262a84-7d68-49e3-99a4-d914598fb065 (Sensor Tower) ; https://techcrunch.com/2026/09/29/openais-latest-features-take-direct-aim-at-the-app-store-model/ ; https://tech.eu/2025/07/23/lovable-becomes-fastest-software-company-ever-to-reach-100m-arr/ ; https://searchengineland.com/google-spam-update-ai-affiliate-sites-seo-experiment-470168 ; https://www.lonelinesseconomy.com/ai-girlfriend-market-2026 (Appfigures companion-app concentration)
