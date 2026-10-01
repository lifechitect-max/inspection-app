# Leverage Hacker — Round 1 Proposals

Lens: "How do we get 100x output per hour?" I map every task in each business to one of four owners: **Claude**, **a system/schedule**, **a freelancer**, or **the founder only**. Then I push as much as possible out of the founder's bucket. Anything where growth means the founder works more hours in a straight line, I kill.

## What I kill first (from the shared research)

- **Flipping modern cards or sealed product to hold.** Modern Pokémon sealed is down 20–50% from its peak, and sports indexes are down 2–11% over 12 months. A part-time flipper makes about $7–14/hour. That is labor with no leverage, plus price risk.
- **Grade-and-flip.** PSA's Value tiers are paused, so the cheapest PSA grade is $79.99 and the expected value is negative on most modern cards. Grading capacity sits with a monopoly-like incumbent (Collectors has about 79% of volume).
- **Random breaks.** The legal tail risk is real (Lesko arbitrations, a qui tam suit, PC 319.3). Breaks also need the founder live on camera, which is the opposite of leverage.
- **Another scanner, price app or deal bot.** That layer is commoditized and partly free, and eBay's 2025–26 terms ban AI scraping and buy-for-me agents.

The pattern: the toll collectors win. That means the platforms, the grader, the licensor and the accessory makers, plus whoever **buys from people who are not collectors**. My three moves sit where volume pays the user whether card prices rise or fall, and where Claude can act as the operations team.

---

## leverage-1: The Collection Buyer Engine (Dean's Cards playbook, run by AI)

**One-liner:** A paid-ads and SEO lead machine that buys inherited and attic card collections from non-collectors at 50–65% of value. Claude does the valuation, offers, listings and pricing. The user does the calls, pickups and shipping.

**The hack (the unfair insight):**
- The cheapest card inventory in America isn't on eBay or at shows. It's in closets, owned by heirs and ex-collectors who want speed and trust, not top dollar.
- Buying at 50–60% of market, not picking the right channel, is "where the money is" (business_models §1).
- Two things decide who wins this business: (a) **paid customer acquisition** and (b) **fast, accurate valuation of messy lots**.
  - Most card dealers are bad at (a). This user is a professional PPC operator, so that is his specific knowledge.
  - Claude collapses (b), the triage step that took a human expert hours, into minutes. For example: junk-wax 1987–94 is worth ~$0; flag pre-1980 vintage, 1990s inserts, 2000s+ rookie autos and WOTC Pokémon.
- Dean's Cards proves the model. It buys "almost 1,000 vintage collections every year" with 15 people, uses **bid software** to generate offers, and sees offers accepted **80%+** of the time.
- Big collections can be **consigned instead of bought**, which uses other people's inventory: no capital at risk, and a 20–25% cut.

**Why now:**
- Buying volume is at records: eBay focus categories +26%, Whatnot $8B+ in H1 2026, and PSA grading records. That means plenty of liquidity to sell into, whatever prices do.
- The cheapest exit channels exist now: Fanatics Collect at 6% (or 0% via FanCash), and Fanatics weekly auctions paying 100% of hammer plus a 2–15% bonus.
- Boomers and Gen X are passing down 1980s–90s collections now. Heirs search "sell inherited baseball cards" and find a handful of dealers with dated sites. This is an inference; I found no search-volume data.
- Vision LLMs can now read a phone photo of a binder page well enough to triage it.

**How Claude runs it (task map):**

| Task | Owner |
|---|---|
| Landing pages and programmatic city/era SEO pages ("sell inherited sports cards in Tampa", "what are 1990 Donruss worth") | Claude builds and publishes them (Higgsfield website builder or a hosted page) |
| Photo-intake form with shared DB: seller uploads photos and answers 5 questions | Claude builds it (Artifact with db capability) |
| Triage each submission: identify sets/eras, flag keys, estimate value range, draft offer at 50–65% of conservative resale | Claude, every morning on a schedule (Routine) |
| Offer emails and follow-ups in the user's voice | Claude drafts via Gmail; user approves |
| Google/Meta ad creation, negative keywords, weekly bid and search-term cleanup | Claude (AdWhispr launch plus a scheduled review); user sets budget |
| Pricing the bought lot: sort into "Fanatics Collect / eBay single / eBay lot / bulk buylist / grade (rare)" | Claude from the user's scans (Fujitsu/Ricoh fi-8170, about $735) |
| Variant-accurate titles and item specifics, eBay Seller Hub Reports CSV, Fanatics Collect listings | Claude generates; user uploads |
| Weekly repricing of stale listings and P&L dashboard | System (scheduled Routine) |
| Phone calls, house visits, paying sellers, scanning, packing, shipping | **Founder** (shipping can move to a local freelancer at month 4+) |

