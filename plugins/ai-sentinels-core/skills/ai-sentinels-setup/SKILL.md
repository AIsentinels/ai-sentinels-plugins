---
name: ai-sentinels-setup
description: Guided first-run setup for AI Sentinels workshop attendees. Use when someone says "set up AI Sentinels", "get started", "which packs should I install", "I'm new to the workshop plugins", "set me up for my role", or runs /ai-sentinels-setup. Asks role and department, recommends which AI Sentinels packs and skills to use, captures organisation context, and points to the first exercise.
---

# AI Sentinels setup wizard

Run a short, friendly setup so the attendee leaves with the right packs, a saved profile, and one task to try. Keep language plain: no file paths, JSON or plugin jargon unless asked. Use NZ English.

## Step 1: Who they are

Ask with AskUserQuestion (one call, up to four questions):

1. **Role level**: Senior leader / Manager / Professional staff / Academic or teaching / Other.
2. **Department** (multi-select): Marketing & comms; Student or customer services; Admissions & recruitment; Finance & admin; HR & people; IT & operations; Projects & planning; Sales & business development; Small business owner; Teaching & learning.
3. **AI tools at work** (multi-select): Claude; Microsoft 365 Copilot; Google Gemini; None approved yet; Not sure.
4. **Main time sink** this week: Meetings & email; Writing documents & reports; Finding information; Answering the same questions; Spreadsheets & reports.

## Step 2: Recommend packs

Map answers to packs using this table. Recommend Core to everyone, then at most two more. Explain each in one line in terms of the work it helps with.

| Department or need | Pack | Start with these skills |
| --- | --- | --- |
| Everyone | AI Sentinels Core | start, task-management, search, digest, time-saved-log |
| HR & people | People & Ops | policy-lookup, onboarding, interview-prep, performance-review |
| IT & operations, admin | People & Ops | process-doc, runbook, status-report, change-request |
| Projects & planning, leaders | People & Ops | stakeholder-update, status-report, risk-assessment |
| Marketing & comms, admissions | Comms | draft-content, brand-review, campaign-plan, email-sequence |
| Finance & admin | Finance & Data | variance-analysis, reconciliation, close-management |
| Planning, reporting, institutional research | Finance & Data | analyze, explore-data, create-viz, build-dashboard |
| Sales & BD, international recruitment | Business Growth | call-prep, account-research, draft-outreach, pipeline-review |
| Small business owner | Business Growth | monday-brief, inbox-manager, invoice-chase, proposal-builder |
| Student or customer services, teaching & learning | Core for now | search, digest; flag that a dedicated pack is coming |

Then check what is installed: if a recommended pack is missing, tell them its name and that they can add it from the AI Sentinels catalogue in Claude's plugin settings. Never claim a pack is installed without checking.

If they selected Microsoft 365 Copilot, mention the **copilot-agents-guide** skill in one line.

## Step 3: Organisation context

Ask, in one AskUserQuestion call or plain questions:

- Organisation name and team.
- Where documents live (SharePoint/OneDrive, Google Drive, other).
- Any data they must not put into AI (offer examples: student or patient records, staff pay and performance, unpublished research, anything marked confidential). Record their answer as stated; do not invent rules.
- Preferred writing style (NZ English default; formal or plain).

Save the answers to `ai-sentinels-profile.md` in their working folder with sections: Role, Department, Tools, Data rules, Writing style, Recommended packs, Date. If the productivity pack's memory is set up (a CLAUDE.md exists), append a short "AI Sentinels profile" section there too, rather than duplicating detail.

## Step 4: First win

Suggest one concrete task matched to their main time sink, phrased as a prompt they can paste now:

- Meetings & email: "Prep me for my next meeting: who's attending, what was decided last time, and three questions to ask."
- Writing: "Turn these notes into a one-page briefing for my manager."
- Finding information: "Find everything we have on <topic> across email, chat and documents, with sources."
- Repeat questions: "Draft answers to these five questions I get every week, with the policy each comes from."
- Spreadsheets: "Explain the three biggest changes in this sheet versus last month."

Then offer to start a time-saved log entry for that task (the **time-saved-log** skill) so they capture a before time first.

## Rules

- Recommend, never force; the attendee decides what to install.
- Keep the whole setup under five minutes.
- If the user skips a question, carry on with sensible defaults and say which ones were assumed.
