# Emerge Career: Ops Take-Home

This is the work you'd do in your first 90 days, not a puzzle.

**Time box: 3 hours. Deadline: 4 days from receipt.**

Use Claude Code (or any AI tool) for the analysis and code. We care about your judgment and how you direct it, not whether you hand-write pandas. Read `CLAUDE.md` first.

---

## Context

Emerge trains justice-impacted people for CDL careers in NYC, Sacramento, and Boston. The funnel:

1. **Create account (CA).** Student signs up and builds a training plan.
2. **First video (FV).** Student completes Lesson 1. This is activation.
3. **Course complete (CC).** Student finishes all 21 lessons.
4. **Permit (CLP).** Student passes the Commercial Learner's Permit written exam at the DMV.

Roughly 1 in 10 signups holds a permit. Most loss happens between first video and course complete.

Your job: find where students drop, pick the lever to pull, and build a dashboard so the team can operate it.

## The data

Synthetic exports in `data/`. Snapshot taken **September 15, 2026 at 6:00 AM ET**. Field definitions in `data/DATA_DICTIONARY.md`.

| File | Grain | Rows |
|---|---|---|
| `data/students.csv` | one row per student | ~3,000 |
| `data/lesson_events.csv` | one row per completed lesson | ~20,000 |
| `data/lessons.csv` | one row per lesson in the course | 21 |
| `data/seats_by_city.csv` | one row per city | 3 |

The data is not clean. Demand outstrips supply about 10 to 1:

| City | Students | Seats |
|---|---|---|
| NYC | ~2,000 | 200 |
| Sacramento | ~750 | 75 |
| Boston | ~250 | 25 |

---

## Deliverables

### 1. A Google Doc (1,000 words max; write this yourself)

Four sections:

- **Problems.** Where does the funnel break, for whom, and by how much?
- **Priority.** Which problem are you tackling first, and why?
- **Interventions.** What will you run? Who does it target, what is the format and cadence, who owns it?
- **Measurement.** What is the one number you are moving? How do you prove the intervention moved it?

Diagrams welcome. 1,000 words is a hard cap. Share with link-anyone-can-comment and include the link when you submit.

### 2. A dashboard (renderable, not raw code)

Something the team can open to monitor the cohort and track whether interventions are working. HTML or a spreadsheet. Source code in `analysis/`.

---

## How we evaluate

- Critical thinking
- Strategy
- AI fluency
- Prioritization and execution

## Ground rules

The data is synthetic. Questions? Email us. If we can't answer fast, make a call, write down the assumption, and keep going.