**User's tasks:**
- Fund buys and take calls.
- Do pickups within about 90 minutes of home, and accept ship-ins nationwide with prepaid labels.
- Scan cards, ship orders, and approve every offer and every ad budget.

**First 30 days:**
1. Days 1–3: Claude builds the site (one money page plus 20 SEO pages), the photo-intake form and an offer calculator rubric. The user opens Fanatics Collect and eBay seller accounts and buys the scanner.
2. Days 4–7: Launch Google Search ads at $30/day on "sell baseball card collection", "inherited sports cards", "sell old pokemon cards" and similar, with strict negatives. Run a Meta lookalike test at $15/day. Post the offer on local Facebook groups and Nextdoor *as yourself* (no spam).
3. Days 8–30: Work every lead in 24 hours. Target 3–5 purchases with $3–5k deployed. List everything within 72 hours of buying.
4. Kill or keep rule at day 30: cost per closed deal under $200 **and** realized gross margin at least 35% on the first lots sold. If either fails, cut budget and push SEO plus consignment-only.

**Path to the goal (real math, stated assumptions):**
- **Per bought collection (assumed average):** buy $1,200 at about 55% of realizable value, which means about $2,180 gross sales.
  - Fees blended 10% (Fanatics 6% / eBay ~13–15%): −$218
  - Shipping and supplies 4%: −$87
  - Duds and price drift 8%: −$175
  - Net proceeds ≈ $1,700, so **gross profit ≈ $500**
- **Acquisition (assumption to test):** $2 CPC, 6% click-to-lead, 20% lead-to-close gives about **$170 per closed deal**. Net per deal ≈ **$330**.
- **Consigned collections over about $3k value:** seller gets 75% of net, user keeps 25%. On an $8k gross lot: $8,000 − 8% fees = $7,360 net, and the user keeps **$1,840**, with no capital at risk.
- **Capital limit:** $15k at a roughly 45-day cash cycle funds about $10k/month of buys, about 8 collections/month.
- **Honest middle outcome at month 12:** 8 buys × $330 = $2,640, plus 1.5 consignments × $1,840 = $2,760, so **≈ $5.4k/month net before tax**. Time is about 20–25 hours/week.
- **Upside:** reinvest profits so capital reaches about $30k, then run 15–20 buys/month plus 3 consignments, for **$10–12k/month**. Shipping and scanning then move to a part-time helper at about $18/hour.
- **Downside:** CPC or close rate is half of what I assumed, so about $1.5–3k/month. That is still positive, because inventory bought at 55% has a margin cushion even in a 20% drawdown.
- Dean's Cards sanity check: about 1,000 collections/year with 15 staff is about 5–6 collections per person per month. A solo operator at 8–10/month with Claude as the back office is a believable 1.5–2x labor-leverage claim, not a fantasy.

**Evidence:**
- Dean's Cards (about 1,000 collections/year, 15 people, bid software, 80%+ acceptance, 1,000+ cards sold per day): https://www.deanscards.com/about-us ; https://www.deanscards.com/sell-your-baseball-cards
- Cash offers run 60–70% of market (All Vintage Cards): https://allvintagecards.com/inherited-baseball-cards/ ; https://allvintagecards.com/sell-your-baseball-cards/ ; Remi Card Trader pays 60% of eBay average: https://sell.remicardtrader.ca/en/products/buying-card
- Consignment fee benchmarks: Probstein ~9% (forum, older): https://forums.collectors.com/discussion/comment/10407226 ; PSA Vault 7–16%, and 15–20% at many consignors: https://pregradecards.com/blog/best-marketplaces-sell-graded-cards-2026
- Fanatics Collect 6% fee / 0% FanCash: https://support.fanaticscollect.com/en_us/buy-now-fees-ry33QCXaxe.md ; https://www.si.com/collectibles/fanatics-collect-eliminates-seller-fees-new-fancash-payouts-program
- eBay bulk CSV upload for sports-card singles (5,000 lines/day): https://export.ebay.com/en/services-tools/seller-hub/uploading-your-listings-in-bulk-using-reports-tab/
- Fujitsu/Ricoh fi-8170 card scanner about $735: https://www.ebay.com/p/21061138243
- Record buyer liquidity: eBay Q2'26 https://ebay.q4cdn.com/610426115/files/doc_financials/2026/q2/2026_Q2_eBay_Earnings_Presentation_Final.pdf ; Whatnot H1 2026 https://finance.yahoo.com/small-business/articles/whatnot-raises-545mn-series-g-150151629.html

