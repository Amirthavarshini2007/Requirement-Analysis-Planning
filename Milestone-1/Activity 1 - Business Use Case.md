# Activity 1: Business Use Case

## The problem

The school IT helpdesk receives multiple incident requests daily from students and teachers, such as Wi-Fi issues, projector failures, password problems, and slow computers.

Currently, IT staff manually review each request and assign a category, which is:

- **Time-consuming** — every ticket is read and triaged by a person before work can start.
- **Error-prone** — manual triage leads to inconsistent categories and mis-routed tickets.
- **Not scalable** — as request volume grows, the manual process cannot keep up.

## The objective

Automate ticket classification using **ServiceNow Flow Designer**: when a ticket is created in the School IT Ticket table, the flow analyzes keywords in the *Short description* field and automatically sets:

| Keywords found | Category | Subcategory |
|---|---|---|
| WiFi / Wi-Fi / Network | Network | Wi-Fi |
| Projector | Hardware | Projector |
| Forgot password | Access | Forgot Password |
| Slow Computer | Performance | Slow Computer |

After classification, the caller receives an instant email confirmation that their ticket was logged.

## The outcome

- Zero-touch triage: tickets are categorized the moment they are created.
- Consistent, structured data via dependent Category → Subcategory choice fields.
- Immediate caller acknowledgment through automated email notifications.
- IT staff can focus on resolving issues instead of routing them.
