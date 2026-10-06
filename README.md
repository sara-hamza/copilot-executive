# copilot-executive

## What it does

Executive Briefing: converts reports, notes and spreadsheets into decisions, risks, priorities and executive briefs.

Part of the **department-copilots** suite: local-only copilots where the employee provides the input, Claude analyses it on the machine, and the employee decides what to do. No CRM, NMS, email or system integrations.

## Install

```bash
claude plugin marketplace add sara-hamza/department-copilots
```

```bash
claude plugin install executive@department-copilots
```

Drop in the department reports, board papers, meeting notes and spreadsheets for the period and ask "what matters?". Get back a one-page brief, the decisions that need you, and a consolidated risk view, each point traceable to the document and page it came from.

| Command | Use when |
|---|---|
| `/executive:brief <reports and notes>` | One page: 3 things going well, 3 needing attention, key risks, decisions required, likely impact |
| `/executive:decisions <reports and notes>` | Only the decisions required, each with options, recommendation basis, deadline and owner |
| `/executive:risks <reports and notes>` | Consolidated risk view across the sources with likelihood and impact as the sources state them |

Requires `copilot-common` (its document-reader and spreadsheet-reader do the file reading; writing-helper sets the executive tone).

Reference knowledge lives in `skills/executive-briefing/references/`. Risk scales and decision deadlines there are sensible defaults marked `CUSTOMISE`; align them to the company's risk framework and delegations.

The briefing summarises and frames. It does not make the decision or add facts the sources do not contain.
