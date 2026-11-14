# Verification: categories and earnings track

- **Date accessed:** 2026-11-14
- **Scope:** Report section "Money concentrates in genre series, while AI floods the low-content shelves" (all subsections, the category table and "What a sale and a page read pay"), the earnings figures in the opening paragraph, and the "Time to income" paragraph.
- **Method:** I fetched primary pages with `curl -sL -A 'Mozilla/5.0'`. I rendered JS or bot-blocked pages (AuthorMedia, the KDP community forum, Substack) with Playwright/Chromium. I parsed HTML with a stdlib Python script. pdftotext and pypdf were not available, so for PDFs I used a stdlib zlib stream extractor with glyph decoding, and I extracted the embedded slide images from the ALLi PDF and read them visually. I also read chart images from Written Word Media directly. Raw downloads are in `scratchpad/dl_earn/`.
- **Status key:**
  - **CONFIRMED:** read on the authority's own page or paper.
  - **CORRECTED:** the primary source gives a different value; the right value is stated.
  - **CONTRADICTED:** the primary source says otherwise.
  - **NOT FOUND ON PRIMARY:** the figure does not appear on the primary source.
  - **PRIMARY UNREACHABLE:** the primary source could not be opened.
  - **SECONDARY ONLY:** the source the report cites is itself secondary, so the claim was checked against that page only.

---

## A. Written Word Media (WWM) 2025 indie author survey

Primary page: https://www.writtenwordmedia.com/2025-indie-author-survey-results-insights-into-self-publishing-for-authors/. The `/2025-indie-author-survey-results/` URL serves the same page. It was published 2025-12-02 and modified 2026-01-15.

**A1. "1,346 responses, self-reported, skewed toward prolific commercial-fiction writers"**
- WWM: "Among the 1,346 authors who responded…". Also: "Because Written Word Media's audience skews toward commercial indie fiction, our genre mix reflects that." Romance is 21%, fantasy 14%, sci-fi 8%, thriller 8%, mystery 7%.
- **CONFIRMED.**
- One nuance: WWM says the sample skews toward commercial fiction, not toward "prolific" writers. Calling it prolific is the report's inference, although it is a fair one given the catalogue averages in A6.

**A2. "44% earn $100 or less a month"**
- WWM: "While 44% of authors earn $100 or less, the majority—56%—are earning over $100 monthly."
- **CONFIRMED** on WWM's own page. It no longer needs the label "figures from a secondary analysis".

**A3. "13% earn over $5,000 and 8% earn over $10,000"**
- WWM: "authors making over $5,000 per month account for 13% of respondents… 8% of authors who answered the survey report making over $10,000 per month."
- Bar chart: under $100 ≈44%, $101-499 ≈22%, $500-999 ≈5%, $1,000-4,999 ≈15%, $5,000-9,999 ≈5%, over $10,000 ≈8%.
- **CONFIRMED.** The two bands overlap: the 8% is part of the 13%.

**A4. "About 80% of authors with 1-3 books earning under $100 a month"**
- WWM, section 5: "Authors with 1–3 books: About 80% fall into the under $100/month band."
- **CONFIRMED.**
- New details from the same passage: authors with 5-9 books have a "median income… around $50/month". Authors with 25+ books have a "median income ≈ $3,000/month" and "40%+ of them earn $5,000+/month".

**A5. "Authors earning $5,000-7,500 a month had a median catalogue of about 30 titles"**
- WWM has no $5,000-7,500 band and reports no median catalogue by band. The bands are under $100, $100-499, $500-999, $1,000-4,999, $5,000-9,999 and over $10,000.
- The chart "Books Published By Monthly Earnings" (`wp-content/uploads/2025/11/Books-Published-Over-Monthly-Earnings-1.png`) shows **average** books published, read off the bars:

  | Monthly income | Average books (approx.) |
  |---|---|
  | Under $100 | ≈10 |
  | $100-499 | ≈13 |
  | $500-999 | ≈26 |
  | $1,000-4,999 | ≈35 |
  | $5,000-9,999 | ≈54 |
  | Over $10,000 | ≈63 |

- **NOT FOUND ON PRIMARY.** Corrected reading: $5k-10k earners average about 54 books, and $1k-5k earners average about 35.

