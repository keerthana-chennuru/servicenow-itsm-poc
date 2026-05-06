# servicenow-itsm-poc
POC ITSM Management – Custom Tables &amp; Update Sets

### 📌Overview

Designed and built a custom ITSM application to streamline Incident, Change, and Problem
management in ServiceNow. The solution extends core platform tables using best-practice
inheritance patterns and manages configuration deployment using structured Update Sets.

### 🎯Objectives

Build a custom ITSM application in Global scope following ServiceNow best practices
Extend base ITSM tables to maintain core platform inheritance and functionality
Manage configurations across modules using separate, structured Update Sets
Ensure clean, error-free promotion of configurations across instances



## 📖 What Was Built

### Custom Tables (Table Inheritance):

Three custom tables were created, each extending a standard ServiceNow ITSM table:
Custom Table System Name Extends
POC Incident table u_poc_incident_table Incident
POC Change table u_poc_change_table Change Request
POC Problem Management table u_poc_problem_management_table Problem

| Custom Table System Name | Extends |
|---|---|
| POC Incident table | `u_poc_incident_table` | Incident |
| POC Change table | `u_poc_change_table` | Change Request |
| POC Problem Management table | `u_poc_problem_management_table` | Problem |<img width="297" height="92" alt="Picture2" src="https://github.com/user-attachments/assets/b9c2ed66-3156-4730-ac2c-e91e7fbd7502" />


Extending base tables means all inherited fields, business rules, and platform logic from the
parent table are automatically available no duplication required.

### Update Sets Management:

Separate Update Sets were maintained for each module to ensure modular, controlled

### Deployment:

#### Update Set Purpose Status:

POC Inc Incident table configurations Complete
POC change Change table configurations Complete
POC prb Problem table configurations Complete
POC ITSM Management Full application scope Complete
Service Catalog work Catalog configurations Complete


### Commit & Preview Process:

All Update Sets were validated through the Preview → Commit workflow before being applied,
ensuring zero collisions and error-free migration.

--------

## ⚙️Technical Details

1. Application Scope: POC ITSM Management (Global)
2. Update Set Strategy: Separate sets per module (Incident, Change, Problem)
3. Table Design: Inheritance-based (avoids data duplication, reuses platform logic)
4. Deployment: Preview validated before commit; dependency order maintained



## 💡Key Challenges & Solutions

- Challenge: Managing multiple Update Sets without causing dependency errors during
promotion.
- Solution: Maintained a deliberate promotion order tables first, then configurations to
prevent missing reference errors.
- Challenge: Avoiding accidental changes in the wrong Update Set.
- Solution: Always verified the active Update Set before making any configuration change.
- Challenge: Scoped application migration.
- Solution: For scoped apps, used Application XML export/import instead of relying solely on
Global update sets to prevent scope mismatch errors.



## ✅Skills Demonstrated

ServiceNow Table Design & Inheritance

ITSM Process Knowledge (Incident, Change, Problem)
Update Set Management & Promotion
Application Scoping (Global scope)
Configuration Dependency Management
Error-free instance-to-instance migration

----

## ⚠️Common Mistakes to Avoid

- Forgetting to set the correct Update Set as current before making changes
- Making changes in the wrong application scope
- Committing Update Sets without previewing first
- Using one large Update Set for everything (makes rollback and debugging difficult)
- Mixing Global and scoped update sets for scoped applications

----

## 📸Screenshots

<img width="297" height="92" alt="Picture2" src="https://github.com/user-attachments/assets/fc2fbca4-a749-49a1-aae0-0b1d68f1ca75" />

------

<img width="452" height="257" alt="Picture3" src="https://github.com/user-attachments/assets/16abae62-f63b-4103-a10f-0f8a3748f378" />

------

<img width="452" height="259" alt="Picture4" src="https://github.com/user-attachments/assets/23e0015d-ac81-42ed-b52d-ed6394931fd3" />

-------

<img width="452" height="192" alt="Picture5" src="https://github.com/user-attachments/assets/453a4cf7-f6ce-4737-86d1-4167139e68ed" />

------

<img width="452" height="203" alt="Picture6" src="https://github.com/user-attachments/assets/79c1d0b2-7698-499f-a038-b1bc6ab7f2f2" />

------


<img width="452" height="241" alt="Picture7" src="https://github.com/user-attachments/assets/e3ae51f7-9e3c-4464-a9b2-706b0379d87b" />

------

<img width="447" height="361" alt="Picture8" src="https://github.com/user-attachments/assets/a2ad3609-fe20-4fe1-82c3-dcae6ed6f9e9" />





