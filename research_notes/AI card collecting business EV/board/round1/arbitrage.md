# Arbitrage Hacker — Round 1 Proposals

**Lens:** Where is something still priced wrong? Who in the card economy is paying human prices for work Claude does for pennies, and who is selling below value because they lack information?

**Date:** 2026-10-01

## Overall verdict (2-3 sentences)

**Conditional yes.** Holding card inventory is -EV for this user right now. Modern Pokemon and sports prices are falling 10-50%, PSA's cheap tiers are paused (the cheapest PSA tier is now $59.99-79.99), free deal bots have taken away the speed edge, and the research puts a part-time flipper at about $7-14/hour. Two gaps are still mispriced in his favor. First, card sellers pay human-agency prices for ads and listing work that Claude can do. Second, non-collectors (heirs, estates) sell whole collections for well under market because they can't tell what they have. The business is +EV only if it lives in those two gaps and never holds speculative modern inventory.

## Where the gaps are (price vs AI cost)

| Gap | Market price today | Our cost to deliver with Claude | Gap | How long it lasts |
|---|---|---|---|---|
| Ads management for card sellers (eBay Promoted Listings, Whatnot Promote/Boost) | Amazon PPC agencies: $1,500-5,000/mo, floor about $2,000/mo | ~1.5-2 user hrs/client/week + $50/mo tools | Very large | 2-4 yrs, until card-specialist agencies show up |
| Collection appraisal and triage from photos | Dealers do it free but slowly, as the hook for buying at 40-70% of market | Minutes per collection (vision ID + comps) | Information gap of 30-60% of market value | Lasts as long as people inherit cards. AI appraisal apps narrow it slowly. |
| Listing and repricing aged shop inventory | Consignment 15-40%; COMC 5% + 10% cash-out + $0.65/card + 16 weeks | Claude IDs, prices and writes CSVs; the shop or user photographs | 10-25 points of GMV | 1-3 yrs, until shop software (CardCloud, TCG Sync) adds AI |
| Fanatics Collect auction channel vs eBay | eBay takes about 15.4% of a $100 single; consigners take 15-40% | Fanatics weekly auctions pay 100% of hammer + a 2-15% bonus on $50+ cards | 15-30 points | Until Fanatics ends the subsidy (it is a land-grab subsidy and will end) |

---

## arbitrage-1: Card Seller Ad & Fee-Leak Desk

**One-liner:** Run eBay Promoted Listings and Whatnot Promote/Boost for card sellers, plus AI title and item-specifics cleanup, at half of agency prices. Claude does about 80% of the work.