**A6. "Median titles by income band" (requested check)**
- WWM 2025 publishes **averages** by income band (the chart above), not medians.
- Its only median-type statements run the other way: median income by catalogue size (5-9 books ≈ $50/month; 25+ books ≈ $3,000/month).
- ALLi's commentary (https://selfpublishingadvice.org/written-word-media-opens-2026-indie-author-survey/, 2026-10-03) paraphrases this as "those earning $10,000 or more a month generally having over sixty titles".
- **CORRECTED.** The values are averages, and they are higher than the report implies.

**A7. "Authors with 10+ books and an engaged email list were the most likely to earn full-time income, though the survey itself warns this is correlation"**
- WWM: "The $1,000+ group almost always has: More books (often 10+, and very often series); An active email list; Regular marketing spend."
- Email (section 12):
  - Average list size by band: under $100 = 902; $100-500 = 1,405; $500-1k = 2,743; $1k-5k = 3,986; $5k-10k = 7,488; over $10k = 18,327.
  - "Authors with an email list earn a median of ~$300/month. Authors without a list earn a median of ~$15/month. That's a 20x difference."
- Correlation caveats appear on the page ("Correlation vs Causation", in the KU section; "This doesn't prove that 'spend = success'", in the marketing section). They are not attached to the email finding specifically.
- **CONFIRMED in substance.** Adding the email figures would strengthen the paragraph.

**A8. "Amazon top revenue source for 83%" (from the notes)**
- WWM: "83% of respondents naming it as their top revenue source… from 91% in 2023 to 87% in 2024 and 83% this year."
- **CONFIRMED.**

**A9. "No survey splits income by AI use"**
- WWM 2025: there is no AI question. ALLi's commentary confirms: "I don't think… there was an AI question last year. There is one this year."
- The WWM 2026 mid-year survey (see New findings) reports AI attitudes by income stage, but not income by AI use.
- ALLi 2025 reports AI use and perceived impact ("70 percent said its use as a tool had 'some impact' or a 'strong positive impact'") but no income split.
- **CONFIRMED.** Still true as of 2026-11-14.

**A10. Does a 2026 WWM survey exist?**
- WWM's **2026 Mid-Year Author Survey** (https://www.writtenwordmedia.com/2026-mid-year-indie-author-survey/, 2026-06-23) has 582 respondents and uses different income tiers.
- The **2026 end-of-year survey** opened in October 2026 (ALLi news, 2026-10-03). Its results were not published as of 2026-11-14: https://www.writtenwordmedia.com/2026-indie-author-survey-results/ returns 404, and the WWM RSS feed to 13 Nov 2026 has no results post.
- **CONFIRMED.** Partial 2026 data exists; the full 2026 survey results are pending.

## B. Older survey: "17 books / 29 books"

**B1. "Older survey data (year unverified, pre-2024) puts $250-999/month at about 17 books on average and $1,000-4,999 at about 29"**
- The real source is the WWM **2020** author survey, "The Evolution of an Author: How to Go from Zero to $100k from Your Writing": https://www.writtenwordmedia.com/the-evolution-of-an-author-how-to-go-from-zero-to-100k-from-your-writing/. It was published 2020-12-04 and had "over 1,000 authors".
- WWM's figures:

  | Stage | Monthly income | Average books |
  |---|---|---|
  | One | $0-249 | "around 6" |
  | Two | $250-999 | "average 17" |
  | Three | $1,000-4,999 | "an average of 29" |
  | Four | $5,000-9,999 | "over 36" |
  | Five | Over $10,000 | 42 (per the Goodreads blog that quotes it) |

- The Goodreads blog the report cites is Rachel Neumeier's post of 17 Dec 2020, quoting this WWM page.
- **CONFIRMED** on WWM's own page. Year: **2020**. These are **averages**, and WWM itself notes "these numbers are averages."

## C. ALLi 2025 author income survey

Primary source: ALLi, "The Big Indie Author Data Drop 2025" (PDF, Dec 2025): https://www.allianceindependentauthors.org/wordpress/wp-content/uploads/2025/12/The-Big-Indie-Author-Data-Drop-2025-UPDATE-PAGES.pdf. Also ALLi's facts page, https://www.allianceindependentauthors.org/facts/ (the `?p=483` URL; modified 2026-07-23).

