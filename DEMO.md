# 🎬 Project Demo — Auto Ticket Classification using Flow Designer

This walkthrough demonstrates the complete working solution. Each step is backed by the evidence screenshot linked below.

## Live demonstration sequence

1. **Create a ticket** — New record in the *School IT Ticket* table: Caller = System Administrator, Short description = `WiFi not working in lab` → **Submit** (ticket SCH0001006 created).
2. **Automatic classification** — The flow (trigger: Record Created, Category is empty) classifies the ticket instantly:
   - Category → **Network**, Subcategory → **Wi-Fi**
   - ![Classified ticket](Milestone-4/Activity%203%20-%20Test%20Scenario%203%20(Projector%20Ticket%20Auto%20Classified).png)
3. **Email confirmation** — System Logs → Emails shows "Your Request for the issue has been submitted." sent to the caller (Body: "Ticket confirmation message."), source header `X-ServiceNow-Source: Flow Designer`.
   - ![Email log](Milestone-4/Activity%202%20-%20Test%20Scenario%202%20(Email%20Notification%20Log).png)
4. **The automation** — Flow Designer flow "Auto Classify School IT Tickets" (Global, Published & Active): If/Else-If chain on Short-description keywords → Update Record → Send Email.
   - ![Flow](Milestone-3/Activity%201%20-%20Auto%20Classification%20Flow%20(Published).png)

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
![Update set](Milestone-5/Activity%201%20-%20Update%20Set%20Complete%20State%20(35%20updates).png)
