# Round 1: Marketing Hacker proposals

Lens: what offer makes saying no feel stupid? Where is attention cheapest, and who pays without checking comps?

Date: 2026-10-01. Inputs: MISSION.md, the four research notes, plus my own searches. Keyword volume and CPC numbers below come from live Google Keyword Planner data pulled through AdWhispr this session (US, search only).

---

## The insight behind all three moves

The research notes agree that card *trading* is a toll road. eBay, Whatnot, PSA and Fanatics take 6–16% plus grading fees. Prices for modern product are efficient and falling, and a part-time flipper makes about $7–14/hour. The same notes also say the one variable that matters most is **buying below market**: "Buying cheaper (at 50–60% of market, from collections or estate buys) matters much more than which channel you sell on. That is where the money is."

My read as the marketing hacker: the user's edge isn't card knowledge, which he lacks. His edge is **paid customer acquisition** (Amazon PPC, ads, marketplaces), and Claude can multiply it. Hobbyists trading with hobbyists leaves no spread. **Non-hobbyists** do leave a spread:
- **Non-hobbyist sellers**: heirs, parents and ex-collectors who don't know what their cards are worth and want speed, safety and fairness more than the top price.
- **Non-hobbyist buyers**: gift givers who pay for meaning, not comps.

Attention on the seller side is cheap. Live Keyword Planner data puts seller-intent card searches at **$1–5 CPC with Low-to-Medium competition** (table in marketing-1). That's cheap compared with junk-car or "we buy houses" leads at $50–244 per lead. So the moves sit where the knowledge gap is, and they buy attention that hobby dealers aren't buying well.

---

## marketing-1: "Attic Money" (AI-triaged collection-buying engine)

**One-liner:** A local "we buy card collections" brand. Paid search plus a free AI photo estimate brings non-hobbyists who want to sell, and the user buys at 40–55% of resale value and resells through the cheapest channels.

**The hack (unfair insight):**
- Every dealer says the money is made on the buy. Almost none of them market the buy side well. They wait for walk-ins and word of mouth.
- Seller-intent searches cost $1–5 a click, and nobody frames the buyer's real fear: "I'll get ripped off because I don't know what I have."
- The offer the market is missing is **radical transparency as the closer**. "Send photos. In 24 hours you get a free AI-assisted estimate showing *what every key card actually sold for*. Then we make a cash offer and show the math. Take it, or keep the report free. Prefer more money and no speed? We'll consign it instead."
- This is Schlitz's steam-cleaned bottles: every honest dealer already does the comps math, but nobody puts it in the ad. Show it first and you own "the dealer who shows you the receipts."
- The AI photo triage also solves the category's biggest cost, which is wasted trips to look at worthless junk-wax collections. Claude screens the photos first, so the user only drives to deals that are worth it.

**Why now:**
- Record transaction volume means resale liquidity is high. Whatnot did $8B+ in H1 2026, eBay focus categories are +26%, and cards are eBay's #1 growth driver.
- The Pokémon 30th anniversary (Sept 2026 sellouts, mainstream press) is reminding millions of 30–40-year-olds that their childhood binders might be worth something. 19% of US adults bought Pokémon cards in a 6-month window.
- The boomer estate wave puts sports collections on the market every week. EstateSales.net reportedly lists about 75,000 sales a week, and roughly 10–22k estate-sale companies operate in the US.
- PSA's Value-tier pause and backlog push more sellers to sell raw now rather than grade first.
- Buying-side transaction businesses earn on volume regardless of price direction. Inventory turns in weeks, so the user isn't speculating.

**How Claude runs it (most of the work):**
- Builds the site and "Free Card Estimate" funnel: a photo-upload form, an AI first-pass identification (set, year, key cards, junk-wax flag) and a lead database. Publishes it as a hosted page with a shared DB.
- Writes 50+ Google Search ad variants and RSA assets on the keyword clusters below, plus Meta ads aimed at "inherited / cleaning out the attic / parents' house" audiences. Launches and manages them through AdWhispr (the user approves the budget).
- Triages every lead within hours. It identifies cards from photos, pulls comps from compliant sources (130point and manual sold checks, never eBay restricted-API data piped into an LLM), estimates resale value, and drafts the offer letter with the math shown.
- Drafts all follow-ups (Gmail), books appointments (Calendar), and writes the "estimate report" PDF each seller receives. That report is the proof asset.
- After purchase it writes listings and titles, picks the channel (Fanatics Collect 0–6%, Whatnot, eBay, COMC for bulk singles, bulk lots for junk), and keeps the P&L dashboard.
- Mines Reddit, forum and review language ("I don't want to get ripped off", "my dad's cards") for ad copy. On a weekly Routine it checks CPC and lead quality and rewrites losing ads.