The page the report cites, https://selfpublishingadvice.org/2025-author-income-survey/, is the survey **launch** announcement (2025-09-11) and contains no 2025 results.

**C1. "$13,500 median annual income"**
- PDF slide "2025 Income survey results: median": last year (gross) **$13,500**; year before $10,001; prior survey $12,749; "Growth since 2023 survey 6%"; "All figures normalized to USD."
- Facts page: "median self-published author income was $13,500, growing at a healthy 6% year-on-year."
- **CONFIRMED.**
- Notes:
  - The figure is **gross** income.
  - The facts page calls the 6% "year-on-year", but the slide shows it is growth since the 2023 survey, about two years. Within-survey growth from the prior year was 35% ($10,001 to $13,500).
  - ALLi also says the 2023 survey's median was for **2022** income. That explains why the notes found the $12,749 figure labelled with two different years.

**C2. "It covers only authors who spend over half their working time on publishing or earn over half their income from it"**
- Launch page eligibility: "must have independently published at least one book in English, and must spend at least half their time on or make half their income from activities related to writing and publishing."
- PDF: "Over 1,800 responses were received from indie authors globally, with 1,520 qualified responses."
- **CONFIRMED.** Add **n = 1,520 qualified** (from more than 1,800 responses). The 2023 survey had "over 2,000".

