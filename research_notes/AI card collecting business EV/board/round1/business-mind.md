# Business Mind — Round 1 Proposals

Lens: Buffett, Munger, Bezos, Collins, Leonard. One question: **does this compound and last 10 years?**
Date: 2026-10-01. Sources: the four shared research notes, plus my own searches. I also pulled live Google Keyword Planner data through the AdWhispr connector (US, 2026-10-01).

---

## Overall verdict (2-3 sentences)

**It depends.** An AI-leveraged card business is +EV for this user only if he sits on the **supply side as a trusted buyer of collections**, earning a toll on record transaction volume. It is -EV if he holds modern inventory and bets on price. The research shows modern sealed and singles down 20-50%, PSA's cheap tiers paused, breaking under legal attack, and the median part-time flipper making about $7-14/hour. AI is not the moat here, because everyone has it. The moat is **trust with sellers who aren't in the hobby, a lead machine (his PPC skill), and a referral network**. Those compound, and Claude does most of the work behind them.

What I kill outright: holding modern sealed, grading arbitrage (cheapest PSA tier is now $59.99 Standard at 90-100 business days, and the Value tiers are still paused), random breaks and repacks, building another scanner, pricing app or deal-alert bot, and anything built on eBay restricted-API data.

---

## The insight behind all three moves

Every source agrees that **"the money is in the buying"**: collections bought at 50-60% of market beat any choice of selling channel. Meanwhile 2026 has handed sellers very cheap exits: Fanatics Collect charges 6%, or 0% if paid in FanCash, and its weekly auctions pay 100% of the hammer price. Courtyard charges 0%. So the scarce input is not selling capacity. It is **access to motivated sellers who don't know the market**: heirs, downsizers, and parents of grown kids.

Those people search Google, and the CPCs are cheap for intent this strong (live Keyword Planner, US):

| Keyword | Searches/mo | CPC (top of page) |
|---|---:|---|
| sell pokemon cards near me | 8,100 | $1.34-$4.48 |
| sell pokemon cards | 6,600 | $1.14-$3.84 |
| sell baseball cards near me | 4,400 | $1.38-$3.39 |
| sell sports cards near me | 4,400 | $1.38-$3.39 |
| best place to sell pokemon cards | 2,400 | $1.39-$5.21 |
| sports card buyers | 2,400 | $1.16-$5.52 |
| places that buy pokemon cards near me | 2,400 | $1.40-$4.18 |
| sell sports cards | 1,900 | $1.33-$3.84 |
| baseball card appraisal (+ near me) | 720 + 590 | $1.08-$3.25 |
| sports card appraisal (+ near me) | 390 + 390 | $1.17-$3.21 |

The user already runs paid search for a living. That is his **hedgehog**: what he is best at (paid acquisition), what drives the economics (cheap supply), and a long-term tailwind (the $84-124T boomer wealth transfer, in which heirs are "buried under baseball cards"). All three overlap here.

---

## business-mind-1: The Heir Desk (collection buying and consignment desk, local first)

**One-liner:** A trusted, transparent "sell your inherited or old card collection" desk. Paid search and referral partners bring the sellers, and Claude does the valuation work. Sellers choose cash now (50-65% of comps) or consignment (around 15-20% commission).

**The hack:** Most "we buy collections" operators are lowballers, and sellers know it. The research flags "don't take the first offer" and "never mail cards sight unseen" as standard advice to heirs. The unfair edge is **radical transparency at near-zero cost**. Claude produces an itemized valuation report with comps for every submission, free and within 24 hours. Then the desk makes two offers side by side. Trust converts at a higher rate than a lowball, and it earns reviews and referrals. Those are the compounding assets. A second edge: most collection buyers are hobbyists who don't know how to run Google Ads, and this user does.

**Why now:**
- Record volumes and cheap exits: eBay GMV is +14% and cards are its #1 growth driver, Whatnot GMV is over $8B for H1 2026, Fanatics Collect charges 6%/0%, and Courtyard charges 0%. A bought collection can be liquidated faster and cheaper than ever, even as modern prices soften.
- Vintage (pre-1975) held value through 2022 and is still strong. Inherited collections skew vintage and 1980s-90s.
- The wealth transfer is underway. Bloomberg (Nov 2025) describes heirs "buried under an avalanche of baseball cards."