**User's tasks:**
- Set up the accounts (Google Ads, Meta, business entity, payment method), approve ad budgets and fund purchases.
- Take calls and visits and close deals in person, or handle mail-ins.
- Do the physical work: sort, photograph, ship and pack.
- Learn enough to spot vintage keys and fakes, with Claude's cheat sheets. Use PSA/CGC cert lookups on every slab bought.

**First 30 days:**
1. Days 1–3: Claude builds the landing page, estimate form and offer-letter template. The user sets up Google Ads in a 25–40 mile radius.
2. Days 3–7: launch $30/day of Google Search spend on "sell baseball cards near me / where to sell my pokemon cards / sports card appraisal near me". Add Google Business Profile, Nextdoor and Facebook groups. Claude sends personal outreach to 30 local estate-sale companies and 10 estate attorneys offering a free "card check" for their clients (a referral channel).
3. Days 7–30: target 40–60 leads, 8–12 qualified, 3–5 closed buys. Each buy is a $300–2,000 test, capped at $5k total deployed in month 1.
4. Kill or iterate: if cost per *qualified* lead is above $120 after $900 of spend, rewrite the offer and the geo before scaling.

**Path to the goal (real math):**

| Input | Assumption | Basis |
|---|---|---|
| Blended CPC | $2.50 | Keyword Planner seller-intent range $1.0–5.2 |
| Click → submitted lead | 10% | Photo-upload form; conservative |
| Cost per lead | $25 | calc |
| Lead → worth buying ($300+ resale) | 25% | Lots of junk wax; triage filters it out |
| Qualified → closed | 40% | Transparent offer; competitor Card Conduit pays ~70% of market by mail, so the local pitch has to be speed, cash and trust |
| Leads per closed deal | 10 → **ad CAC ≈ $250/deal**, blended about $175 once referrals and organic search kick in | calc |
| Avg resale value per deal | $2,500 | mix of Pokémon binders, vintage sports lots, graded slabs |
| Buy price | 45% = $1,125 | Shops pay 50–70% of market for in-demand modern singles and 25–50% cash on buylists |
| Realized net after fees, shipping and unsold residue | 78% of resale = $1,950 | Fanatics Collect/Whatnot mix about 8–11% fees; bulk drag |
| **Gross profit per deal** | **$825 − $175 CAC ≈ $650** | calc |

- **To reach $7.5k/month:** about 12 deals/month. Ad spend is about $2.1k/month and working capital is about $15–20k with 4–6 week turns. Labor is about 6–8 hrs per deal, so roughly 20–24 hrs/week with Claude doing the listing and comps work.
- **Honest middle outcome:**
  - Months 1–3: 3–6 deals/month, roughly $1.5–3.5k/month profit, with mistakes and a learning tax.
  - Months 6–12: 8–12 deals/month, **$5–7.5k/month**.
  - Upside: a single vintage find (a 1950s–60s Hall of Famer, a WOTC holo binder) can pay for a quarter, but don't plan around it.
- **Path past $10k:** expand the radius to mail-in nationally (the same funnel) and sell the overflow leads to partner shops (marketing-3).

**Evidence:**
- Keyword Planner via AdWhispr, US, pulled 2026-10-01:
  - "sell pokemon cards near me" 8,100/mo, Low competition, $1.34–4.48
  - "where to sell my baseball cards" 4,400, $1.20–3.50
  - "sell sports cards near me" 4,400, $1.38–3.39
  - "where should i sell my pokemon cards" 2,900, $1.27–3.91
  - "sports card buyers" 2,400, $1.16–5.52
  - "who buys sports cards near me" 2,400, Low, $1.03–3.53
  - "baseball card appraisal" 720, $1.08–3.25
