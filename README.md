# Sunny Bhanu

**Senior SAP ABAP Consultant · EY GDS**
S/4HANA · Clean Core Extensibility · ABAP Cloud / RAP · CDS · OData · AMDP · RICEFW

[![LinkedIn](https://img.shields.io/badge/LinkedIn-sunnybhanu-0A66C2?logo=linkedin&logoColor=white)](https://www.linkedin.com/in/sunnybhanu/)
![ABAP](https://img.shields.io/badge/ABAP-7.5x%20%7C%20ABAP%20Cloud-0FAAFF)
![S/4HANA](https://img.shields.io/badge/S%2F4HANA-RISE%20Private%20Cloud-1C4E80)
![Certified](https://img.shields.io/badge/SAP%20Certified-ABAP%20for%20SAP%20HANA%202.0-F0AB00)

---

## About

SAP ABAP technical consultant with 5.5+ years across S/4HANA implementation, migration and enhancement projects in **MM, PM, SD and FI**. I deliver the full RICEFW range — reports, interfaces, conversions, enhancements, forms — with a recent focus on **clean-core extensibility on RISE private cloud**: released BAdIs, CDS views, RAP and OData in preference to modifying standard SAP.

I own developments end to end: read the functional spec, challenge it where it is wrong, write the technical spec, build, unit test and transport DEV → QAS → PRD.

## What you will find here

The repositories on this profile are **client-free reference implementations** of design patterns I have used on real projects. Each one documents *why* the design was chosen, not just the code.

| Repository | Pattern | Why it matters |
|---|---|---|
| [abap-salv-runtime-capture-wrapper](https://github.com/sunny-bhanu/abap-salv-runtime-capture-wrapper) | Wrap a standard report with `SUBMIT … AND RETURN` + `CL_SALV_BS_RUNTIME_INFO`, enrich the result and redisplay | Adds columns to a standard ALV with **zero modification, zero enhancement, zero Z-copy** — the design that survived a clean-core scorecard where an implicit enhancement did not |
| [abap-badi-me2n-longtext-column](https://github.com/sunny-bhanu/abap-badi-me2n-longtext-column) | `ME_CHANGE_OUTTAB_CUS` BAdI + append structure + `STATICS` hashed buffer around `READ_TEXT` | Extends ME2N output through the SAP-documented BAdI and cuts expensive STXH/STXL reads to one per item |
| [abap-badi-pm-notification-duplicate-check](https://github.com/sunny-bhanu/abap-badi-pm-notification-duplicate-check) | `NOTIF_EVENT_SAVE` → `CHANGE_DATA_AT_SAVE` with status-aware duplicate detection | Blocks a duplicate breakdown notification in IW21/IW22 using the BAdI's own `EV_SUBRC / EV_MSG*` protocol, not an inline `MESSAGE` |
| [abap-custom-tab-standard-transactions](https://github.com/sunny-bhanu/abap-custom-tab-standard-transactions) | Custom tab in ME51N–ME53N (`ME_GUI_PO_CUST`) and ME21N–ME23N (screen exit `MM06E005`) with a popup ALV | Shows how to cross the BAdI ⇄ module-pool boundary with SAP memory IDs and how to get around the ME21N GUI-status restriction with `AT EXIT-COMMAND` |
| [abap-cds-amdp-odata-rap-examples](https://github.com/sunny-bhanu/abap-cds-amdp-odata-rap-examples) | CDS views with associations and `CASE`, AMDP table function, SEGW OData V2 notes, RAP managed BO skeleton | The modern read/expose stack used for analytical and transactional Fiori apps |
| [abap-performance-patterns](https://github.com/sunny-bhanu/abap-performance-patterns) | `FOR ALL ENTRIES` done safely, parallel cursor, hashed/sorted tables, selective field lists | The before/after versions of the optimisations that fixed slow production reports |

## Core competencies

- **Enhancement techniques** — BAdI (classic & new), function/screen/menu/customer exits (CMOD/SMOD), implicit enhancements, BTE — chosen by upgrade safety, not convenience
- **Clean core / S/4HANA** — released API & CDS-based extensibility, ATC remediation, SPDD/SPAU, custom code migration, OSS Note implementation
- **Reporting** — classical, interactive and ALV (`REUSE_ALV`, `CL_GUI_ALV_GRID`, `CL_SALV_TABLE`), SAP Query
- **Modern stack** — CDS (joins, associations, annotations), AMDP / HANA table functions, OData V2 (SEGW, DPC/MPC extension classes), RAP, SAPUI5 / Fiori Elements, SAP BTP
- **UI & screens** — module pool programming, Screen/Menu Painter, subscreens, custom tabs in standard transactions
- **Integration & data** — BAPIs, RFC-enabled FMs, IDocs, LSMW, VOFM routines, data migration
- **Forms** — Adobe Forms, SmartForms, SAPscript, NACE output configuration
- **Performance** — ST05 / runtime analysis, buffering strategies, SQL optimisation
- **Functional exposure** — MM (PR/PO, stock), PM (equipment, notifications, orders, measuring points), SD (orders, pricing, deliveries), FI (vendor ledger, GL)

## Selected project work

- **S/4HANA implementation, RISE private cloud (infrastructure & construction)** — owned multiple RICEFW objects end to end in MM/PM/FI: clean-core wrapper report for MR51, ME2N BAdI enhancement, PM Equipment Master extension with 23 custom fields via `ITOB0001`, custom stock tabs in purchasing transactions, PM notification business-rule validation, OData + SAPUI5 fuel-consumption application posting goods issues through `BAPI_GOODSMVT_CREATE`, vendor account statement (report + SmartForm).
- **S/4HANA 2023 custom code remediation** — ATC-driven remediation with ADT quick fixes, SPDD/SPAU, replacement of obsolete objects; CDS analytical views and AMDP table functions consumed in custom reports and OData services.
- **Automotive OEM (via Capgemini)** — procurement visibility ALV reports, material master programs on `BAPI_MATERIAL_SAVEDATA`, table maintenance generators, SAPscript / NACE output determination, production support.

## Certifications & education

- SAP Certified — ABAP for SAP HANA 2.0
- Microsoft Azure Fundamentals (AZ-900)
- B.Tech, Computer Science & Engineering — Presidency University, Bengaluru

---

> All code on this profile is written from scratch as generic reference material. It contains no client data, client-specific naming or proprietary logic.
