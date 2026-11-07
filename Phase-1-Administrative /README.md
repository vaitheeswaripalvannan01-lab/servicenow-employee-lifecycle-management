# Employee Lifecycle Management (ServiceNow)

A scoped ServiceNow application to manage employee onboarding and offboarding requests.
**Phase 1: Administrative (Implementation)**

## Demo video
[Watch the 2-minute walkthrough](PASTE-YOUR-VIDEO-LINK-HERE)

The video shows: creating an onboarding request, Department filling the Assignment group, Assigned to filtered by group, switching to Offboarding, state changes on the Process Flow bar, and the Knowledge suggestions.

## Problem
New hire and exit tasks were scattered across emails and chats. Managers, HR, IT and Facilities had no single place to see what was requested, who owned it, or what was still pending. This led to missed steps, such as a laptop or access card not being ready on day one, and unreturned assets after an employee left. This app keeps one request per employee with clear status, ownership and rules, so every team works from the same record.

## What I built

| Area | Details |
|---|---|
| **Application** | Scoped app with an application menu and filtered list modules |
| **Tables** | Employee Request and Onboarding Task, linked by a Parent request reference with a related list |
| **Form design** | Tabs (Dates, Requirements, Offboarding, Notes), choice, reference and radio button fields |
| **Formatters** | Process Flow, Activities (filtered), Contextual Search Results |
| **Rules** | Mandatory fields, UI policies, client scripts, data policy |
| **Automation** | Data lookup (Department to Assignment group), dependent Assigned to, dot walking |
| **Knowledge** | Knowledge base with categories and articles, Knowledge lookup on Short description |

## Challenges and fixes
- A mandatory empty field cannot be hidden with `setDisplay`, so the script clears the mandatory flag first.
- UI policy reversal clashed with the client script, so visibility is handled in the script and mandatory rules in the policies.
- Short description had to be a String field for Knowledge search to work.
- Contextual Search needed a table configuration, a search field and a context with a searcher.

## Tech used
ServiceNow PDI, Studio, UI policies, data policies, client scripts (JavaScript), data lookup, reference qualifiers, Knowledge Management

## Design note
The tables are standalone, so SLA and built-in approvals are not available. A production version would extend the Task table.

## Next phases
- Service catalog and Flow Designer
- Business rules, script includes and notifications