**Biggest risk:** Lead economics are unproven, since I found no CPC or volume data for "sell my card collection" terms. A related risk is buying a fake or altered card in a lot. Mitigations: test with $1k of ad spend before scaling, check every slab cert, and set a rule to never pay out on a single key card over $500 without a second-source check.

**Confidence: 7/10**

---

## leverage-2: The Picks-and-Shovels Accessory Brand (Amazon plus TikTok Shop)

**One-liner:** Launch a private-label card *protection and display* brand. Start with one premium SKU, such as graded-slab storage/display or a zip binder for a specific game. Run it on the user's home turf, Amazon PPC, with Claude producing all listings, creative and bid optimization on a schedule.

**The hack (the unfair insight):**
- Every card bought, whether a pack, single, slab or bulk lot, needs a sleeve, a toploader, a binder or a box. Accessories carry **65–70% gross margins**, the highest in the hobby (business_models §4).
- Demand tracks **unit volume**, which is at records: 10B Pokémon cards printed a year and 26.6M cards graded. Card **prices** don't matter here, so a market correction doesn't hurt this business the way it hurts flippers.
- The user doesn't need hobby expertise. He needs Amazon PPC skill, which he already sells to other people on Upwork. This is Naval's "specific knowledge plus leverage": use the skill on his own asset instead of renting it out by the hour.
- Proof that outsiders can win this category:
  - **Vault X** was founded in 2021 and now has a 9-pocket zip binder at about 10k units/month on Amazon. Its store is estimated at $1.7–3.1M/month (third-party estimate, treat as directional).
  - **Arjiekwei**, an unknown private label, sells about 10–20k units/month of toploader packs at $23.99, alongside Ultra Pro.

**Why now:**
- The SCOTUS IEEPA ruling (Feb 20, 2026) removed the "reciprocal" tariffs. China is still at about 34% effective. That is painful, but it is now a known number rather than a moving target, and Vietnam or India sourcing lowers it.
- TikTok Shop US is projected at $23.4B in 2026 (+48%), and trading cards plus accessories make up about **81% of collectibles sales** there. That is a second channel Amazon-only competitors ignore.
- Retail traffic is surging. Target expects more than $1B in trading-card sales, GameStop collectibles grew 57%, and new collectors need everything at once.

**How Claude runs it (task map):**

| Task | Owner |
|---|---|
| Niche selection: review-mining the top 30 ASINs in sleeves, toploaders, binders, slab storage and one-touch magnets to find the unmet complaint (e.g., slabs scratching in boxes, binder rings denting cards, no Riftbound/One Piece-sized options) | Claude |
| Supplier RFQ emails, spec sheets, landed-cost and tariff model per SKU | Claude drafts via Gmail; user chooses the supplier |
| Listing copy, keyword map, A+ content, main image and lifestyle images, short demo videos | Claude (Adobe background removal and design, Higgsfield video) |
| PPC structure, daily search-term harvesting, bid rules and negative keywords, as a scheduled job from the user's exported reports | Claude plus a schedule; user approves budget changes |
| TikTok Shop affiliate outreach to card creators, paid on commission only | Claude drafts the outreach; creators are paid on results |
| Reorder alerts, P&L, weekly report | System |
| Seller Central account, payments, sample QC, trademark filing | **Founder** |

**User's tasks:** Open the Brand Registry trademark (about $350 USPTO plus filing help), approve the supplier, check the physical samples (sleeve fit is make-or-break), fund inventory, and make final PPC calls.

**First 30 days:**
1. Week 1: Claude produces a niche scorecard for 10 candidate SKUs: demand (ASInsight/Helium-style estimates), review gaps, price points, and landed cost with tariff. Pick 1 hero SKU priced at $19–35, since cheap sleeves at $7.99 can't carry FBA fees plus PPC.
2. Week 2: Send RFQs to 8 suppliers and order 3 samples. File the trademark. Claude drafts the brand name, packaging copy and listing.
3. Weeks 3–4: Approve the sample and place the first order of 500–800 units (about $3–5k landed). Meanwhile, Claude builds the PPC launch plan and a TikTok creator list of 50 names.
4. Realistic timing: first sales around days 45–60, after freight and FBA check-in. This is a slower start than leverage-1.

**Path to the goal (real math):**
- **Per unit at $24.99:**
  - Landed COGS including ~34% China tariff: −$5.50
  - FBA fulfillment plus fuel: −$4.50
  - 15% referral: −$3.75
  - PPC at about 14% TACoS: −$3.50
  - Returns and storage: −$0.75
  - **Net ≈ $7.00/unit (28%)**
