# 🎬 Project Demo — Auto Ticket Classification using Flow Designer

**Final status: Project Progress 90% — all 12 tasks delivered for review.**

This walkthrough demonstrates the complete working solution. Every activity is mapped to its evidence below.

## Live demonstration sequence

1. **Create a ticket** — New record in the *School IT Ticket* table: Caller = System Administrator, Short description = `WiFi not working in lab` → **Submit** (ticket SCH0001006 created).
2. **Automatic classification** — The flow (trigger: Record Created, Category is empty) classifies the ticket instantly: Category → **Network**, Subcategory → **Wi-Fi**.
3. **Email confirmation** — System Logs → Emails shows "Your Request for the issue has been submitted." sent to the caller (Body: "Ticket confirmation message."), source header `X-ServiceNow-Source: Flow Designer`.
4. **The automation** — Flow Designer flow "Auto Classify School IT Tickets" (Global, Published & Active): If/Else-If chain on Short-description keywords → Update Record → Send Email.

## Evidence index — every activity

| Milestone | Activity | Evidence |
|---|---|---|
| 1 — Requirement Analysis & Planning | Activity 1: Business Use Case | [Business Use Case document](Milestone-1/Activity%201%20-%20Business%20Use%20Case.md) |
| 1 | Activity 2: Creation of New Update Set | ![update set](Milestone-1/Activity%202%20-%20Creation%20of%20New%20Update%20Set%20(Project%20Update%20Set).png) |
| 1 | Activity 3: Navigation steps in Picture View | ![nav](Milestone-1/Actiity-3(Navigation%20steps%20in%20picture%20view).png) |
| 2 — Backend Development & Configuration | Activity 1: Creation of Custom Table | ![table](Milestone-2/Creation%20of%20Custom%20Table%20to%20Store%20Ticket%20Records.png) |
| 2 | Activity 2: Field Creation and Data Type Configuration | ![fields](Milestone-2/Field%20Creation%20and%20Data%20Type%20Configuration.png) · ![fields 2](Milestone-2/Field%20Creation%20and%20Data%20Type%20Configuration%20(2).png) |
| 2 | Activity 3: Dependency Between Category and Subcategory | ![dependency](Milestone-2/Implementing%20Dependency%20Between%20Category%20and%20Subcategory%20Choice%20Fields.png) |
| 3 — Automation using Flow Designer & Email Notification | Activity 1: Auto Classification using Flow design | ![flow](Milestone-3/Activity%201%20-%20Auto%20Classification%20Flow%20(Published).png) |
| 4 — Testing, Validation & Security | Activity 1: Test Scenario 1 | ![s1](Milestone-4/Activity%201.png) |
| 4 | Activity 2: Test Scenario 2 (email check) | ![emails](Milestone-4/Activity%202%20-%20Test%20Scenario%202%20(Email%20Notification%20Log).png) · ![record](Milestone-4/Activity%202%20-%20Email%20Record%20(Flow%20Designer%20source%2C%20Target%20SCH0001003).png) |
| 4 | Activity 3: Test Scenario 3 | ![s3](Milestone-4/Activity%203%20-%20Test%20Scenario%203%20(Projector%20Ticket%20Auto%20Classified).png) |
| 5 — Deployment & Conclusion | Activity 1: Make Update set to Complete State | ![update set](Milestone-5/Activity%201%20-%20Update%20Set%20Complete%20State%20(35%20updates).png) |
| 5 | Conclusion | ![90%](Milestone-5/Conclusion%20-%20Project%20Progress%2090pct.png) |

## Test matrix (executed)

| Ticket | Short description | Auto-assigned | Status |
|---|---|---|---|
| SCH0001002 | WiFi not working in library | Network / Wi-Fi | ✅ |
| SCH0001003 | Projector not turning on. | Hardware / Projector | ✅ |
| SCH0001004 | WiFi not working in library | Network / Wi-Fi | ✅ |
| SCH0001005 | Projector not turning on. | Hardware / Projector | ✅ |
| SCH0001006 | WiFi not working in computer lab | Network / Wi-Fi | ✅ |

## Deployment artifact

Update set **"Project Update Set"** (Global) — State: **Complete**, 35 customer updates, exported to XML for import into any instance.