- Competitor benchmark, Card Conduit mail-in buyer: about 70% of TCGplayer market, about 3-week process. https://cardconduit.com/reviews/2DA0-3M
- Shop buy rates: 50–70% of market for in-demand singles; buylists 25–50% cash. https://tcgsync.com/glossary/buylist ; https://www.elitefourum.com/t/selling-to-a-lgs/44871
- "Be a buyer": a shop owner urges marketing the buy side, and callers who "simply want to unload… often older material" are ready to deal. https://www.sportscollectorsdaily.com/be-a-buyer-shop-owner-urges-tenacity-marketing/
- Inherited-collection demand content and attic-find stories. https://allvintagecards.com/inherited-baseball-cards/ ; https://www.fox5vegas.com/2023/12/28/man-finds-600-rarest-century-old-baseball-cards-late-fathers-closet
- Junk-wax reality (lead-quality risk): 1986–93 base cards sell for 1–10 cents. https://www.deseret.com/sports/2022/8/29/23326810/what-are-my-junk-wax-era-baseball-cards-worth/
- Estate-sale scale. https://gitnux.org/estate-sale-industry-statistics/ ; https://www.homelight.com/blog/estate-sale-companies/
- Buying below market is the profit driver, plus fee math: business_models_unit_economics.md §1 and §7.
- Cost-per-lead comparison (junk removal $50–75+, real estate $25–100). https://thevalleymarketinggroup.com/blog/junk-removal-google-ads-cost-per-lead-2026/ ; https://clicksgeek.com/?p=17340

**Biggest risk:** Lead quality. Most "my dad's cards" are worthless junk wax, and the user could overpay on the cards that do matter because he lacks expertise (fakes, trimmed vintage, wrong parallels). A buy-price cap, cert checks and Claude's pre-visit triage are mandatory.

**Confidence: 7/10**

---

## marketing-2: "The Card From Their Childhood" (non-random, personalized graded-card gift)

**One-liner:** A gift brand that sells a real, graded card of the recipient's favorite original-151 Pokémon (or their childhood sports hero), in a premium display box with a personal story card. Priced on meaning ($89–$249), not on comps.

**The hack:**
- This is Halbert's coat-of-arms letter for cards: personalization makes a $25 object a $99 gift.
- Gift buyers (partners, parents, friends of 30-somethings) don't check 130point. A PSA 8 1999 Base Set common costs about $20–55 on eBay. To a gift buyer, "an authentic, professionally graded 1999 card of *his* Pokémon, in a display box with a note about why it matters" is worth $99+.
- This is not a mystery box. The buyer picks the exact card, which avoids the randomized-product gambling scrutiny now hitting breakers and mystery slabs.

**Why now:**
- The Pokémon 30th anniversary is in the mainstream news right now, and Q4 gifting starts in weeks.
- 19% of US adults bought Pokémon cards for themselves in 6 months. Adults 18+ are the fastest-growing toy buyers.
- Retail sellouts (30th Celebration gone in minutes, Target 2-per-SKU limits) mean a gift buyer *can't* walk into Target and buy the thing. A curated, guaranteed-in-stock gift solves that.
- Mystery graded-slab gifts already sell at Best Buy (Cosmic Slabs), which proves non-hobbyists buy graded slabs as gifts. Our version is chosen, not random.

**How Claude runs it:**
- Builds the storefront and quiz ("Which Pokémon did they love at 8 years old?").
- Writes per-order story cards (personalized, about 150 words) and product copy.
- Generates ad creative: unboxing-style images and video via Higgsfield/Adobe, 50 hooks per angle ("Don't buy him a pack. Buy him his childhood.").
- Launches and optimizes Meta/TikTok through AdWhispr.
- Maintains the "buy-on-order" sourcing sheet (cheapest graded copy per Pokémon, refreshed weekly) and drafts customer-service replies.

**User's tasks:**
- Set up the store and payments.
- Buy each card when an order lands (human-placed purchase on eBay/TCGplayer).
- Pre-buy about 30 top-seller SKUs (Pikachu, Charmander, Squirtle, Bulbasaur, Eevee, Gengar and others) for Q4.
- Pack the gift boxes, ship, and handle returns.
- Do a trademark-safe brand review: no Pokémon logos or names in the brand, only factual description of genuine product.

