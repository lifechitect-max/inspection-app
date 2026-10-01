# Growth Hacker: Round 1 Proposals

Lens: where does this spread by itself? Paid acquisition is renting customers. I'm looking for loops, bigger platforms to ride, and corners where we can show up first.

Date: 2026-10-01

## Overall verdict

**Conditional.** Inventory speculation, breaks, grading arbitrage and another AI scanner or alert bot are -EV or crowded for a solo operator in fall 2026. Modern prices are already falling 20-50%, PSA's cheap tiers are paused, breaks face lottery lawsuits, and scanners are free. The +EV play is a **sourcing spread**: buy from non-collectors (heirs, downsizers, estate liquidators) at 40-60% of market and sell at market. AI makes the top of that funnel close to free and spreadable. The ceiling is the user's own hands and capital, so the honest middle outcome is about $3-6k/month profit by month 12, with $10k/month reachable only if the loop compounds.

My cross-cutting read: two of the three moves are distribution engines for the same profit pool, which is buying collections below market. That is deliberate. The only reliable margin left in this market is in buying, not selling. The research note puts it plainly: "buying cheaper matters much more than which channel you sell on" ([business_models_unit_economics.md §1](../../business_models_unit_economics.md)).

---

## growth-1: The Attic Appraisal Engine

**One-liner:** A free, honest "What's my old card collection worth?" AI photo-triage site that Claude builds and runs. Programmatic pages and a liquidator referral loop feed it, and it turns into collection buys at 45-60% of market.

