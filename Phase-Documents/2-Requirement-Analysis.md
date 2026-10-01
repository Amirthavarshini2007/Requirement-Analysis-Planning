# 2. Requirement Analysis — Solution Requirements & User Stories

## Functional requirements
| ID | Requirement |
|---|---|
| FR-1 | Maintain a custom table **School IT Ticket** storing caller, issue description, category, subcategory, state and assignment fields |
| FR-2 | Auto-number every ticket (prefix SCH) |
| FR-3 | Classify tickets automatically on creation from Short-description keywords (WiFi/Wi-Fi/Network → Network+Wi-Fi; Projector → Hardware+Projector; Forgot password → Access+Forgot Password; Slow Computer → Performance+Slow Computer) |
| FR-4 | Run classification only when Category is empty (never overwrite manual triage) |
| FR-5 | Category → Subcategory dependency: only valid subcategories are selectable per category |
| FR-6 | Email the caller automatically after classification ("Your Request for the issue has been submitted.") |
| FR-7 | Provide the update set export for deployment to other instances |

## Non-functional requirements
- No-code implementation (Flow Designer only, no scripting)
- Classification latency: near-real-time (background flow on record insert)
- Maintainability: single flow, declarative configuration, update-set managed

## User stories
1. As a **student**, I submit an IT issue with a short description so that I don't need to know the right category.
2. As a **teacher**, I receive an automatic email confirming my ticket was logged.
3. As the **system**, I classify each new ticket by keywords and set Category/Subcategory.
4. As **IT staff**, I receive correctly categorized tickets so I can start resolving immediately.
5. As the **helpdesk manager**, I export the update set so the solution can be deployed to other instances.