**First 30 days:**
1. Week 1: source 30 PSA/CGC graded vintage commons and uncommons ($20–55 each, about $1,000) and 50 premium boxes. Claude builds the store, quiz and 20 creatives.
2. Week 2: put $50/day on Meta with 3 angles (nostalgia, "sold out everywhere," "the gift he'll actually keep"). Run a parallel Etsy listing set.
3. Weeks 3–4: keep the angle with CAC under $35 and kill the rest. Prepare Black Friday / Christmas bundles.
4. Kill test: if blended CAC is above $45 at a $99 AOV after $1,500 of spend, stop. Keep the inventory, which resells near cost.

**Path to the goal:**
- Per $109 average order:
  - Card $35 + box and print $8 + shipping $7 + payment fees $4 = $54 COGS, leaving **$55 gross margin**.
  - Meta median e-commerce cost per purchase is about $38 (lifestyle about $30), giving **about $17–25 net per paid order**. With referrals and organic short-form video, blended CAC of about $25 gives **about $30/order**.
- **To reach $7.5k/month:** about 250 orders/month at a $30 net, which is unlikely outside Q4.
- **Honest middle outcome:**
  - Q4 2026: 300–600 orders total, $6–15k profit for the quarter.
  - Off-season: $1–2.5k/month, with Valentine's Day and Father's Day spikes (the sports-hero version).
  - Annualized that's about **$2–4k/month average**. It's a good seasonal side brand, not the core business.

**Evidence:**
- PSA 8 Base Set commons around $20–55. https://ebay.com/b/Pokemon-TCG-Professional-Sports-Authenticator-PSA-Base-Set-Grade-8-Individual-Collectible-Card-Game-Cards/183454/bn_93430718 ; https://www.pokeprices.io/set/Base%20Set/card/pikachu-1999-2000-58
- Mystery graded slabs sold as gifts at Best Buy. https://www.bestbuy.ca/en-ca/product/cosmic-slabs-lite-pack/19630887
- Keyword Planner via AdWhispr: "pokémon gifts for adults" 1,300/mo at $0.37–2.64; "gifts for pokemon lovers" 590; "pokemon card frame" 1,300 at $0.26–0.61; "graded card display case" 1,300. Gift search volume is small, which tells us this is a social-discovery (Meta/TikTok) play, not search.
- Meta e-commerce median cost per purchase about $38 (Triple Whale, about 35k brands); lifestyle about $30. https://influee.co/blog/how-much-do-facebook-ads-cost
- Adult Pokémon buyers 19%. https://www.retailbrew.com/stories/2025/06/06/collectible-trading-cards-and-adults-drive-toy-sales-in-2025-circana
- 30th Celebration sellouts and limits: market_size_and_cycle.md §2.

**Biggest risk:** Paid-social CAC eats a $55 margin, and the offer may be too easy to copy. There's also IP and ad-policy friction from Pokémon trademarks in ads, so creative has to describe the product, not brand it.

**Confidence: 4/10**

---

## marketing-3: "Seller Pipeline for Card Shops" (pay-per-qualified-seller lead engine, no inventory)

**One-liner:** Run the marketing-1 funnel *for* local card shops and dealers. They pay only for qualified, photo-verified collection sellers delivered to their door, so the user never holds inventory.

**The hack:**
- Shops need **supply**, not more buyers. Every Whatnot seller and shop competes for the same sealed allocation, while the free margin sits in collections walking in the door.
- Shop owners are hobbyists, not marketers. Most have never run a "we buy" search campaign.
- The user's day job *is* PPC, and Claude can stamp out a branded funnel per shop in an hour.
- Risk-reversal offer: "**You pay $75 only when a seller with photos of a collection worth $300+ books a visit. No retainer, no contract. The first 3 are free.**" Saying no means turning down free inventory.

**Why now:**
- Record volumes mean shops can flip whatever they buy.
- The cheap-PSA-tier pause and modern sealed price drops make sealed product less profitable for shops, so collection buys are the margin.
- Thousands of shops opened in the 2020–26 boom (TheCardShopFinder alone lists about 1,500 across 50 states and adds more weekly).
- Seller-intent CPCs are still $1–5. Lead-gen pricing in other local verticals runs $25–244 per lead, so $75 for a seller who could hand the shop $500–1,000 of gross profit is easy to justify.

