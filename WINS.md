# What I built — WIP_HEART and more (Dec 2025 → Oct 2026)

Joined R Studio (couture garment business, Ludhiana) on 4 Dec 2025 as a fresher
with no coding background. Built everything below myself, using Claude Code to
write the code — I decide what gets built, explain the business to it, check
every number against the floor, and catch it when it is wrong.

The business ran on three systems that disagreed with each other: **MIDAP**
(production steps), **CBX** (old software) and **Oracle** (billing). Nobody
trusted any number.

## The main system — WIP_HEART
Web app (React + FastAPI + Postgres/Supabase), used every working day by
~18 users: both MDs, production, dispatch, sales.

| What | Before | After |
|---|---|---|
| **Stock** — what is on the shelf | Nobody knew without walking the racks | Stock built from three systems; within **1.3%** of the 21 Sep 2026 physical count (1,320 vs 1,303 pcs) |
| **"Where is this piece / who got it / how many made?"** | ~1 hour per style, no one owned the task, MDs asked daily | Answered in seconds in the catalogue / WIP tracker |
| **Dispatch records** | MIDAP captured **52%** of real dispatches | **75%** by manual fixes (lots wrongly shown "still on shelf" fell **790 → 203**); now **API-integrated → should be 100%** (to verify: last month's dispatch count, system vs Oracle = ___ / ___) |
| **Delays** | The delay signal was thrown away at import (58 delayed rows in the whole table) | Delay Report shows what's stuck and who to call (e.g. 127 lots stuck at one printing step) |
| **Second brand (KK)** | Not in the system | Own stock count, catalogue, stock view — kept separate from R Studio |
| **Running cost** | — | Near zero; fixed a data-usage problem that had got the database cut off |

Pages: WIP tracker, Production Board, Dispatch Queue, Delay Report, Stock Board,
Photo Catalogue (live stock per style, Sangini vs Raja, price, who bought it,
returns, total ever made), Daily Flow (pieces in/out per day, any date range),
Produce/Hold decisions, Repeats, Decisions (Push / Discount / Produce more).

## Other software
- **SDWL AI LENS** — sales dashboard with product thumbnails: who bought what,
  when, what came back, revenue. **Used daily by the MDs to decide what to sell
  today, to whom, and how much.**
- **Designer Directory** — tracks designers' submitted designs. Before: **zero**
  visibility of designer output. Now performance can be measured.

## Feedback
The MDs have praised the catalogue, AI LENS and the Designer Directory many times.
(Still to recall: one specific moment + what it helped with.)

## Interview stories (Amazon Leadership Principles)
- **Dive Deep:** Daily Flow showed 76 pieces sold on 9 Oct; Oracle's sheet said 78.
  I didn't accept it — traced the 2 missing pieces to MT (made-to-measure) bills
  1516 and 1517, which the stock model deliberately excludes. Now shown separately.
- **Dive Deep:** spotted the catalogue was ~50 pieces short of the stock board
  when it "looked fine" — styles on the shelf with no catalogue entry were being
  dropped. Fixed so catalogue total = board total for both brands.
- **Ownership:** built the entire stock system alone — reconciling three systems
  that disagree, against physical counts.
- **Customer Obsession:** catalogue designed around how the MD and Manish
  (dispatch) actually work — e.g. a party filter that is Manish's packing list.
- **Bias for Action / Frugality:** ran everything on near-zero spend.

## Still to fill in
- How many "where is X?" questions per day before → hours saved per month.
- One decision the MDs made with AI LENS, with its result.
- The best praise moment.
