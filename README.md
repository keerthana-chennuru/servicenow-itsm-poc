# 🛠️ POC ITSM Management – Custom Tables & Update Sets

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&pause=1000&color=6A9FBF&width=600&lines=ServiceNow+ITSM+Custom+Application;Custom+Tables+%7C+Update+Sets+%7C+Table+Inheritance;Proof+of+Concept+%7C+Global+Scope" alt="Typing SVG" />

![Platform](https://img.shields.io/badge/Platform-ServiceNow-green?style=for-the-badge&logo=servicenow)
![Scope](https://img.shields.io/badge/Scope-Global-blue?style=for-the-badge)
![Type](https://img.shields.io/badge/Type-Proof%20of%20Concept-orange?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen?style=for-the-badge)

---

## 📌 Overview

Designed and built a custom ITSM application to streamline **Incident**, **Change**, and **Problem** management in ServiceNow. The solution extends core platform tables using best-practice inheritance patterns and manages configuration deployment using structured Update Sets.

---

## 🎯 Objectives

- ✅ Build a custom ITSM application in **Global scope** following ServiceNow best practices
- ✅ Extend base ITSM tables to maintain core platform inheritance and functionality
- ✅ Manage configurations across modules using **separate, structured Update Sets**
- ✅ Ensure clean, **error-free promotion** of configurations across instances

---

## 🏗️ What Was Built

### Custom Tables (Table Inheritance)

Three custom tables were created, each extending a standard ServiceNow ITSM table:

| Custom Table Name | System Name | Extends |
|---|---|---|
| POC Incident table | `u_poc_incident_table` | Incident |
| POC Change table | `u_poc_change_table` | Change Request |
| POC Problem Management table | `u_poc_problem_management_table` | Problem |

> 💡 Extending base tables means all inherited fields, business rules, and platform logic from the parent table are automatically available — **no duplication required.**

---

### Update Sets Management

Separate Update Sets were maintained for each module to ensure modular, controlled deployment:

| Update Set | Purpose | Status |
|---|---|---|
| `POC Inc` | Incident table configurations | ✅ Complete |
| `POC change` | Change table configurations | ✅ Complete |
| `POC prb` | Problem table configurations | ✅ Complete |
| `POC ITSM Management` | Full application scope | ✅ Complete |
| `Service Catalog work` | Catalog configurations | ✅ Complete |

### Commit & Preview Process

```
Preview Update Set → Fix Errors → Commit → Verify
```

All Update Sets were validated through the **Preview → Commit** workflow before being applied, ensuring **zero collisions** and error-free migration.

---

## ⚙️ Technical Details

```yaml
Application Scope  : POC ITSM Management (Global)
Update Set Strategy: Separate sets per module (Incident, Change, Problem)
Table Design       : Inheritance-based (avoids data duplication)
Deployment         : Preview validated before commit
Dependency Order   : Tables first → then configurations
```

---

## 💡 Key Challenges & Solutions

### Challenge 1 — Managing Multiple Update Sets
> **Problem:** Dependency errors during promotion of multiple Update Sets.  
> **Solution:** Maintained a deliberate promotion order — **tables first, then configurations** — to prevent missing reference errors.

### Challenge 2 — Wrong Update Set Activation
> **Problem:** Accidental changes in the wrong Update Set.  
> **Solution:** Always verified the **active Update Set** before making any configuration change.

### Challenge 3 — Scoped Application Migration
> **Problem:** Scope mismatch errors during migration.  
> **Solution:** Used **Application XML export/import** instead of relying solely on Global update sets for scoped apps.

---

## ✅ Skills Demonstrated

![ServiceNow](https://img.shields.io/badge/ServiceNow-Table%20Design%20%26%20Inheritance-green?style=flat-square)
![ITSM](https://img.shields.io/badge/ITSM-Incident%20%7C%20Change%20%7C%20Problem-blue?style=flat-square)
![Update Sets](https://img.shields.io/badge/Update%20Sets-Management%20%26%20Promotion-orange?style=flat-square)
![Scoping](https://img.shields.io/badge/Application-Global%20Scope-purple?style=flat-square)
![Migration](https://img.shields.io/badge/Migration-Error--free-brightgreen?style=flat-square)

- 🔧 ServiceNow Table Design & Inheritance
- 📋 ITSM Process Knowledge (Incident, Change, Problem)
- 📦 Update Set Management & Promotion
- 🌐 Application Scoping (Global scope)
- 🔗 Configuration Dependency Management
- 🚀 Error-free instance-to-instance migration

---

## ⚠️ Common Mistakes to Avoid

| ❌ Mistake | ✅ Best Practice |
|---|---|
| Forgetting to set correct Update Set as current | Always verify active Update Set before changes |
| Making changes in wrong application scope | Double-check scope before every configuration |
| Committing without previewing first | Always Preview → Fix → then Commit |
| One large Update Set for everything | Use separate Update Sets per module |
| Mixing Global and scoped update sets | Use Application XML for scoped apps |

---

<div align="center">

**Made with ❤️ by Keerthana Chennuru**

![ServiceNow](https://img.shields.io/badge/Built%20on-ServiceNow-green?style=for-the-badge)

</div>



