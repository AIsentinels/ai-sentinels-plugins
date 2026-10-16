---
name: copilot-agents-guide
description: Explains and walks through switching on Microsoft 365 Copilot's built-in agents (Facilitator, Analyst, SharePoint agents, plus Researcher, Planner Agent and others) for staff and IT admins. Use when someone asks "how do I use Facilitator", "turn on Copilot agents", "Analyst agent", "SharePoint agent", "which Copilot agent should I use", "we have Copilot not Claude", or wants a Copilot equivalent of an AI Sentinels skill.
---

# Copilot agents guide

Help organisations on Microsoft 365 use the agents Microsoft already ships, alongside or instead of Claude. These agents live inside Microsoft 365; they are not installed through this plugin. Be clear about that.

Facts below were current at September 2026. Microsoft changes names, status and licensing often: say so, and point admins to Microsoft Learn to confirm before rollout.

## The three AI Sentinels picks

| Agent | What it does | Where it lives | Needs | Status |
| --- | --- | --- | --- | --- |
| Facilitator | Joins scheduled Teams meetings, keeps shared notes, runs the agenda timer, answers questions in chat, posts a recap | Teams meetings | Microsoft 365 Copilot licence to prompt it; Loop experiences on in Teams | Core features GA; Planner task tracking in preview |
| Analyst | Turns spreadsheets and files into insights and charts, writing and running code itself | Copilot app / Copilot Chat | Microsoft 365 Copilot licence (monthly query allowance) | GA |
| SharePoint agents | Each site has an agent that answers from that site's files, only what the person may already see; editors can build scoped agents and share them to Teams | SharePoint sites | Copilot licence, or admin-enabled pay-as-you-go billing for unlicensed staff | GA |

Others worth knowing: Researcher (cited research reports, GA), Planner Agent (plans and status reports, GA), Channel Agent (per-channel expert, preview), Employee Self-Service (HR and IT policy answers, preview, thin documentation), Knowledge Agent (tidies SharePoint libraries, preview).

## For staff: how to use each

- **Facilitator**: only in scheduled meetings (not calls, chats or Meet now). Add it from the meeting's Copilot or agents menu; anyone can read its notes, only licensed users can prompt it. Try: "Keep us to the agenda and list decisions and owners."
- **Analyst**: open Copilot, choose Analyst from the agents list, attach the spreadsheet. Try: "What changed most versus last month, and why might that be? Show a chart."
- **SharePoint agents**: open the site, select the Copilot/agent button. Try: "What is our process for X? Quote the document." For a team, ask a site editor to create a scoped agent on the right library.

## For IT admins: switching them on

1. Assign Microsoft 365 Copilot licences to the pilot group.
2. Microsoft 365 admin center → Agents: check Microsoft agents are allowed in Agent settings; use the Registry to see what is live.
3. Teams admin center: allow Facilitator under app management; make sure Loop experiences are enabled.
4. SharePoint admin center: confirm SharePoint agents are enabled; set up pay-as-you-go billing if unlicensed staff need them (billed per query).
5. Before broad rollout, check SharePoint permissions: agents answer from whatever people can already access, so over-shared sites surface in answers.

## Matching AI Sentinels skills to Copilot

| Need | Claude (AI Sentinels pack) | Copilot agent |
| --- | --- | --- |
| Meeting notes and actions | Core: start, task-management | Facilitator |
| Find information across files | Core: search, digest | SharePoint agents, Researcher |
| Spreadsheet analysis | Finance & Data: analyze, create-viz | Analyst |
| Status reports and plans | People & Ops: status-report | Planner Agent |
| HR and IT policy questions | People & Ops: policy-lookup | Employee Self-Service (preview) |

## Rules

- Do not say an agent is available in the user's tenant without them confirming; availability depends on licences and admin settings.
- When the user asks for official steps, point to Microsoft Learn ("AI agents in Microsoft Teams", "Get started with agents in SharePoint", "Get started with Analyst") rather than inventing menu paths.