**The hack (unfair insight):**
- Each year, roughly 250k to 1.2M US estate sales and countless garage cleanouts turn up boxes of cards. The people holding them are not collectors. Their search is "are my old baseball cards worth anything?"
- Today, a local shop answers that by offering 25-50% of value, or "pennies on the dollar" ([Dean's Cards](https://www.deanscards.com/how-much-money-to-expect-when-i-sell-my-baseball-cards)). Online buyers like All Vintage Cards quote 60-70% within 48 hours of receiving photos ([All Vintage Cards](https://allvintagecards.com/inherited-baseball-cards/)).
- Nobody gives these people a fast, free, honest triage, so we do. Most collections are junk wax worth pennies per card ([Giant Sports Cards](https://giantsportscards.com/blogs/blog/junk-wax-era-are-my-90s-sports-cards-worthless)). Telling 85% of people "it's mostly worthless, here's what to keep" builds the trust that wins the other 15%: pre-1980 vintage, 1993 SP Jeter, 1989 UD Griffey, and **1999-2003 WOTC Pokemon binders from millennials' childhood bedrooms**. Vintage is at record prices while modern falls ([market_size_and_cycle.md §3](../../market_size_and_cycle.md)).
- **The loop:** every triage report is a branded, shareable PDF or link that heirs forward to siblings ("Grandpa's cards: here's what's in the box"). Every estate liquidator who sends a box gets a **two-sided reward**: a 10% finder's fee to the liquidator and a free full appraisal for their client. Liquidators already take 25-50% of proceeds and hate cards because they can't price them ([ElderLawAnswers](https://www.elderlawanswers.com/the-ins-and-outs-of-estate-sales-15056)). Finder's fees to liquidators are an established dealer practice ([BookThink](https://www.bookthink.com/0176/176estate1.htm)). Roughly 45,000 liquidators operate in the US ([Gitnux, weak](https://gitnux.org/estate-sale-industry-statistics/)), so one liquidator becomes a repeat lead source and refers peers.

**Why now:**
- The boomer estate wave is under way, and hobby forums expect boomer estates to keep bringing cards to market ([Collectors Universe forum](https://forums.collectors.com/discussion/766872/baby-boomers-generation-in-the-next-15-years)).
- Vintage and high-end cards are at records: a $16.49M Pikachu sold in Feb 2026 and vintage baseball "shows no signs of cooling". Sell-side liquidity is at all-time highs: eBay card GMV is the #1 growth driver, and Whatnot did $8B+ in H1 2026.
- The 2026 grading squeeze means heirs can't easily "just get it graded".

**How Claude runs it (about 80% of the work):**
1. **Day 1-3: build the site.** It has a photo upload, a vision model that identifies cards, era, set and stars, and returns a triage verdict in three buckets: "bulk," "worth a closer look," and "call us." Claude writes the branded, shareable report template. Pricing comes from non-eBay-API sources (PriceCharting, manual 130point checks, our own sold logs) to respect eBay's June 2025 API terms ([ai_tools_and_edges.md §3](../../ai_tools_and_edges.md)).
2. **Programmatic pages.** Claude writes 500-2,000 long-tail pages, one per set-year: "1989 Upper Deck baseball cards worth," "1999 Pokemon base set binder value," "1972 Topps complete set value," "what to do with inherited football cards." Each page uses one template, with a checklist of the 5-15 cards that matter in that set and a CTA to "upload your box."
3. **Liquidator outreach.** Claude builds a list of estate-sale companies in a 2-3 hour drive radius from estatesales.net and estatesales.org company directories. It drafts personal emails through Gmail, sends at a human-paced cadence and logs follow-ups. The user approves the template once.
4. **Daily routine.** Claude triages every upload within hours and drafts offers with a price sheet the user approves. After each buy it writes the listings: variant-accurate titles and the right channel per card (Fanatics Collect at 6% for graded, eBay for vintage raw, Whatnot for lots).
5. **Weekly dashboard.** Leads, triage mix, close rate, cost per lead by source, inventory age and realized margin per deal.

**User's tasks:** form an LLC, open buying accounts, make phone calls on high-value leads (Claude writes call scripts), do in-person pickups and pay (cash or Zelle), photograph and ship, and attend 1 show a month to sell bulk and buy more. Capital: $5-15k revolving. About 12-18 hours a week.

**First 30 days:**
- **Wk 1:** site, triage tool, 100 programmatic pages and the liquidator list are live. Claude also drafts local "I buy card collections, free honest appraisal" posts for FB Marketplace, Nextdoor and Craigslist; the user posts them.
- **Wk 2:** email 150 liquidators within the radius. Goal: 10 replies, 3 partners.
- **Wk 3:** first 2-3 buys, kept small ($200-1,000 each). Log every comp, buy price and sale.
- **Wk 4:** 300 more pages are live. Test a $300 Google Ads budget on "sell baseball card collection [city]" to measure cost per qualified lead. The Collectibles category averages about $4 CPC ([WordStream](https://www.wordstream.com/blog/google-ads-cost)). Kill the test if cost per qualified lead is over $150.

**Path to goal (real math):**
- **Unit economics of one "worth a look" deal:**
  - The collection has $3,000 of market value in sellable cards. We buy it at 50%, for $1,500.
  - We sell across channels for about 87% net after fees (blended across Fanatics Collect at 6%, eBay at 15% and Whatnot at 11%), giving $2,610. Shipping, supplies and bulk write-off cost about $150.
  - **Profit per deal: about $960, a 32% margin on sales and 64% on cost**, with roughly 45-60 days to turn.
- **The funnel:**
  - About 10% of leads have $1k+ of sellable value, and we close about 35% of those, so **about 3.5 deals per 100 leads.**
  - **$5k/month profit needs about 5-6 deals a month, which means about 150 leads a month.**
  - Expected lead sources by month 6:
    - Liquidator partners: 30 at about 1 lead/month each, so 30 leads.
    - Local posts and word of mouth: about 30.
    - Organic programmatic SEO: 5k-15k visits/month at a 1% upload rate, so 50-150.
    - Paid search only where cost per qualified lead is under $150.
- **Honest middle outcome:** about $1-2k/month by month 4 and **about $4-6k/month by month 12**, on $25-35k/month of sales with $10-15k of capital rotating.
- **Upside:** a few whale estates (a single $20k+ vintage collection nets $5-8k) and a liquidator network that compounds past 60 partners. **Downside:** SEO stays slow, leads are mostly junk wax, and the business stays at about $1-2k/month. In that case cut it to the liquidator channel only.

**Evidence:**
- 60-70% cash offers within 48 hours of photos are the market norm for online buyers: [All Vintage Cards](https://allvintagecards.com/inherited-baseball-cards/), [BaseballCardBuyer via Cardboard Connection](https://www.cardboardconnection.com/the-connections-top-go-to-for-selling-your-vintage-cards)
- Local shops pay 25-50% or pennies on book: [Dean's Cards](https://www.deanscards.com/how-much-money-to-expect-when-i-sell-my-baseball-cards)
- Liquidators charge 25-50% commission and finder's fees are standard practice: [ElderLawAnswers](https://www.elderlawanswers.com/the-ins-and-outs-of-estate-sales-15056), [BookThink](https://www.bookthink.com/0176/176estate1.htm), [Sports Collectors Daily on estate planning for collections](https://www.sportscollectorsdaily.com/why-your-sports-collection-needs-to-be-part-of-an-estate-plan/)
- Estate sale volume, 250k to 1.2M a year depending on definition (weak source): [Gitnux](https://gitnux.org/estate-sale-industry-statistics/)
- Junk wax is mostly worthless, with a few known exceptions: [Giant Sports Cards](https://giantsportscards.com/blogs/blog/junk-wax-era-are-my-90s-sports-cards-worthless), [Underpriced 1990s guide](https://www.underpriced.app/blog/1990s-baseball-cards-value-guide-2026)
- Sell-side fees and the flip margin math: [business_models_unit_economics.md §1, §7](../../business_models_unit_economics.md)

**Biggest risk:** lead volume. Programmatic SEO for "what are my cards worth" competes with established SEO sites (thecardshopfinder, underpriced.app, cardmavin). If organic search stalls, the business depends on liquidator relationships, which is slower but stickier. Secondary risk: buying a fake or altered vintage card. Mitigation: verify slab certs and run Claude's image-forensics checklist on any buy over $500.

**Confidence: 7/10.** This is the only move here where the margin source (a buy-side information gap with non-collectors) is structural rather than cyclical.

---

## growth-2: "Attic Roadshow" Live Appraisal Show

**One-liner:** A twice-weekly live show on Whatnot, simulcast to TikTok Live, where anyone can hold their old cards up to the camera for a free, honest on-air appraisal. Claude clips every segment into short-form, and the show sells straight singles auctions. No breaks.

**The hack:**
- *Antiques Roadshow* is a 25-year-old proven format that nobody runs natively for cards on a live-commerce platform.
- **Every guest is a distribution node.** Someone getting Grandpa's 1968 Topps appraised on air tells their whole family to watch, and the "we found $X in the attic" clip is the kind of thing people share because it says something about them (the Spotify Wrapped principle).
- The show solves Whatnot's cold-start problem for a new seller, which is having no audience. It does that by giving away the one thing everyone with a shoebox wants, a valuation.
- Whatnot pays for part of the loop: there is a **two-sided $10/$10 referral credit** ([referralcodes.com](https://www.referralcodes.com/shop/what-not-referral)), shareable seller referral codes ([Value Added Resource](https://valueaddedresource.net/whatnot-launches-selling-api-improved-discovery-and-referral-codes)), and a new-seller sales-match bonus ([dealhack](https://dealhack.com/coupons/whatnot)).
- Guests who want to sell become buys on the spot. The show doubles as a sourcing engine (it pairs with growth-1 but runs standalone).

**Why now:**
- Whatnot is at $8B+ GMV in H1 2026 and a $20B valuation. It is still pushing creator programs: a UK Creator Program launched May 2026 pays cash and credits for content ([conductatlas Whatnot ToS](https://conductatlas.com/platform/whatnot/whatnot-terms-of-service/seller-commission-and-fee-terms/)), and new tiered fees take effect Sept 21, 2026.
- TikTok is pushing collectibles hard. It partnered with Panini on in-app World Cup cards in June 2026 ([TikTok Newsroom](https://newsroom.tiktok.com/tiktok-and-panini-partner-to-launch-a-global-digital-collectible-card-experience-tied-to-fifa-world-cup-2026?lang=en)), and trading cards were about 81% of TikTok Shop collectibles sales ([SmartScout/Echotik via search](https://www.smartscout.com/blog/tiktok-shop-statistics-2026)).
- Fanatics Collect launched creator programming with 24 partners in June 2026, which shows platforms are paying for card content ([ai_tools_and_edges.md §6](../../ai_tools_and_edges.md)).
- Breaks are under lottery-law attack ([risks_and_failures.md §3](../../risks_and_failures.md)), so a show built on straight singles and appraisal is differentiated and legally clean.

**How Claude runs it:**
- **Before each show:** Claude collects guest submissions through a form on the growth-1 site, pre-identifies every card, pulls comps and writes a run-sheet with the talking point, value range and "fun fact" for each guest segment. It also prices and orders the auction lots.
- **After each show:** Claude cuts the recording into 15-25 vertical clips with hooks, plus captions. That means writing 50 hook variants a week and scheduling them through the Higgsfield TikTok publishing tools and YouTube Shorts. It tracks views, shares and follows per clip and doubles down on the winning format ("what's in the shoebox," "the one card that paid for the cleanout," "WOTC binder reveal").
- **Ongoing:** Claude drafts guest invite DMs, thank-you messages with the referral code, and the weekly show calendar.

**User's tasks:** host 2 shows a week of about 2 hours each (on camera, a phone plus a ring light is enough), handle and ship sold items, make buy offers to guests on air or after, and create the Whatnot and TikTok seller accounts. About 10-12 hours a week.

**First 30 days:**
- **Wk 1:** Claude writes the show format, segment rules (honest-appraisal pledge, no breaks, no repacks) and 20 pilot clip scripts. The user films 10 "what's in the shoebox" shorts using cards bought locally for $200-500.
- **Wk 2:** first 2 live shows, sourced from 5 local guests (friends, FB group members) plus $1-2k of singles to auction.
- **Wk 3-4:** 4 more shows and 60+ clips posted. Measure live viewers, guest-to-viewer multiplier, clip share rate and follows. **Kill or pivot the format if no clip reaches 10k views by day 30.**

**Path to goal (real math):**
- Whatnot net margin on singles bought at 50-60% of market and sold at about 90-100% of market is roughly 25-35% after an 11% fee and supplies.
- Revenue = shows a month × GMV per show:
  - Month 3: 8 shows × $1,000 = $8k GMV, about $2k profit.
  - Month 12: 9 shows × $3,000 = $27k GMV, **about $6-8k profit**.
- Honest middle: $10-15k a month of GMV by month 9-12, so **about $2.5-4k a month of profit**, plus whatever sourcing it feeds into growth-1.
- Viral coefficient target: each guest brings at least 3 new viewers and about 5% of new viewers become buyers. If guests average under 1 new viewer, the loop is not working and this becomes a plain Whatnot shop.

**Evidence:**
- Whatnot scale, seller earnings claims (self-reported) and creator sponsorship density: [Sacra](https://sacra.com/research/whatnot-at-359m-yr/), [ecommercebonsai Whatnot stats](https://ecommercebonsai.com/whatnot-statistics/), [SponsorRadar TwicebakedJake](https://sponsorradar.com/channels/twicebakedjake) (23 Whatnot-sponsored videos)
- Referral mechanics: [Value Added Resource](https://valueaddedresource.net/whatnot-launches-selling-api-improved-discovery-and-referral-codes), [referralcodes.com](https://www.referralcodes.com/shop/what-not-referral)
- Fee tiers: [Tubefilter, Sept 17 2026](https://www.tubefilter.com/2026/09/17/whatnot-new-commission-rates-lower-three-percent/)
- TikTok collectibles push: [TikTok Newsroom](https://newsroom.tiktok.com/tiktok-and-panini-partner-to-launch-a-global-digital-collectible-card-experience-tied-to-fifa-world-cup-2026?lang=en), [Retail Dive on TikTok Shop collectibles](https://retaildive.com/news/tiktok-shop-collectibles-comic-manga/736391)
- The creator ecosystem is crowded but loyalty is to the seller, not the platform: [wearefounders Whatnot profile](https://www.wearefounders.uk/whatnot-how-a-livestream-shopping-app-became-the-billion-dollar-empire-nobody-saw-coming/)

**Biggest risk:** live commerce is crowded, and Whatnot discovery favors established sellers. If the appraisal format doesn't pull guests, this becomes a me-too singles stream earning $5-15 an hour. The user must also be comfortable on camera.

**Confidence: 5/10.**

---

## growth-3: First Home Base for the Naruto Card Game (Summer 2027)

**One-liner:** Show up first on the next big TCG. Claude builds the go-to English fan hub for Bandai's Naruto Card Game (card database, spoiler tracker, deck builder, pull-rate and price tracker, Discord) 9 months before launch. It then monetizes the audience at launch through a singles shop, affiliate links and ads.

**The hack:**
- New TCGs are under-supplied early on, and the first credible hub becomes the default bookmark. Piltover Archive, a free Riftbound database and deck builder, drew **262k visits in Aug 2025, two months before Riftbound launched** ([Semrush](https://it.semrush.com/website/piltoverarchive.com/overview)).
- The Naruto Card Game is Bandai's next global launch. It uses a **Leader-based system like One Piece** ([Anime Corner](https://animecorner.me/naruto-card-game-reveals-first-gameplay-details-card-designs-ahead-of-summer-2027-launch/)), and One Piece became the world's #3 TCG. Naruto is an even bigger global IP among millennials and Gen Z.
- Bandai keeps showing that demand outruns supply at launch. Gundam starter-deck preorders sold out before the July 2025 release ([Siliconera](https://www.siliconera.com/4-gundam-card-game-starter-decks-will-be-sold-at-launch/)), and Riftbound's second-set preorders sold out "in seconds" ([Sheep Esports](https://www.sheepesports.com/articles/pre-orders-for-spiritforged-english-version-begin-on-january-12/en)).
- As of today a search shows **no dominant database or deck-builder hub** for the new game, only legacy fan wikis and SEO blogs.

**Why now:**
- Bandai revealed rules and card designs on July 29, 2026 and demoed the game at Gen Con. The worldwide launch is Summer 2027 ([ICv2](https://www.icv2.com/articles/news/view/62661/bandai-announces-naruto-card-game)).
- The window to become the default hub is the next 9 months. After launch, the hub land-grab is over.

**How Claude runs it (about 90% of the work):**
- **Build:** the site (card database schema, a spoiler tracker updated from Bandai's official reveals and Japanese social posts with translation, a deck builder with export, and "which Leader should I play" explainers), plus programmatic pages per card, Leader and archetype.
- **Content:** 3-5 posts a week and a Discord bot that posts every new reveal. Claude also sets up the launch email list, offering "preorder alerts plus the launch pull-rate tracker" as the incentive.
- **Built-in loop:** every deck the deck builder exports carries a "built on [site]" image card for sharing to Discord, Reddit and X. A public "spoiler season" leaderboard rewards community submitters.
- **At launch:** Claude writes TCGplayer affiliate integration on every card page (3.5% ([TCGplayer docs](https://docs.tcgplayer.com/docs/tcgplayer-affiliate-program))) and launches the user's own singles store on TCGplayer and Whatnot, promoted from the hub.

**User's tasks:**
- Register the domain and the Discord, TCGplayer and affiliate accounts.
- Show up as the human face: attend 1-2 Bandai events or locals, and do occasional on-camera content.
- At launch, buy sealed product at distributor or retail, open it, and list singles (Claude prices them).
- Optionally apply for a Bandai retailer allocation later.
- About 5-8 hours a week until launch, more after.

**First 30 days:**
- **Wk 1:** domain, a database of every revealed card (with translation), a spoiler tracker and the Discord are live.
- **Wk 2:** deck-builder MVP with shareable deck images; 40 SEO pages ("Naruto Card Game release date," "how the Leader system works," one per revealed Leader).
- **Wk 3-4:** seed the hub in r/narutotcg-type subreddits, Discord servers and One Piece TCG communities (ToS-compliant, transparent self-promotion). Target 2k email signups by day 60.
- **Kill criterion:** under 10k monthly visits by month 4.

**Path to goal (real math):**
- **Pre-launch (months 1-9):** about $0-500 a month. This is a build-the-audience phase and does not meet the 12-month goal alone.
- **Launch (months 10-14):** take the Piltover benchmark at about 50%, roughly 130k visits and about 300k pageviews a month:
  - Ads: about $10-15 RPM (gaming sits at the low end ([Blogging Guide](https://bloggingguide.com/guides/raptive/))), so $3-4.5k.
  - TCGplayer affiliate: 3.5% × about $30-60k of referred GMV, so $1-2k.
  - Own singles shop: $10k GMV at about 20%, so $2k.
  - **That gives about $6-8k a month at peak launch hype.**
- **Honest middle:** traffic halves after launch, as Piltover's did (-50% the following month), so **about $3-4k a month sustained**. Hub value is durable only if the game lasts. One Piece did; Lorcana cooled.

**Evidence:** Piltover Archive traffic ([Semrush](https://it.semrush.com/website/piltoverarchive.com/overview)); Naruto Card Game launch details ([ICv2](https://www.icv2.com/articles/news/view/62661/bandai-announces-naruto-card-game), [Anime Corner](https://animecorner.me/naruto-card-game-announced-by-bandai-global-launch-planned-for-2027/)); One Piece at #3 and Riftbound as the fastest-growing TCG ([market_size_and_cycle.md §2](../../market_size_and_cycle.md)); Riftbound sellouts ([GosuGamers](https://www.gosugamers.net/news/77887-league-of-legends-tcg-riftbound-explodes-in-popularity-after-launch-as-demand-surges)); TCGplayer affiliate at 3.5% ([TCGplayer docs](https://docs.tcgplayer.com/docs/tcgplayer-affiliate-program)).

**Biggest risk:**
- **Timing and IP:** revenue arrives after month 10, and the game could flop (Lorcana-style cooling) or Bandai could ship its own strong official database.
- **No info gap:** the launch is simultaneous worldwide, so the Japan-first information lag that early One Piece sellers enjoyed doesn't exist.
- **Copyright:** card images need careful fan-site use within Bandai's guidelines.

**Confidence: 4/10.** It's a bold, cheap option (mostly Claude's time) on a possible One Piece-scale launch, and it makes the best side bet alongside growth-1.

---

## Killed from my lens (one line each)
- **Another scanner or "collection worth" app:** commodity, with dozens of clones on the App Store ([AppFollow listings](https://apps.appfollow.io/ios/snapdex-card-value-scanner/6745400103?country=ie)).
- **Pure affiliate or programmatic price-guide site:** eBay pays 1-4% and TCGplayer 3.5%, which doesn't reach $5k/month without about 1M monthly visitors.
- **Paid-ads-driven breaks or repacks:** renting customers into the format under the most legal risk.
