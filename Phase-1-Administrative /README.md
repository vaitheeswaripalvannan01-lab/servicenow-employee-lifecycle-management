# Employee Lifecycle Management (ServiceNow)

A scoped ServiceNow application to manage employee onboarding and offboarding requests.
**Phase 1: Administrative (Implementation)**

## Demo Video

[Watch the 2-minute Employee Lifecycle Management walkthrough](https://www.youtube.com/watch?v=_p9C5L2T0ok)

The video shows: creating an onboarding request, Department filling the Assignment group, Assigned to filtered by group, switching to Offboarding, state changes on the Process Flow bar, and Knowledge suggestions.

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

See the screenshots below for each part.

## Screenshots

### 1. Application and table
| ServiceNow Studio application | Custom table |
|:---:|:---:|
| <img width="450" alt="servicenow studio application" src="https://github.com/user-attachments/assets/c9023163-4157-46c6-a8e6-1e997254f0b7" /> | <img width="450" alt="custom-table" src="https://github.com/user-attachments/assets/9aef2632-5afe-4ace-96da-aff61a308ac1" /> |

### 2. Form
<img width="800" alt="employee-form" src="https://github.com/user-attachments/assets/e93ba298-a00b-4516-89db-444b752ed6c5" />

### 3. Rules
| UI policy | Data policy |
|:---:|:---:|
| <img width="450" alt="ui-policy" src="https://github.com/user-attachments/assets/c2ff1fbf-b432-41fb-aa4a-8938cebce365" /> | <img width="450" alt="data-policy" src="https://github.com/user-attachments/assets/006a6ce5-3bc8-43a6-b7d1-3d3f93f2ccbd" /> |

### 4. Automation and knowledge
| Data lookup rule | Knowledge article |
|:---:|:---:|
| <img width="450" alt="data-lookup-rule" src="https://github.com/user-attachments/assets/0613e0f8-f694-4762-b628-65ccf77f3b29" /> | <img width="450" alt="knowledge-article" src="https://github.com/user-attachments/assets/be157974-a3fd-4d24-8ca7-6e6d38899af2" /> |

## Challenges and fixes
- **Hiding a whole tab:** A UI policy can only hide single fields, so I used a client script with `setSectionDisplay()` to show the Offboarding and Requirements tabs based on Request type.
- **Knowledge search not working:** Short description was a dropdown instead of a text field. Changing it to a text field fixed the search.

## Tech used
ServiceNow PDI, Studio, UI policies, data policies, client scripts (JavaScript), data lookup, reference qualifiers, Knowledge Management

## Design note
The tables are standalone, so SLA and built-in approvals are not available. A production version would extend the Task table.

## Next phases
- Service catalog and Flow Designer
- Business rules, script includes and notifications
