# Verification: marketing, discovery and risks (report sections "Discovery takes money and time…" and "The biggest risks…")

- **Date accessed:** 2026-11-14
- **Method:** curl (`-A 'Mozilla/5.0'`) and headless Chromium (Playwright) for most pages; HTML/PDF text extracted with local scripts (PDFs via Ghostscript `txtwrite`). ftc.gov returns an Akamai-generated "Page Not Found"/403 to both curl and headless Chromium, **including the ftc.gov homepage**. The 404 the earlier run saw was a bot block, not a dead URL. FTC pages were read through WebFetch, and the complaint PDF was saved by WebFetch and then text-extracted locally. The FTC rule text and penalty figures were read in the Federal Register on govinfo.gov. Amazon.com help pages were sometimes 403 for headless Chromium and loaded on retry.
- **Status key:** CONFIRMED = read on the authority's own page. CORRECTED = the claim needs a different value or wording, which is given. CONTRADICTED = the source says otherwise. NOT FOUND ON PRIMARY. PRIMARY UNREACHABLE.

---

## Section: "Discovery takes money and time, and Amazon's review rules are strict"

### 1. Income correlates with series and catalogue size (Written Word Media 2025)
- URL: https://www.writtenwordmedia.com/2025-indie-author-survey-results-insights-into-self-publishing-for-authors/amp/
- The page lists "Catalog Size" as a factor and "More books (often 10+, and very often series)" among the traits of higher earners. It also lists "Read-through from series".
- **Status: CONFIRMED** on WWM's own survey page. The survey is self-selected and the link is correlational, as the report says.

### 2. Genre CPC about $0.20-$0.40 (romance/mystery) and $0.40-$0.80 (fantasy/thriller) (PublishDrive)
- URL: https://www.publishdrive.com/amazon-ads-for-authors
- The page as served today has no genre CPC table. It says: "A low CPC of 25¢ means it costs 25¢ every time someone clicks on your ad. On average, one in ten people who click will buy your book."
- **Status: NOT FOUND ON PRIMARY.** The cited page does not contain the genre ranges. Drop them or find another source. The "1 in 10 converts" figure is PublishDrive's unsourced assertion.

### 3. $3.49 royalty at 8% conversion gives a maximum CPC of about $0.28 (Vappingo)
- URL: https://www.vappingo.com/word-blog/?p=11834 ("Amazon Ads and Book Pricing: Break-Even Strategy")
- The current page uses a different example: "If a format earns $3.00 royalty and one in ten qualified ad clicks converts, the rough break-even CPC is $0.30."
- **Status: CORRECTED.** The arithmetic in the report ($3.49 × 0.08 = $0.28) is right, but the cited page now shows $3.00 × 10% = $0.30. Either present the number as the report's own arithmetic or quote Vappingo's current example.

### 4. ACoS understates the value of ads for a series because of read-through (ScribeCount)
- URL: https://scribecount.com/author-resource/troubleshooting-author-resources/amazon-ads-dashboard
- Quote: "ACOS alone is misleading because it only measures the royalty from the advertised title, not the read-through revenue from subsequent books in a series."
- **Status: CONFIRMED** (vendor page).

### 5. A consultant advises building an email list before paying for Facebook or Amazon ads (Self-Publishing Advice, Ricardo Fayet)
- URL: https://selfpublishingadvice.org/ricardo-fayet-on-marketing/
- Fayet says: "Facebook ads still work. Amazon ads still work." He tells beginners to "focus on … free or discounted promotions, advertising—Amazon, Facebook, BookBub—email marketing." He also says to "at least experiment with" Facebook ads.
- **Status: CONTRADICTED.** He lists ads and email side by side and does not say "list before ads". The report misattributes this advice.

