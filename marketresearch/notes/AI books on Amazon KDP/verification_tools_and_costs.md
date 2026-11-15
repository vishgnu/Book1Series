# Verification: tools and costs (primary sources)

- **Date accessed:** 2026-11-14
- **Scope:** report section "A working setup costs hundreds of dollars until you pay for human editing", its setup-cost table, and the "Startup budget" paragraph.
- **Method:** I fetched vendor pages with `curl` and rendered JS-priced pages with headless Playwright (Chromium). Where a vendor blocked both (HTTP 403 from adobe.com and helpx.adobe.com), I used WebFetch, which returns a model summary of the page, so those rows are marked "via WebFetch". Raw downloads are in `scratchpad/dl_tools/`.
- **Currency caveat:** this machine geolocates to Germany. Several vendors (ChatGPT, Claude, NovelCrafter, ProWritingAid, Vellum) served EUR prices. NovelCrafter shows "19% tax included"; Vellum shows "Price does not include VAT". USD is given where the vendor's page or source also exposed it. Sudowrite, Midjourney, NovelAI, Atticus, KDSpy, Publisher Rocket and Bowker showed USD only.
- A row is CONFIRMED only if the figure was read on the vendor's own page.

## Price and terms check

| Item | Report's figure | Verified figure (USD; EUR where shown) | Vendor URL | Status |
|---|---|---|---|---|
| ChatGPT Plus | $20/month | **€23/month** (EUR page; monthly only for Plus). USD amount is injected client-side by geo and was not shown to this IP. Also seen: Go €8/month, Pro from €103/month | https://chatgpt.com/pricing | **NOT FOUND (USD)**: EUR price verified; openai.com and help.openai.com return 403 |
| Claude Pro | $20/month | **$20/month billed monthly; $17/month on annual ($200 billed up front)**. EUR: €18 monthly; €15/month annual (€180 up front) | https://claude.com/pricing | CONFIRMED (adds annual option) |
| Sudowrite | $19/$29/$59 a month | Monthly: **$19 / $29 / $59** (Hobby & Student / Professional / Max). Yearly toggle: **$10 / $22 / $44 per month** ("Up to 50% off"). USD only | https://sudowrite.com/pricing | CONFIRMED (monthly) |
| NovelCrafter | ~$4-$20/month + own API | **$4 / $8 / $14 / $20 USD monthly** (Scribe / Hobbyist / Artisan / Specialist). DE page: €4.32 / €8.64 / €15.11 / €21.59 monthly, **19% VAT included**; annual €43.19 / €86.36 / €151.13 / €215.90 ("2 Months off"). AI is BYOK from Hobbyist up (Scribe has no AI). 21-day free trial | https://www.novelcrafter.com/pricing | CONFIRMED |
| NovelAI | $10-$15/month | **Tablet $10/month, Scroll $15/month, Opus $25/month**. Subscriptions renew every 30 days | https://docs.novelai.net/en/subscription/ (vendor docs; novelai.net/pricing 404s) | CONFIRMED |
| Midjourney | ~$10/month | **Basic $10/month; annual $96 ($8/month)**. Standard $30, Pro $60, Mega $120 per month. Companies with more than $1M gross annual revenue must buy Pro or Mega | https://docs.midjourney.com/hc/en-us/articles/27870484040333-Comparing-Midjourney-Plans | CONFIRMED |
| Adobe Firefly | $5-10/month | **Firefly Standard US$9.99/month** (2,000 credits). Pro US$19.99 (US$9.99 for the first 6 months, offer ends Dec 6). Pro Plus US$49.99. **No ~$5 tier seen.** | https://www.adobe.com/products/firefly/plans.html | **CORRECTED** (via WebFetch; direct fetch 403) |
| Firefly IP indemnification | "nobody checked Adobe's indemnity terms" | Plans page: "Enterprise customers can also access ... IP indemnification through enterprise-specific plans" and "Eligible enterprise customers can also receive IP indemnification for select Adobe Firefly outputs." **No individual or team plan lists indemnity.** The page does call outputs "safe for commercial use" | same | CONFIRMED: enterprise only (via WebFetch). Adobe's legal product description (helpx) returned 403 |
| Atticus | $147 once, cross-platform | **$147**; FAQ: "Atticus is a one-time purchase and will include all future updates". Windows, Mac, Linux, Chromebook. (The $249 on the page is Atticus's Vellum comparison column) | https://www.atticus.io/ | CONFIRMED |
| Vellum | $199.99-$249.99, Mac only | **Vellum Ebooks $199.99; Vellum Press $249.99** (ebooks + paperbacks), "Price does not include tax". DE: €179.99 / €219.99 excl. VAT. "Vellum is only available for Mac", macOS 14 or newer | https://vellum.pub/ | CONFIRMED. Note: print needs Press ($249.99) |
| Reedsy Studio | free | "Studio's core writing and formatting features are completely free". Premium add-ons exist (Studio Essential, Outlining), 30-day trial; prices not captured | https://reedsy.com/studio | CONFIRMED (core free) |
| KDSpy | $79 one-time | **$79 one-time**, "zero monthly recurring fees" (shown as a discount from a "regular" $197). 60-day refund. Browser extension, PC and Mac | https://www.kdspy.com/ | CONFIRMED |
| Publisher Rocket | $199 one-time | **$199 "One-Time Payment"**, lifetime access (struck-through $299) | https://publisherrocket.com/ | CONFIRMED |
| ProWritingAid | about $120/yr | Premium **€120/year (€10/month billed yearly)**; €30/month billed monthly; lifetime €399. Premium Pro €144/year, €36/month, €699 lifetime. USD not shown to this IP | https://prowritingaid.com/pricing | CONFIRMED in EUR only (USD NOT FOUND) |
| Bowker ISBN | 1 for $125, 10 for $295 | **1 ISBN $125; 10 for $295** ($29.50 each); 100 for $575; 1,000 for $1,500; 1 ISBN + barcode $150. **Bowker is "the official ISBN Agency for publishers physically located in the United States and its territories"** | https://www.myidentifiers.com/identify-protect-your-book/isbn/buy-isbn | CONFIRMED. **Flag:** German partners are not Bowker customers. A German ISBN comes from the German agency (MVB); its price was not checked |
| KDP free ISBN | free for print, KDP-only; ebooks need none | "You can use a free ISBN from KDP (paperback and hardcover books only)"; "Free ISBNs from us can only be used on KDP"; imprint shows "Independently published"; "eBooks and low-content books are the only formats where an ISBN is optional" | https://kdp.amazon.com/en_US/help/topic/G201834170 | CONFIRMED |
| Human cover (Reedsy) | $880 avg, mostly $625-$1,250, 9,600+ projects | "we analyzed over 9,600 cover design collaborations on Reedsy in 2025 ... average cost ... is $880 ... most projects fall between $625 and $1,250" | https://reedsy.com/blog/book-cover-design-cost/ | CONFIRMED. Note: Reedsy's own self-publishing cost guide says "Cover design: $930 on average" |
| Copy edit / proofread, 80k words (Reedsy) | $2,160 / $1,600 (via Chapter) | Reedsy's table for an 80,000-word book: Developmental **$2,880**, Copy editing **$2,160**, Proofreading **$1,600**. Total editing "$2,160 and $5,050" (heading says $2,160-5,040) | https://reedsy.com/blog/guide/how-to-self-publish-a-book/cost-to-self-publish/ | CONFIRMED on Reedsy's own page (the citation can move from Chapter to Reedsy) |

## Recomputed setup totals (first year, USD)

These totals use list prices verified above, with the report's components. Assumptions: a chatbot costs $240/yr at $20/month, or $200/yr on Claude annual. ChatGPT's USD price is unverified, so $240 is assumed; in EUR it costs €276/yr (€23 x 12). Prices exclude any VAT not shown.

| Setup | Arithmetic | Recomputed | Report | Status |
|---|---|---|---|---|
| Lean (one title) | Low: Claude Pro annual $200 + Midjourney Basic 3 months $30 = **$230**. High: one chatbot monthly $240 + Firefly Standard 12 x $9.99 = $119.88 → **$359.88**. Reedsy Studio, KDP ISBN and free grammar tiers cost $0 | **about $230-$360** | $300-$450 | **CHANGES.** Components can't reach $450, and the low end can be lower |
| Recommended, base | Low: $480 (2 x $240) + Atticus $147 + AI images $60 (6 months Midjourney Basic) = **$687**. High: $480 + $147 + $120 (Midjourney 12 x $10, or Firefly $119.88) + KDSpy $79 + ProWritingAid ~$120 (€120) = **$946**. Using Claude annual instead lowers each end by $40 ($647) | **about $690-$950** ($650 with Claude annual) | $700-$950 | Holds |
| Recommended + one human cover | $687 + $880 = **$1,567**; $946 + $880 = **$1,826** (Reedsy's typical range $625-$1,250 gives $1,312-$2,196) | **about $1,570-$1,830** | $1,550-$1,850 | Holds |
| Comfortable (first title) | Low: NovelCrafter Hobbyist 12 x $8 = $96 + Atticus $147 + Publisher Rocket $199 + cover $880 + copy edit $2,160 + 1 Bowker ISBN $125 = **$3,607**. High: Sudowrite Max 12 x $59 = $708 + Vellum Press $249.99 + Rocket $199 + cover $880 + copy edit $2,160 + 10 Bowker ISBNs $295 = **$4,491.99**. With a $1,250 cover the high end is $4,861.99; adding two chatbots ($480) gives $4,971.99. Excludes NovelCrafter API spend and any proofread ($1,600) | **about $3,600-$4,500** (up to ~$5,000 with a top-range cover and chatbots) | $3,500-$5,500 | **Partly changes.** The low end holds. The listed components don't reach $5,500 unless a proofread or other items are added |

### Notes for the report writer
1. **Firefly:** "$5-10/month" should read "about $10/month" (US$9.99). Firefly's IP indemnity applies only to eligible enterprise plans, not the individual plan two partners would buy. "Safest for commercial use" is Adobe's own claim, not indemnified coverage.
2. **ChatGPT Plus:** the USD price could not be read. The German price is €23/month, so two chatbots cost German buyers about €492/yr (ChatGPT €276 + Claude €216 monthly), not $480.
3. **Bowker is US-only.** For German partners, the "Bowker ISBNs" line in the comfortable setup should become a German ISBN agency purchase (price not verified here), or KDP's free ISBN.
4. **Vellum** needs Press ($249.99) for print, and Ebooks ($199.99) covers ebook only. It runs only on macOS 14 or newer.
5. **Editing and cover figures** can be cited to Reedsy directly instead of Chapter. Reedsy's two pages disagree on the average cover cost ($880 vs $930).
6. **Annual billing** lowers several items: Claude $17/month, Sudowrite $10/$22/$44 per month, Midjourney $8/month, NovelCrafter "2 months off".
