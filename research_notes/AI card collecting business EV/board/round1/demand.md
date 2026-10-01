# Demand Finder: Round 1 Proposals

**Lens:** Who is already paying for this, even badly? Follow the money, find the bad version, and sell before you build.

**Date:** 2026-10-01. Working assumptions from MISSION: $5k–25k of risk capital, 15–25 hrs/week, US-based, able to attend local shows.

---

## The demand scorecard (what I hunted, what I found)

| Demand pool | Proof of payment | Price | Volume signal | Trend | Top complaint (= the spec) |
|---|---|---|---|---|---|
| **Gift buyers who can't find Pokémon** (parents, grandparents) | One Amazon bundle listing has **30K+ bought in the past month**; another has 10K+; a 100-card lot shows 200+/week. One eBay 100-card bundle has **7,765 sold**. | $11–28 | Very high, peaks Nov–Dec | Up: retail shortage is at max print capacity, Walmart has moved to lotteries, and a new factory isn't expected until about 2028 | Duplicates, filler energy cards, "is it real?", not gift-ready |
| **Non-hobbyists holding a "shoebox" collection** (inherited or downsizing) | Dealers buy at **30–70% of value**. Just Collect, Throwback and others run "free appraisal, we travel to you" funnels. Invest in Baseball pays a **10% finder's fee** on six-figure collections. | 30–70% of market | Steady, and driven by demographics (Boomers downsizing) | Flat to rising | "Don't take the first offer", fear of being lowballed, no idea what they have |
| **Estates, executors and insurers needing a value** | Appraisers charge **$150–350/hr**. PSA paid appraisals start at $200. | $150–500 per job | Steady | Flat | Slow, expensive, and most generalists don't know cards |
| **Card sellers paying for listing labor** | Fiverr Whatnot VA gigs, remote "eBay + Whatnot listing VA" job posts, COMC intake at $0.65–2/card | $0.40–2/card | Medium | Up | Variant errors, slow turnaround. *Not chosen: offshore VAs and SaaS tools compete on price.* |
| **Restock alerts** | Paid Discords at $5.99–8.99/mo | | High | | **Killed:** free alternatives everywhere, plus a scalping-adjacent reputation |
| **Breaks, sealed spec, grading flips** | Yes, but… | | | | **Killed:** about 14% flip margin (about $7/hr), PSA Value tiers paused, live gambling lawsuits, modern sealed down 20–50% |

**The pattern:** the money a newcomer can actually capture is not in the hobby. It is at the hobby's two edges:

1. **The supply edge.** People who don't know what they have sell to whoever makes it easy.
2. **The gift edge.** People who don't care about rarity buy whatever is in stock, genuine and wrapped.

Hobbyists fight over the middle (singles, sealed, grading). Those three moves are the ones I chose.

---

## demand-1: Shoebox Desk, an AI photo-appraisal funnel that buys local collections

**One-liner:** Run a local "we'll tell you what your old cards are worth, free, in 24 hours" funnel. Buy the good collections at 40–50% of market, and liquidate through the cheapest channels.

**The hack (the unfair insight):**
- Every flipping study in our research ends with the same line: *"buying cheaper matters much more than which channel you sell on."*
- The only place to buy at 40–50% of market without being a hobby insider is from non-hobbyists. Today they are served by:
  - (a) local shops that lowball them, or
  - (b) vintage dealers who only want pre-1980 cards.
- AI lets a newcomer do what used to take 20 years of expertise: triage 500 photos of a shoebox in minutes, flag the 12 cards that matter, and pull comps.
- Trust is the second hack. Show the seller the comp sheet and give three options:
  - cash now at 40–50%,
  - consign at an 80/20 split,
  - or a free do-it-yourself guide.
- In a market full of scams and lowballers, being the transparent buyer *is* the moat.

**Why now:**
- Boomers own a reported 42% of homes sold in 2025 and are downsizing collections.
- Vintage and blue-chip cards are at records ($16.49M Pikachu). Modern prices are falling, so sellers who sell now and buyers who resell quickly both win.
- Record platform volume (eBay, Whatnot, Fanatics Collect) means liquidity is the best it has ever been.
- PSA opened a $59.99 "Standard" tier on 2026-09-14, so the best 1–2 cards from a collection can be graded again economically.