### 6. BookBub Featured Deals cost about $570-$940 per fiction deal (third-party 2025 estimates)
- Primary URL: https://www.bookbub.com/partners/pricing (static fetch gives 403; the page renders in Chromium)
- BookBub's own current chart, as fee for a Free / $0.99 deal:
  - **All regions:** Fantasy $467 / $586; Science Fiction $496 / $616; Romantasy $421 / $528; Contemporary Romance $620 / $765; Cozy Mysteries $671 / $832; Thrillers $762 / $948; Crime Fiction $758 / $947; Psychological Thrillers $740 / $925; Women's Fiction $832 / $1,027; Historical Fiction $897 / $1,109.
  - **United States only:** Fantasy $319 / $387; Science Fiction $369 / $446; Romantasy $287 / $348; Contemporary Romance $504 / $611; Cozy Mysteries $514 / $623; Thrillers $571 / $692; Crime Fiction $542 / $657; Women's Fiction $669 / $810; Historical Fiction $728 / $882.
  - **International only:** about $116-$290 for these genres.
  - **Higher deal prices:** a $3+ deal costs far more, for example Thrillers $3,583 for all regions and $2,673 for the US.
- The cited Writers Helping Writers post does **not** contain the $570-$940 figures. It reports one deal: a $0.99 fantasy novel, international only, that cost "$196".
- **Status: CORRECTED.** Use BookBub's own chart. For mainstream genre fiction at free or $0.99, a deal costs about **$290-$880 US-only** or **$420-$1,110 across all regions**, and $1,000-$4,200 at prices above $0.99. The Writers Helping Writers citation does not support the figure.

### 7. BookBub accepts about 25% of submissions; third parties claim 4-20%
- **https://insights.bookbub.com/?p=65:** returns 404 (dead link).
- **BookBub Partners Blog, "How the BookBub selection process works":** https://insights.bookbub.com/how-bookbub-selection-process-works/ (updated 15 Oct 2026). Quote: "only about 25% of submissions will be chosen for a Featured Deal."
- **BookBub Support, "Submission requirements and advice":** https://support.bookbub.com/articles/submission-requirements-and-advice/ (updated 9 Mar 2023). Quote: "we're only able to select about 10-15% of the books that get submitted for BookBub Featured Deals in the US."
- **BookBub blog (updated 7 Mar 2024):** editors "get on average 300 Featured Deal submissions per day".
- **Status: CORRECTED.** BookBub publishes two figures of its own: about 25% overall (blog) and 10-15% for US deals (support page). The conflict is not "BookBub vs third parties". Replace the dead `?p=65` link.

### 8. BookTok divided over AI; "AI accusation" pile-ons (Ypulse, Good Story Co.)
- **Ypulse:** returned HTTP 202 with an empty body (bot wall). **Status: PRIMARY UNREACHABLE.**
- **Good Story Co.:** https://goodstoryco.substack.com/p/the-ai-accusation-heard-round-booktok. The page exists, titled "The AI Accusation Heard 'Round BookTok: You Thought It Was AI, But It Was Just Strategy". **Status: CONFIRMED** that the page exists with this subject. It is commentary, not data.

### 9. Amazon has banned incentivised reviews (outside Vine) since October 2016
- Primary URL: https://www.aboutamazon.com/news/innovation-at-amazon/update-on-customer-reviews (published 3 Oct 2016)
- Quotes: "we updated the community guidelines to prohibit incentivized reviews unless they are facilitated through the Amazon Vine program." Also: **"The above changes will apply to product categories other than books. We will continue to allow the age-old practice of providing advance review copies of books."**
- Marketplace Pulse (26 Oct 2016) quotes the same carve-out for books.
- **Status: CORRECTED.** The date and the Vine exception are right, but the 2016 change **exempted books**: ARCs stayed allowed. Today's rule for books is #10.

### 10. Review swaps and friends-and-family reviews are prohibited; free ARCs "in exchange for reviews" count as incentivised (Goat Consulting) [the report marked this "unverified against Amazon's text"]
- **Amazon Community Guidelines:** https://www.amazon.com/gp/help/customer/display.html?nodeId=GLHXEX85MENUE4XF
  - Under "What's allowed": "Review free books (advanced reader copies) from authors or publishers. However, they can't require a review in exchange for free books or try to influence your opinion."
  - Customers may NOT: "Post reviews on products from sellers, authors, brands, or artists that you have a personal connection with."
  - Customers may NOT: "Create, edit, or remove a review in exchange for compensation, including payments, refunds, discounts, products, gift cards…"
  - "We don't allow people to create, edit, or post content about their own products or services. The same goes for products and services offered by: Friends, Relatives, Employers, Business associates, Competitors."
  - Consequences: "Remove their content; Limit their ability to use community features; Suspend or terminate their account; Withhold payments."
