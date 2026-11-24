[README 858a67b3af6383a2acc401b231d416da.md](https://github.com/user-attachments/files/35379385/README.858a67b3af6383a2acc401b231d416da.md)
# README

# When a company in SIC 28 (Chemicals/Pharma) announces better-than-expected earnings, does its stock earn a higher return around the announcement?

**Author:** Amy Nguyen · BAN 4550, Fall 2026 · Industry: 28 Chemicals/Pharma

## The question

Harry Potter wants to know if, when a company in SIC 28 (Chemicals/Pharma) announces better-than-expected earnings, its stock earns a higher return around the announcement date.

## Main result

In Chemicals & Pharma (SIC 28), companies in the high-earnings-surprise group experience an average 3-day abnormal return of +1.61%, compared to -1.44% for the low-surprise group, resulting in a 3.05 percentage-point difference (n = 2,577). This positive correlation is even more pronounced in our peer industry, Non-Depository Credit (SIC 61), where the High-minus-Low spread increases to 5.88 percentage points (+3.30% vs. -2.58%, n = 530). Across both industries, the 95% confidence intervals for the High and Low groups do not overlap, reinforcing that stronger-than-expected earnings are consistently associated with higher stock returns.

Main figure

![Main figure](README/Unknown.png)

Main figure

## Comparison with my partner’s industry

What differs, one reason you proposed, and what the data showed when you checked it.

*In **Chemicals & Pharma (SIC 28)**, the High SUE group outperformed the Low SUE group by 3.05 percentage points (t = 6.28, p = 0.0) over the 3-day window. Because the t-statistic is well beyond 2, the return gap is large relative to the noise in the data--and if there were truly no difference between the groups, a gap this large would happen by chance less than 0% of the time (p < .05), confirming the difference is statistically real.*

*For every .01 increase in SUE (an earnings surprise equivalent to 1% of the previous quarter's stock price), the 3-day abnormal return increases by an average of .11 percentage points using raw CAR, or .10 pp using winsorized CAR. Both coefficients are highly statistically significant (p<.0001), indicating that the relationship is not driven by extreme outliers. However, the low R^2 of .6% suggests that earnings surprises account for only a small portion of short-term stock return volatility.*

*In **Non-Depository Credit (SIC 61)**, the High SUE group outperformed the Low SUE group by 5.88 percentage points (t = 6.71, p = 0.0) over the 3-day window. Because the t-statistic is well beyond 2, the return gap is large relative to the noise in the data--and if there were truly no difference between the groups, a gap this large would happen by chance less than 0% of the time (p < .05), confirming the difference is statistically real.*

*For each .01 increase in SUE, the average 3-day abnormal return in Non-Depository Credit rises by .25 percentage points (or .24 pp using winsorized data), representing more than twice the sensitivity observed in Chemicals & Pharma. Earnings surprises also account for a considerably larger proportion of 3-day return variation in SIC 61 (R^2 ~ 5%, compared to .6% in SIC 28).*

***Does b stay about the same?**
Adding Year Fixed Effects (Model 2 Yr FE): Yes. Including C(fyearq) has almost no effect on the slope in either industry, changing from .0963* to .0947* in SIC 28 and from .2359* to .2358* in SIC 61. This confirms that the positive relationship is not explained by broader calendar-year economic fluctuations.
Adding the Loss Interaction (Model 3 Loss): When distinguishing profitable quarters (loss = 0) from loss-making quarters (loss = 1), the baseline slope b for profitable firms becomes larger, rising to .1738* in SIC 28 and .2446* in SIC 61. However, the negative interaction terms (sue:loss = -.1202 in SIC 28 and -.1786* in SIC 61) indicate that stock prices respond considerably less to quarterly EPS surprises when firms report losses. This results in a net slope of .1738 − 0.1202 = 0.0536 for loss-making SIC 28 firms and 0.2446 − 0.1786 = 0.0660 in SIC 61. Additionally, loss-making announcements are associated with lower average returns overall (loss = -0.0109 in SIC 28 and 0.0434 in SIC 61).*

### The Share of Loss-Making Firms

If SIC 28 has a much higher share of loss-making announcements, those unprofitable biotech firms pull down SIC 28’s overall slope and High-minus-Low spread.

Chemicals and Pharma (SIC 28) includes hundreds of biotech companies that are pre-revenue, heavily focused on R&D, and often unprofitable (loss = 1), while Non-Depository Credit (SIC 61) consists primarily of established, profitable lenders (loss = 0). Loss-making firms respond much less to quarterly EPS surprises (b = .054 compared to .174 for profitable firms in SIC 28).

A two-panel or grouped chart comparing (a) the % of loss-making announcements in SIC 28 vs. SIC 61, and (b) the High-minus-Low CAR spread (or regression slope b) split by Profitable (loss = 0) and Loss-making (loss = 1) firms across both industries.

![image.png](README/image.png)

This figure offers direct and visual numerical evidence supporting our hypothesis that Chemicals & Pharma’s smaller overall CAR spread is largely attributable to its higher concentration of unprofitable, R&D-stage biotech firms.

- Panel A (More than twice the share of loss-making firms): 35.9% of announcements in Chemicals & Pharma (SIC 28) come from loss-making quarters (EPS<0), compared to just 14.9% in Non-Depository Credit (SIC 61). This represents a 21.0 percentage point difference, or a 2.4x higher share of unprofitable quarters.
- Panel B (Weaker SUE response among loss-making firms in SIC 28): Within Chemicals & Pharma, the High-minus-Low CAR spread decreases by 42.3% when comparing profitable quarters (3.36 pp) with loss-making quarters (1.94 pp). In contrast, Non-Depository Credit shows almost no decline between profitable (4.84 pp) and loss-making (4.76 pp) announcements.
- Narrowing the industry gap: When examining only profitable firms (EPS ≥ 0), the difference in spreads between SIC 61 and SIC 28 is nearly cut in half, decreasing from 2.83 pp overall (5.88 pp vs. 3.05 pp) to 1.48 pp (4.84 pp vs. 3.36 pp). This supports the conclusion that SIC 28’s lower overall sensitivity is substantially influenced by pre-revenue biotech companies, whose valuations rely more on clinical trial outcomes and FDA milestones than on quarterly EPS.

![image.png](README/image%201.png)

This event-window chart ([-5, +5] days) supports our 3-day window and illustrates post-earnings drift. There are 2 important findings

1. Stable pre-announcement trend: All 3 SUE lines remain relatively flat and close to 0% before the announcement, suggesting minimal pre-earnings information leakage.
2. Sharp Day 0-1 repricing + Post-Earnings Announcement Drift (PEAD): On Day 0 and Day +1, High SUE stocks rise to approximately +1.8%, while Low SUE stocks fall to around -1.6%, capturing most of the market reaction within our [-1, +1] event window. Instead of reversing, the two groups continue to diverge through Day +5, reaching approximately +2.1% vs. -1.9% (a roughly 4.0 pp spread). This illustrates classic post-earnings announcement drift, in which the market takes several days to fully incorporate earnings surprises.

## Advice for the client

- **Business implication:** Pfizer should compare its earnings sensitivity with profitable pharmaceutical peers (b = 0.174, +3.36 pp High–Low CAR spread) rather than the overall Chemicals & Pharma industry average (b = 0.096, +3.05 pp spread), which is diluted by unprofitable R&D-focused biotech firms (35.9% loss-making quarters). Consistently exceeding prior-year quarterly EPS generates reliable immediate 3-day abnormal stock gains. However, management should also provide clear forward guidance and pipeline updates, as clinical developments can outweigh backward-looking EPS surprises.
- **Limitation:** Our earnings surprise measure (SUE) captures year-over-year changes in GAAP EPS (epspxq vs. four quarters earlier), rather than differences from Wall Street analyst consensus estimates. Additionally, the low R² (0.006 in SIC 28) indicates that quarterly EPS surprises account for less than 1% of short-term, 3-day stock return variation.
- **Next questions:**
    - **Predictive**: Can combining quarterly SUE with analyst consensus surprises, clinical-trial catalyst dates, and forward revenue guidance help accurately forecast 30-day post-earnings abnormal stock returns for large-cap pharmaceutical firms?(Requires IBES consensus EPS estimates, ClinicalTrials.gov/FDA catalyst records, and 30-day CRSP daily returns.)
    - **Prescriptive**: Should Pfizer's investor relations team release major clinical-trial readouts alongside quarterly earnings announcements or announce them separately to maximize positive 3-day CAR and minimize post-announcement return volatility? (Requires timestamped SEC Form 8-K press-release records distinguishing standalone earnings announcements from bundled pipeline updates.)

## Data

- Sources: Compustat (`comp.fundq`), CRSP (`crsp.dsf`, `crsp.dsi`), accessed through WRDS. Add or remove tables to match your work.
- **The data are not included in this repository** because of the WRDS license. Someone with WRDS access can rebuild the results by running the notebook with the link file in the same folder.
- Sample period: Quarterly earnings announcements (rdq) between January 1, 2021, and December 31, 2024, with fundamental data pulled from June 2019 onward to calculate EPS from four quarters earlier.
- Sample filters (Rules 1–6):
    1. A known earnings announcement date (rdq is not missing).
    2. The announcement date falls within the 2021–2024 period.
    3. A valid standardized unexpected earnings measure (sue) can be calculated using current and four-quarter-ago EPS.
    4. The previous quarter's closing stock price is at least $5 (|prc_1q_ago| >= $5) to exclude penny stocks.
    5. Earnings surprise magnitude is limited to 100% of the stock price (|SUE| <= 1) to filter out extreme outliers.
    6. All 3 trading days ([-1, 0, +1] around day0) have valid CRSP daily stock and market returns (days_found == 3).
    For regressions, 3-day CAR is also winsorized at the 1st and 99th percentiles.

## How the tables fit together

Each row in the final dataset is uniquely identified by the primary key `(gvkey, datadate)`, representing one firm's quarterly earnings announcement. This connects Compustat fundamentals (`gvkey`) with CRSP daily stock returns (`permno`) only when the company's link dates are valid (`linkdt <= datadate <= linkenddt`). To calculate year-over-year earnings surprises without calendar-date misalignment, we use a sequential quarter index `qnum = fyearq * 4 + fqtr` to self-join data from four quarters earlier (`qnum + 4`) and one quarter earlier (`qnum + 1`). For the event window, **Day 0** is defined as the first open trading day in `crsp.dsi` on or after the announcement date (`date >= rdq`), automatically moving weekend and holiday announcements to the next market opening. Abnormal returns are then summed across three consecutive trading days: `[day0 - 1, day0, day0 + 1]`.

| **Merge Step** | **Left Table** | **Right Table** | **Join Keys & Type** | **Purpose** |
| --- | --- | --- | --- | --- |
| **1. Link** | `comp.fundq` | `ccm_link.csv` | `gvkey` (`inner`) | Attach CRSP `permno` & `ticker`; filter `linkdt <= datadate <= linkenddt` |
| **2. Lags** | `panel` | `panel`(shifted) | `gvkey`, `qnum`(`left`) | Attach `eps_4q_ago` (`qnum + 4`) & `prc_1q_ago`(`qnum + 1`) to compute `SUE` |
| **3. Day 0** | `events` | `crsp.dsi` | `date >= rdq`(`cross` + `min`) | Map each announcement date (`rdq`) to its first open trading day (`day0`) |
| **4. Returns** | `window`(`-1, 0, +1`) | `crsp.dsf` + `crsp.dsi` | `permno`, `tday`(`left`) | Pull daily `ar = ret - vwretd` across 3 trading days and sum into `CAR` |

## How I checked the results

1. **Expected:** We anticipated that our code would generate zero duplicate `(gvkey, datadate)` keys and accurately reflect Pfizer's primary financial records. Specifically, our retrieved GAAP Basic EPS (`epspxq`) and prior-quarter closing price (`prc_1q_ago`) were expected to match Pfizer's earnings press release and Google Finance, while manually summing the three daily abnormal returns should produce the same CAR as our calculation.

2. **Found:** For Pfizer's Q3 2024 earnings release (`rdq = 2024-10-29`), our dataset matched the reported $0.79 Basic EPS and closely aligned with the prior quarter-end closing price on June 28, 2024 ($27.98 vs. $27.99 on Google Finance, due to exchange rounding). Our manually calculated 3-day CAR also matched the notebook's output to four decimal places.

3. **Did:** We reviewed the five largest CAR outliers against actual clinical-trial catalysts, conducted sensitivity tests excluding the top five extreme events and the most frequently occurring company to confirm that our SUE group rankings remained consistent, and winsorized CAR at the 1st and 99th percentiles in our regressions to prevent extreme biotech stock movements from distorting the slope.

## Changes since Project 2

| What was wrong | How I fixed it | How the results changed |
| --- | --- | --- |
| Check 4 Explanation | Added more explanation | Further judgment was given for each of the other 4 companies. |
| Part 4 sign | Fixed the sign | The average CAR for the Low SUE group accurately reflected a -0.0144 | -1.44% instead of 0.0144 | -1.44% |
| Q2 comment “Company counts are given as a range and 'no single firm dominates' is stated, not tested. Test it, e.g., remove the top company and recompute.” | Seemed to be feedback for Q1 and not Q2—went ahead and assumed this and had AI help me. | We now see the changes in sample size & company breadth, where no individual firm makes up even 2% of any group, showing stability after removing ANT, the top company. We see insignificant change in average CARs and ranking. |
| Appendix A “you should have specified which parts you received help with.” | Specified which parts/prompts used to receive help in each section | The table column “What I asked, and what I changed in the AI's answer” was filled for each row |

## Where the code came from

The class notebook, Gemini, or your own changes. If you used Gemini, say for which steps.

same chat: [https://share.gemini.google/mdaaKvWOYNEb](https://share.gemini.google/mdaaKvWOYNEb)

- Asked Gemini for guidance on repeating the analysis for SIC 61. Did all adjustments by hand.
- Asked clarifying questions
- Asked for majority of steps and paraphrased responses

## Files

```
notebooks/   Project3.ipynb (runs top to bottom on WRDS JupyterHub)
figures/     main_figure.png, merge_map.png, ...
docs/        Last_First_Project3.pdf (slides)
README.md
```
