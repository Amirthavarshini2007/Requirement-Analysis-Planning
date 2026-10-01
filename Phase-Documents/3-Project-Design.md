# 3. Project Design — Data Design & Flow Design

## Table design — School IT Ticket (u_school_it_ticket)
| Field | Type | Details |
|---|---|---|
| Number | Auto Number | Prefix SCH (SCH0001001+) |
| Caller | Reference → sys_user | Ticket raiser |
| Category | Choice | Network, Hardware, Access, Performance |
| Subcategory | Choice (dependent on Category) | Wi-Fi, Projector, Forgot Password, Slow Computer |
| Short description | String(100) | Classification keyword source |
| Description | String(4000) | Details |
| State | Choice | New, In progress, On hold, Resolved, Closed |
| Assigned Group | Reference → sys_user_group | |
| Assigned to | Reference → sys_user | |

Dependency configuration: Subcategory dictionary `use_dependent_field = true`, `dependent = Category`; each subcategory choice carries dependent_value network/hardware/access/performance.

## Flow design — "Auto Classify School IT Tickets" (Global)
- **Trigger:** Record Created on School IT Ticket WHERE Category is empty
- **If** Short description contains WiFi / Wi-Fi / Network → Update: Category=Network, Subcategory=Wi-Fi
- **Else If** contains Projector → Update: Hardware / Projector
- **Else If** contains Forgot password → Update: Access / Forgot Password
- **Else If** contains Slow Computer → Update: Performance / Slow Computer
- **Send Email** → To: Caller.email, Subject: "Your Request for the issue has been submitted.", Body: "Ticket confirmation message."

## Data flow (level 1)
Caller → [School IT Ticket record created] → (Flow: keyword evaluation) → [Update Record: Category/Subcategory] → [Send Email to Caller] → Caller inbox
