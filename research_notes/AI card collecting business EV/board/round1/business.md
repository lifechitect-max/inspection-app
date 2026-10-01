# Business Hacker: Round 1 Proposals

**Lens:** How does each customer make us money fast? Who pays us before we pay anyone? What's the recurring piece?

## Napkin read before the ideas

Working assumptions from MISSION: $5k–25k risk capital, 15–25 hrs/week, US-based, can show up in person. Goal: $5k–10k/month profit within 12 months.

**Kill list (the models a solo operator should not run):**
- **Holding modern inventory:** -EV right now. Modern Pokémon sealed and singles are 20–50% off their peaks, and sports indexes are down 2–11% over 12 months (market_size §3).
- **Part-time flipping:** about $7–14/hr before tax (business_models §7).
- **Grading arbitrage:** about -$45/card at PSA Regular $79.99 while the Value tiers are paused (business_models §2).
- **Random breaks:** live gambling and lottery litigation, with about 70 claimants against Whatnot plus an unsealed qui tam suit (risks §3).
- **AI scanner or price-tool SaaS:** commoditized. CollX gets about $2.20/user/yr, and Card Dealer Pro sells for $9–59/month.

All of these models either pay the toll or need capital locked up for months.

**Where the money is:** in the toll booths and the sourcing. Three facts point there:
1. Volume is at records while prices fall. That favors businesses paid on transaction volume, not on price direction.
2. "Buying below market is where the money is." Shops pay 50–60% of market for collections and 10% finder's fees are the hobby norm.
3. The user's unfair edge is **paid acquisition**, which almost no card dealer or show promoter is good at. Google Keyword Planner shows seller-intent card keywords at **$1–5 CPC** with tens of thousands of searches a month (pulled this session; table below).

So all three moves below either get paid first or take a cut, and each uses PPC as the engine. None of them depends on card prices going up.

---

## business-1: Show Runner (monthly local card shows, vendor-prepaid)

**One-liner:** Promote a recurring monthly card show in a hotel ballroom or event hall. Vendors prepay for tables, attendees pay at the door, and the user's ad skill fills the room.

**The hack:** This is a Costco/Dell cash cycle. Vendors pay 100% of table fees **2–6 weeks before** the venue bill is due, so the customer funds the event. The promoter holds no inventory and has no exposure to card prices, only to foot traffic. Most local shows are marketed through Facebook groups and word of mouth. A promoter who can run geo-targeted Meta and Google ads, with a CPC of $1–5 on "card show near me" style intent, draws more attendees than the competition. More attendees bring more vendors, which brings higher table prices and a waitlist. A second edge comes free: the promoter sees every collection that walks through the door. That is a free sourcing channel for business-2.

**Why now:**
- Vendor demand is outrunning supply. Pasadena's Front Row Card Show went from 300 tables (Nov 2024) to 540 (early 2026), and organizers reported a **375-table waitlist**.
- A gym promoter running 125 tables twice a month "turned dealers away every show" and could have sold 150–160.
- The Arizona State Card Show started at **15–20 tables a month in 2018** and filled Chase Field in March 2026.
- Collectibles transaction volume is at all-time highs: Whatnot GMV is roughly doubling, eBay collectibles is its #1 growth driver, and GameStop collectibles is up 57%.

**How Claude runs it:**
- Builds and hosts the show website, vendor application, floor map and ticket page as an Artifact with a shared DB for vendor and attendee lists. Can also use the Higgsfield website builder.
- Scrapes and assembles a vendor prospect list: Whatnot sellers in the metro, local shop owners, and vendors at neighboring shows found through CardShopFinder and TreasureHunter listings. Drafts and sends personalized outreach through Gmail.
- Writes and launches Meta and Google geo campaigns through AdWhispr. Generates show-promo creatives and short videos with Adobe and Higgsfield.
- Runs the reminder sequence for vendors (load-in, rules, payment), posts countdown content, and writes the post-show recap and sponsor one-pager.
- Tracks the P&L and the vendor rebooking rate on a Routine every week.