**How Claude runs it (about 70% of the work):**
- Builds the landing page and photo-upload intake (Artifact with a shared DB), plus the "what is it worth" triage pipeline: photo → card ID → era sort → comps from non-restricted sources → value range → offer sheet.
- Writes and launches Google Search and Meta ads within a 60-mile radius through AdWhispr, then optimizes them weekly.
- Runs a daily Routine that scans public estate-sale listings (estatesales.net, estatesales.org, Craigslist) for "baseball cards / Pokémon / collection" mentions. It drafts outreach; the user sends it.
- Writes the seller follow-up emails (Gmail drafts).
- Builds the liquidation plan per collection:
  - top cards → Fanatics Collect (6%) or eBay,
  - mid-tier → eBay or Whatnot lots,
  - junk-wax and bulk → demand-2 gift bundles.
- Writes every listing, and runs a P&L tracker per collection.

**User's tasks:**
- Take calls and meet sellers (usually at their home or a coffee shop).
- Pay, pick up, and sort physically.
- Photograph cards for listings.
- Pack and ship.
- Set up and own the accounts (ads, eBay, Fanatics Collect, Whatnot).
- Take a "We Buy Collections" table at 1–2 local shows a month.

**First 30 days:**
- **Days 1–3:** Claude ships the landing page and photo-intake tool. The user creates the ad accounts. This is a fake-door test with a $500 ad budget. **Metric:** cost per lead and the photo-submission rate.
- **Days 4–10:** The user posts in 5 local Facebook groups and Nextdoor ("Free card appraisals, no obligation"). The estate-sale scanner Routine goes live. The user calls 10 local estate-sale companies.
- **Days 11–30:** Make 2–4 buys at no more than 50% of Claude's conservative value, and liquidate the first one fully.
- **Kill or keep:**
  - Keep if cost per *qualified* lead (photos plus more than $750 of real value) is under $150 and the first collection returns at least 40% gross on cost.
  - Kill paid ads (keep the free channels) if cost per qualified lead is over $300.

**Path to the goal (real math; ad cost per lead is an assumption to test in week 1):**
- **Monthly funnel at maturity:**
  - $1,500 ads at an assumed $30 CPL gives 50 leads.
  - 50% send photos, giving 25.
  - About 30% have more than $750 of real value, giving 7–8.
  - 40% of those close, giving 3.
  - Free channels (estate sales, shows, referrals) add 1–2.
  - Total: **about 4.5 buys a month.**
- **Per buy (median):**
  - Realized liquidation value: $2,500.
  - Paid at 45%: $1,125.
  - Blended fees, shipping and supplies at 14%: $350.
  - **Gross profit about $1,025.**
- **Monthly:**
  - 4.5 × $1,025 = $4,600.
  - Less $1,500 ads and $200 tools and tables.
  - **About $2,900/month net, before tax.**
  - Labor is about 45–55 hrs/month, so **about $55–65/hr**.
- **Capital:** a $5–8k revolving float, turning in about 6 weeks.
- **Upside tail:** one $20k vintage shoebox, which appears every few months in any metro, is worth +$7–9k by itself.
- **Honest middle outcome at month 12:** $2.5–4k/month.
- **To reach $5–10k:** this needs 8–10 buys a month, which means a part-time sorter/shipper at $18/hr and a second metro, or the demand-3 partner network feeding leads.