**How Claude runs it:**
- Builds one national brand ("sell your cards near you") with geo pages per partner shop, plus the AI photo-triage form from marketing-1.
- Writes and launches geo-fenced Google and Meta campaigns per territory.
- Scores every lead: identifies cards, estimates value, flags junk wax.
- Routes qualified leads to the shop by email or SMS with photos and an estimate sheet, and logs billing in a shared DB dashboard each shop can see.
- Prospects shops: builds a list of shops from directories and Google Maps (by hand or with compliant tools), writes personalized outreach in the user's voice (Gmail drafts), and drafts the one-page offer and a weekly results report per shop.

**User's tasks:**
- Sales calls and closing shops (phone or in person at local shows).
- Approve ad spend and billing setup, and handle disputes ("that lead didn't show").
- Run the first territory personally for proof, ideally his own area, combined with marketing-1. Out-of-area or oversized leads become the inventory for this business.

**First 30 days:**
1. Week 1: Claude builds the funnel and a 200-shop target list. The user calls 30 shops within 2 hours of home.
2. Week 2: sign 2–3 pilot shops on "3 free qualified sellers." Run $20/day per territory.
3. Weeks 3–4: deliver about 10 qualified sellers per pilot shop, gather a testimonial and an "X bought $Y of cards from our leads" proof stack, then convert to paid at $75/qualified seller (or $1,000/month flat for 15).
4. Kill test: if no pilot shop converts to paid by day 45, fold the engine into marketing-1 only.

**Path to the goal:**
- Cost per qualified seller: $25 cost per lead ÷ about 40% qualified (lower bar: $300+ value, shop-verified) ≈ **$60–65**. At $75 that's thin. At **$100 per qualified seller**, or a $1,200/month retainer for about 15 sellers plus ad pass-through, margin is about $35–40 per lead or about $500–700/month per shop on the retainer.
- **To reach $7.5k/month:** about 12–15 retained shops, which is realistic by month 9–12 if churn stays under 5%/month.
- **Honest middle outcome:** 5–8 shops by month 6 → $3–5k/month. By month 12: 8–12 shops → **$5–8k/month**.
- Very little capital is needed: a few hundred dollars of float on ad spend, then shops prepay.
- **Ceiling:** shops are small and price-sensitive and churn on slow months. That caps it around $10–15k/month for a solo operator unless it becomes a self-serve platform.

**Evidence:**
- Shop directory size, about 1,500 listed across 50 states. https://www.thecardshopfinder.com/ ; https://thecardshopfinder.com/about/
- Shops actively want collections, and buying drives traffic. https://thecardshopfinder.com/faq/do-card-shops-buy-collections/ ; https://www.sportscollectorsdaily.com/be-a-buyer-shop-owner-urges-tenacity-marketing/
- Local lead-gen pricing benchmarks: local services $10–40 shared, exclusive 2–5x; junk removal $50–75. https://clicksgeek.com/?p=17340 ; https://thevalleymarketinggroup.com/blog/junk-removal-google-ads-cost-per-lead-2026/
- Seller-intent CPC data: see the marketing-1 table (Keyword Planner via AdWhispr).
- The agency space for card shops is thin and generic (e.g., LYFE Marketing ran Shopping ads for one shop). Nobody found sells *supply-side* lead gen. https://www.lyfemarketing.com/portfolio-posts/just-rip-it/
- Card shop margins: cards are about 20% while accessories are 65–70%, so a collection buy at 50% of market is the shop's best margin line. business_models_unit_economics.md §4.

**Biggest risk:** Selling to small, cash-tight shop owners is slow and high-touch, and lead-quality disputes ("your leads are junk wax") can kill retention. This is the "agency" trap unless the pay-on-qualified guarantee and AI triage really work.

**Confidence: 5/10**

---

## Overall verdict

**Conditional yes.** Card *trading* (flipping, grading arbitrage, breaking, holding sealed) is close to -EV for this user. It's a toll road run by eBay, Whatnot, PSA and Fanatics, with efficient comps, a modern-price correction underway and survivor-biased earnings stories.

An AI-leveraged business is +EV **if the user plays his actual edge, cheap customer acquisition, at the hobby's knowledge gap.** That means buying collections from non-hobbyists at 40–55% of resale value through a $1–5-CPC funnel (marketing-1), with lead-gen for shops (marketing-3) as the capital-light overflow. The condition is discipline: strict AI pre-triage, a hard buy-price cap, cert checks on every slab, no speculative inventory, and fast turns.