**User's tasks:**
- Pick the metro and the venue, then sign the venue contract.
- Buy event liability insurance and check the state's sales-tax rules for event organizers. Some states require promoters to collect vendors' seller-permit info.
- Make about 10–15 phone calls to anchor vendors.
- Work show day: door, load-in, problems. Take payment through Stripe or Square.

Estimated load: about 8–10 hrs/week in build-up, 10 hrs on show day.

**First 30 days:**
- Days 1–5: Claude maps every existing show within 60 miles to find dates and gaps. Pick a Sunday that conflicts with no other show. Get quotes from 3 venues (hotel ballroom, VFW or Elks hall, fairground building). Hold the date with a refundable deposit if possible.
- Days 5–15 (**pre-sale test**): offer 40 "Founding Vendor" tables at $75, $25 below the planned $100, prepaid and refundable if the show is canceled. **Go/no-go rule:** 25+ paid tables by day 15 means sign the venue. Fewer means refund everyone and try another metro or date. Cash at risk is about $0–500.
- Days 15–30: launch ads at about $20–30/day for 3 weeks. Post in local Facebook groups and on Reddit. Promote "Free AI collection appraisal at the door" as a crowd driver (this also feeds business-2).
- Run show #1 around week 6–8.

**Path to the goal:**

| Stage | Tables × price | Admission | Revenue | Costs (venue, insurance, ads, staff, fees) | Net/show |
|---|---|---|---|---|---|
| Show #1 | 35 × $80 | 250 × $5 | $4,050 | $1,500 + $200 + $700 + $200 + $250 = $2,850 | **~$1,200** |
| Month 6 (proven show) | 70 × $100 | 450 × $5 + $500 sponsor | $9,750 | $2,500 + $200 + $800 + $400 + $350 = $4,250 | **~$5,500** |
| Month 12 middle (2 shows/mo, avg 55 tables @ $90) | $4,950 | $1,500 | $6,450 each | ~$3,600 each | **~$2,850 × 2 = ~$5,700/mo** |

- **Honest middle outcome:** about $4k–6k/month by month 12 from 2 shows a month (two metros, or one metro twice a month).
- **Upside:** 3–4 shows a month, VIP early-entry tickets ($15–20, which is already standard), sponsor tables (grading companies, Whatnot, local shops), and buying collections at your own door. That gets to $10k+/month.
- **Downside:** one dud show costs about $1–2k, capped by the pre-sale rule.
- **Payback:** the first show is roughly cash-neutral to positive because vendors prepay.