- **Amazon "Customer Reviews":** https://www.amazon.com/gp/help/customer/display.html?nodeId=G3UA5WC5S5UUKB5G
  - Amazon removes "A review by someone perceived to have a close personal relationship with the product's owner, author, or artist."
  - It also removes "A positive review from an artist on a peer's album in exchange for receiving a positive review from them." This is Amazon's own example of a review swap.
- **KDP help, "Customer Reviews":** https://kdp.amazon.com/en_US/help/topic/G202101910
  - Quote: "You may provide free or discounted copies of your books to readers, as long as you do not require a review in exchange or attempt to influence the review. Offering anything other than a free or discounted copy of the book, including gift cards, will invalidate a review, and the Amazon Community team will remove it."
- **Status:**
  - Swaps and friends/family/personal-connection reviews: **CONFIRMED** on Amazon's own pages.
  - ARC wording: **CORRECTED.** Giving free ARCs is explicitly allowed. What is banned is *requiring* a review in exchange, influencing its content, or offering anything beyond the book. The report should quote Amazon's text instead of the Goat Consulting tool.

### 11. FTC fake-review rule in force since 21 Oct 2024; bans fake/AI-generated reviews, paid reviews and undisclosed insider reviews; civil penalties of about $51,744 per violation at 2024 rates
- **FTC press release** (14 Aug 2024): https://www.ftc.gov/news-events/news/press-releases/2024/08/federal-trade-commission-announces-final-rule-banning-fake-reviews-testimonials. The URL is valid; read via WebFetch because direct fetches are bot-blocked.
  - It lists the prohibited conduct: fake or false reviews and testimonials, including AI-generated ones; buying positive or negative reviews; insider reviews without disclosure; company-controlled review sites; review suppression; and fake social-media indicators.
  - The rule lets the FTC "seek civil penalties against knowing violators."
- **Federal Register final rule** (89 FR 68034, 22 Aug 2024, 16 CFR Part 465): https://www.govinfo.gov/content/pkg/FR-2024-08-22/html/2024-18519.htm
  - "DATES: This rule is effective October 21, 2024."
  - Sec. 465.4 bars compensation or incentives "conditioned expressly or by implication on, the writing or creation of consumer reviews expressing a particular sentiment, whether positive or negative".
  - Sec. 465.5 covers undisclosed reviews and testimonials by officers, managers, employees and agents, and reviews solicited from immediate relatives or employees.
- **Penalty amount:**
  - Federal Register 17 Jan 2025 (2025-01361): https://www.govinfo.gov/content/pkg/FR-2025-01-17/html/2025-01361.htm. 15 U.S.C. 45(m)(1)(A), knowing violations: "Increase from $51,744 to $53,088".
  - Federal Register 15 Sep 2026 (2026-18853): https://www.govinfo.gov/content/pkg/FR-2026-09-15/html/2026-18853.htm. "the Federal Trade Commission ('FTC')'s civil penalty amounts will remain unchanged during 2026. The FTC will continue to apply the 2025 civil penalty levels." The reason given is that OMB M-26-11 cancelled the 2026 adjustment because the shutdown prevented the October 2025 CPI-U.
- **Status:**
  - Date, effective date and categories: **CONFIRMED.**
  - "Paid reviews": **CORRECTED.** The rule bans incentives tied to a *particular sentiment* (positive or negative), not every compensated review. Compensated reviews also need disclosure under Section 5 and the Endorsement Guides.
  - Penalty: **CORRECTED to up to $53,088 per violation**, the 2025 level, still current in 2026 because no 2026 adjustment was made. Each day of a continuing violation can count separately.

---

## Section: "The biggest risks are dilution, reader distrust, account loss and paid courses"

