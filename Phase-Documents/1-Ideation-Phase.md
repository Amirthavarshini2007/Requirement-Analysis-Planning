# 1. Ideation Phase — Auto Ticket Classification using Flow Designer

## Problem statement
The school IT helpdesk receives multiple incident requests daily from students and teachers (Wi-Fi issues, projector failures, password problems, slow computers). IT staff manually review each request, identify the issue type, select the correct category/subcategory, and inform the caller — a time-consuming, error-prone process that does not scale.

## Proposed solution
Automate ticket triage with **ServiceNow Flow Designer**: when a ticket is created in the *School IT Ticket* table with no category, a flow analyzes keywords in the Short description, sets Category + Subcategory, and emails the caller a confirmation.

## Expected outcomes
- Zero-touch triage — tickets categorized at creation time
- Consistent, structured data via dependent choice fields
- Instant caller acknowledgment via automated email
- Staff time redirected from routing to resolving
