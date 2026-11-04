# Sunny Bhanu

**Senior SAP ABAP Consultant · EY GDS**
S/4HANA · Clean Core Extensibility · ABAP Cloud / RAP · CDS · OData · AMDP · Integration · RICEFW

[![LinkedIn](https://img.shields.io/badge/LinkedIn-sunnybhanu-0A66C2?logo=linkedin&logoColor=white)](https://www.linkedin.com/in/sunnybhanu/)
![ABAP](https://img.shields.io/badge/ABAP-7.5x%20%7C%20ABAP%20Cloud-0FAAFF)
![S/4HANA](https://img.shields.io/badge/S%2F4HANA-RISE%20Private%20Cloud-1C4E80)
![SAP Certified HANA](https://img.shields.io/badge/SAP%20Certified-ABAP%20for%20SAP%20HANA%202.0-F0AB00)
![SAP Certified BAS](https://img.shields.io/badge/SAP%20Certified-Business%20Application%20Studio-F0AB00)
![Azure](https://img.shields.io/badge/Microsoft%20Certified-Azure%20Fundamentals-0078D4?logo=microsoftazure&logoColor=white)

---

## About

SAP ABAP technical consultant with 5.5+ years across S/4HANA implementation, migration and enhancement projects in **MM, PM, SD and FI**. I deliver the full RICEFW range (reports, interfaces, conversions, enhancements, forms) with a recent focus on **clean-core extensibility on RISE private cloud**: released BAdIs, CDS views, RAP and OData in preference to modifying standard SAP.

I own developments end to end: read the functional spec, challenge it where it is wrong, write the technical spec, build, unit test and transport DEV → QAS → PRD.

## What you will find here

The repositories on this profile are **client-free reference implementations** of design patterns I have used on real projects. Each one documents *why* the design was chosen, not just the code.

| Repository | Pattern | Why it matters |
|---|---|---|
| [abap-rap-service-request-draft-bo](https://github.com/sunny-bhanu/abap-rap-service-request-draft-bo) | Complete draft-enabled **RAP business object** (ABAP Cloud, managed, strict 2): early numbering, status actions with feature control, validations, determinations, side effects, DCL, Fiori Elements annotations, ABAP Unit tests | End-to-end transactional app on the clean-core stack, in abapGit layout, ready to pull into a sandbox |
| [abap-rest-integration-kit](https://github.com/sunny-bhanu/abap-rest-integration-kit) | OAuth 2.0 token provider with caching, injectable HTTP transport, retrying REST client, JSON helpers, consolidated S/F response builder, ICF inbound handler | The building blocks behind SAP ↔ Salesforce style REST integrations, testable without a network |
| [abap-salv-runtime-capture-wrapper](https://github.com/sunny-bhanu/abap-salv-runtime-capture-wrapper) | Wrap a standard report with `SUBMIT … AND RETURN` + `CL_SALV_BS_RUNTIME_INFO`, enrich the result and redisplay | Adds columns to a standard ALV with **zero modification, zero enhancement, zero Z-copy**, the design that survived a clean-core scorecard where an implicit enhancement did not |
| [abap-badi-me2n-longtext-column](https://github.com/sunny-bhanu/abap-badi-me2n-longtext-column) | `ME_CHANGE_OUTTAB_CUS` BAdI + append structure + `STATICS` hashed buffer around `READ_TEXT` | Extends ME2N output through the SAP-documented BAdI and cuts expensive STXH/STXL reads to one per item |
| [abap-badi-pm-notification-duplicate-check](https://github.com/sunny-bhanu/abap-badi-pm-notification-duplicate-check) | `NOTIF_EVENT_SAVE` → `CHANGE_DATA_AT_SAVE` with status-aware duplicate detection | Blocks a duplicate breakdown notification in IW21/IW22 using the BAdI's own `EV_SUBRC / EV_MSG*` protocol, not an inline `MESSAGE` |
| [abap-custom-tab-standard-transactions](https://github.com/sunny-bhanu/abap-custom-tab-standard-transactions) | Custom tab in ME51N to ME53N (screen exit `MEREQ001` + BAdI `ME_PROCESS_REQ_CUST`) and ME21N to ME23N (screen exit `MM06E005`) with a popup ALV on the released CDS view `I_MaterialStock` | Shows which hook sees which items, how to hand data to the subscreen without SAP memory so unsaved items work, and how to get around the ME21N GUI-status restriction with `AT EXIT-COMMAND` |
| [abap-rtts-dynamic-pivot-salv](https://github.com/sunny-bhanu/abap-rtts-dynamic-pivot-salv) | Equipment census with **one column per plant created at runtime (RTTS)**, `LOOP AT ... GROUP BY` counts, `CL_SALV_TABLE` subtotals and grand total, deletion-flag filter with `NOT EXISTS` on `JEST`, `I_IWERK` check, ABAP Unit | Turns a monthly spreadsheet pivot into a report whose columns follow the data, with totals the ALV can still sort and filter |
| [abap-cds-amdp-odata-rap-examples](https://github.com/sunny-bhanu/abap-cds-amdp-odata-rap-examples) | CDS views with associations and `CASE`, AMDP table function, SEGW OData V2 notes, RAP managed BO skeleton | The modern read/expose stack used for analytical and transactional Fiori apps |
| [abap-performance-patterns](https://github.com/sunny-bhanu/abap-performance-patterns) | `FOR ALL ENTRIES` done safely, parallel cursor, hashed/sorted tables, selective field lists | The before/after versions of the optimisations that fixed slow production reports |

## Core competencies

- **Clean core / S/4HANA:** released API and CDS-based extensibility, the 3-tier extensibility model, ATC remediation, SPDD/SPAU, custom code migration, OSS Note implementation
- **ABAP Cloud and RAP:** managed and unmanaged business objects, draft, EML, behavior pools, feature and authorization control, ABAP Unit with CDS and Open SQL test doubles
- **Enhancement techniques:** BAdI (classic and new), function/screen/menu/customer exits (CMOD/SMOD), implicit enhancements, BTE, chosen by upgrade safety, not convenience
- **Integration:** REST/JSON APIs with OAuth 2.0 (SAP ↔ Salesforce), consolidated error contracts, BAPIs, RFC-enabled FMs, IDocs, LSMW, VOFM routines, data migration
- **Modern read/expose stack:** CDS (joins, associations, annotations, access control), AMDP / HANA table functions, OData V2 (SEGW, DPC/MPC extension classes) and V4, SAPUI5 / Fiori Elements, SAP BTP
- **Reporting and UI:** classical, interactive and ALV (`REUSE_ALV`, `CL_GUI_ALV_GRID`, `CL_SALV_TABLE`), SAP Query, module pool programming, subscreens, custom tabs in standard transactions
- **Forms:** Adobe Forms, SmartForms, SAPscript, NACE output configuration
- **Performance:** ST05 / SAT / ST12 runtime analysis, buffering strategies, SQL optimisation
- **Functional exposure:** MM (PR/PO, stock), PM (equipment, notifications, orders, measuring points), SD (orders, pricing, deliveries), FI (vendor ledger, GL)

## Selected project work

- **S/4HANA implementation, RISE private cloud (infrastructure and construction):** owned multiple RICEFW objects end to end in MM/PM/FI: clean-core wrapper report for MR51, ME2N BAdI enhancement, PM Equipment Master extension with 23 custom fields via `ITOB0001`, custom stock tabs in ME51N and ME21N (`MEREQ001` + `ME_PROCESS_REQ_CUST`, `MM06E005`), PM notification business-rule validation, OData V2 (SEGW) service behind a SAPUI5 fuel-consumption entry app (8 entity sets, function imports, PM98/PM99 order determination, HR/KM measurement documents through `MEASUREM_DOCUM_RFC_SINGLE_001` in one controlled LUW), vendor account statement (report + SmartForm).
- **S/4HANA project for a real-estate client, SAP ↔ Salesforce integration:** designed the field mapping for 17 REST APIs between SFDC (pre-sales) and SAP (post-sales) and built the SAP side of the Unit Master create/change, Channel Partner, Advance Payment and Completion Certificate APIs: JSON contracts, validations with consolidated S/F error responses, and outbound OAuth 2.0 calls to Salesforce for property status, booking approval and payment milestones.
- **S/4HANA 2023 custom code remediation:** ATC-driven remediation with ADT quick fixes, SPDD/SPAU, replacement of obsolete objects; CDS analytical views and AMDP table functions consumed in custom reports and OData services.
- **Automotive OEM (via Capgemini):** procurement visibility ALV reports, material master programs on `BAPI_MATERIAL_SAVEDATA`, table maintenance generators, SAPscript / NACE output determination, production support.

## Certifications and education

- SAP Certified Development Specialist: ABAP for SAP HANA 2.0
- SAP Certified Development Associate: Build Applications with SAP Business Application Studio
- Microsoft Certified: Azure Fundamentals (AZ-900)
- B.Tech, Computer Science and Engineering, Presidency University, Bengaluru

## Working with me

- Every repository has a README that states the requirement, the options considered and why one was chosen. Start there, then read the code.
- Issues and pull requests are welcome, especially release-specific corrections (most code targets S/4HANA 2022/2023; ABAP Cloud examples target 7.58 / BTP ABAP Environment).
- Reach me on [LinkedIn](https://www.linkedin.com/in/sunnybhanu/).

---

> All code on this profile is written from scratch as generic reference material. It contains no client data, client-specific naming or proprietary logic.
