# AI Sentinels workshop packs

Claude plugins for AI Sentinels workshops (https://aisentinels.me/). Attendees install **Core**, then only the packs that match their role.

| Pack | For | Skills |
| --- | --- | --- |
| AI Sentinels Core (`ai-sentinels-core`) | Everyone | 13 skills + 4 PDF commands: day planning, memory, search across tools, daily digest, PDF review and signing (optional local viewer, needs Node.js), setup wizard, time-saved log, Copilot agents guide |
| People & Ops (`ai-sentinels-people-ops`) | HR, operations, admin, project leads | 26 skills + 1 command: policy answers, onboarding, interviews, reviews, process docs, runbooks, status reports, risk and vendor reviews, stakeholder updates |
| Comms & Marketing (`ai-sentinels-comms`) | Marketing, communications, admissions | 8 skills: content, brand review, campaigns, email sequences, SEO, performance reports |
| Finance & Data (`ai-sentinels-finance-data`) | Finance, planning, reporting | 18 skills: close, reconciliation, variance analysis, audit support, data exploration, charts, dashboards |
| Business Growth (`ai-sentinels-business-growth`) | Sales teams, small business owners | 80 skills: prospecting, call prep, pipeline, forecasts, plus small-business workflows for inbox, invoices, proposals, payroll prep |

## Install

**Claude desktop app (Cowork):** open the plugin settings, add the catalogue `AIsentinels/ai-sentinels-plugins` (https://github.com/AIsentinels/ai-sentinels-plugins), then tick the packs you want. Alternatively upload the individual `.plugin` file for each pack.

**Claude Code:**

```
claude plugin marketplace add AIsentinels/ai-sentinels-plugins
claude plugin install ai-sentinels-core@ai-sentinels
claude plugin install ai-sentinels-people-ops@ai-sentinels   # pick only what you need
```

Then ask Claude: "set up AI Sentinels". The wizard recommends packs for your role, records your organisation's context and data rules, and starts your time-saved log.

## Microsoft 365 Copilot

Facilitator, Analyst and SharePoint agents are switched on inside Microsoft 365, not installed here. The `copilot-agents-guide` skill in Core explains what each does and the admin steps.

## Licence

Apache-2.0. Built on [anthropics/knowledge-work-plugins](https://github.com/anthropics/knowledge-work-plugins), repackaged into role packs with AI Sentinels skills added. See each pack's NOTICE.