**The hack (the unfair insight):**
- The user already sells Amazon PPC on Upwork. Card sellers are a hot, growing niche with no specialist ad agency.
- On Jan 13, 2026 eBay changed Promoted Listings General attribution in the US and Canada. A sale now counts as ad-driven if *any* buyer clicked the ad in the last 30 days. Attribution rates in other markets jumped to 80-90%, so many card sellers are quietly paying 5-12% extra on most of their sales.
- At the same time, Whatnot has new ad products (Promote Full Show with an hourly budget, and 15-minute Boost auctions) that most sellers run by gut feel.
- That gives a sharp, measurable pitch: "We find the ad fees you're leaking and cut them. Then we buy you growth that pays back."
- Claude's edge: pull the seller's own ad reports (CSV export, not restricted eBay API data, so we stay inside eBay's API terms), find wasted ad rate by card tier, rewrite titles and item specifics (parallel, serial, set code). eBay's own AI tool gets these wrong, and the variant problem is the main reason scanners fail. Claude also writes the weekly report.

**Why now:**
- The attribution change is 9 months old and sellers are angry about it (eBay community threads, Value Added Resource coverage).
- Whatnot's tiered fees started Sept 21, 2026, so sellers are now pushing to hit volume tiers, which rewards paid traffic.
- The seller base is growing fast:
  - Whatnot doubled GMV to $8B+ in 2025 and did $8B+ in H1 2026 alone.
  - Sellers earning $10k+/month more than doubled.
  - One in eight Whatnot sellers is full-time.
  - About 4.8M sellers use eBay Promoted Listings.

**How Claude runs it:**
- Builds the audit tool: upload eBay Promoted Listings and sales CSVs, get back an ad-fee-leak report with recommended ad rates by price band.
- Writes the outreach, audit decks and proposals.
- Each week, analyzes client exports, rewrites titles and item specifics in bulk (CSV for eBay File Exchange or Seller Hub), plans Whatnot Boost timing from show analytics, and drafts client reports.
- Runs on a schedule (Routines) to prep each client's weekly packet before the user's review call.
- Publishes a free "eBay ad fee leak calculator" Artifact as the lead magnet.

**User's tasks:**
- Hold the client relationship and sales calls.
- Log in to client ad dashboards and apply changes. Delegated access is the client's choice; Claude does not log in or click.
- Send outreach from his own accounts.
- About 1.5-2 hrs/client/week.

**First 30 days:**
1. Days 1-5: Claude builds the fee-leak calculator and audit template. The user posts a "free eBay ad-fee audit for card sellers" offer, sends it to 50 eBay card stores (store pages are public) and 30 Whatnot sellers, and posts in seller communities. Respect each community's rules on self-promotion.
2. Days 5-15: run 8-10 free audits. Each audit is a 1-page "you leaked $X last 30 days" report plus fixes.
3. Days 15-30: convert 2-3 to paid at an intro price of $500/mo. Add an Upwork/Fiverr productized gig: "Whatnot + eBay ads audit for card sellers, $149."
4. Goal at day 30: 2 paying clients plus 1 case study with real numbers.

**Path to the goal (real math):**
- Price: $750/mo flat, or 25% of verified ad-fee savings plus a growth fee. That is half the Amazon-agency floor. Target clients do $30k-300k/mo GMV.
- Client value check: an eBay card store at $50k/mo GMV with an 8% ad rate and 85% attribution pays about $3,400/mo in ad fees. Cutting that 30% saves about $1,000/mo, so a $750 fee pays for itself.
- Volume (honest middle): 3 clients by month 3, 6 by month 6, 9 by month 12, with 6% monthly churn baked in.
- Revenue at month 12: 9 × $750 = $6,750/mo. Costs: ~$200/mo in tools.
- **Profit: ~$6.5k/mo at month 12. Middle outcome ~$4-6k/mo.**
- Time: about 15-18 hrs/week at 9 clients.
- Path past $10k: hire a VA on Upwork for execution, raise new-client pricing to $1,250, and add performance fees.

**Evidence:**
- eBay Promoted Listings General attribution change, Jan 13, 2026: https://community.ebay.com/forum/selling-57920/topic/promoted-listings-general-attribution-changes-coming-to-us-canada-january-13-2026-153958/ ; https://www.ecomcrew.com/ebay-promoted-listings-attribution-2026/ ; fallout and fee increases: https://www.valueaddedresource.net/ebay-promoted-listings-ad-attribution-update-fallout/
- 4.8M sellers on Promoted Listings; ad rates 2-20%+: https://www.underpriced.app/blog/ebay-promoted-listings-roi-guide-2026
- Whatnot ads (Boosted livestreams, Promote Full Show/Boost): https://valueaddedresource.net/whatnot-launches-ads-with-boosted-livestreams ; https://sacra.com/chat/h/22ee3b40-9f9a-4b1a-9595-37cc6887ba7c/
- Whatnot seller growth (sellers at $10k/mo doubled; 1 in 8 full-time; 3-4 shows/wk ≈ $12k/mo): https://www.tubefilter.com/2026/01/28/whatnot-state-of-live-selling-report-2026-shopping-ecommerce/
- Whatnot tiered commission, Sept 21, 2026: https://www.tubefilter.com/2026/09/17/whatnot-new-commission-rates-lower-three-percent/
- Amazon PPC agency pricing, $1,500-5,000/mo with a ~$2,000 floor: https://salesduo.com/blog/amazon-ppc-management-cost-agency-fees/ ; https://amzdudes.com/amazon-agency-pricing/
- Low-end competition is real (a Fiverr "Whatnot promotion strategy" gig exists): https://fiverr.com/abim_marketing/boost-whatnot-sales-whatnot-promotion-strategy-expert
- eBay AI bulk card listing tool breaking on item specifics: https://www.valueaddedresource.net/ebay-bulk-ai-listing-sports-cards-broken/

**Biggest risk:** Small card sellers are price-sensitive and run on thin margins, and Whatnot's ad levers are limited (15-minute Boosts). Clients may churn once the first savings are captured. Mitigation: sell the ongoing title and listing work, not only the ad fix.

**Confidence: 7/10.** It uses his existing skill, needs no inventory and no capital, and Claude does most of the work. The open question is willingness to pay in this niche, and 10 free audits answer that within 3 weeks.

---

## arbitrage-2: Attic-to-Auction Collection Buyer

**One-liner:** Use Google Ads and estate-sale partners to buy whole inherited collections from non-collectors at 50-60% of liquid market value. Claude appraises from photos in minutes, and the cards sell through the cheapest exit (Fanatics Collect weekly auctions).

**The hack:**
- **Information arbitrage.** Heirs and estate companies cannot tell a 1989 junk-wax box from a 1950s Mantle. Dealers already exploit this, paying 40-70% of value. But they appraise by hand and slowly, so they cherry-pick big collections.
- **Speed.** Claude triages a 200-photo submission in minutes: identification, a liquid-value estimate, and a junk-wax filter. The user can quote every lead the same day and say "no" to 80% of them in 2 minutes instead of 2 hours.
- **Channel.** Fanatics Collect weekly auctions pay 100% of hammer plus a 2-15% bonus on $50+ cards, against about 15.4% all-in on eBay. That adds 15-20 points of margin over a dealer who lists everything on eBay.
- **Attention.** The user is an ads pro. "Where to sell baseball cards" style searches run about 4,400/mo per variant cluster at $1.20-3.50 CPC, and most local dealers run weak campaigns.

**Why now:**
- Record platform volume means fast liquidity. Whatnot, eBay focus categories (+26%) and Fanatics all report record volume.
- Vintage held at records while modern corrects, so buying old collections is the right side of the cycle.
- The free Fanatics seller subsidy is a land-grab that will not last forever.

**How Claude runs it:**
- Builds the landing page, the photo-submission form and the lead database (Artifact with a db).
- Writes and structures the Google Ads campaigns and negatives. The user launches them; the AdWhispr connector can do the launch with his approval.
- Triages every photo set into an itemized estimate with a liquid value, a junk-wax flag and an offer range. Pricing uses licensed or manual comp sources (PriceCharting API, Card Ladder, 130point lookups), never piped eBay restricted-API data.
- Drafts offers and follow-ups (Gmail drafts).
- Writes the estate-sale-company partner pitch and sequence.
- Writes listings and auction-routing decisions for every card bought.
- Keeps the inventory and P&L ledger.

**User's tasks:**
- Make the final offer call.
- Meet sellers or receive shipped collections; inspect and authenticate.
- Pay sellers.
- Photograph and ship to Fanatics Collect, eBay and Whatnot.
- Hold capital.
- About 12-18 hrs/week.

**First 30 days:**
1. Days 1-7: landing page and submission form live. Run a Google Ads test at $40/day on exact and phrase "sell baseball cards / sports card buyers near me" in the user's metro plus a mail-in national campaign. Set up Fanatics Collect and eBay seller accounts and buy a Card Ladder Pro subscription ($20/mo).
2. Days 7-21: Claude emails 150 estate-sale companies within driving range from EstateSales.net listings (Claude drafts, the user sends from Gmail). The offer: "free same-day card appraisal; we buy or consign; 5% finder's fee to you."
3. Days 21-30: target 25 submissions, 5 qualified, 1-2 purchases capped at $1,500 each. Track CAC, close rate, average value per deal and days to liquidate.
4. Kill switch: if average qualified collection value is under $750 after 40 leads, stop paid ads and keep only the estate-partner channel.

**Path to the goal (real math):**

| Line | Monthly, month 6+ (honest middle) |
|---|---|
| Ad spend | $2,000 → ~830 clicks @ $2.40 → 10% submit = 83 leads |
| Qualified ($750+ liquid value) | 20% = ~17; close 35% = 6 deals |
| Estate-partner deals | 10 active partners → 3 deals/mo |
| Deals | 9/mo, average liquid market value $1,800 |
| Buy price | 55% = $990/deal (≈ $8.9k of capital turning about monthly) |
| Net realization | 85% of market after fees and slippage = $1,530 |
| Gross profit | $540 − $40 shipping/supplies = $500 × 9 = $4,500 |
| Minus ads, finder's fees, tools | −$2,000 − $270 − $100 |
| **Net** | **≈ $2,100/mo, plus tail deals** |

- The tail is the point. About 1 collection in 20 holds pre-1975 stars, and one $15k vintage collection bought at 55% adds about $5k of profit.
- **Honest middle: $2-4k/mo by month 12. Upside $8-12k/mo if the estate channel compounds and vintage lands.**
- Capital needed: $10-15k.

**Evidence:**
- Keyword demand and CPC (Google Keyword Planner via AdWhispr, US, pulled 2026-10-01): "where to sell baseball cards" variants ~4,400/mo each at $1.20-3.50; "sports card buyers" 2,400/mo at $1.16-5.52; "sell sports cards near me" 4,400/mo at $1.38-3.39; "pokemon card buyer near me" 1,300/mo; "baseball card appraisal" 720/mo.
- Dealer buy rates of 40-60% on desirable singles and 20-40% on commons: https://thecardshopfinder.com/faq/what-percentage-of-value-do-card-shops-pay/ ; cash offers of 60-70% from mail-in buyers: https://allvintagecards.com/inherited-baseball-cards/
- Competitors offer free appraisal as the buying hook (Dean's Cards, Heritage, Memory Lane): https://www.deanscards.com/collection-information-form ; https://memorylaneinc.com/sports-card-collection-appraisal
- About 22,000 US estate-sale companies; EstateSales.NET hosts 6,000+ companies and 120k+ sales/yr: https://prospeo.io/c/estatesales-net ; https://www.homelight.com/blog/estate-sale-companies/
- Fanatics Collect auctions pay 100% of hammer plus 2-15% bonus on $50+: https://about.fanatics.live/post/selling-your-sports-cards-quick-easy-way ; FanCash 0% fee: https://www.si.com/collectibles/fanatics-collect-eliminates-seller-fees-new-fancash-payouts-program
- Vintage held up in 2022 while modern fell: https://sportscollectorsdigest.com/news/sports-card-market-values-vintage-cards-modern-pwcc-card-ladder

**Biggest risk:** Most inherited collections are 1986-1994 junk wax worth almost nothing, so CAC per *qualified* lead could double. A second risk is buying a fake or trimmed card (PSA reports altered Pokemon +407%). Mitigation: photo triage first, an offer cap per deal until the numbers prove out, and no ungraded high-dollar vintage without in-hand inspection.

**Confidence: 5/10.** The gap is real and durable and the user's ad skill is a real edge, but the result depends on deal mix and on physical work Claude cannot do.

---

## arbitrage-3: Shop Aged-Inventory Liquidity Desk

**One-liner:** Local card shops have stale singles, slabs and sealed product they never get online. We list, reprice and route it to the cheapest channel under the shop's own seller accounts, and take 10% of proceeds with no upfront fee.

**The hack:**
- **Labor arbitrage.** Shop owners say singles are hard to list, repricing is arduous, and staff time disappears into inventory checks. Their alternatives are expensive and slow:
  - Consignment at 15-40%.
  - COMC: 5% + 10% cash-out + $0.65/card intake, about 16 weeks.
  - An eBay VA at about $1,600/mo.
- **Platform arbitrage.** Claude routes each card to its best-net channel:
  - Fanatics Collect auctions for $50+ sports slabs (0% fee plus bonus).
  - TCGplayer for TCG singles.
  - eBay for the rest.
- Most shops don't run that optimization. Their margin on cards is about 20%, and dead stock earns them 0%.
- We hold no inventory and no capital. The shop ships from its own stock.

**Why now:**
- About 6,894 trading card stores in North America, with flat store growth and closures citing online competition. Owners are looking for online sales without hiring.
- TCGplayer raised fees in 2026 (10.75% commission, Direct changes) and Whatnot cut fees for volume sellers, so channel choice now swings margin by about 9 points.
- No AI-native service exists. Shop software (CardCloud, TCG Sync) is DIY.

**How Claude runs it:**
- Builds a shop intake kit: a phone photo rig guide and a bulk-upload portal (Artifact with a db).
- Identifies and variant-checks each card, prices against licensed comps, produces the TCGplayer/eBay upload CSVs and Fanatics auction submissions, and reprices weekly on a Routine.
- Sends each shop a monthly "aged stock → cash" report and drafts the outreach to shops.

**User's tasks:**
- Walk into local shops and sign them; trust is a face-to-face sale.
- Train shop staff on the photo rig, or photograph stock in person for the first batches.
- Do QA on high-value items.
- Collect fees.
- About 8-12 hrs/week.

**First 30 days:**
1. Visit 15 shops within 60 miles. Offer one free pilot: "we list 300 of your oldest cards; you pay 10% of what sells."
2. Run 2 pilots and measure sell-through, net realized versus the shop's tag prices, and staff time.
3. Turn the pilot data into a one-page case study and pitch 30 more shops by email or phone, regionally first.

**Path to the goal (real math):**
- Per shop: $25k of aged stock listed, 12%/mo sell-through = $3,000 GMV/mo × 10% = $300.
- About half of shops add a $250/mo "run our online store" retainer, so the average is about $425/shop/mo.
- Volume: 4 shops by month 4, 8 by month 8, 12 by month 12. 12 × $425 = **$5.1k/mo at month 12. Honest middle $3-4k/mo** (shop churn, slower sell-through).
- Costs: tools ~$100/mo plus mileage.
- Path past the goal: package it as a regional "online desk" with a VA doing photo intake.

**Evidence:**
- About 6,894 trading card stores in North America (Apr 2026): https://rentechdigital.com/smartscraper/business-report-details/list-of-trading-card-stores-in-north-america
- Shop card margins about 20% after the pandemic: https://vmfsusa.com/blogs/business/pokemon-card-vending-machine-the-complete-2026-operator-guide
- Dealer pain (singles hard to list, repricing arduous): https://winventory.ca/partner/features ; https://tcgsync.com/vendor-only
- Consignment at 25-40% for sports card shops and 15-20% at specialists: https://closo.co/blogs/inventory-liquidation/consignment-cost ; https://pregradecards.com/blog/cardsource-vs-canadian-consignment-2026
- eBay listing VA about $1,600/mo: https://stealthagents.com/ebay-listing-virtual-assistant/
- TCGplayer fees and Direct changes: https://help.tcgplayer.com/hc/en-us/articles/201357836-Fees ; https://seller.tcgplayer.com/blog/simpler-and-more-predictable-fees-coming-for-tcgplayer-direct-june-18
- Shop closures citing online competition: https://www.sportscollectorsdaily.com/tag/sports-card-shop-closing/

**Biggest risk:** The ceiling is small per shop ($300-500/mo), so the business needs 12+ shops, which is a slow local sale. Shops may balk at sharing seller-account access. Aged stock may be aged because it is overpriced, and repricing it lowers the shop's margin, which can sour the relationship.

**Confidence: 5/10.**

---

## Ranking and sequencing (arbitrage view)

1. **Start arbitrage-1 (Ad & Fee-Leak Desk) in week 1.** It needs no capital, it is his existing skill, and paying clients can come within 30 days. It also teaches him who the volume card sellers are.
2. **Fund arbitrage-2 (Collection Buyer) with arbitrage-1 cash flow from month 3,** with a hard cap on capital per deal. The client relationships from arbitrage-1 double as an exit channel: sell bought collections wholesale to client sellers.
3. **arbitrage-3 is optional.** It is a lower-ceiling, local add-on if he enjoys shop relationships.

**What we own when the gaps close:** a client list of volume card sellers, an estate-partner network and lead database, and a proprietary comp and triage dataset. Those survive after AI makes the labor cheap for everyone.

**What I kill:**
- Japan and Cardmarket import arbitrage: the 15% tariff, the end of de minimis, and Apify actors already scanning the spread.
- eBay underpriced-alert bots: free and against eBay's terms.
- Grading flips: PSA Value tiers paused, $59.99-79.99 floor.
- Modern sealed speculation: 15-25% drawdowns.
- Breaks and repacks: lottery lawsuits.