**C3. "One report puts the mean in the same sample above $80,000 [unverified]"**
- PDF slide "2025 Income survey results: averages": last year (gross) **$84,995**; year before $70,643; 2023-survey average $82,607.
- **CORRECTED and now verified:** the 2025 mean is **$84,995**.
- The "over $80,000" figure the report found came from the **2023** survey page (https://selfpublishingadvice.org/incomesurvey/, 2023-04-17: "The average income was over $80,000"; the chart shows mean 82k vs median 12k). The two surveys give similar means, so the report's conclusion that a few authors earn most of the money still holds.

**C4. "Earlier ALLi median $12,749" (from the notes)**
- 2023 survey page: "In 2022, the median income of 'primary income' self-publishing authors… was $12,749."
- **CONFIRMED.** It is 2022 income, from the survey published in 2023.

**C5. Average catalogue (new)**
- PDF: "The average is now approximately 14 books per author." The facts page says the same: "average number of books… was 14."

## D. AI-books preprint (arXiv 2607.20349) and the NBER paper

Primary: Chakrabarty, Liu, Ginsburg & Dhillon, "Generative AI floods and dilutes the market for books", arXiv:2607.20349. v1 was submitted 22 Jul 2026; I read **v3 (3 Aug 2026)**, full text at https://arxiv.org/html/2607.20349v3. It is labelled "Working Paper Under Review".

**D1. Authorship (the report implies this paper may be by Reimers & Waldfogel)**
- The arXiv authors are Tuhin Chakrabarty, Xinyue Liu, Jane C. Ginsburg and Paramveer Dhillon. AI Weekly lists the affiliations as Stony Brook, Columbia Law, Michigan/MIT; I did not check those on arXiv.
- Reimers & Waldfogel is a **separate** NBER paper (w34777), which the arXiv paper cites as ref. [12] and contrasts with its own method.
- **CONTRADICTED.** "Coverage that appears to describe the same study" is wrong: there are two different studies.

**D2. "14,419 self-published genre-fiction titles (2023 to June 2026)"**
- Paper: "14,419 randomly selected self-published ebooks belonging to genre fiction that were published between January 2023 and March 2026… daily sales through June 2026."
- **CONFIRMED, with one correction to the window:** releases ran from Jan 2023 to Mar 2026, and sales were tracked to 29 June 2026.

**D3. Sales panel**
- Paper: a "proprietary panel maintained by a major 'Big Five' publisher… approximately 500,000 ASINs… approximately 95% or more of daily unit volume in the eBook market."
- **CONFIRMED.**

**D4. "Substantial AI text 20% of titles, 12.1% of sales, 11.3% of revenue"**
- Paper: "Books with substantial AI text make up 20% of all books in our sample but earn only 12.1% of sales and 11.3% of revenue." Table 1: 2,880 titles at the >25% cutoff.
- **CONFIRMED.** "Substantial" means more than 25% of the full text was flagged by the detector.

**D5. "No-AI books 62.9% of titles and 72.5% of revenue"**
- Paper: "books with no AI text account for 62.9% of books and a larger 71.7% of sales and 72.5% of revenue."
- **CONFIRMED.**

**D6. "Titles with any sales grew 19.2x while revenue grew 8.9x"**
- Paper: "Between January 2023 and March 2026, the cumulative catalog of released books grew 38.3-fold and the number of books selling in a quarter grew 19.2-fold. Meanwhile, the quarterly sales and revenue grew only 7.3-fold and 8.9-fold."
- **CONFIRMED.** These are multiples of the 2023 Q1 level as of 2026 Q1, measured within the sampled set.

**D7. "Revenue per book fell in six of eight genres" (the report attributes this to Reimers & Waldfogel coverage)**
- arXiv paper: "Revenue per book fell in six of eight genres for all books… and in seven of eight for books with no AI text alone… when comparing the 2023 and 2025 launch cohorts."
- **CONFIRMED but misattributed.** The finding belongs to the arXiv paper (Chakrabarty et al.), not to Reimers & Waldfogel.

**D8. "About half of 2025 books sold on Amazon contain AI text, up from 23% in 2023" (Reimers & Waldfogel)**
- Primary: NBER Working Paper 34777, "AI and the Quantity and Usage [earlier: Quality] of Creative Products: Have LLMs Boosted Creation of Valuable Books?". It was issued Jan 2026 and revised; I read both the rev1 PDF and the current PDF at https://www.nber.org/papers/w34777.
- Abstract: AI-containing books' "rising share – topping half of 2025 releases".
- Table, column "AI share" ("the weighted average annual AI-detected share"): **2023 23.12%, 2024 33.57%, 2025 52.70%**.
- Text: the AI-detected share of titles "peaks at 30 percent in 2023, 45 percent in 2024, and over 60 percent in 2025" (monthly peaks).
- Detection used Pangram on **1,000-word Amazon previews** of a 48,193-title subsample across all categories, not only fiction.
- **CORRECTED.** The figures cover **new e-book releases**, not "books sold". "About half of 2025 releases, up from about 23% in 2023" is right as a weighted annual average. The monthly peaks are 30%, 45% and over 60%.

**D9. "Amazon reportedly said its internal metrics did not show that growth but declined to share figures" (cited to AI Weekly)**
- The AI Weekly page (https://aiweekly.co/alerts/study-ai-books-gain-amazon-share-as-catalog-outpaces-revenue) contains no Amazon statement, and neither does The Decoder's article.
- **NOT FOUND ON PRIMARY** (nor on the cited secondary). Drop it, or find the real source.

**D10. "AI-heavy output earns less per title than human writing on average"**
- Consistent with D4/D5 in the arXiv paper, and with the NBER finding that "AI-containing books are less used".
- **CONFIRMED** as an average.
- The arXiv paper also finds that the no-AI lead **narrowed** across cohorts, and that some AI titles reached high revenue (see New findings).

## E. Category table

**E1. "Romance is about 55% of top-100 Kindle titles"**
- The figure appears in AuthorMedia's *mystery/thriller* segment (23 Mar 2026), https://www.authormedia.com/zeitgeist-mystery-thriller-suspense-k-lytics-report/: "MTS accounts for 33% of the top 100 Kindle titles. Romance leads with 55%, and women's fiction sits at 9%." It does not appear on the romance-segment URL the report cites.
- The cited romance page (3 Mar 2026) instead says "Romance accounts for roughly 70% of Kindle ebook sales on Amazon."
- **SECONDARY ONLY.** The figure is correct as relayed from K-lytics, but the citation URL is wrong. The K-lytics reports themselves are paid and were not read.
- Note that 55 + 33 + 9 is more than 100%, so titles evidently count in several categories.

**E2. "Top-100 titles averaging about 641 estimated daily sales"**
- AuthorMedia romance page: "K-lytics reports an average sales rank of 93 for the top 100 **romance** titles, which translates to an estimated 641 daily sales per title. By comparison, mystery, thriller, and suspense average about 218… science fiction and fantasy… around 283."
- **CORRECTED.** The 641 figure is for the top 100 *romance* titles, not top-100 Kindle titles overall. Secondary source, and the figure is a K-lytics model estimate.

**E3. "Its share is loosening" (Jane Friedman)**
- https://janefriedman.com/romances-grip-on-kindle-bestseller-lists-is-loosening/ (2026-08-19) is paywalled. The public teaser reads: "While romance remains the top-selling genre for Kindle, its share of the market dropped in the US, with mystery/thriller/suspense gaining."
- **CONFIRMED (teaser only).** Secondary source.

**E4. "Mystery/thriller about 33% of top-100 and gaining share"**
- 33%: see E1. "Gaining": Jane Friedman teaser. AuthorMedia MTS page: "Over the last six months, the category has shown a modest upward trend."
- **SECONDARY ONLY.** Consistent with the cited sources.

**E5. "Cozy fantasy, LitRPG named by K-lytics as the hottest niches of 2026"**
- AuthorMedia (13 Jul 2026), on the K-lytics Summer 2026 SF&F reports: "Cozy Fantasy is the single best opportunity in the entire report, with a 23.1 sales-to-competition ratio… 60 daily sales per top-20 title against only 2,576 competing books." Also: "GameLit & LitRPG… posts a 14.8 ratio… LitRPG is the most structurally undersupplied success story."
- **SECONDARY ONLY.** It matches the source. The headline "hottest niches" is AuthorMedia's wording; K-lytics' metric is a demand-to-supply ratio.
- Useful context from the same page:
  - SF&F supply grew 18% in a year (983,093 to 1,162,272 titles).
  - 78 of the top-100 Fantasy titles are in KU, taking 83% of royalties.
  - 89% of Fantasy bestsellers are in series.
  - K-lytics' royalty figures are "estimates modeled from sales rank".

**E6. Low-content: "gold rush that got crowded" (Naomi Jane) and "2025 algorithm change hurt listings" (The Write Moves)**
- Naomi Jane (2025-12-15): "low-content books on Amazon KDP felt like a gold rush… The low/medium content ecosystem is huge - and also very crowded." **CONFIRMED** (secondary blog).
- The Write Moves URL returns 404 as of 2026-11-14. **PRIMARY UNREACHABLE** (dead link).

**E7. "One anecdote: $18k over four years (about $375/month)"**
- The figure does not appear on the cited Naomi Jane post, in either the curl or the Playwright render. The page has no figures for $18k, earnings or four years.
- **NOT FOUND.** Drop it, or find the real source.

**E8. "About 70% of books built in one AI tool fall in illustrated/activity/children's formats" (KDP Builder)**
- The KDP Builder page was revised on 9 Sep 2026 and is now titled "KDPBuilder Platform Snapshot 2026: 484 Projects, 331 Creators". Its change log lists the first-edition claim "70% illustrated or activity titles; fiction 8.7%" as corrected.
- Current text: "Illustrated or activity titles (adding children's books) reached 59.1% (286 of 484)… Fiction was 8.1%." It adds: "It is not a survey of authors, not a sample of Amazon KDP, and not industry research."
- **CORRECTED:** the value is **59.1%** of 484 project starts. Vendor data, and very small.

**E9. "Originality.ai scan found AI in 77-90% of 844 self-help titles"**
- Originality.ai's own page: https://originality.ai/blog/likely-ai-success-self-help-book-study. It describes "a study of 844 books in Amazon's 'Success' subcategory… all published… between Aug. 31 and Nov. 28 [2025]". Findings:
  - 762 books (90%) likely used AI in at least one of three elements: description, author bio, sample text.
  - 651 (77%) had likely AI writing in the book sample.
  - 666 (79%) had likely AI-written summaries.
- **CONFIRMED** on the primary page.
- Precision: the sample is the "Success" subcategory of Self-Help, books published in that three-month window. The test was run on samples and previews, not full texts. Originality.ai sells AI detection, so it has a commercial interest. The KuCoin summary can be replaced with the primary URL.

## F. What a sale and a page read pay (KDP)

**F1. "Ebook royalties are 35% or 70%"**
- KDP help G200644210: "You can choose between two royalty options for each of your eBooks: the 35% royalty option and the 70% royalty option."
- **CONFIRMED.**

**F2. "70% has historically required $2.99-$9.99" and "two secondary sites say the band widened to $12.99 from 7 July 2026 [unverified/conflicting]"**
- KDP help G200634560, "eBook List Price Requirements": "Effective July 7, 2026, the 70% royalty option price band is $2.99-$12.99 on Amazon.com, expanding from the previous range of $2.99-$9.99, with equivalent changes in other KDP marketplaces."
- FAQ: "The previous $9.99 maximum list price for the 70% royalty option has been in place since 2007."
- UK and EU maximums are now £12.99 and €12.99; India is ₹… up to 15.99 in that table.
- **CONFIRMED by Amazon.** The current 70% band is **$2.99-$12.99**. Remove the "unverified/conflicting" label.

**F3. "Delivery fee of $0.15 per MB in the US"**
- KDP help G200634500, "Digital Book Pricing Page" (last updated 21 Apr 2026): "Amazon.com: US $0.15/MB". Amazon.de/fr/es/it/nl are €0.12/MB; Amazon.co.uk is £0.10/MB.
- G200644210 adds: "average delivery costs are $0.06 per unit sold."
- The price-band FAQ confirms the delivery-cost rule did not change.
- **CONFIRMED.** Note that the US rate sits on G200634500, not on G200644210.

**F4. "Paperback royalty is 60% of list price minus printing cost"**
- KDP help G201834330, "Paperback Royalty": "KDP now offers both a 50% or 60% royalty rate on paperbacks… The royalty rate for your title depends on the list price."
- For Amazon.com: **50% at list prices ≤ $9.98, 60% at ≥ $9.99**. Amazon.de and other EU stores: 50% at ≤ €9.98.
- Expanded Distribution pays 40%. Royalty = (rate × list price) − printing costs.
- **CORRECTED.** The rate is 60% only at a list price of $9.99 or more; cheaper paperbacks earn 50% minus printing.

**F5. "Kindle Unlimited pays from a monthly fund divided by total pages read (KENP)"**
- KDP help G201541130, "Royalties in Kindle+": "The amount you earn from the KDP Select Global Fund will be determined based on your share of total pages read or listened to by Kindle+ subscribers… We announce the size of the fund monthly in our community forum."
- KENP help G5HHMLVVEW48MQYW: "a maximum of 3,000 Kindle Edition Normalized Pages (KENP) Read per title per customer."
- **CONFIRMED.** Kindle Unlimited has been renamed **Kindle+**, and audiobooks now draw on the same fund (see New findings).

**F6. "Trackers put it at roughly $0.0042-$0.0050 per page in 2025-2026, e.g. about $0.00482 in April 2026"**
- Amazon announces the **fund size** but does not publish a per-page rate. profitable.app: "Amazon publishes the Global Fund directly but does not publish the resulting per-page rate". WWM's KDP fund page computes its rate from dashboard data ("We manually calculate the rate using the subscription royalties divided by the total KENP pages (filtered for the US)").
- WWM US per-page series (https://www.writtenwordmedia.com/kdp-global-fund-payouts/, updated 20 Oct 2026):

  | Month | US per-page rate |
  |---|---|
  | Jan 2025 | $0.004091 |
  | Apr 2025 | $0.004443 |
  | Jul 2025 | $0.004192 |
  | Oct 2025 | $0.005007 |
  | Jan 2026 | $0.004202 |
  | Apr 2026 | $0.004820 |
  | May 2026 | $0.004888 |
  | Jun 2026 | $0.004615 |
  | Jul 2026 | $0.004221 |
  | Aug 2026 | $0.005170 |
  | Sep 2026 | $0.005365 |

- profitable.app: April 2026 = $0.00482.
- **CORRECTED** (secondary trackers, which agree with each other). The range is **about $0.0041-$0.0054 across Jan 2025 to Sep 2026**. The April 2026 value of $0.00482 is confirmed by both trackers. The latest value (Sep 2026) is $0.005365.

**F7. KDP Select Global Fund: Amazon's own figure (requested check)**
- KDP Select page (https://kdp.amazon.com/self-publishing/KDPSelect, server-rendered banner): "Total KDP Select Author Earnings **October 2026 • $71.1 Million**."
- **CONFIRMED** for October 2026.
- Earlier months were not reachable on Amazon: the KDP community announcements thread is JS-only and its old URLs 404. WWM's series, which it says comes "directly from Amazon":

  | Month | Global Fund |
  |---|---|
  | Jan 2026 | $62.2M |
  | Feb 2026 | $61.7M |
  | Mar 2026 | $65.9M |
  | Apr 2026 | $64.3M |
  | May 2026 | $66.9M |
  | Jun 2026 | $63.6M |
  | Jul 2026 | $67.6M |
  | Aug 2026 | $66.0M |
  | Sep 2026 | $65.9M |

- The notes' "$69.3M for September 2026" conflicts with WWM's $65.9M. The KDP page now shows October, so September could not be re-checked on Amazon. **PRIMARY UNREACHABLE** for months before October 2026.

**F8. Arithmetic: "300-page read ≈ $1.35 at $0.0045; $4.99 sale at 70% ≈ $3.40"**
- 300 × 0.0045 = $1.35.
- 0.7 × $4.99 = $3.49, minus delivery (about $0.06-0.15 for 0.4-1 MB) ≈ $3.34-3.43.
- **CONFIRMED** [inference].
- At the Sep 2026 rate of $0.005365, a 300-page read pays about $1.61.

## G. Opening paragraph and "Time to income"

**G1. "Roughly 80% of authors with 1-3 books earn under $100 a month"**
- See A4. **CONFIRMED.**

**G2. "$1,000+ a month tends to coincide with about 20-30 titles"**
- WWM 2020: $1,000-4,999 averages 29 books.
- WWM 2025: $1,000-4,999 averages about 35, and $500-999 about 26.
- **CORRECTED.** Current data says about 35 titles on average for $1k-5k/month, and over 50 for $5k+. These are averages, and the mean is skewed by very prolific authors.

**G3. "Meaningful monthly income coincides with roughly 17-30 titles"**
- The 17 and 29 figures are 2020 WWM averages. The 2025 figures are higher: about 26 books for $500-999 and about 35 for $1k-4,999.
- **CORRECTED.** Use about 25-35 titles (2025 averages), or state that the figures date from 2020.

**G4. Time to income: "under $100/month at 1-3 books, about $250-999/month around 17 books, about $1,000+/month around 20-30 books"**
- The first is confirmed (2025). The other two are 2020 averages with different band edges.
- Also, under-$100 authors in 2025 average about 10 books, not 1-3. Many authors with sizeable catalogues still earn under $100.
- The pacing arithmetic ("17 titles takes about 17 months…") rests on the outdated 17/29 figures. At 2025 averages, 26 and 35 titles mean about 26 and 35 months at one book a month, or about 4.3 and 5.8 years at one book every two months.
- **CORRECTED.**

**G5. "A 2026 study reports books with substantial AI text ≈20% of titles but ≈11% of revenue; revenue per title falling"**
- See D4 and D6. **CONFIRMED.**

---

## New findings

1. **Kindle Unlimited is now "Kindle+" (since 22 Oct 2026), and audiobooks are paid from the same fund.**
   - KDP's help and Select pages now say Kindle+.
   - Per KDP help G201541130, enrolled ebooks and audiobooks earn from the KDP Select Global Fund, "measured in Kindle Edition Normalized Pages (KENP)". Each page is paid once per subscriber across formats, and immersive reading pays the higher rate.
   - WWM (22 Oct 2026): Virtual Voice audiobooks are **auto-included** when the ebook is in KDP Select. ACX titles qualify only if exclusive with Whispersync, and Royalty Share titles are excluded at launch. Amazon has not announced per-format rates.
   - Implication: page reads now compete with audiobook "pages" for the fund. The per-page rate after October 2026 is unknown. The report's KU wording and its KENP arithmetic should be qualified.
2. **The 70% ebook band rose to $2.99-$12.99 on 7 July 2026** (Amazon, G200634560). This is the first change since 2007, and it raises the per-sale royalty ceiling. At $12.99, 70% is about $9.09 minus delivery.
3. **Paperback royalty is two-tier:** 50% below $9.99 and 60% at $9.99 and above on Amazon.com. Most genre-fiction paperbacks priced at $12.99-$16.99 get 60%.
4. **WWM 2026 mid-year survey** (582 self-selected respondents, June 2026):
   - Overall: 30% report a declining business, 23% growing, 22% steady. The "Got Traction" tier ($2,500-10,000/month) has the most decline, at 36%. Respondents attribute it to "the Amazon A10 algorithm change" and ACX royalty restructuring.
   - "Growing" authors are more likely to be accelerating output (64% vs 36%), using a newsletter (58% vs 43%), doing translations (38% vs 23%), and using AI as a tool for ads, covers, translation and narration.
   - Starting-out authors see AI "almost entirely negatively" ("Fast buck AI books flooding the market making discoverability almost impossible").
   - KDP exclusive vs wide made no difference among optimistic authors (46% vs 47%).
5. **The 2026 WWM end-of-year survey includes an AI question** (ALLi, 3 Oct 2026). Results are not out yet; they could provide the first income-by-AI-use data.
6. **ALLi 2025 (n = 1,520 qualified):**
   - Median gross income $13,500 and mean $84,995. The mean is about 6.3 times the median.
   - Average catalogue about 14 books.
   - "A notable drop in the Amazon-exclusive distribution model and a corresponding rise in the creator [direct-sales] model."
   - Among authors who use AI, 67% use it for images and 77% for promotional text.
7. **Methods and limits of the arXiv paper (Chakrabarty et al.):**
   - Detection: Pangram v3.3 on full texts, chapter by chapter. The vendor reports a 0.04% false-positive and 0.14% false-negative rate. That is vendor-reported, and The Decoder notes a newer Pangram 4 exists.
   - Sample: stratified random sample of 15,000 drawn from titles whose sales rank ever went below 1.5 million, of which 14,419 were analysed. Eight genre clusters; General Romance is 28.8% of the sample.
   - Revenue is **gross consumer spending** before Amazon's cut. The panel **does not separate KU page reads from purchases**.
   - Bylines are counted per pen name, so output is understated.
   - Results are observational; the KU finding is "heterogeneity… not… a causal effect".
   - The no-AI lead **narrowed** across cohorts. In KU-heavy genres it is 8.5 points (sales) and 8.4 points (revenue) smaller.
   - Some AI books do succeed. The top AI byline grossed $1.7M from 8 titles; the top AI book took $643K on 80,431 sales; 287 of 385 continuing AI adopters raised their output.
   - Successful AI books reuse more rare expressions from existing books (45.0% vs 37.7% for Top-50).
   - In Fantasy/Supernatural/Horror, where AI arrived "latest and least", no-AI revenue per book **rose 35%**.
   - The paper calls itself a "Working Paper Under Review", and some text was AI copy-edited (disclosed).
8. **Reimers & Waldfogel (NBER w34777) is separate and broader.**
   - Data: a stratified random sample of about 333,000 releases representing about 10 million Amazon ebooks from 2020 to 2025, plus AI detection on 1,000-word previews of 48,193 titles.
   - Monthly releases rose from about 100k to over 300k by late 2025.
   - AI books are "less used". "Author selection accounts for most of the AI usage differential". Incumbent authors kept non-AI output stable.
   - The paper thanks Pangram Labs for support.
   - Consumer-surplus estimates differ between the paper (about 7% in 2025) and the NBER Digest (about 5% for 2023-25 and about 10% at the peak rate). They come from different scenarios.
9. **K-lytics context (via AuthorMedia, secondary):** SF&F competing titles grew 18% in a year while top-of-category demand was "trending sideways over the past 18 months". This is K-lytics' own version of the dilution finding.
10. **Dead or changed sources in the category table:**
    - The Write Moves link returns 404.
    - The KDP Builder report was rewritten: 70% became 59.1%, and the report retitled itself a "platform snapshot".
    - The $18k low-content anecdote is not on the cited page.
    - The Amazon "internal metrics" quote is not on the cited page.
