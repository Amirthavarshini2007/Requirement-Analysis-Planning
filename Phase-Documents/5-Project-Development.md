# 5. Project Development — Implementation Record

## Build order
1. **Update set** "Project Update Set" (Global, In progress) created and set as current — all configuration captured (35 customer updates).
2. **Table** School IT Ticket created via Tables form with auto-number (NumberMaintenance) — SCH prefix verified by test insert.
3. **Fields** created per spec: Caller, Category, Subcategory, Short description, Description, State, Assigned Group, Assigned to.
4. **Choices** loaded: Category (network/hardware/access/performance), State (New…Closed), Subcategory with dependent values.
5. **Dependency** applied on Subcategory dictionary (use_dependent_field=true, dependent=Category).
6. **Flow** "Auto Classify School IT Tickets": trigger Record Created (Category empty) → If/Else-If keyword classification → Update Record ×4 → Send Email.
7. **Activation**: flow compiled and published (snapshots created, Deactivate available).

## Evidence (see repo folders)
- Milestone-2: table, fields, dependency screenshots
- Milestone-3: flow canvas (Published)
- Milestone-4: classified tickets SCH0001002–SCH0001006, email log, email record with Flow-Designer source header
- Milestone-5: update set Complete
