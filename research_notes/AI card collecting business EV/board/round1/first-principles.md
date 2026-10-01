# Round 1 — The First Principles Thinker

Lens: What's actually true here, underneath the assumptions? Break the card economy into raw parts, find the cost that AI just collapsed, and look for the price that hasn't caught up yet.

## Step 0: The teardown (assumptions, marked FACT or GUESS)

Where does the money in a card actually go? Take a $100 card that moves from an attic to a collector:

| Raw part | Who takes it | Size | Status |
|---|---|---|---|
| Making the card | Topps/Fanatics, TPCi, Bandai | primary sale | FACT: licensors print to demand (Pokemon ~10B cards/yr, max capacity) |
| Marketplace toll | eBay 13.25%+, TCGplayer ~13.7%, Whatnot ~11.6%, Fanatics Collect 6%/0% | 0–15% | FACT (business_models note §1) |
| Grading toll | PSA $25–80/card, Value tiers paused June 2026 | $17–150/card | FACT |
| **Appraisal + sourcing spread** | Whoever buys the collection: dealers pay **40–60%** of market for whole collections | **40–60%** | FACT ([pokemonpricetracker](https://www.pokemonpricetracker.com/blog/posts/how-to-sell-pokemon-cards-maximize-your-profit-in-2026), [allvintagecards](https://allvintagecards.com/inherited-baseball-cards/)) |
| **Listing labor** | Consignors charge 9–25% (Probstein ~9%, local shops 15–25%, COMC ~$0.65/card + 20% cash-out) | 9–30% | FACT ([closo](https://closo.co/blogs/fees/consignment-fee), [forums.collectors.com](https://forums.collectors.com/discussion/comment/10939567)) |
| Price direction | Whoever holds inventory | ±20–70% | FACT that it's volatile; GUESS which way. Modern is falling 20–50% from peaks |

**The key fact:** the biggest slice in the chain isn't the platform fee or the grading fee. It's the **40–60% spread between what an untrained seller gets and what the card is worth**. That spread exists because of three costs:
1. **Appraisal labor.** A human expert needs hours to sort 3,000 cards and find the 40 that matter.
2. **Uncertainty.** The dealer lowballs because they can't price fast and might be wrong.
3. **Junk-wax filtering.** Most "old card collections" are 1987–94 junk worth ~$6–20 per 1,000 ([search summary, bulk lots 2026](https://www.100clubil.org/item/medium-flat-rate-sports-card-bulk-approx/)). Dealers burn time on calls that go nowhere, so they price that wasted time into every offer.

All three are **cognitive costs**, and AI vision plus LLM pricing has just pushed them close to zero. A Ricoh fi-8170 scans ~2,500 cards an hour, front and back ([Card Dealer Pro](https://www.carddealerpro.com/best-card-scanners/ricoh-fujitsu-8170)). Identification is commoditized ([ai_tools note §2](../../ai_tools_and_edges.md)). **The spread is still priced as if a human expert does the appraisal by hand. That's the gap: the battery-pack moment for cards.**

**What won't change in 10 years:** people inherit and outgrow stuff they don't understand, and they want it gone fast, fairly and without hassle. Collectors want verified cards at fair prices. Both sides want trust. The Great Wealth Transfer (~$90T) comes with an avalanche of physical collections ([Bloomberg, Nov 2025](https://prod.cm.bloomberg.com/news/features/2025-11-14/millennials-gen-x-set-to-inherit-boomers-antique-collectible-fortunes)). Millennials who own 1999–2003 WOTC Pokemon binders are now 30–40 with mortgages. Vintage held value in 2022 while modern fell 50–73% (risks note §1).

**Inversion: how to guarantee failure in cards in 2026:**
- Bet on price direction with modern product. Sealed is at or below MSRP, and modern singles are down 20–50%. **KILL.**
- Grading arbitrage at PSA's $79.99 Regular tier. EV is negative on most cards (business_models note §2, Scenario B: −$45/card). **KILL until Value tiers reopen.**
- Randomized breaks or repacks. Lottery suits are live under CA PC 319/319.3. **KILL.**
- Building another scanner, price index or eBay deal bot. It's commoditized and free, and it gets *worse* as AI improves. **KILL.**
- "Bulk picking" by the 1,000. Raw-material math: <1% of commons are worth >$1, and per-order fees take 28%+ on a $2 card. **KILL.**

**What's left is the opposite of what most people try.** Don't bet on cards going up. Sell the appraisal and the trust, take the spread on *off-market supply*, and stay indifferent to price direction. Every move below is built that way, and each gets *better* as AI gets better.

---

## first-principles-1 — The 24-Hour Collection Buyer

**One-liner:** A remote-first "we buy card collections" desk. Sellers text photos, Claude appraises in hours, and the user pays 55–65% of market (above the 40–50% dealers offer), then resells through the cheapest channels.

**The hack (unfair insight):** Dealers' 40–60% discount mostly pays for appraisal labor and junk-wax tire-kicking. When appraisal costs about $0, you can (a) **pay sellers more and still clear 25–35% gross**, (b) **take the small leads** ($300–1,500) that dealers won't drive to, and (c) **screen out junk wax before spending a minute or a mile**. The user's actual skill, Google Ads, is exactly what this business needs, because the scarce input in cards is *supply*, not buyers. Buyers are abundant: Whatnot did $8B+ GMV in H1 2026, and eBay's focus categories grew 26%.

**Why now:**
- Record transaction volume means fast exits. eBay, Whatnot, Fanatics Collect and PSA all hit records in 2026.
- Modern prices are falling, so sellers of *vintage and WOTC* collections hold the asset that kept its value (risks note §1).
- Estate and downsizing flow is accelerating: boomers held 42% of 2025 home sales and are downsizing ([Bloomberg](https://brp-prod-bcc.bloomberg.com/news/articles/2025-11-14/how-to-handle-a-parent-s-estate-what-to-keep-sell-and-throw-out)).
- eBay's Authenticity Guarantee fell to **$200** for raw and graded singles ([Value Added Resource](https://www.valueaddedresource.net/ebay-trading-card-threshold-packaging-updates/)). Mid-value raw cards now sell with buyer trust built in, which makes them more liquid to resell.

**How Claude runs it:**
1. Builds the intake site, an Artifact with a shared DB: "Upload 3 photos of your binder or box, get a range in 24 hours." It also builds the lead tracker and a deal P&L dashboard.
2. Writes and launches Google Search ads on seller-intent terms ("sell my baseball card collection", "inherited sports cards", "sell old pokemon cards", "who buys card collections near me"), plus Meta lookalikes via AdWhispr. The user reviews budgets.
3. **Triage:** Claude reads the photos and tags era and set. It flags vintage (pre-1980), WOTC Pokemon 1999–2003, 2000s RCs, autos, slabs and junk wax. It gives a value band and either fast-declines junk politely (with a bulk-donation tip) or books a call.
4. Itemized appraisal from the user's in-hand scans: ID, variant and condition notes, with comps from non-restricted sources (130point, PriceCharting, Card Ladder/Collectr subscription, Fanatics Collect). Then a written offer at a set % of market. It never pipes eBay restricted-API data into the LLM ([eBay API terms](https://www.ecommercebytes.com/2025/07/18/ebay-restricts-developers-from-using-its-data-to-train-ai/)).
5. **Exit routing per card:** Fanatics Collect auctions (100% of hammer) or Buy Now (6%) for graded; eBay for raw $200+ (Authenticity Guarantee); a Whatnot or show-table lot for the middle; bulk sold by the box. Claude writes every listing and re-prices weekly.
6. Fraud hygiene: slab cert lookup, image-reuse check and measurement checklist on vintage before payment.

**User's tasks:** Ad accounts and payment. Phone calls with sellers (Claude writes the script). Pick up local collections or receive shipped ones (prepaid insured label). Scan cards with an fi-8170 (~$1,000–1,400). Pack and ship sales. Attend 1 show a month to sell the middle tier and buy at the table. Sign off on every offer over $2,000.

**First 30 days:**
- Week 1: Claude builds the intake page and offer engine and drafts ads. The user buys the scanner, opens a Fanatics Collect seller account and sets a $1,500 ad test budget.
- Week 2: Ads go live in a 60-mile radius plus a "ship it to us" national offer. Claude emails 40 local estate-sale companies (6,000+ nationally; [EstateSale.com figure](https://www.homelight.com/blog/estate-sale-companies/)) offering a 5–10% finder's fee on referred collections.
- Weeks 3–4: Target 30 photo submissions, 8 qualified, 3 bought. Track cost per qualified lead and spread realized on the first resales.
- **Kill test:** if cost per closed deal is over $400 *and* the median qualified deal is under $1,000 market after 60 days, stop ads and fall back to estate-company referrals only.

**Path to the goal (real math):**
- Average qualified deal: $2,500 market value (GUESS; distribution is skewed, with many $500s and a few $10k+).
- Buy at 55% = **$1,375**. Realized resale ≈ 90% of market after mixing channels (some lots go cheaper) = $2,250.
- Costs: fees, shipping, supplies and occasional grading ≈ 9% = $200. Gross per deal ≈ **$675**.
- Acquisition cost per closed deal: CPC ~$2–4 (category CPCs are $1.15–2.29 for head terms, [rankhero](https://www.rankhero.com/keywords/sports-card); seller-intent long tail is a GUESS at higher). About 6% lead rate, 30% qualified, 40% close gives **~$250/deal**, blended lower with estate referrals. **Net ≈ $425/deal (31% on cost).**
- **Capital is the limiter.** $15k turning every ~6 weeks is ~8.5 turns/yr, so ~$128k bought/yr × 31% ≈ **$40k/yr ≈ $3.3k/month**.
- Reinvest profits plus a **"consign instead" option** at 15% for sellers who want more. That needs no capital and lets you take deals bigger than your bankroll. Together these reach **$5–7k/month by month 10–12** at ~12–16 deals/month.
- **Honest middle outcome:** $2.5–4k/month at month 12 on $15k. $6–8k/month in year 2 with $30k working capital or a strong consignment book. **Upside:** one $20k+ vintage or WOTC estate in a month (these exist; they're the reason the ads pay).

**Evidence:**
- Dealer offer norms are 40–60% for whole collections, 60–70% cash offers on sorted collections ([pokemonpricetracker](https://www.pokemonpricetracker.com/blog/posts/how-to-sell-pokemon-cards-maximize-your-profit-in-2026), [allvintagecards inherited guide](https://allvintagecards.com/inherited-baseball-cards/)).
- Inherited collections range from "$50 to $50,000," and junk wax is mostly worthless ([allvintagecards](https://allvintagecards.com/inherited-baseball-cards/)).
- Scanner throughput is 2,500 cards/hr ([Card Dealer Pro](https://www.carddealerpro.com/best-card-scanners/ricoh-fujitsu-8170)).
- Ricoh/PFU and Kronozio launched a "turn trading card collections into cash" scanner bundle (Aug 2026), a signal that the collection-liquidation market is getting tooled ([PFU press release](https://www.pfu-us.ricoh.com/about-us/press-releases/2026/08/pfu-america-inc-and-kronozio-introduce-document-scanner-powered-bundle)).
- Exit fee spread: 0–6% at Fanatics Collect vs 15% at eBay (business_models note §1).
- Vintage resilience in the 2022 drawdown ([SCD](https://sportscollectorsdigest.com/news/sports-card-market-values-vintage-cards-modern-pwcc-card-ladder)).

**Biggest risk:** Buying a fake or altered vintage card, or overpaying into a falling comp. Mitigate with in-hand inspection before payment, cert checks, valuing at 30-day comps minus a haircut, and never buying modern sealed.

**Confidence: 7/10.** This is the oldest business in the hobby, rebuilt on a collapsed cost. It's directly matched to the user's PPC skill, and it's indifferent to price direction because the spread is set at purchase.

---

## first-principles-2 — The Invisible Back Office (AI listing desk for card shops and estate liquidators, paid on rev share)

**One-liner:** Card shops and estate liquidators sit on thousands of unlisted singles because listing costs staff hours. We turn their scans into variant-accurate, priced eBay/TCGplayer/Shopify listings and run the online store, for 8–10% of what sells.

**The hack:** Listing a card is still priced as human labor: consignors take 9–25%, and COMC takes ~16 weeks plus $0.65/card. Rebuilt from raw parts, scanning takes 1.4 seconds per card and vision+LLM identification and pricing costs a fraction of a cent. So the real cost to list a card is now **cents**. Most shops don't want *software*: Kronozio ($199), Card Dealer Pro (CollX) and TCG Automate all exist and still leave the work to the shop. They want the *outcome*. Software is a commodity; a done-for-you service on rev share is not. The edge is **variant accuracy** (parallel, serial, set code, language), which is exactly where eBay's bulk AI tool has broken ([VAR](https://www.valueaddedresource.net/ebay-bulk-ai-listing-sports-cards-broken/)) and where scanners "lose points" ([EyevoTCG](https://eyevotcg.com/blog/best-pokemon-card-scanner-apps-2026/)).

**Why now:**
- Shop card margins collapsed to ~20% after the pandemic (business_models note §4). Shops need online sell-through of dead inventory, and shops are closing ([SCD closures](https://www.sportscollectorsdaily.com/tag/sports-card-shop-closing/)).
- Dealers' stated pains are getting singles online, repricing in fast markets, and inventory scattered across spreadsheets ([CardCloud/Winventory](https://winventory.ca/partner/features)).
- Scanners are now marketed to shops for scan-to-list (PFU/Kronozio, Aug 2026), so client-side scanning is becoming normal.

**How Claude runs it:** Ingest scan folders from Drive. Identify each card to the variant and flag low-confidence ones for human QA. Price from non-restricted comp sources and condition notes. Generate listing CSVs (eBay File Exchange / TCGplayer / Shopify). Write titles to search best practice and reprice weekly on a schedule. Send each client a weekly sell-through report by Gmail. Claude also prospects: it builds a shop and liquidator list, writes outreach and books calls.

**User's tasks:** Sell to shops: calls, plus visits to 5–10 local shops. Sign rev-share agreements. Get delegated access to clients' marketplace accounts (the client owns the account). Spot-check QA on high-value cards. Optionally run a "we scan it for you" day at a shop with the user's own scanner.

**First 30 days:**
- Free pilot with 2 local shops: list 500 of their cards each, at ≥$5 value.
- Measure ID accuracy, listing time per card and 30-day sell-through.
- Turn the pilot results into a one-page case study. Claude drafts it and emails 150 shops and 100 estate-sale companies.
- **Kill test:** if fewer than 2 of the first 15 pitched shops sign after the case study, fold this into FP-1 as an internal tool only.

**Path to the goal (real math):**
- Per active client, cards we list sell **~$6–10k GMV/month** after a 60-day ramp (GUESS; depends on the shop's backlog quality).
- Fee **8%** gives **$480–800/month per client**, plus a $300–500 setup fee.
- Costs: tools and API ~$50/client/month. User time ~2 hrs/client/month after onboarding.
- **10 clients ≈ $5–7k/month at ~85% margin. Honest middle: 4–6 clients by month 9–12 ≈ $2.5–4k/month.** It stacks with FP-1, because the same pipeline lists FP-1's inventory.

**Evidence:**
- Consignment rates: Probstein ~9%, local shops 15–25%, COMC fees and cash-out ([closo](https://closo.co/blogs/fees/consignment-fee), [forums.collectors.com](https://forums.collectors.com/discussion/comment/10939567)).
- Kronozio is software at $199 plus 10% on its own marketplace ([search summary](https://whatsyourtech.ca/?p=45642)). This proves willingness to pay for tooling; the gap is labor.
- eBay's bulk AI listing failures ([VAR](https://www.valueaddedresource.net/ebay-bulk-ai-listing-sports-cards-broken/)).

**Biggest risk:** Small shops are cheap and slow to trust an outsider with their account and inventory. Sales cycle and churn could keep this at 3–4 clients.

**Confidence: 5/10.** The unit economics are excellent, but distribution is the unknown. It has the most leverage per hour if it lands.

---

## first-principles-3 — Off-Market Supply Exchange (AI-qualified collection leads, sold to dealers by territory)

**One-liner:** Run the seller-intent ad engine nationally. Claude photo-triages every lead into a scored, itemized "deal packet," and the user sells exclusive packets to vetted dealers in each region for a flat fee or a 5–10% finder's fee on closed deals.

**The hack (contrarian truth):** Most people think the card business is about finding *buyers*. It isn't. Demand is a firehose (Whatnot, eBay, Fanatics). **The scarce resource is off-market supply: collections in closets that never touch a marketplace.** Dealers fight over it with "We Buy" signs, show tables and mailers. Today a raw "I have old cards" form fill is nearly worthless to a dealer, because 70%+ are junk wax. An **AI-qualified packet** (photos, era tags, flagged key cards, estimated value band, seller's timeline) is worth 10x more, because it saves the dealer the wasted drive. The ads are the user's craft; the qualification is Claude's. No inventory, no capital at risk, no price-direction exposure.

**Why now:** Estate and downsizing flow is rising (see FP-1). Platform volumes are at records, so dealers have exit liquidity and want inventory. The fee war (Whatnot cuts to 6–6.5%, Fanatics Collect at 0–6%) means high-volume dealers make more per card and can pay more to acquire supply.

**How Claude runs it:** Builds the national intake funnel and a territory-routing database (Artifact + db). Writes and optimizes the ads. Triages every submission with vision. Writes the deal packet. Matches it to the dealer in that territory and emails it. Tracks close and dispute status, invoices, and runs a monthly dealer scorecard so sellers get fair offers. Seller consent to share their details is built into the form. Claude also recruits dealers: it builds lists from show exhibitor pages and shop directories and writes outreach.

**User's tasks:** Manage ad budget and accounts. Sign dealer agreements and handle billing. Vet dealers with a short call plus references, because seller trust is the product. Handle disputes. Leads inside the user's own radius can go to FP-1 instead.

**First 30 days:**
- Sign 5 dealers in 5 metros on a free first-3-leads trial.
- Spend $1,500 on ads across those metros. Target 20 qualified packets delivered.
- Ask each dealer what they'd pay per packet tier: "$500–2k est.", "$2–10k", "$10k+".
- **Kill test:** if fewer than 3 of 5 dealers will pay at least 2x your cost per qualified packet, stop.

**Path to the goal (real math):**
- Cost per qualified packet ≈ $40–80, using the FP-1 funnel assumptions (GUESS until tested).
- Price per packet: Tier A $50, Tier B $150, Tier C $400 or 7% finder's fee on close (GUESS; validate in month 1).
- Blended ~$130 revenue per packet vs ~$60 cost gives **~$70 margin**.
- 100 packets/month = **$7k/month** net of ad spend. **Honest middle: 40–70 packets/month by month 9 ≈ $3–5k/month.** It scales with ad budget and dealer count, not with capital or the user's hands.

**Evidence:**
- Dealers already pay finder-style spreads and buy whole collections at 40–60% ([allvintagecards](https://allvintagecards.com/inherited-baseball-cards/)).
- Search demand exists at scale: "baseball card" ~90.5k/mo and "pokemon cards" ~1.8M/mo head terms ([rankhero](https://www.rankhero.com/keywords/baseball-card), [rankhero pokemon](https://www.rankhero.com/keywords/pokemon-card)). Seller-intent long tail is UNVERIFIED and must be pulled in Google Keyword Planner on day 1.
- The estate liquidator network (6,000+ companies) is a secondary lead source ([HomeLight](https://www.homelight.com/blog/estate-sale-companies/)).

**Biggest risk:** Lead quality and trust. If dealers lowball the sellers you send them, reviews and ad costs go up and the engine dies. Vetting dealers and publishing an "offer floor" policy is mandatory. Platform ad policies on "we buy" ads also need checking.

**Confidence: 5/10.** The insight is strong and it uses the user's real skill, but two numbers are unproven: what dealers will pay per lead, and seller-intent CPCs. Both are cheap to test in 30 days.

---

## How the three fit (and the order)

They share one engine: **seller-intent ads + Claude photo triage + Claude listing pipeline.**
- Start with **FP-1**. It proves the funnel economics with the user's own money and builds the comp and appraisal playbook.
- Spill leads outside the user's radius or capital into **FP-3**.
- License the listing pipeline to shops as **FP-2** once it's battle-tested on FP-1 inventory.

None of the three needs card prices to go up.

## Overall verdict

**Conditional yes.** An AI-leveraged card business is +EV for this user only if it sells *appraisal, listing labor and trust* and takes the spread on off-market supply. In that setup AI collapses the dealer's biggest cost and the user's PPC skill solves the hobby's real scarcity, which is supply. It is -EV if it bets on price direction (modern sealed or singles, PSA-$80 grading arb) or on randomized mechanics, which describes most of what newcomers do in 2026. Honest middle: $3–4k/month by month 12 on $15k. $5–10k/month needs reinvestment, consignment or the lead-exchange layer.
