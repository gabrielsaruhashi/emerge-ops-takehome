# CLAUDE.md

Guardrails for any AI coding assistant working in this repo. The candidate may add to this file but should not delete rules.

## What this repo is

A take-home for an Ops role at Emerge Career. Emerge trains justice-impacted adults for CDL careers in NYC, Sacramento, and Boston. The data in `data/` is synthetic, exported as of 2026-09-15 06:00 ET. Definitions are in `data/DATA_DICTIONARY.md`. Read it before writing any analysis.

## Hard rules

1. **Never send, post, or schedule anything.** No SMS, email, WhatsApp, Slack, or API calls to messaging tools.
2. **No network calls for data.** Everything you need is in `data/`. Don't fetch, scrape, or invent outside data.
3. **Don't modify files in `data/`.** Treat them as read-only source. Write cleaned copies to `analysis/` if you need them.
4. **Every number must be computed from the files.** No estimates presented as findings. If a number came from a script, the script lives in `analysis/` and reruns from scratch.
5. **Show denominators.** Every rate states its numerator, denominator, and which students were included or excluded.
6. **Flag data problems. Don't silently fix them.** When you find inconsistent values, duplicates, test rows, or fields that disagree with each other, list what you found, how many rows, and what you did about it in `analysis/DATA_NOTES.md`.
7. **Correlation is not cause.** Several fields (group chat, study hall, training plan) are things students choose. Say so whenever you use them to argue for an intervention.

## Funnel definitions (use these, don't invent new ones)

- **CA** = every real student row in `students.csv`.
- **First Video** = student completed lesson 1.
- **Course Complete** = student completed lesson 21.
- **Permit** = `permit_result = passed`.
- Stage rates are step-to-step: FV/CA, CC/FV, Permit/CC.
- Recent signups haven't had time to finish. When you report a rate, say which signup window it covers and why.
- When `lessons_completed` and `lesson_events.csv` disagree, trust `lesson_events.csv` and log the mismatch.