**How Claude runs it:**
- Builds and ships the site: a landing page plus a photo-upload intake form. It's hosted as an Artifact with a shared database as the deal pipeline/CRM, or on the Higgsfield website builder.
- Writes and launches Google Search campaigns through AdWhispr, then monitors and adjusts them daily on a Routine.
- Triages each submission from photos: era, sets, likely keys, junk-wax flags. It then drafts the itemized valuation report from public sold comps, entered by hand or from non-restricted sources (no eBay restricted API), with a cash offer and a consignment estimate.
- Drafts all seller emails in Gmail (the user approves before sending) and books calls on Calendar.
- After purchase: writes variant-accurate listing titles, item specifics and descriptions, picks the channel per card (Fanatics Collect for graded and $200+, eBay for mid raw, bulk lots to shops), and keeps per-deal P&L.
- Runs the partner program: finds local estate-sale companies, senior move managers and estate attorneys, and drafts outreach and one-pagers.

**User's tasks:**
- Create and verify the accounts (Google Ads, Fanatics Collect, eBay, business entity, bank) and fund the ads.
- Take calls and meet sellers in person.
- Inspect, photograph and ship the cards.
- Make the final call on every offer.
- Learn the vintage basics and authentication red flags. With PSA reporting counterfeits up 125% and altered cards up 407%, this is non-negotiable.
- Show up once a month at a local show to build relationships.

**First 30 days:**
1. **Week 1:** Claude builds the site, intake form, pipeline and valuation report template. The user forms an LLC, opens accounts, and sets a $1,000-1,500 ad budget focused on a 50-mile radius.
2. **Week 2:** Launch Search ads on "sell sports/baseball/pokemon cards near me", "sports card buyers" and "appraisal". Claude drafts outreach to 40 local estate-sale companies and senior move managers, offering a free valuation for their clients and a 5% finder's fee on closed buys.
3. **Weeks 3-4:** Close the first 2-4 deals. Track cost per lead, qualify rate (est. market value of $1,000+), close rate and realized margin per deal. **Kill or continue gate at day 60:** cost per qualified lead under $150 and realized gross margin of at least 25% of market value.

**Path to the goal (real math):**
- **Funnel at about month 9:**
  - $1,500/mo of ads at about $3 CPC brings ~500 clicks. At 6% form conversion that is ~30 submissions, plus ~6/mo from referral partners.
  - About 25% qualify (market value of $1,000+), so ~9. Closing about 65% of those as a buy or consignment gives ~6 buys and ~2 consignments a month.
- **Per buy:**
  - Average market value is ~$2,500 (a fat tail: most are $800-2,000, and the occasional vintage lot is $10k+). Buy at 55% = $1,375.
  - Realize ~85% of market after fees, postage and supplies (a mix of Fanatics 6% and eBay ~15%) = $2,125, so **~$750 gross per deal**.
- **Per consignment:** a $3,000 collection at an 18% commission, after absorbing ~6-8% in platform fees, nets **~$300**.
- **Honest middle outcome at month 12:**
  - Gross: 6 × $750 + 2 × $300 + bulk resale of ~$300 = **$5,400/mo gross**.
  - Net: minus $1,500 ads and $200 tools = **~$3,700/mo net before tax**.
  - Working capital needed: ~$12-15k on a 45-day turnover.
  - Time: about 18-22 hrs/week (~8 hrs per deal).
- **Path to $5-10k/mo:**
  - Grow referral partners, which are free leads, to ~50% of deal flow.
  - Raise average deal size by targeting vintage-specific searches and partners.
  - Add a second metro with a part-time runner hired on Upwork.
  - At 10 deals/mo and a $3,000 average, the desk makes ~$9k/mo net.
- **Downside:** 3 deals/mo, giving ~$800/mo net, and the user's time is underpaid.
- **Sellability:** a desk with a documented lead machine, reviews and partner contracts could plausibly sell for 1.5-3x yearly profit to a regional dealer. That multiple is my judgment, not sourced. It also depends on the owner less than a flipping business does, because the leads come from systems rather than his personal network.

