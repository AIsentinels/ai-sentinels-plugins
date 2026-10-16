---
name: ai-sentinels-setup
description: Guided first-run setup for AI Sentinels workshop attendees. Use when someone says "set up AI Sentinels", "get started", "which packs should I install", "I'm new to the workshop plugins", "set me up for my role", or runs /ai-sentinels-setup. Asks role and department, recommends which AI Sentinels packs and skills to use, captures organisation context, and points to the first exercise.
---

# AI Sentinels setup wizard

Run a short, friendly setup so the attendee leaves with the right packs, a saved profile, and one task to try. Keep language plain: no JSON or plugin jargon unless asked, and mention a file path only when asking where to save. Write in the English the attendee chooses in Step 3 (until then, match how they write).

AskUserQuestion takes at most four options per question and adds "Other" automatically, so keep every option list to four.

## Step 1: Who they are

Ask with AskUserQuestion (one call, four questions):

1. **Role level**: Executive or senior leader / Manager or team lead / Professional or specialist staff / Business owner or founder.
2. **Area of work** (multi-select): Leadership & strategy; Finance, data & reporting; People, operations & IT; Sales, marketing & customers.
3. **AI tools at work** (multi-select): Claude; Microsoft 365 Copilot; Google Gemini; None approved yet or not sure.
4. **Main time sink** this week: Meetings & email; Writing documents & reports; Finding information; Spreadsheets & reports.

Then narrow the department with one more AskUserQuestion call: one multi-select question for each area they picked (skip any area they did not pick):

| Area picked | Department options |
| --- | --- |
| Leadership & strategy | Executive office or CEO; Board & governance; Strategy & transformation; Risk & compliance |
| Finance, data & reporting | Finance & accounting; Data & analytics; Planning & reporting; Procurement |
| People, operations & IT | HR & people; Operations; IT; Projects & PMO |
| Sales, marketing & customers | Sales & business development; Marketing & comms; Customer or student services; Small business |

If they type something else under "Other" (for example teaching & learning, admissions, legal), use it as stated and pick the closest row below.

## Step 2: Recommend packs

Map answers to packs using this table. Recommend Core to everyone, then at most two more. Explain each in one line in terms of the work it helps with.

| Department or need | Pack | Start with these skills |
| --- | --- | --- |
| Everyone | AI Sentinels Core | start, task-management, search, digest, time-saved-log |
| Executive office, board & governance | People & Ops | stakeholder-update, status-report, risk-assessment |
| Executive office, strategy & transformation | Finance & Data | variance-analysis, analyze, build-dashboard |
| Risk & compliance | People & Ops | risk-assessment, compliance-tracking, vendor-review |
| HR & people | People & Ops | policy-lookup, onboarding, interview-prep, performance-review |
| Operations, IT | People & Ops | process-doc, runbook, status-report, change-request |
| Projects & PMO | People & Ops | stakeholder-update, status-report, risk-assessment, roadmap-update |
| Procurement | People & Ops | vendor-review, process-doc |
| Finance & accounting | Finance & Data | variance-analysis, reconciliation, close-management, financial-statements |
| Data & analytics, planning & reporting | Finance & Data | analyze, explore-data, create-viz, build-dashboard |
| Marketing & comms, admissions | Comms | draft-content, brand-review, campaign-plan, email-sequence |
| Sales & business development, international recruitment | Business Growth | call-prep, account-research, draft-outreach, pipeline-review |
| Small business, business owner or founder | Business Growth | monday-brief, inbox-manager, invoice-chase, proposal-builder |
| Customer or student services, teaching & learning | Core for now | search, digest; flag that a dedicated pack is coming |

For an executive or senior leader, lead with the leadership rows even if they also picked other areas.

Then check what is installed: if a recommended pack is missing, tell them its name and that they can add it from the AI Sentinels catalogue in Claude's plugin settings. Never claim a pack is installed without checking.

If they selected Microsoft 365 Copilot, mention the **copilot-agents-guide** skill in one line.

## Step 3: Organisation context

Ask, in one AskUserQuestion call or plain questions:

- Organisation name and team.
- Where documents live (SharePoint/OneDrive, Google Drive, other).
- Any data they must not put into AI (offer examples: customer or student records, staff pay and performance, board papers, deal or pricing information, unpublished research, anything marked confidential). Record their answer as stated; do not invent rules.
- Writing style: which English (New Zealand, Australian, British, US) and tone (formal or plain).

## Step 4: Save the profile (only where they say)

Draft the profile with sections: Role, Department, Tools, Data rules, Writing style, Recommended packs, Date. Then ask where to save it with AskUserQuestion, before writing anything:

- If a `handover/` folder exists in the working folder (as in the AI Sentinels workshop practice pack), offer `handover/ai-sentinels-profile.md` first and mark it recommended.
- Offer `ai-sentinels-profile.md` in the working folder.
- Offer "Don't save it, just show it to me".
- "Other" lets them type a different folder or file name.

Rules for saving:

- Write exactly one file, at the path they chose. Do not create, edit or move any other file.
- If that file already exists, show what would change and ask before overwriting.
- If the write is blocked or denied, do not try another location. Show the profile in the chat so they can copy it.

**CLAUDE.md**: never create one, and never change an existing one unless the attendee agrees explicitly. If a CLAUDE.md exists, ask a separate yes/no question: "Add a short AI Sentinels profile section (three to five lines pointing to your profile) to CLAUDE.md?" Show the exact lines first. Default to no; if they skip or say anything other than yes, leave CLAUDE.md untouched.

## Step 5: First win

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
- The only writes this skill makes are the profile file at the path the attendee chose and, with an explicit yes, the CLAUDE.md section. Anything else (a time-saved log entry, notes) is a separate request.