### 12. AI text in about half of new books, revenue per title falling (The Decoder)
- URL: https://the-decoder.com/ai-generated-books-are-flooding-amazon-and-tanking-sales-for-human-authors/ (15 Aug 2026)
- The article reports **Chakrabarty et al.**: 14,419 self-published e-books (Jan 2023-Mar 2026). Books with substantial AI content (>25% of text) are "20 percent of the catalog" and bring 11.3% of revenue. The catalogue grew 38.3x while revenue grew 8.9x. Revenue per book fell in 6 of 8 genres (7 of 8 for books with no AI text). AI titles reached up to 31% of new Top-25 entries. The study is "observational and associational".
- The page contains no "about half of new books" figure. That number comes from Reimers & Waldfogel via Office Chai, which is outside this track.
- **Status: CORRECTED.** Revenue per title falling: CONFIRMED on the cited page. "About half" does not appear in The Decoder; cite the source of that figure or use The Decoder's 20%-of-catalogue figure.

### 13. Kindle Unlimited's fixed fund spreads thinner as more AI titles enrol (Book Riot, no data)
- URL: https://bookriot.com/can-kindle-unlimited-survive-ai/
- Page subtitle: "As AI-generated books flood the Kindle Unlimited space, can the service survive without better restrictions?"
- **Status: CONFIRMED** as opinion. The Decoder article adds data: the dilution pattern is stronger in genres with high KU availability, a revenue-share gap 8.4 points smaller, but the researchers draw no causal link.
- Also see New finding A on the Kindle+ name.

### 14. YouGov/Black Château poll, 1,000 US adults, August 2025; most want disclosure; 61% less fulfilled
- URL: https://yougov.com/en-us/articles/52728-reality-checks-talkshow-ai-books-desiree-duffy (YouGov, by Brian Reitz, **6 Aug 2025**)
- Quotes:
  - "a five-question survey of 1,000 Americans"
  - "Most US adults want to be informed about any AI contribution to a book's creation (56%)… An additional 19% … if AI helped with at least 10% of the book's content."
  - "61% feeling either somewhat or much less fulfilled overall"
  - Literary fiction: 54% "much less fulfilled". Business, instructional or self-help nonfiction: 43%.
  - 28% say AI should not be used at any stage. 40% accept AI for line or copy editing.
- **Status: CONFIRMED** on YouGov's own page. Cite YouGov, not Journal of Cyber Policy; the `?p=343982` link now returns 404. YouGov gives no fieldwork date: 6 Aug 2025 is the publication date. The 61% is among "American readers".

### 15. Swedish survey: two-thirds negative about AI-written books, 3% positive (DEV Community, unverified)
- Primary URL: https://forlaggare.se/wp-content/uploads/2026/04/Bokbarometern-2026.pdf (Svenska Förläggareföreningen, *Bokbarometern 2026*, April 2026)
- Foreword: "två tredjedelar av svenskarna är negativt inställda till AI-genererad litteratur, och bara 3 procent är positiva", which translates as "two thirds of Swedes are negative toward AI-generated literature, and only 3 percent are positive."
- Method: "Under perioden 12–16 januari 2026 har Kantar Media … genomfört 1 031 intervjuer" (Sifo panel, online). Analysis by Karl Berglund and Ann Steiner of Uppsala University.
- **Status: CONFIRMED.** Cite the Swedish Publishers' Association PDF instead of DEV Community.

### 16. Apple Books uses an "AI Generated by" credit
- URL: https://help.apple.com/itc/applebooksstoreformatting/en.lproj/static.html (Apple Books Formatting and Content Guidelines)
- 1.13: "Book content that is AI-generated (i.e., a material portion of the content is generated by an AI-based tool …), must be labeled as such using 'AI Generated by' artist role and declaring the AI-generated creation method in the description. AI-assisted content (i.e., AI has been used as a tool in idea generation, research, editing, or producing cover images for a book composed by a human author …) does not require disclosure."
- See also 2.9 and 4.8.
- **Status: CONFIRMED.** Note that Apple *accepts* AI-generated books with a label and does not require disclosure of AI-assisted work, which is looser than "stricter than Amazon" implies.

### 17. Draft2Digital reportedly turns away most AI books it receives
- **D2D Content Guidelines** (last updated 27 Oct 2025): https://draft2digital.com/content-guidelines/
  - "While we support AI-assisted content we do not accept content that has been generated entirely by AI/LLMs that has not gone through extensive editing from a human."
  - "We are not a destination for … individuals who seek to publish 100% AI-generated books".
