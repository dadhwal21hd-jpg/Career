# Interview Prep — 10 weeks

**Daily slot: 10:30–11:30 am (most productive time). Phone away. Problems only — no notes, no study docs.**

Goal: analyst roles — AMEX Risk Analyst (stretch), pharma / healthcare analytics (ZS, IQVIA, Axtria), supply-chain / retail-tech analyst.

## Rules

1. Same hour every day. Missed a day? Do it the next day — never skip two in a row.
2. Solve, don't read. If stuck for 15 min, look at the answer, then solve it again tomorrow without looking.
3. One line in the log below every day. Tell Claude at the start of each session.
4. Stop at 60 minutes, even mid-problem. Frustrated? Stop early — that's tiredness, not stupidity.

## The daily hour (10:30–11:30)

| Minutes | Do |
|---|---|
| 0–10 | Redo one old problem from a blank screen (oldest in "Pick up here") |
| 10–50 | 1–2 new problems. Stuck 15 min → Query Stepper or the answer, then mark it for redo |
| 50–60 | Tell Claude "log it" → log updated and pushed |

- **Quiet moments at work:** light stuff only — step through a problem in the Query Stepper (`visuals/`), or add one Amazon story to WINS.md. No new problems.
- **Sunday:** redo 3 old problems with no help. Any that fail go back on the list.
- **Home:** `git pull` before starting.

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
| 15 Oct | 1 | Problem 7 solved alone (visits with no transaction: LEFT JOIN + IS NULL). Learned: every SELECT column must be in GROUP BY or an aggregate; saw ON vs WHERE outputs; **self-join** — wrote employee + boss query myself, with LEFT JOIN to keep Raja. **Rising Temperature** — correct query written (self-join + `T.recordDate = Y.recordDate + 1`; first try had the −1 on the wrong side) | ✅ |
| 16 Oct | 1 | Rising Temperature: found own ON rule `T.recordDate - Y.recordDate = 1` (date − date = days, Postgres only). **Average Time of Process per Machine** — stuck on writing the 4-rule self-join; saw the answer (rule: re-solve tomorrow) | ✅ |
| 17 Oct | 1 | **Average Time of Process per Machine** — solved (4-rule self-join clicked: s = start rows, e = end rows; fixed `::numeric`). **Employee Bonus** — solved first try (LEFT JOIN + `OR bonus IS NULL`). Students and Examinations — learned GROUP BY with 3 columns (commas, not AND), **CROSS JOIN** = empty attendance register, then LEFT JOIN + `COUNT(e.col)` for zeros; chaining joins (each join attaches to the result so far). Saw the full answer explained line by line. Comic: https://claude.ai/artifact/1WzijCt1S2bZqTEsq1jP5U | ✅ |
| 19 Oct | 2 | **Students and Examinations** — solved from a blank screen after 2 fixes (subject rule in ON; show columns from the register `s.`/`sub.`, count from `e.`). Learned: GROUP BY can hold columns not in SELECT, never the reverse. Built the Query Stepper (`visuals/`). New daily slot 10:30–11:30 am | ✅ |
| 20 Oct | 2 | **Managers with at Least 5 Direct Reports** — solved alone (self-join + GROUP BY + `HAVING COUNT >= 5`); tip: name aliases by role (`w` worker, `m` manager), say the sentence first. **Confirmation Rate** — first try joined the table twice (rows got copied → wrong rate); fixed with one LEFT JOIN + `AVG(CASE WHEN …)`. Learned: COUNT/SUM are calculated at GROUP BY (that's why HAVING can use them); **CASE WHEN** (label per row, or inside SUM/AVG to count/rate some rows); made-up city drill solved first try. ON vs WHERE now clear. **Average Time redo** — from a blank screen, logic perfect, only 3 typos | ✅ |
| 21 Oct | 2 | **Confirmation Rate redo** — blank screen, only missed GROUP BY (found it himself). **Not Boring Movies** — solved (`id % 2 != 0`; first sorted by id instead of rating — reread the last line before submitting). Learned: `!=` is case-sensitive in Postgres → `LOWER(col)`; can't reuse a SELECT alias in the same SELECT (repeat the maths). Started Average Selling Price — stopped, brain fog. Later: learned BETWEEN, COALESCE (first non-NULL), alias rules (table nicknames everywhere; column aliases ORDER BY, + GROUP BY in Postgres), CASE WHEN = Excel IF (label rows, or count some rows inside SUM/AVG). First Average Selling Price attempt: right shape (LEFT JOIN, BETWEEN, GROUP BY) — stopped, frustrated | ✅ |
| 22–23 Oct | 2 | — (skipped) | ❌ |
| 24 Oct | 2 | Raise role-play with "Raja sir" (got 35 → 40k + June review at 45+; fix for the real day: ₹ numbers + get it in writing). **Average Selling Price** — rough try fixed 3 of 4 traps alone (total money ÷ total pieces, BETWEEN order, date rule in ON); saw clean version, then typed it myself; learned `NULLIF(x, 0)` for division by zero. **Project Employees I** — first try | ✅ |
| 25–26 Oct | 2 | — (website launch week) | ❌ |
| 27 Oct | 2 | **Average Selling Price redo** — blank screen, all 4 traps + NULLIF, perfect. Learned: scalar subquery `(SELECT COUNT(*) FROM Users)` = one number; ORDER BY two columns (second breaks ties). Percentage of Users — got confused | ✅ |
| 28 Oct | 2 | **Percentage of Users Attended a Contest** — by eye → sentence → first try (worked out no JOIN needed). **Queries Quality and Percentage** — fixed: subquery ignores GROUP BY (counted whole table) → `SUM(CASE WHEN rating < 3 THEN 1 ELSE 0 END)`; CASE without ELSE gives NULL (AVG skips it). Managers revisit confused → added to Query Stepper | ✅ |
| 29 Oct | 3 | **Revision day.** Blank-screen redos: **Managers with 5 Direct Reports** ✅ (fixed `> 5` → `>= 5`), **Students and Examinations** ✅ (typos: hyphen, comma; forgot ORDER BY), **Rising Temperature** ✅ first try (`t.recordDate - 1 = y.recordDate`). **Confirmation Rate** — stuck on how CASE WHEN runs → added to Query Stepper; big click: piles are stacks of whole rows (was picturing them vertically). Added 3 "Basics" lessons to the Stepper (WHERE vs HAVING, COUNT(*) vs COUNT(col), GROUP BY two columns + SELECT rule). New pre-submit check: scan for `-` and `,` inside names | ✅ |
| | 3 | **Pick up here:** (a) redo **Confirmation Rate** from a blank screen (first 10 min); (b) **Monthly Transactions I** (CASE WHEN); (c) test the rule on one real row before submitting | |
| | 1 | | |
| | 1 | | |

*Add a row each day. One line is enough.*

## My case study (fill in weeks 7–8)

- **Problem:** stock numbers disagreed across MIDAP, CBX and Oracle — nobody trusted them.
- **What I did:**
- **Result:** system stock within ~1% of the physical count.
- **What I learned:**
