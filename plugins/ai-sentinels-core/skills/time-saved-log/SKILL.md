---
name: time-saved-log
description: Records how long tasks take before and after using AI, and turns the log into hours saved and dollar value. Use when someone says "log my time", "start a baseline", "how much time did AI save", "time-saved log", "ROI of AI", "record before and after", "workshop ROI", or runs /time-saved-log. Supports a per-person log and a team summary for AI Sentinels workshops.
---

# Time-saved log

Give each workshop attendee, and their organisation, a credible number for what AI saves. Credibility matters more than size: record what people actually report, label estimates as estimates, and never inflate.

## Files

Keep one CSV in the user's working folder: `ai-sentinels-time-log.csv`, with header:

`date,person,department,task,frequency_per_week,minutes_before,minutes_after,quality_check_minutes,status,notes`

- `status` is `baseline` (before only), `measured` (before and after both timed) or `estimated` (after is a guess).
- `person` may be initials or "anon" if the user prefers.
- Create the file if missing; append, never overwrite earlier rows.

## Mode 1: Add a baseline

When a user names a task they want to try with AI:

1. Ask: task in a few words, how often per week, and minutes it takes today without AI.
2. Append a `baseline` row.
3. Tell them to come back after trying it with AI.

## Mode 2: Record the after

1. Find the matching baseline row (ask if several match).
2. Ask: minutes with AI, and minutes spent checking or fixing the AI output. Checking time counts; it is part of the real cost.
3. Update the row to `measured` (or `estimated` if they are guessing) rather than adding a duplicate.

## Mode 3: Report

Compute with code, not mental arithmetic:

- Saved per run = minutes_before − (minutes_after + quality_check_minutes)
- Hours saved per week = saved per run × frequency_per_week ÷ 60
- Hours per year = weekly × 44 working weeks (state this assumption; let the user change it)
- Dollar value = hours per year × loaded hourly rate. Ask for the rate; if unknown, offer NZ$60/hour as a placeholder and label it as an assumption.

Report:

- A short table per task: before, after incl. checking, saved per week, status.
- Totals split by `measured` versus `estimated`, so leaders see which numbers are evidence.
- Any task where AI took longer: list it plainly. Negative results are useful.
- One sentence a manager could repeat, e.g. "Across 6 measured tasks, the team saves about 4.5 hours a week (≈200 hours a year)."

## Team summary (for facilitators)

When given several attendees' CSVs, merge them, drop names unless the organisation has agreed to share them, and report by department. Highlight the top three tasks by hours saved and any department with no measured results yet.

## Rules

- Never fill in times the user did not give. Missing after-times stay `baseline`.
- Do not store personal data beyond the name or initials the user chooses.
- Round sensibly: minutes to whole numbers, hours to one decimal place.