- **Indie Author Magazine** (2 Feb 2026, interview with CEO Kris Austin), secondary:
  - "Draft2Digital rejects between 40 percent and 75 percent of all book submissions—and it's almost entirely AI-generated nonfiction."
  - "Thousands of AI-generated books arrive at Draft2Digital every single day … the company turns most of them away."
- **Status:**
  - Policy: **CONFIRMED** on D2D's own page.
  - "Turns away most": CONFIRMED only as the CEO's statement in the interview. Add that the rejections are mainly AI nonfiction and that the overall rejection rate is 40-75%.

### 18. Kobo lists AI-generated content among its rejection reasons
- **Kobo Writing Life help, "Why was my Book Rejected or Blocked?":** https://kobowritinglife.zendesk.com/hc/en-us/articles/360058975712-Why-was-my-Book-Rejected-or-Blocked. Under "unsatisfactory or incomplete experience", the list includes "Wholly or partially AI generated".
- **Kobo Content Policy:** https://www.kobo.com/contentpolicy. "Kobo reserves the right to reject content … that is wholly or partially created by digital text-generation algorithms".
- **Status: CONFIRMED.** Kobo is the strictest on the wording, since even "partially" AI-generated text can be rejected.

### 19. IngramSpark bars AI-only books
- URL: https://www.ingramspark.com/content-guidelines (also the 1 Oct 2023 Catalog Integrity post)
- It refuses "Content created using automated means, including but not limited to content generated using artificial intelligence* or mass-produced processes."
- **Acceptable:** AI "used only in an assistive way"; work where the "majority … written or created using human creativity"; and AI-assisted work (including translation) "with significant and material human editorial review and contribution with proper attribution".
- **Unacceptable:** "Works created solely using generative AI."
- It adds: "Proper attribution of creation must accompany all works."
- **Status: CONFIRMED.** Add that IngramSpark requires attribution for AI-assisted work.

### 20. Google Play Books (not named in the report; checked as requested)
- URL: https://support.google.com/books/partner/answer/1067634 (Publisher Content Policies)
- No AI-specific rule appears. Review uses "a combination of automated and human evaluation". Quality rules target low-value, repetitive or freely available content.
- **Status: NOT FOUND ON PRIMARY** (no AI-specific policy).

### 21. "A heavily AI-generated catalogue is close to locked into Amazon" [inference]
- **Status: CORRECTED (inference too strong).**
  - Apple accepts AI-generated books with an "AI Generated by" label.
  - D2D accepts AI-assisted books with extensive human editing.
  - IngramSpark accepts AI-assisted books with attribution.
  - Kobo is the outlier.
- Only *unedited, wholly AI-generated* books are close to Amazon-only, and Apple, which D2D also distributes to, may still take those books with a label, though D2D's own policy blocks wholly AI-generated books.

### 22. Authors report sudden KDP terminations, sometimes with royalties withheld (Writers Weekly, AuthorMedia)
- **Writers Weekly:** https://writersweekly.com/angela-desk/amazon-kdp-terminates-another-authors-account-and-keeps-her-royalties. It describes "many reports of Amazon KDP terminating authors' accounts without warning" (anecdotal).
- **AuthorMedia:** https://www.authormedia.com/why-amazon-is-terminating-innocent-authors/. An interviewed consultant estimates roughly a third deserved, a third the account holder's unknowing fault, a third false positives (anecdotal).
- **Amazon's own wording, KDP Terms and Conditions** (Last Updated 21 Oct 2026): https://kdp.amazon.com/terms-and-conditions
  - Section 3: "We are entitled to terminate this Agreement … or suspend your Program account at any time if we have concerns with your account, or activity relating to your account … We will notify you upon termination and will provide instructions regarding how to appeal that termination if you believe it is in error."
  - Section 5.4.8: "Upon termination … we may withhold all Royalties due for a period of three months"; "If we terminate this Agreement because you have breached your representations and warranties or our Content Guidelines, you forfeit all Royalties not yet paid to you"; and on deceptive, fraudulent or illegal activity, "we may permanently withhold payments".
  - Section 4.2: "If we terminate your account, you will not establish a new account."
