# README_template

# When a company in SIC 28 (Chemicals/Pharma) announces better-than-expected earnings, does its stock earn a higher return around the announcement?

**Author:** Amy Nguyen · BAN 4550, Fall 2026 · Industry: 28 Chemicals/Pharma

## The question

Harry Potter wants to know if, when a company in SIC 28 (Chemicals/Pharma) announces better-than-expected earnings, its stock earns a higher return around the announcement date.

## Main result

Two or three sentences with your key number, then one figure.

Main figure

![Main figure](https://app.notion.comfigures/main_figure.png)

Main figure

> Example: *Stores near campuses sold 18% more during exam weeks; other stores showed no change.*
> 

## Comparison with my partner’s industry

What differs, one reason you proposed, and what the data showed when you checked it.

## Advice for the client

- **Business implication:** what the client should do or learn.
- **Limitation:** one reason to be careful (data, sample size or method).
- **Next questions:** one predictive and one prescriptive question.

## Data

- Sources: Compustat (`comp.fundq`), CRSP (`crsp.dsf`, `crsp.dsi`), accessed through WRDS. Add or remove tables to match your work.
- **The data are not included in this repository** because of the WRDS license. Someone with WRDS access can rebuild the results by running the notebook with the link file in the same folder.
- Sample period and rules: [period, filters].

## How the tables fit together

Your merge map (image) and two or three sentences on the keys and the date rule.

Merge map

![Merge map](https://app.notion.comfigures/merge_map.png)

Merge map

## How I checked the results

Your most useful check in two or three sentences: what you expected, what you found, what you did.

## Changes since Project 2

| What was wrong | How I fixed it | How the results changed |
| --- | --- | --- |
| Check 4 Explanation | Added more explanation | Further judgment was given for each of the other 4 companies. |
| Part 4 sign | Fixed the sign | The average CAR for the Low SUE group accurately reflected a -0.0144 | -1.44% instead of 0.0144 | -1.44% |
| Q2 comment “Company counts are given as a range and 'no single firm dominates' is stated, not tested. Test it, e.g., remove the top company and recompute.” | Seemed to be feedback for Q1 and not Q2—went ahead and assumed this and had AI help me. | We now see the changes in sample size & company breadth, where no individual firm makes up even 2% of any group, showing stability after removing ANT, the top company. We see insignificant change in average CARs and ranking. |
| Appendix A “you should have specified which parts you received help with.” | Specified which parts/prompts used to receive help in each section | The table column “What I asked, and what I changed in the AI's answer” was filled for each row |

Write “None” if there was nothing to fix.

## Where the code came from

The class notebook, Gemini, or your own changes. If you used Gemini, say for which steps.

- Asked Gemini for guidance on repeating the analysis for SIC 61. Did all adjustments by hand.
- 

## Files

```
notebooks/   Project3.ipynb (runs top to bottom on WRDS JupyterHub)
figures/     main_figure.png, merge_map.png, ...
docs/        Last_First_Project3.pdf (slides)
README.md
```