**Evidence:**
- Pasadena Front Row show at 540 tables, nearly double, with a 375-table waitlist: [Pasadena Now](https://www.pasadenanow.com/weekendr/collectibles-convention-returns-to-pasadena-with-record-vendor-lineup/) (search snippet; the page was blocked for full fetch).
- Promoter running 125 tables twice a month, turning dealers away; promoter revenue streams are tables, admission, sponsors and autographs: [SCD "Card Show Boom"](https://sportscollectorsdigest.com/news/card-show-boom-sports-card-shows-continue-to-enjoy-incredible-growth-success-in-hobby); [SCD George Johnson interview, 1,500+ shows](https://sportscollectorsdigest.com/cards/interview-with-show-promoter-george-johnson).
- AZ State Card Show grew from 15–20 tables to Chase Field: [Cronkite News, 2026-03-17](https://cronkitenews.azpbs.org/2026/03/17/asu-alumnus-grows-arizona-state-card-show/).
- Typical 2026 hotel shows have 100–130 tables with $5 or free admission (Honolulu, San Diego, Tucson): [CardShopFinder Tucson](https://thecardshopfinder.com/event/tucson-card-vault-ii-tucson-2026-09/); [CardShopFinder San Diego](https://thecardshopfinder.com/event/collectors-corner-card-show-san-diego-2026-10/); [TreasureHunter Honolulu](https://www.treasurehunter.show/show/pokemon-sports-cards-more-honolulu-hi-2026-09-27).
- Table fees: $75–200 at regional shows, $40 at a small NJ show, $125–175 in 2026 listings: [CardShopFinder sell at shows](https://thecardshopfinder.com/guides/card-shows/sell-at-card-shows/); [Mercer County NJ](https://visit.mercercountynj.gov/event/hightstowns-sports-card-collectibles-show/).
- Venue costs: Dallas hotel ballrooms $600–2,500/day, a municipal 5,000 sq ft ballroom $350/day: [Tagvenue Dallas](https://tagvenue.com/us/hire/hotel-ballrooms/dallas); [City of Houghton rates](https://www.cityofhoughton.com/wp-content/uploads/2026/08/Ballroom-Rates.pdf).
- A card-show business with brand, database and venue relationships is listed at a $120k ask on $72k revenue, which shows these businesses carry real resale value: [BizQuest listing](https://www.bizquest.com/business-for-sale/high-margin-collectibles-and-promotions-business-with-seller-support/BW2533161/).

**Biggest risk:** a crowded local calendar or an established promoter who retaliates by booking the same weekend, and a hobby downturn shrinking the vendor pool. The pre-sale go/no-go and Claude's competitor-calendar map keep the downside to a few hundred dollars.

**Confidence: 7/10**

---

## business-2: The Collection Desk (PPC seller funnel: buy, consign or refer every lead)

**One-liner:** Run Google and Meta ads to people who want to sell a collection. Claude triages the photos within an hour. The user then buys the best collections outright, consigns the high-end vintage for a commission, and refers the rest to partner shops for a 10% finder's fee, so every lead gets monetized.

**The hack:** In this hobby the money is made at the buy, not the sell. Shops pay 50–60% of market, and offers on the same collection differ by 30–50%. Most dealers source passively at shows and walk-ins. The user can buy **seller intent** on Google for $1–5 a click, and almost no card dealer runs disciplined PPC. Claude removes the expensive part of the buy desk, which is appraisal labor. It reads photos, identifies era and set (and filters out junk wax), pulls comps from non-restricted sources, and writes a tiered offer. Monetizing all three outcomes (buy, consign, refer) means even leads you don't want still pay for themselves. That is client-financed acquisition: the referral and consignment revenue covers the ad spend, and outright buys are the profit.

**Why now:**
- Seller-intent search volume is large and cheap. Live Keyword Planner data from this session:

| Keyword | Searches/mo | CPC (top of page) |
|---|---|---|
| sell pokemon cards near me | 8,100 | $1.34–4.48 |
| sell sports cards near me | 4,400 | $1.38–3.39 |
| sell baseball cards near me | 4,400 | $1.38–3.39 |
| sports card buyers | 2,400 | $1.16–5.52 |
| places that buy pokemon cards near me | 2,400 | $1.40–4.18 |
| best place to sell sports cards | 1,600 | $1.53–4.11 |
| baseball card buyers near me | 1,600 | $0.74–2.94 |
| baseball card appraisal | 720 | $1.08–3.25 |

  Plus dozens more long-tail terms; roughly 25k–40k seller-intent searches/month in the US after deduping close variants.
- The boomer and Gen-X wealth transfer is under way. Inherited-collection guides say value is concentrated in about 20 cards, and selling whole returns 40–60% of sorted retail. That gap is the profit pool.
- Exit channels are at record liquidity (Whatnot $8B+ in H1 2026). Low-fee exits exist: Fanatics Collect at 6%, Courtyard at 0%, Whatnot down to 6–7.75% at tier.

**How Claude runs it:**
- Builds the landing pages ("Get a free AI appraisal + cash offer in 24 hrs," with separate Pokémon, sports-vintage and inherited-collection variants) and a photo-upload intake form backed by an Artifact DB.
- Writes and launches Google Search plus Meta campaigns through AdWhispr, and runs negative-keyword and bid hygiene weekly. This is the user's Amazon PPC skill applied directly.
- **Triage within an hour:** vision ID of era, set, key cards and condition flags, then a junk-wax filter, a value band, and a recommended route (buy / consign / refer / decline politely). Drafts the offer email and follow-ups.
- Builds the partner-shop network: researches and emails 20–40 shops and dealers nationwide to sign a 10% finder's-fee agreement, routes referred leads, and tracks payouts.
- For bought inventory: writes the listings, sets the channel plan (Whatnot vs. Fanatics Collect vs. eBay), preps Whatnot show run-sheets, and keeps a weekly cash-conversion report.
- Compliance stays human-in-the-loop: no auto-buying, and no eBay restricted-API data goes into the LLM.

**User's tasks:**
- Fund and approve every buy (target: pay ≤55% of market).
- Handle local pickups and in-person meetings for big collections.
- Receive mail-ins (prepaid insured labels), photograph cards, ship sales.
- Sign partner-shop agreements.

Estimated load: about 10–15 hrs/week.

**First 30 days:**
- Days 1–7: Claude builds the landing pages, intake and triage pipeline. The user sets up Google Ads and Meta accounts. Start with a **$40/day test**, split 60/40 between the local metro (pickup) and national mail-in for vintage only.
- Days 7–21: Claude signs 10+ partner shops (the 10% finder's-fee template) so that day-one leads have a home. Reach target: 40–60 photo submissions.
- Days 21–30: complete 2–4 outright buys, 1–2 consignment intakes and 5+ referrals. **Kill or scale metric:** cost per *qualified* lead (est. market ≥$500, not junk wax) under $150, and an average qualified market value of $2,000 or more.

**Path to the goal (month 12 middle case, $3,000/month ad spend):**
- At $3 CPC and 7% landing conversion, cost per submission is about $43. About 25% qualify, so a qualified lead costs about $170. That gives about 18 qualified leads a month, plus about 10 free ones from shows and SEO, for ~28 total.
- Route by outcome:

| Route | Share of 28 leads | Economics | Monthly gross profit |
|---|---|---|---|
| Buy | 30% → ~8 buys | $2,500 avg market, pay 55% ($1,375), net 82% after fees/haircuts ($2,050) → $675 each | **~$5,400** |
| Consign | 15% → ~4 | $3,000 avg sale, 18% commission | **~$2,150** |
| Refer | 25% → ~7, half close | Shop pays ~$1,200; 10% fee = $120 each | **~$420** |
| **Total** | | | **~$7,950** |

- Less $3,000 ads and about $300 supplies, shipping labels and tools leaves **≈ $4,650/month profit**.
- Working capital: about $11k in buys a month, turning in about 30–45 days (Whatnot/Fanatics sell-through), so **$12–15k revolving**.
- **Honest middle:** $3k–5k/month by month 12.
- **Upside:** the heavy tail. One $20k vintage estate at 55% clears $5k+ in a single deal.
- **Downside:** leads skew to junk wax and kids' Pokémon binders, cost per qualified lead runs over $300, and the desk ends up roughly break-even, which you'd see in month 1–2 for about $1.5k of ad spend.

**Evidence:**
- Shops pay 50–60% of market for collections (vintage 50–60%, slabs 60–80%), and offers vary 30–50%: [CardShopFinder: what % shops pay](https://thecardshopfinder.com/faq/what-percentage-of-value-do-card-shops-pay/).
- 10% finder's fees are standard (Invest In Baseball on six-figure collections; OTIA 10% up to $100k): [Cardboard Connection](https://www.cardboardconnection.com/invest-baseball-100k-finders-fee); [OTIA FAQ](https://otia.com/faq).
- Consignment commissions: 15–25% at local shops for high-value items, 5–10% at PWCC-type houses: [PreGradeCards consignment comparison](https://pregradecards.com/blog/cardsource-vs-canadian-consignment-2026).
- Inherited collections: value concentrates in about 20 cards, whole-sale returns 40–60% of sorted retail, and junk wax (1981–94) is near bulk value: [AllVintageCards](https://allvintagecards.com/inherited-baseball-cards/); [Estimonia](https://estimonia.com/blog/inherited-baseball-card-collection-what-to-do).
- Keyword volumes and CPCs: Google Keyword Planner via AdWhispr, pulled 2026-10-01 (table above).
- Exit fees: Fanatics Collect 6%, Courtyard 0%, Whatnot tiered 6–8% from 2026-09-21: [Fanatics Collect fees](https://support.fanaticscollect.com/en_us/buy-now-fees-ry33QCXaxe.md); [Tubefilter](https://www.tubefilter.com/2026/09/17/whatnot-new-commission-rates-lower-three-percent/).

**Biggest risk:** lead quality. Most "sell my cards" searchers hold low-value modern or junk-wax cards, which pushes cost per qualified lead past the math. Mitigations: the photo-first gate, vintage-only national targeting, and refer-out economics on the rest. A secondary risk is buying fakes or altered cards. Policy: no unslabbed high-end Pokémon buys, verify slab certs, and get a dealer second opinion on anything over $1k.

**Confidence: 6/10**

---

## business-3: Whatnot Growth Desk (an Amazon PPC playbook for card sellers' live shows)

**One-liner:** A productized monthly retainer for mid-size Whatnot card sellers ($15k–100k per 4 weeks). It covers Boosted Livestream bidding, off-platform Meta and TikTok traffic to shows, and a daily short-form clip machine. Prepaid monthly, with Claude doing about 80% of the delivery.

**The hack:** Whatnot only recently launched seller ads (Boosted Livestreams, bid in 15-minute slots). Whatnot is hiring ads PMs and engineers focused on seller ROAS. Searches for third-party Whatnot ads managers turn up essentially nobody, just a few Fiverr "promote your livestream" gigs. This looks like Amazon PPC in 2015: a new auction, sellers who don't know how to bid, and no agencies yet. The user already sells Amazon PPC management on Upwork. The skill transfers directly, and the vertical is the hottest one on the platform: cards are the majority of Whatnot's GMV.

**Why now:**
- Whatnot GMV went from $8B+ in 2025 to $8B+ in **H1 2026 alone**, at a $20B valuation (Aug 2026).
- A new tiered commission (Sept 21, 2026) rewards sellers who cross volume thresholds: 8% drops toward 6–6.75%. Every seller near a tier line now has a measurable reason to buy growth.
- Ads already raise Whatnot's effective take to about 12.5% of GMV, so sellers are already spending. Whatnot touts about 30% ROI on Boost.
- Whatnot has launched a Seller API and seller permissions, which allows reporting without password sharing.

**How Claude runs it:**
- Builds each client's weekly dashboard from Seller Hub and API exports: show-level GMV, viewers, boost spend, cost per new buyer and repeat rate. Writes the bid plan by time slot and category.
- Builds and launches off-platform Meta and TikTok campaigns to the show link through AdWhispr, plus retargeting.
- Cuts stream VODs into 5–10 clips a week, captions them and schedules them through Higgsfield TikTok publishing.
- Writes show titles, thumbnails, giveaway mechanics (compliant, not random-break lotteries) and run-of-show scripts.
- Prospects sellers by watching category feeds and drafts outreach. Writes the case studies.

**User's tasks:**
- Sales calls and onboarding.
- Click-execution inside client accounts where the API doesn't reach, using delegated team access only.
- Quality-check Claude's weekly reports.

Estimated load: about 1.5–2 hrs/client/week.

**First 30 days:**
- Week 1: Claude studies the top 50 card sellers' show cadence and boost usage and builds a "Whatnot Ads Audit" template.
- Week 2: offer **3 free audits plus a 30-day pilot at $500 prepaid** to sellers found through Whatnot, Instagram and Discord. Also post it as a productized offer on Upwork, the user's home turf.
- Weeks 3–4: run the pilots and publish one before/after case study (viewers, GMV and cost per new buyer).
- **Go/no-go:** 2 of 3 pilots convert to $1,000/month retainers.

**Path to the goal:**
- Price: $1,000/month (3-month minimum, first month prepaid), or $750 plus 3% of GMV above baseline. Claude-side delivery cost is about $50–100 per client.
- Volume: 6 clients by month 6 and 8–10 by month 12, at about 10% monthly churn.
- **Middle case at month 12:** 8 clients × $1,000 = **$8,000/month at about 90% margin, ≈ $7,000 profit**, with about 15 hrs/week of user time.
- **Honest middle, after slower sales:** 5–6 clients, about $5k/month.
- Value check for the client: a seller doing $50k per 4 weeks at about 15–20% margin needs about a 15% GMV lift to clear a $1,000 fee. That is plausible with boost plus outside traffic, but each client must be proven.

**Evidence:**
- Whatnot Boosted Livestreams launched as an auction for 15-minute featured slots, with ROAS metrics in Seller Hub: [Value Added Resource](https://www.valueaddedresource.net/whatnot-launches-ads-with-boosted-livestreams/).
- Ads push effective take to about 12.5% of GMV: [Sacra](https://sacra.com/chat/h/22ee3b40-9f9a-4b1a-9595-37cc6887ba7c/).
- About 30% Boost ROI touted, plus seller permissions: [Sacra seller OS](https://sacra.com/chat/h/68577c91-82ba-4359-aa1d-b54c64204b63).
- Seller API: [VAR](https://valueaddedresource.net/whatnot-launches-selling-api-improved-discovery-and-referral-codes).
- Whatnot hiring ads PMs focused on seller ROAS: [Built In job post](https://builtincharlotte.com/job/product-manager-ads-promo/8226967).
- Whatnot $8B+ GMV in H1 2026, $20B valuation: [Inc.](https://www.inc.com/jennifer-conrad/whatnot-just-clinched-a-20-billion-valuation/91386777).
- Tiered commission from Sept 21, 2026: [Tubefilter](https://www.tubefilter.com/2026/09/17/whatnot-new-commission-rates-lower-three-percent/).
- Seller base: 500+ sellers at $1M+ annualized (Whatnot self-reported): [ecommercebonsai](https://ecommercebonsai.com/whatnot-statistics/).
- An agency pricing comp: TikTok Shop's own managed service runs $10k flat + 10–20% commission: [FiveX](https://fivex.com/blog/tiktok-shop-agency-pricing-profit-control/).
- Demand signal: a Fiverr "promote your Whatnot livestream" gig exists: [Fiverr](https://br.fiverr.com/ikeoluwha/be-whatnot-social-media-manager-for-live-stream).

**Biggest risk:** Whatnot could commoditize its own ads (auto-boost, in-house account managers for top sellers), and live sellers have thin margins and churn fast. This is the most "agency-like" of the three. It wins only because the user's existing skill transfers and the platform's ad product is new.

**Confidence: 5/10**

---

## Considered and parked
- **Buying a retiring owner's card shop with seller financing.** This is a classic buy-don't-build play. Listings show $123k SDE on $866k revenue, $330k SDE on $1M, and owner financing offered. But asking prices run $80k–375k, the shop needs a manager, and Claude gives little leverage. It becomes a Year-2 option once show and desk cash flow exists. ([BizQuest listings](https://www.bizquest.com/business-for-sale/profitable-retail-sports-card-and-collectibles-store-866k-revenue/BW2478694/); [retiring owners, Santa Maria Times](https://santamariatimes.com/news/local/sportscard-fantasys-ending-game-after-32-years-closing-sale-underway/article_062071b7-c2f9-4428-8d68-3cbce5a8936f.html))
- **AI listing service for dealers.** Killed. Card Dealer Pro does it for $9–59/month, so there is no pricing power.

## Synergy (if the board stacks them)
Show Runner (1) is a free lead source for the Collection Desk (2): "Bring your collection: free AI appraisal at the door." The desk's inventory can then sell at your own shows and on Whatnot. Run 1 + 2 together in one metro, and add 3 only if the user wants a no-inventory service income.

## Overall verdict
**Conditional yes.** The card hobby is -EV for this user as an *inventory or speculation* business:
- Modern product is in a 20–50% drawdown.
- Grading arbitrage is closed while PSA's cheap tiers are paused.
- Flipping pays about $7–14/hr.
- Breaks carry gambling litigation.

It is +EV as a *toll-booth and sourcing* business, where the user's paid-acquisition skill is the edge: vendors prepaying for show tables, a take rate on every collection lead, and retainers from sellers. The honest middle outcome is about $5k/month profit by month 12 from Show Runner plus the Collection Desk, with $10k+ possible if a second show metro or a big estate buy lands.