- **Status: CONFIRMED.** Withheld or forfeited royalties and the appeal route are in Amazon's own terms. Cite them alongside the anecdotes. No public KDP help page on appeals or reinstatement was found; the appeal instructions arrive in the termination notice. The "90% never reinstated" figure has no source, as the report already says.

### 23. Abnormal page-read, download or review spikes are cited as termination triggers (Written Word Media)
- **WWM, "KDP Account Health: What Can Get Authors Banned"** (29 May 2026): https://www.writtenwordmedia.com/kdp-account-health/
  - It lists "Manipulating Kindle Unlimited page reads, reviews, rankings, or sales" and the red flag "Artificial page-read spikes".
  - It also lists "Joining review swaps" and "Asking family, employees, or close collaborators for biased reviews".
  - "Download spikes" is not on the page.
- **Amazon's own text:**
  - KDP "Sales Ranking" help (https://kdp.amazon.com/en_US/help/topic/G201648140): "If we determine that your book's purchasing or borrowing activity originates from accounts that are attempting to manipulate our services, it may result in termination of your account and loss of royalties."
  - KDP Select terms §5(b): Amazon may withhold royalties on all Digital Books "for a period of up to 90 days while we investigate".
- **Status: CONFIRMED,** with a small correction: WWM says *page-read* spikes, not download spikes. Prefer the Amazon quotes.

### 24. FTC: on 13 April 2026 Publishing.com and principals to pay $1.5M; false earnings claims for "AI Publishing Academy" and "Publishing Accelerator"; illusory refund guarantees, some conditioned on positive testimonials; undisclosed employee reviews; most buyers never earned the promised income
- **Press release** (13 Apr 2026, read via WebFetch): https://www.ftc.gov/news-events/news/press-releases/2026/04/publishingcom-pay-15-million-misleading-consumers-about-how-much-income-they-could-earn-using
  - The URL in the report is correct; the 404 is ftc.gov bot-blocking non-browser clients.
  - Defendants: Publishing.com LLC, CEO Christian Mikkelsen and CPO Rasmus Mikkelsen.
  - The release gives the $1.5M and quotes the pitch: "copy the EXACT system hundreds of my students use to make $1k to $3k a month in passive income".
  - It describes the "no questions asked" guarantee with conditions buried in fine print.
  - Undisclosed reviews were written by "employees or by relatives of the Mikkelsens"; testimonials were incentivised with "prizes, cash, or additional services"; the company at times "conditioned refunds on consumers providing positive testimonials".
  - It says most consumers "never achieved the income the company promised in its advertising". The Commission voted 2-0.
- **Case page** (FTC File No. 242 3055, Docket C-4836): https://www.ftc.gov/legal-library/browse/cases-proceedings/242-3055-publishingcom-matter
  - Complaint (Apr 2026): https://www.ftc.gov/system/files/ftc_gov/pdf/2423055publishingcomcomplaint.pdf
  - Final complaint and final order: https://www.ftc.gov/system/files/ftc_gov/pdf/2423055c4836publishingcomfinalorder.pdf
- **Final order press release** (2 Jul 2026, 2-0 vote): https://www.ftc.gov/news-events/news/press-releases/2026/07/ftc-approves-final-order-against-publishingcom-settling-allegations-it-misled-consumers
- **Complaint details:**
  - ¶12: "Respondents have typically charged $1,995 for their AIA program … Respondents generally have sold the Publishing Accelerator program for $9,800."
  - ¶10: AIA was formerly "Audio Income Academy" (Sept 2019), then "Audiobook Impact Academy" (Sept 2022), and was renamed AI Publishing Academy in April 2023.
  - ¶11: Publishing Accelerator launched in March 2022 and included the Publishing.ai software.
  - ¶8 and ¶17: marketing ran through "free videos".
  - ¶25: "over 200 video testimonials", some from employees or people connected to them.
  - ¶26: a testimonial contest with a "$10,000 'grand prize'".
  - ¶13: consumer complaints, including "over $49,000 in advertising expenses alone".
- **Status: CONFIRMED.** One refinement: the FTC says refunds were *at times* conditioned on positive testimonials, and the undisclosed reviews were by employees *and relatives*. The final order was approved on 2 July 2026; the report should mention it.

### 25. The course cost about $1,995 (Publishers Marketplace)
- Publishers Lunch (13 Jan 2025, secondary, citing Business Insider): Publishing.com "charges users $1,995".
- FTC complaint ¶12: "typically charged $1,995" for AIA. The press release says "up to $1,995".
- **Status: CONFIRMED** on the FTC complaint. Add that the upsell, Publishing Accelerator, was "generally" sold for **$9,800**. That matters for the "more than double the tool budget" comparison, which understates the exposure.

### 26. Scammers use Amazon trademarks to sell fake "KDP" services (Writer Beware)
- URL: https://writerbeware.blog/2023/07/07/how-scammers-are-using-amazon-and-amazon-trademarks-to-rip-writers-off/ (posted 7 Jul 2023, updated 9 Jul 2026)
- Quotes: "Any ghostwriting or publishing service provider using the Amazon name, its trademarks, or variations thereof (such as AMZ or Kindle Publisher) are scams". Also: "the _only_ genuine Amazon publishing platform is Amazon's Kindle Direct Publishing."
- Update dated 6/25/26: "Amazon has won a multi-million dollar judgment in its suit against Amazon scammers. Unfortunately that hasn't slowed the imposters down".
- **Status: CONFIRMED.**

### 27. Warning signs: income promises, free-video funnels, refunds tied to testimonials, undisclosed paid reviews
- **Status: CONFIRMED** against the FTC complaint (¶¶6-8, 17, 25-26).

---

## New findings

**A. KDP now calls Kindle Unlimited "Kindle+".**
- KDP help pages read today say "Your Kindle eBooks and audiobooks enrolled in KDP Select are included in Kindle+, where you're eligible to earn royalties from the KDP Select Global Fund … measured in … (KENP)" (https://kdp.amazon.com/en_US/help/topic/G201541130).
- The page also forbids marketing that "incentivizes Kindle+ customers to read … in exchange for compensation of any kind" and says Amazon has "systems in place to monitor for potential manipulation".
- The report uses "Kindle Unlimited" throughout. Check the naming and whether audiobooks now count toward KENP.

**B. Amazon explicitly allows ARCs for books.** Since 2016, books have been exempt from the incentivised-review ban for ARCs, and the current Community Guidelines and KDP help say so. The practical rule for authors: free or discounted copies are fine, but no required review, no influence over it and no extras such as gift cards.

**C. FTC civil penalty is $53,088 per violation,** the 2025 level. There was no 2026 adjustment (FR 2026-18853, 15 Sep 2026).

**D. Publishing.com details.** The Publishing Accelerator upsell sold for about $9,800. The final FTC order was approved on 2 July 2026 (Docket C-4836).

**E. BookBub's own acceptance figures conflict.** One page says 25% overall; another says 10-15% for US Featured Deals. Fees on BookBub's live chart vary widely by genre, and US-only deals cost less than the "all regions" figures.

**F. Retailers other than Kobo label or accept AI-assisted work.** Apple accepts AI-generated books with a label. IngramSpark and D2D accept AI-assisted work with human editing, and IngramSpark requires attribution. Only Kobo names "partially" AI-generated content as grounds for rejection.

**G. FTC pages block automated fetches.** ftc.gov blocks curl and headless Chromium with an Akamai "Page Not Found"/403, even for the homepage. Future verification should use WebFetch or the govinfo Federal Register copies.

**H. Dead or changed citations in these sections:**
- insights.bookbub.com/?p=65 returns 404.
- journalofcyberpolicy.com/?p=343982 returns 404.
- Writers Helping Writers does not contain the BookBub price figures.
- PublishDrive does not contain the genre CPC ranges.
- The Vappingo example has changed to $3.00 × 10%.
- Self-Publishing Advice does not say "list before ads".
- The Decoder does not contain the "about half" figure.

**Not checked:** Amazon Ads for KDP help pages (not needed for the claims as worded). Ypulse could not be reached.
