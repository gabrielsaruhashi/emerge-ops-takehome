# Emerge Career: Ops Take-Home

Thanks for taking the time. This is the work you'd do in your first 90 days, not a puzzle.

**Time box: 3 hours.**

**Deadline: submit within 4 days of receipt.**

**Use Claude Code (or your AI tool of choice) for the analysis and code.** We care about your judgment and how you direct the tool, not whether you hand-write pandas. Read `CLAUDE.md` first; it sets the rules your AI tool should follow in this repo.

---

## Context

Emerge Career trains justice-impacted people for CDL (commercial driver's license) careers in **NYC, Sacramento, and Boston**. The path looks like this:

1. **Create account (CA).** Student signs up and usually builds a training plan (pace, study days, target permit date).
2. **First video (FV).** Student finishes Lesson 1. This is activation.
3. **Course complete (CC).** Student finishes all 21 online lessons.
4. **Permit (CLP).** Student sits the Commercial Learner's Permit written exam in person at the DMV and passes.

Today, roughly **1 in 10 signups ends up holding a permit.** Most of the loss happens between the first video and finishing the course.

Your job: figure out where students drop, decide which lever to pull, and build a dashboard so the team can operate it.

## The data

Synthetic exports live in `data/`. The snapshot was taken **September 15, 2026 at 6:00 AM ET**. The field-by-field definitions are in `data/DATA_DICTIONARY.md` (same content as a spreadsheet in `data/README.csv`).

| File | Grain | Rows |
|---|---|---|
| `data/students.csv` | one row per student (user summary) | ~3,000 |
| `data/lesson_events.csv` | one row per lesson a student completed | ~20,000 |
| `data/lessons.csv` | one row per lesson in the course | 21 |
| `data/seats_by_city.csv` | one row per city (training seats we can fund) | 3 |

The data is not perfectly clean. Real exports never are. Demand already outstrips supply — we have roughly one seat for every ten students who sign up:

| City | Students | Seats |
|---|---|---|
| NYC | ~2,000 | 200 |
| Sacramento | ~750 | 75 |
| Boston | ~250 | 25 |

---

## Deliverables

### 1. `COMMUNITY_PLAN.md` — your written plan (1,000 words max; write this yourself)

Four sections:

- **Problems.** What did you find in the funnel? Where does it break, for whom, and by how much?
- **Priority.** Which problem are you going to work on first, and why that one over the others?
- **Interventions.** What will you actually do? Who does it target, what's the format and cadence, who owns it?
- **Measurement.** How do you know it's working? Name the metric and how you'd prove the intervention moved it.

Diagrams or images are welcome if they add clarity. Word limit is a hard cap — we value conciseness.

### 2. A dashboard — renderable, not raw code

Build something the team can open to monitor the cohort and track whether the interventions are working. HTML or a spreadsheet. Put the source code in `analysis/`.

---

## How we'll evaluate

- **Critical thinking**
- **Strategy**
- **AI fluency**
- **Prioritization & execution**

## Ground rules

- The data is synthetic. No real students are in it.
- Questions? Email us. If we can't answer fast, make a call, write down your assumption, and keep going.