**Evidence:**
- Dealers pay 30–70% of value: [thecardshopfinder FAQ](https://thecardshopfinder.com/faq/what-percentage-of-value-do-card-shops-pay/)
- Buyers running free-appraisal and travel funnels: [Just Collect free appraisal](https://blog.justcollect.com/just-collect-offers-free-appraisal-if-you-want-to-sell-your-sports-cards); [Throwback Sports Cards, Metro Detroit](https://www.throwbacksportscards.com/sports-card-buyer-near-me-in-metro-detroit)
- 10% finder's fee on six-figure collections: [Cardboard Connection / Invest in Baseball](https://www.cardboardconnection.com/invest-baseball-100k-finders-fee)
- Seller fear ("don't take the first offer"): [allvintagecards, inherited collections](https://allvintagecards.com/inherited-baseball-cards/)
- Boomer downsizing (42% of homes sold in 2025): [Go Back to the Past](https://www.gobacktothepast.com/blog/694-time-to-downsize-but-how-much-is-your-collection-worth)
- Consignment rates of 15–25% at shops, 10% at Green Gate: [pregradecards consignment comparison](https://pregradecards.com/blog/cardsource-vs-canadian-consignment-2026); [Green Gate](https://help.greengatehobbies.com/en/article/what-is-the-commission-rate-1naqlsl/)
- PSA Standard $59.99 (from 2026-09-14): [thecardshopfinder](https://thecardshopfinder.com/blog/psa-standard-tier-express-increase/)
- Flip margins, fees and the "buy cheaper" finding: our `business_models_unit_economics.md` §1 and §7

**Biggest risk:** most shoeboxes are junk-wax and worthless, so lead quality could make paid acquisition negative. The mitigation is to lean on free channels and on Claude's photo triage before anyone drives anywhere.

**Confidence: 6/10**

---

## demand-2: Gift-Ready Genuine, Q4 card gift bundles for people who can't find Pokémon

**One-liner:** Turn near-worthless bulk (Pokémon commons and holos, plus sports team lots) into gift-ready, no-duplicate, guaranteed-genuine bundles and starter kits. Sell them to parents and grandparents during the Nov–Dec rush.

**The hack (the unfair insight):**
- Bulk is worth $0.01–0.04 a card to hobbyists. In a bundle it is worth $0.20–0.35 a card to gift buyers who just want "real Pokémon cards for Jake, in stock, arrives by the 20th."
- That market is visibly huge:
  - A single Amazon bundle shows **30K+ bought in the past month**.
  - One eBay 100-card lot has **7,765 sold**.
- The incumbents' reviews tell you exactly how to win:
  - "more duplicates than expected," "four of the same card,"
  - 3.2–3.9 star listings,
  - fear of fakes.
- So the spec is:
  - No duplicates, no energy filler, recent sets only.
  - A guaranteed ex/V.
  - A photo of the exact contents.
  - A gift box with a "Pokédex checklist" insert.
- The sports twist: a **"Pick your team" 50-card NFL/MLB lot**. Junk-wax and modern base cards cost pennies, and personalization lifts the price from $5–10 to $15–25 on Etsy and eBay.
- Its bulk supply comes from demand-1 for nearly free. **This is the outlet that makes demand-1's bulk profitable.**

**Why now:**
- Pokémon is printing at maximum capacity, demand still outruns supply, and a new factory isn't expected until about 2028.
- Walmart moved to lottery drops, and Target has 2-per-SKU limits.
- The 30th Celebration waves land Oct 2, Oct 30 and Nov 6, 2026, which means peak gift demand meets empty shelves.
- Today is Oct 1. There are exactly enough weeks to source, test and scale before Black Friday.

**How Claude runs it (about 60%):**
- Writes every listing, title and keyword set for eBay, Walmart Marketplace, Etsy (the team lots) and a Shopify store.
- Uses Higgsfield and Adobe for product imagery, unboxing-style short videos and TikTok posts.
- Runs Meta and Google Shopping ads via AdWhispr. Researches competitor ads first.
- Builds the bundle-spec sheet and the "no duplicates" pick lists for assemblers.
- Tracks inventory and sell-through, reprices daily, and handles customer messages.
- Runs a Routine that watches TCGplayer and Whatnot bulk-lot prices to restock ex/V cards and holos at the lowest unit cost.

**User's tasks:**
- Buy bulk from local shops ($8–10 per 1,000 is a typical shop buy rate), Whatnot bulk lots, and demand-1 collections.
- Buy 1,000+ bulk ex/V cards before mid-November.
- Assemble bundles. Hire a $15–18/hr local helper at more than 300 units a week.
- Ship, and own the accounts.
- **Do not lead with Amazon:** Pokémon is a gated brand there (reported $1,000 fee plus manufacturer invoices), and seller-made bundles can be treated as brand manipulation. Use Amazon only if it is ungated later.

**First 30 days:**
- **Days 1–5:** Source 20,000 bulk cards, 300 ex/V and 500 holos (about $500–700). Claude ships 3 eBay SKUs plus 2 Etsy team-lot SKUs:
  - 50 cards + 1 ex at $14.99
  - 100 cards + 2 ex at $22.99
  - Starter Gift Kit (binder + 100 cards + 3 ex/V + gift box) at $34.99
- **Days 6–20:** Run $20/day of Promoted Listings and $15/day of Meta tests to a Shopify page. **Metric:** units a day per SKU and conversion rate.
- **Days 21–30:** Keep the 2 winning SKUs, pre-buy Q4 bulk to cover about 2,000 units, and line up the helper. **Kill test:** fewer than 5 units a day across channels by day 30, at a positive unit margin.

**Path to the goal (real math; postage and ad cost per unit are assumptions):**
- **100-card + 2 ex bundle at $22.99, free shipping:**
  - COGS about $3.50 (bulk $1.50, holos $0.60, 2 ex/V $0.80, box/insert/mailer $0.60).
  - Postage about $4.75.
  - eBay fees about $3.45.
  - Ads about $1.40.
  - Assembly labor $0.60.
  - **Net about $9.30/unit.**
- **Starter Kit at $34.99:** **about $12–13 net/unit.**
- **Q4 (Nov 1–Dec 20), middle case:** 25 units/day × 50 days = 1,250 units × about $10 = **about $12,500 profit in the season.**
- **Off-season:** about 4–6 units/day (birthdays, Pokémon Day, Easter) → about $1,200–1,800/month.
- **Annualized middle:** about $25–30k/year. That means about $5–6k/month only in Q4, and about $1.5k/month otherwise.
- **Reaching a steady $5k/month** needs about 17–20 units a day year-round, from multichannel plus a TikTok Shop and creator program. That is plausible but not the base case.

**Evidence:**
- Amazon volume: 30K+ and 10K+ bought in the past month on 50-card bundles, and 3K+ on a 100-card lot (search snippet of an Amazon results page; Amazon pages were blocked for direct fetch, so re-verify): [Amazon search: Pokémon cards for sale](https://www.amazon.com/pokemon-cards-sale/s?k=pokemon+cards+for+sale); [Amazon 100-card lot, "200+ bought in past week"](https://www.amazon.com/meta-labwear-Pokemon-TCG-Guaranteed/dp/B016BY59PO)
- eBay: a 100-card bundle with 7,765 sold; lots at $12.99–20: [eBay listing](https://www.ebay.com/itm/187957157635); [unpackhits $16.99](https://www.ebay.com/str/unpackhits); [betterbulkbuys $16.50](https://www.ebay.com/str/betterbulkbuys)
- The complaints (duplicates; 3.2–3.9 star bundles): [Walmart 100-card lot, 3.2★](https://www.walmart.com/ip/Pokemon-TCG-100-Card-LOT-Rare-COM-UNC-Holo-Guaranteed-EX-GX-VMAX-V-MEGA-OR-Full-Art/113076839); [Walmart Mega Box, 886 reviews, 3.9★](https://www.walmart.com/ip/1680273320)
- Team lots at $4–11 on eBay: [Pick-your-team lot](https://www.ebay.de/itm/286514932214)
- Bulk costs: [pokemonpricetracker bulk guide](https://www.pokemonpricetracker.com/pokemon-cards-cost); [Knight and Day bulk buy rates](https://knightanddaygames.com/pages/sell-us-your-bulk)
- Shortage and lotteries: [Dexerto, Walmart lottery](https://www.dexerto.com/pokemon/pokemon-fans-now-need-lottery-luck-to-buy-cards-at-walmart-3404656/); [My Nintendo News, 10B cards at max capacity](https://mynintendonews.com/2026/05/31/the-pokemon-company-says-10-billion-pokemon-cards-were-printed-in-the-last-year/)
- Amazon brand gating and bundle risk: [SellerEngine gated brands](https://sellerengine.com/new-requirements-for-amazon-gated-brands/amp/); [Amazon UK seller forum, bulk Pokémon](https://sellercentral.amazon.co.uk/seller-forums/discussions/t/d5809a09-18dd-4f6e-bfda-91fb0b409ec6)

**Biggest risk:** this is a crowded, commodity-priced, seasonal category, so margin depends on low bulk cost and on assembly labor staying cheap. Avoid anything "mystery" or random-chase (lottery-law exposure) and anything non-genuine or "compatible" (IP risk). Every bundle lists its guaranteed contents.

**Confidence: 6/10** (demand proof is the strongest of the three, but the economics are thin and seasonal)

---

## demand-3: Estate Card Desk, a B2B report-and-broker service for estate-sale companies and senior move managers

**One-liner:**
- Estate-sale companies, senior move managers and estate attorneys keep hitting the same problem: "there's a box of cards, what do we do?"
- Sell them a 48-hour card inventory and market-value report ($149–499, paid by the estate).
- Then broker the sale to the best of 3 vetted buyers for a 5–10% finder's fee.
- No inventory and almost no capital.

**The hack (the unfair insight):**
- The people who *find* collections are not hobbyists. They are estate liquidators, and they already:
  - pay generalist appraisers $150–350/hr,
  - or give cards away to the first dealer who shows up.
- Claude can produce a professional, card-by-card report from photos for a few dollars of compute. That is the "bad version" (slow, expensive, generalist), made 10x faster and cheaper.
- Dealers already pay finder's fees, Invest in Baseball openly offers 10%. So one partner relationship yields recurring, pre-qualified, out-of-market collections with two revenue lines.
- It also feeds demand-1 locally. Disclose clearly, and never appraise *and* buy the same lot yourself.

**Why now:**
- The Boomer downsizing wave is under way.
- Record buyer demand and liquidity mean dealers compete for collections.
- AI vision plus comps make card-level reports trivially cheap to produce.
- No incumbent owns "cards for estate professionals." Search for card-shop and estate marketing turned up generalists only.

**How Claude runs it (about 85%):**
- Builds the partner portal: an upload link, a status tracker, and the report delivered as a branded page or PDF.
- Runs the photo → ID → comps → value-range report pipeline, with a confidence flag on every card.
- Finds and lists estate-sale companies and senior move managers by metro from public directories.
- Drafts the partner outreach (email sequences via Gmail drafts).
- Runs the "best of 3 bids" process with vetted dealers.
- Tracks finder's fees and invoices.

**User's tasks:**
- Partner sales: calls, and coffee with estate-sale owners.
- Sign finder's-fee agreements with 5–10 dealers (national vintage buyers plus local shops).
- Approve every report before it goes out.
- Occasionally photograph a collection in person.
- Handle the legal and compliance basics: label the product "market value report, not a USPAP-certified appraisal," and refer IRS/estate-tax cases over $5k to credentialed appraisers.

**First 30 days:**
- **Week 1:** Claude ships the portal and a sample report (built from a real shoebox, the user's own or a friend's), plus a list of 150 estate-sale companies and move managers across 3 metros.
- **Week 2:** The user calls and emails 50 of them. The offer is "first report free," so the fake door is a free report. **Metric:** how many send a real collection within 14 days.
- **Weeks 3–4:**
  - Deliver 5–10 free or discounted reports.
  - Sign 3 dealers for finder's fees.
  - Broker 1–2 sales.
  - Convert 3+ partners to paid reports.
- **Kill test:** fewer than 3 active partners after 60 days.

**Path to the goal (real math):**
- **Maturity (month 9–12, middle case):** 12 active partners × 1 job/month = 12 reports × $225 avg = $2,700.
- **Brokering:** 40% get brokered. Average sale $3,000 × 7% fee = $210 × 5 = $1,050.
- **Total about $3,750/month.** Costs are about $200 (tools, compute) and **no inventory capital**.
- **Hours:** about 8–12 hrs/month of user time per 10 jobs plus sales time, which is very high $/hr.
- **To reach $5–10k:** 25 partners across 3–4 metros (portal and reports are remote; only sales is local), or upsell consignment management at a 15% take.

**Evidence:**
- Appraiser rates of $150–350/hr, card appraisers at $200 first hour + $150/hr: [ThePricer](https://www.thepricer.org/how-much-does-card-appraisal-cost/); [Globe and Mail on executors valuing estates](https://arc-dev.theglobeandmail.com/investing/globe-advisor/advisor-practice/article-how-executors-can-determine-the-value-and-tax-implications-of)
- PSA paid appraisals from $200: [PSA Appraisals](https://www.psacard.com/appraisals)
- Estate-sale companies already brokering card collections: [Lion & Unicorn on sports memorabilia in estate sales](https://lionandunicorn.com/selling-sports-memorabilia-in-estate-sales-how-to-appeal-to-serious-collectors/); [estatesales.org card-specialist companies](https://estatesales.org/company/22719)
- Insurance and inventory demand from AARP members: [AARP "Protect What You Collect"](https://www.aarp.org/home-living/protect-what-you-collect/)
- Finder's fees paid by buyers: [Invest in Baseball 10% fee](https://www.cardboardconnection.com/invest-baseball-100k-finders-fee)

**Biggest risk:**
- Partner sales cycles are slow.
- Report fees may face pushback because "the dealer appraises for free." The fallback is to make the report free and live on finder's fees plus demand-1 buys.
- Appraisal-vs-buyer conflict of interest must be handled openly.

**Confidence: 5/10**

---

## Overall verdict

**Conditional yes.**
- An AI-leveraged card business is +EV for this user **only if it plays the edges of the hobby**:
  - sourcing from non-hobbyist sellers (demand-1 and demand-3),
  - and selling to non-hobbyist gift buyers (demand-2).
- It is not +EV if it competes in the middle. Flipping, sealed speculation, grading arbitrage and breaking net about $7/hr or carry tail risk for a newcomer.
- The three moves stack: demand-3 and demand-1 bring in collections, and demand-2 turns their worthless bulk into revenue. That makes the honest middle outcome about $3–5k/month by month 12, with $5–10k needing a helper and a second metro.

**Board recommendation from my lens:**
- Start demand-2 **this week**, since the Q4 window is closing.
- Run demand-1 and demand-3 as one funnel from October onward.