**Evidence:**
- Buying at 50-60% of market is where the money is, and a typical flip nets 14% (business_models_unit_economics.md §1, §4, §7).
- Buyers' offers: Remi Card Trader pays 60% of the average eBay value; shop buylists pay 40-60% of market in cash, 25-50% in some guides — [allvintagecards inherited guide](https://allvintagecards.com/inherited-baseball-cards/); [StorePass buylist explainer](https://storepass.co/blog/what-is-a-buylist-how-tcg-stores-buy-cards-from-customers)
- Exits: Fanatics Collect charges 6%, or 0% with FanCash — [SI](https://www.si.com/collectibles/fanatics-collect-eliminates-seller-fees-new-fancash-payouts-program); [Fanatics press release](https://www.fanaticsinc.com/press-releases/fanatics-launches-new-collectibles-marketplace-fanatics-collect)
- Proof the model works at scale: Just Collect (founded 2006) has bought and sold over $50M, flies out to buy collections, and offers free appraisals — [Just Collect at the National](https://blog.justcollect.com/just-collect-continues-purchasing-collections-at-the-national)
- Consumer pricing for appraisals: written appraisals from $200, and $100-300/hr — [ThePricer](https://www.thepricer.org/how-much-does-card-appraisal-cost/); [AJ Sports](https://ajsports.ca/pages/appraisals)
- Wealth transfer: [Bloomberg, Nov 2025](https://prod.cm.bloomberg.com/news/features/2025-11-14/millennials-gen-x-set-to-inherit-boomers-antique-collectible-fortunes); [Masterworks, June 2026](https://www.masterworks.com/academy/posts/the-great-wealth-transfer-84-trillion-dollars-and-the-next-generation)
- Partner pool: an estimated 10,500-22,000 US estate-sale companies — [Gitnux](https://gitnux.org/estate-sale-industry-statistics/); [HomeLight](https://www.homelight.com/blog/estate-sale-companies/)
- Keyword volumes and CPCs: the table above (Google Keyword Planner via AdWhispr, 2026-10-01).

**Biggest risk:** Adverse selection. Most inherited collections are 1987-94 junk wax worth almost nothing. Add the risk of overpaying for a fake or altered vintage card, and the desk can burn ad money on unqualified leads. The fix is a strict photo pre-qualification gate before any visit, and paying only after the cards are in hand.

**Confidence:** 7/10

---

## business-mind-2: Buy-Counter Fill (seller-lead engine for card shops, territory-exclusive)

**One-liner:** Card shops make their margin by buying collections cheaply, yet almost none of them advertise to sellers. Sell each shop an exclusive metro territory of photo-qualified seller leads, generated by the user's PPC skill and Claude's local SEO pages.

**The hack:** This is Munger's incentives applied. Agencies sell shops "more customers," but a shop's real profit lever is **more collections walking in to sell**. Cash buylists pay 40-60% of market, and in-store resale at full retail carries no platform fee. So the user sells the thing that maps directly to the shop's profit: qualified sellers, with photos and an estimated value attached, delivered to one exclusive shop per metro. That makes it **a network, not an agency**. Each metro page and review adds to a consumer-facing "where to sell your cards in [City]" brand that compounds organically, while the paid search keeps it fed from day one.

**Why now:**
- "Sell pokemon cards near me" (8,100/mo) and "sell sports/baseball cards near me" (4,400/mo each) cost only $1.3-4.5 per click. Many shops don't bid at all.
- Shops' sealed margins have collapsed to about 20%, while buylist and accessory margins carry them, so supply is their bottleneck.
- Shops are closing over online competition. The ones that survive need a sourcing advantage over Whatnot and eBay sellers.

**How Claude runs it:**
- Builds a templated multi-city site ("Sell your cards in Austin", etc.), with honest guides and a photo intake form.
- Runs a pre-qualification check on each submission: what it is, rough value band, and whether it's bulk or keys.
- Routes the lead to the territory shop by email/SMS draft, logs it in a shared Artifact database the shop can see, and asks the shop for the outcome to measure close rate and ROI.
- Writes and manages the Google Ads (AdWhispr), weekly shop reports, outreach to the ~963 shops in the public directory, and the one-pagers.

**User's tasks:**
- Sales calls to shop owners. He already sells services on Upwork.
- Contracts, billing and the ad accounts. The shop pays ad spend on its own card or reimburses it.
- Monthly review calls with each shop.
- A stated rule to avoid conflicts: never run this in a metro where he runs business-mind-1 himself, and pass out-of-area leads from the Heir Desk to partner shops.

**First 30 days:**
1. **Week 1:** Claude builds the template site and lead router, and runs keyword volumes for the top 30 metros.
2. **Week 2:** The user calls 30 shops (Claude drafts the list, scripts and a free 2-week pilot offer). Goal: 3 pilot shops in 3 metros.
3. **Weeks 3-4:** Pilots live with $300-500 of ad spend per shop. Measure qualified leads per $100 and the shop-reported close rate. Convert pilots to paid only if the shop's math is clearly positive.

**Path to the goal (real math):**
- **Price:** $500/mo base per exclusive territory plus $30 per qualified lead. The shop pays ad spend of $500-1,000/mo.
- **Lead economics (calc):**
  - At $3 CPC and 8% form conversion with 50% qualified, a qualified lead costs ~$75 in media. $750 of spend gives a shop ~10 qualified leads/mo.
  - At a 40% close rate the shop gets ~4 collections/mo. At ~$2,000 market value bought at 50% and resold in-store near retail, that is ~$900 gross each, or ~$3,600 for the month.
  - The shop's total cost is ~$1,550 ($750 spend + $500 base + $300 per-lead fees), so it roughly doubles its money. That's thin enough that lead quality must be policed hard.
- **Honest middle outcome at month 12:** 7 shops × ($500 + 10 × $30) = **$5,600/mo revenue at ~85-90% margin, ~$4,800/mo profit**. That takes ~12-15 hrs/week, with Claude doing the build, monitoring and reporting.
- **Path to $10k+:** 12-15 shops, plus organic SEO pages lowering lead cost over time. That is the compounding part: paid search rents traffic, while the city pages and reviews are owned.
- **Downside:** shops churn after 3 months because their close rate is low, leaving 2-3 shops and ~$2k/mo.
- **Sellability:** recurring B2B revenue plus a portfolio of SEO pages is the cleanest asset of the three to sell, at roughly 2.5-4x yearly profit (my judgment).

**Evidence:**
- Keyword volumes and CPCs: the table above (Keyword Planner via AdWhispr, 2026-10-01).
- Shop economics: card margins about 20%, accessories 65-70%; buylists pay 40-60% cash, and credit pays 20-30% more (business_models_unit_economics.md §4) — [StorePass](https://storepass.co/blog/what-is-a-buylist-how-tcg-stores-buy-cards-from-customers); [TCG Sync buylist glossary](https://tcgsync.com/glossary/buylist)
- Shop count: the Card Shop Finder lists 963 shops in 45 states, which is a floor, not a census — [thecardshopfinder](https://www.thecardshopfinder.com/)
- Shop closures and pressure: [SCD shop-closing tag](https://www.sportscollectorsdaily.com/tag/sports-card-shop-closing/)
- No incumbent "lead network for card-shop buy counters" turned up in search. Results were generic SEO "sell near me" pages.

**Biggest risk:** The unit economics are thin. If shops close fewer than about 25% of leads, or most leads are junk-wax bulk, shops churn and the network never compounds. This is a single-channel bet on Google Ads until the organic pages mature.

**Confidence:** 5/10

---

## business-mind-3: Collection Legacy Plan (catalog, insurance schedule and heir plan for serious collectors)

**One-liner:** For collectors aged 50 and up with $10k+ collections: a done-for-you inventory, an insurance-ready schedule, an annual revaluation and a sealed "letter to heirs" (what it's worth, how to sell it, who to call). It comes with a locked-in consignment rate when the time comes.

**The hack:** This is the Berkshire **float** move. Each customer pays a small fee now, and the business accumulates a **proprietary map of who owns which valuable collections and when they will come to market**, plus a contractual first call when they do. Collectr and CollX track collections for hobbyists. Nobody serves the collector's **heirs**, the people who later get lowballed. Insurers ask for photos, certs, receipts and current values to pay claims, so the catalog has a clear "why now" for the collector. The heir letter builds trust across generations.

**Why now:**
- The wealth transfer ($84-124T) is underway.
- Fraud is up: PSA reports $200M+ in fakes and alterations intercepted, so documented provenance is worth more.
- Collectibles insurers need documentation at claim time.
- AI finally makes a done-for-you catalog cheap to produce. From slab photos and binder pages, Claude extracts structured data, cert numbers and comps for pennies, work that used to cost $100-300/hr.

**How Claude runs it:**
- Ingests the customer's photos (slab fronts/backs, binder pages) and extracts set, number, grade and cert into structured inventory.
- Builds a private, branded Artifact page per customer: their collection, values and the heir letter.
- Generates an insurance-schedule PDF and runs an annual revaluation Routine.
- Drafts the marketing: Meta ads to 45+ collectors, outreach to estate-planning attorneys and collectibles-insurance agents, and show handouts.

**User's tasks:**
- Sales and partner relationships with attorneys, insurance agents and local shows.
- Quality-checking the high-value items.
- Taking payments.
- Wording the plan carefully: a "valuation summary," not a qualified appraisal, so no tax or IRS appraisal claims.
- Honoring the consignment lock, which needs business-mind-1 or a partner consignor in place.

**First 30 days:**
1. Claude builds the intake flow, a sample catalog and the heir-letter template.
2. The user signs 5 beta collectors from a local show or Facebook groups at $99 to refine the product.
3. Pitch 10 estate-planning attorneys on bundling it as a client add-on.

**Path to the goal (real math):**
- **Price:** $249 setup (up to 500 items, $0.50/item beyond) plus $120/yr Legacy plan (revaluation, updated schedule, heir letter, consignment at 10%).
- **Honest middle outcome at month 12:** 80 setups ($20k) and 60 annual plans ($7.2k ARR), about **$2.3k/mo average, ~$1.5-2k net after ads**. On its own this business **does not hit $5-10k/month in 12 months.**
- **Why it compounds anyway:**
  - At an average catalogued value of ~$15k, 80 customers put ~$1.2M of mapped supply under a first-call agreement.
  - If ~8% comes to market each year via sale or estate, that is ~$96k of consignment at 10% = ~$9.6k/yr by year 2, growing every year as the base grows.
  - Annual plans renew at near-zero marginal cost.
- **Its real role:** this is the moat **feeding business-mind-1**, the 10-year bet that looks slow now. A standalone it is not.

**Evidence:**
- Insurers want documentation (photos, certs, receipts, current values), and appraisals above certain thresholds — [thecardshopfinder insurance guide](https://thecardshopfinder.com/blog/how-to-insure-valuable-card-collection/); [Pokemon card insurance guide](https://www.pokemonpricetracker.com/guides/pokemon-card-insurance); [CollectInsure](https://collectinsure.com/?p=6439)
- Professional appraisal pricing is $200+ per report and $100-300/hr — [ThePricer](https://www.thepricer.org/how-much-does-card-appraisal-cost/)
- Fraud growth: [SI on the PSA fraud report](https://www.si.com/collectibles/psa-report-reveals-200m-fake-cards)
- Wealth transfer and heirs: [Bloomberg](https://prod.cm.bloomberg.com/news/features/2025-11-14/millennials-gen-x-set-to-inherit-boomers-antique-collectible-fortunes)
- Collection trackers are proven but sold to hobbyists: CollX ~$10M revenue, Collectr eight figures, both at $8-25/mo (ai_tools_and_edges.md §2; business_models_unit_economics.md §5).

**Biggest risk:** Slow, expensive customer acquisition. Serious older collectors are hard to reach and may see free apps as "good enough." The payoff is years out, so cash flow can't carry the user in year 1.

**Confidence:** 4/10

---

## How the three fit (the flywheel)

**Heir Desk (cash engine)** → reviews and a valuation dataset → cheaper leads and better offers → more deals.
**Buy-Counter Fill** monetizes the leads the desk can't serve (other metros), with no capital.
**Legacy Plan** builds the long-dated supply float that comes back to the desk.

**Recommended order:** start business-mind-1 in one metro. Bolt on business-mind-2 by month 3-4 using the same ad machine. Add business-mind-3 only once the desk is profitable.