- **$7.5k/month net** needs about 1,070 units/month, about 36/day, across 3–5 SKUs. The category leaders do 5–10k/month per SKU, so this is a mid-pack position, not a top spot.
- **Capital:** 3 months of inventory at 1,000 units/month × $5.50 is about $16.5k at scale. Start with $3–5k and fund growth from profit.
- **Honest middle outcome at month 12:** 2–3 SKUs at 300–500 units/month total each, which comes to **$3–5k/month net**. Time is under 8 hours/week after launch, and the business is a sellable asset (Amazon brands sell for about 2.5–4x SDE; general knowledge, not sourced here).
- **Upside:** One SKU breaks into the top 10 of its sub-niche, plus TikTok Shop creator flywheel, for $10k+/month.
- **Downside:** The hero SKU stalls because of a price war with Chinese sellers. You liquidate at cost and lose about $2–4k.

**Evidence:**
- Top toploader/sleeve ASINs at about 10k units/month (Arjiekwei $23.99; Ultra Pro toploaders $17.95; 1,000-count sleeves $9.99): https://www.asinsight.com/report/US/sports-card-top-loaders ; https://www.asinsight.com/report/US/card-sleeves
- Vault X growth and binder at about 10k/month: https://brandsearch.co/brands/vaultx.com ; https://www.asinsight.com/report/US/trading-card-binder
- Accessories 65–70% gross margin at shops: business_models §4 (AOL/VMFS citations there)
- TikTok Shop: collectibles about 81% trading cards and accessories (https://retaildive.com/news/tiktok-shop-collectibles-comic-manga/736391); 2026 US GMV $23.4B (https://www.emarketer.com/content/tiktok-shop-becoming-major-us-ecommerce-player)
- Tariffs after the SCOTUS ruling, China about 33.9% effective: https://globaltradealert.org/reports/SCOTUS-IEEPA-Tariff-Impact ; https://www.dlapiper.com/en/insights/publications/2026/02/us-supreme-court-holds-ieepa-does-not-authorize-tariffs
- FBA fees 2026 (15% Toys referral; small standard from $3.22; fuel surcharge): https://novadata.io/resources/blog/amazon-seller-fees-explained ; https://ecomcircles.com/blog/amazon-fba-fees/
- Unit volume drivers: 10B Pokémon cards/year (https://mynintendonews.com/2026/05/31/the-pokemon-company-says-10-billion-pokemon-cards-were-printed-in-the-last-year/); 26.6M cards graded in 2025 (https://www.si.com/collectibles/over-26-million-cards-graded-in-2025-how-the-market-exploded)

**Biggest risk:** The category is commoditized. Chinese sellers at $7.99 and Ultra Pro's brand pull compress price, and tariff policy can still move (Section 122/301). The fix is differentiation (a specific game, slab-specific, display or premium) plus at least 30% margin before PPC on every SKU, or don't launch it.

**Confidence: 6/10**

---

## leverage-3: Shop Online Desk (Claude as the online back office for card shops, paid on revenue share)

**One-liner:** Local card shops sit on 50k–200k singles they never list because listing is slow and repricing is painful. The user signs shops to a "we list and reprice, you ship" deal at 10% of online GMV. Claude does the listing pipeline. The shop's own inventory and account carry the capital.

**The hack (the unfair insight):**
- This uses other people's inventory **and** other people's labor. The shop owns the cards, the eBay or TCGplayer account and the shipping. The user owns the pipeline.
- The bottleneck in card e-commerce is **variant-accurate data entry**: parallel, serial, set code, language and condition. eBay's own AI bulk lister breaks on cards, and scanners mis-value variants (ai_tools §2, §4).
- A Claude vision-to-structured-JSON-to-CSV pipeline fixes exactly that. The marginal cost per card is cents, against about $0.65–$2/card COMC intake or 9–20% consignment.
- No capital at risk and no price risk. The business is a codebase plus contracts: an **asset**, not hours.

**Why now:**
- Shop card margins are down to about 20% after the pandemic, and shops are closing over online competition, so owners need online revenue.
- eBay's bulk CSV upload supports sports-card singles at up to 5,000 lines/day, so there is a sanctioned, ToS-compliant pipe. That means no scraping and no bots: the shop uploads files it controls.
- Whatnot's Seller API is closed to new applicants, so live-commerce tools can't easily automate shops. eBay and TCGplayer bulk files can be automated.

**How Claude runs it (task map):**

| Task | Owner |
|---|---|
| Shop staff feed cards through a $735 duplex scanner; images auto-sync to a shared Google Drive folder | Shop (system) |
| Nightly Routine: read new scans, identify card and variant, condition notes, comp range (from the shop's own Card Ladder/130point lookups or Fanatics FMV, not eBay restricted-API data), output eBay Seller Hub CSV and TCGplayer upload | **Claude on a schedule** |
| Weekly repricing file for stale listings, monthly GMV report and invoice | System |
| Outreach to shops: researched, personalized emails or visits, low volume, CAN-SPAM-clean | Claude drafts; user sends and visits |
| QA sample of 5% of listings, onboarding call, contract | **Founder** |

**User's tasks:**
- Sell and sign shops, starting with local ones in person.
- Do QA spot checks.
- Handle invoicing disputes.
- Optionally offer a "scan day" service where he brings the scanner, at $300 per day.

**First 30 days:**
1. Days 1–7: Claude builds the pipeline on 500 cards the user buys as test stock, with an accuracy target of 98%+ on set/number/variant across Pokémon, sports and One Piece. It also builds a 1-page offer and an ROI calculator.
2. Days 8–20: Visit 10 local shops and call 20 more. Offer a free 1,000-card pilot.
3. Days 21–30: Run 2 pilots. Measure listings per hour, error rate and sell-through. Convert pilots to 10%-of-GMV contracts with a $299 setup fee.

**Path to the goal (real math):**
- **Per shop:** 20k aged singles at an average of $8. At 5%/month sell-through, that is 1,000 cards, or about $8k online GMV/month. At 10%, the user earns **about $800/shop/month**.
- **Costs:** Model/API compute is about $50–100 per shop per month (estimate). User time is about 2 hours/shop/month for QA and reporting.
- **Target:** 8–10 shops gives **$6.4–8k/month**. One directory alone lists **963 US shops** in 45 states, so 10 shops is about a 1% hit rate nationally, or fewer if the user sticks to driving distance.
- **Honest middle outcome at month 12:** 5 shops at about $600, plus scan-day and setup fees, comes to **≈ $3–4k/month**. It needs very little capital ($1–2k for a demo scanner and test stock). Time is about 10–15 hours/week, mostly selling.
- **Upside:** Productize it as "AI listing desk" for Whatnot and eBay power sellers and for estate/consignment dealers, priced per card, at $10k+/month.
- **Downside:** Shops refuse revenue share, or listing errors cause returns and the shop churns.

**Evidence:**
- A mid-size TCG store holds 50k–200k singles line items and retail tools "collapse": https://tcgsync.com/blog/tcg-inventory-management-guide
- Dealer pain: singles hard to list, repricing arduous, show chaos: https://winventory.ca/partner/features ; https://tcgsync.com/vendor-only
- eBay AI bulk card lister broken on brand, number and player: https://www.valueaddedresource.net/ebay-bulk-ai-listing-sports-cards-broken/ ; scanners fail on variants: https://eyevotcg.com/blog/best-pokemon-card-scanner-apps-2026/
- eBay bulk CSV for sports-card singles: https://export.ebay.com/en/services-tools/seller-hub/uploading-your-listings-in-bulk-using-reports-tab/ ; https://community.ebay.com/t5/Seller-Tools/Sports-card-bulk-listing-help-needed/m-p/31908240/highlight/true
- Consignment price anchors (COMC $0.65–$2/card intake plus 5% and 10% cash-out; Probstein about 9%; PSA Vault 7–16%): business_models §1 ; https://pregradecards.com/blog/best-marketplaces-sell-graded-cards-2026
- 963 shops listed: https://thecardshopfinder.com/about/ ; shop margins about 20% and closures: business_models §4, risks §6
- Whatnot Seller API closed to new applicants: https://developers.whatnot.com/docs

**Biggest risk:** This is B2B selling to small, cash-strapped, skeptical owners. Sales cycles and churn may cap it at a few shops, and accuracy errors land on the shop's seller rating. It is the most founder-sales-dependent of the three.

**Confidence: 5/10**

---

## Overall verdict (Leverage Hacker)

**Conditional yes.** An AI-leveraged card business is +EV for this user **only** if he stays out of price speculation (modern flips, grading, sealed, breaks), which is negative or zero EV for a newcomer. He should instead put his real edge, paid acquisition, into a volume business where Claude is the back office.

My pick is **leverage-1 (Collection Buyer Engine)**. It has the fastest cash, a margin cushion that survives a 20% drawdown, a Dean's Cards-proven model, and roughly a $5k/month middle outcome at 12 months. **leverage-2** is the lower-time, asset-building hedge that doesn't care about card prices.

Honest middle outcome across moves: $3–6k/month net by month 12. $10k+ requires the ad funnel economics in leverage-1 to validate in the first $1k test.
