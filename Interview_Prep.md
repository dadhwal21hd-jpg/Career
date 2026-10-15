# Interview Prep — 10 weeks

**Daily slot: 4:00–5:00 pm. Phone away. Problems only — no notes, no study docs.**

Goal: analyst roles — AMEX Risk Analyst (stretch), pharma / healthcare analytics (ZS, IQVIA, Axtria), supply-chain / retail-tech analyst.

## Rules

1. Same hour every day. Missed a day? Do it the next day — never skip two in a row.
2. Solve, don't read. If stuck for 15 min, look at the answer, then solve it again tomorrow without looking.
3. One line in the log below every day. Tell Claude at the start of each session.

## The plan

| Week | Do | Done when |
|---|---|---|
| 1–2 | **SQL basics** — days 1–3: SQLBolt lessons 1–12 (https://sqlbolt.com, 4 a day). Then LeetCode "SQL 50" (https://leetcode.com/studyplan/top-sql-50/), 2–3 a day | Easy problems without help |
| 3–4 | **SQL advanced** (window functions, CTEs) + **Excel** (pivots, XLOOKUP, charts) | Medium SQL in ~15 min |
| 5–6 | **Statistics** — averages, spread, distributions, hypothesis tests, A/B, regression (StatQuest) + **one Power BI dashboard** | Explain a p-value and a regression in plain words |
| 7–8 | **Python pandas** — load, clean, group, merge + **write the stock-reconciliation case study** (1 page + 3-min story) | Tell the story without notes |
| 9 | **Domain** — pharma analytics terms, or credit risk for AMEX (default, delinquency, logistic regression, KS / Gini) | Explain how a bank decides who gets credit |
| 10 | **Mock interviews + apply to 15–20 roles** | Applications out |

## Daily log

| Date | Week | What I did (count it) | Done? |
|---|---|---|---|
| 10 Oct | 1 | SQLBolt lessons 1–4 | ✅ |
| 10 Oct | 1 | SQLBolt lessons 5–8 | ✅ |
| 12 Oct | 1 | Lesson 8 practice + COUNT / GROUP BY / HAVING / execution order | ✅ |
| 13 Oct | 1 | SQLBolt lessons 9–18 (all done) | ✅ |
| 14 Oct | 1 | LeetCode SQL 50: problems 1–6 done (#4 redone with DISTINCT; #6 used LEFT JOIN … USING). Learned: DISTINCT vs GROUP BY, operators run left to right, REPLACE/LENGTH/TRIM word count | ✅ |
| | 1 | **Pick up here:** (a) problem 7 onward; (b) retype `HAVING SUM(amount) > 10000` (alias not allowed in HAVING); (c) predict ON vs WHERE in a LEFT JOIN: buildings A,B + employees Ravi,Sita — which query still shows B?; (d) redo 3 old problems from scratch in 3–4 days | |
| | 1 | | |
| | 1 | | |

*Add a row each day. One line is enough.*

## My case study (fill in weeks 7–8)

- **Problem:** stock numbers disagreed across MIDAP, CBX and Oracle — nobody trusted them.
- **What I did:**
- **Result:** system stock within ~1% of the physical count.
- **What I learned:**
