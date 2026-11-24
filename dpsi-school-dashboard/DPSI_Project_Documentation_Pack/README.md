# DPSI School Manager — Complete Project Documentation Pack

**Documentation version:** 1.0  
**Prepared:** 24 November 2026  
**Product:** DPSI School Manager  
**Purpose:** Product definition, engineering guidance, delivery control, privacy/security governance, user operations, quality assurance and launch planning.

> **Important status statement**  
> This package describes and controls the path to a production school management system. It does **not** make the supplied application production-ready, and it is not a certification of security, legal compliance or operational readiness. The supplied application baseline is an interactive HTML/CSS/Vanilla JavaScript prototype with browser `localStorage` demo data. It is not a secure, shared, multi-user school information system. Do not enter actual student, guardian, medical, safeguarding, staff or financial information into the prototype. Production use must wait until the required backend, database, identity/permissions, privacy controls, integrations, backup/restore, tests, operational procedures and formal approvals have been implemented and verified.

---

## 1. What is included

This pack is split into six editable Word documents, one project-control workbook, and reference files from the existing application.

| File | Purpose | Primary audience |
|---|---|---|
| `docs/01_DPSI_School_Manager_Master_Product_and_Requirements_Handbook.docx` | Product purpose, problem/opportunity statement, scope, capabilities, exclusions, stakeholder benefits, users/roles, workflows, business rules, all tracker features, non-functional requirements, risks and decisions | Product owner, school leadership, business analyst, developers |
| `docs/02_DPSI_School_Manager_Technical_Architecture_Security_and_Privacy.docx` | Proposed architecture, environments, data entity groups, integrity rules, API conventions, security, privacy, Uganda regulatory review points, integrations and technical decisions | Architect, developers, security/privacy owners, hosting team |
| `docs/03_DPSI_School_Manager_QA_UAT_and_GoLive_Acceptance_Plan.docx` | QA strategy, QA-001–QA-018 suite, department UAT scenarios, defect severity, evidence, responsibilities, GO-001–GO-015 release gates and approvals | QA lead, developers, department owners, release manager |
| `docs/04_DPSI_School_Manager_User_Administration_and_Operations_Handbook.docx` | Role guidance, standard operating procedures, daily/weekly/term routines, migration, account lifecycle, deployment, backup/restore, incident response, service/support and training | School administrators, department users, IT/support and operations |
| `docs/05_DPSI_School_Manager_Product_Overview_and_Client_Brief.docx` | Client-facing product story, problem context, proposed capabilities, benefits by stakeholder, deployment approach, maturity statement, discovery/demo agenda and lead qualification questions | Product owner, sales, school leadership and prospects |
| `docs/06_DPSI_School_Manager_Project_Governance_Forms_and_Templates.docx` | Reusable requirements approval, UAT sign-off, migration reconciliation, privacy review, change request, incident report, release sign-off and decision-log templates | Project lead, school approvers, data owners, QA and operations |
| `registers/DPSI_School_Manager_Project_Control_Workbook.xlsx` | Live editable register for all 146 features, 15 NFRs, 11 proposed roles, 18 QA tests, risks, decisions, integrations and 15 go-live gates | Entire delivery team |

### Reference material

- `reference/DPSI_School_Manager_Development_Tracker.docx` — the original supplied development tracker, retained as a source reference.
- `reference/Original_Project_README.md` — previous project README, retained for traceability.
- `reference/dpsi-school-manager-full-project.zip` — existing front-end prototype source archive.
- `reference/dashboard-preview.png` — approved dashboard visual reference.

---

## 2. Recommended reading order

1. Start with the **Master Product and Requirements Handbook**. Agree on the problem being solved, scope, modules, roles, business rules, assumptions and what is explicitly excluded.
2. Review the **Technical Architecture, Security and Privacy Specification** with the technical lead and school privacy/legal representatives. Approve architecture, hosting, data ownership, tenant approach, identity, integrations and privacy decisions before handling real data.
3. Use the **Project Control Workbook** as the day-to-day delivery register. Assign owners, priority, delivery phase, target date, verification status and evidence for every feature.
4. Use the **QA, UAT and Go-Live Acceptance Plan** throughout each sprint and before every release. Do not treat the acceptance cases as passed until they have actually been run and evidence recorded.
5. Use the **User, Administration and Operations Handbook** to plan operating procedures, access management, migration, backup, support, incident handling and user training.
6. Use the **Governance Forms and Templates** to obtain written decisions, change approvals, migration acceptance, privacy review, UAT and production go-live approval.
7. Use the **Product Overview and Client Brief** for stakeholder discussions and prospect demonstrations. Replace all contact placeholders and adjust commercial statements to the actual business offering before external publication.

---

## 3. How to use the project-control workbook

The workbook is a working control register, not merely a report. Keep it in a shared, access-controlled project location and nominate one person to maintain it.

- **Overview:** roll-up of counts and status. Confirm formula results after editing or opening in a compatible spreadsheet application.
- **Feature Register:** source of truth for each feature ID, prototype baseline, priority, delivery status, owner, phase/sprint, target date, UI/backend/database/access/QA state, evidence and notes.
- **NFR Register:** measurable non-functional requirements and their acceptance state.
- **Roles & Access:** proposed role/access matrix. Treat as draft until approved by the school.
- **QA & UAT:** test execution and evidence register. Initial status is Not run; populate actual test results.
- **Risk Register:** risks, mitigations, owners and status.
- **Decision Log:** decisions requiring an accountable approver and date.
- **Go-Live Checklist:** mandatory release gates. Initial state is Not done.
- **Integrations:** provider/owner/dependency tracking. Do not label an integration production verified until an end-to-end production test has succeeded.

Use the approved status vocabulary in the workbook. A prototype feature marked DEMO or PARTIAL is not automatically production-complete. Mark a feature **Done** only when the approved acceptance criteria pass and evidence is attached or referenced.

---

## 4. Product problem and proposed value

DPSI School Manager is intended to provide a unified operational workspace for school administration, learner lifecycle, academic operations, finance, communication and supporting services.

The product discovery hypothesis is that some schools may manage learner and operational information across separate registers, spreadsheets, paper records, messages or departmental tools. This can create repeated data entry, fragmented visibility, slow reporting, inconsistent records and difficulty tracking responsibility. These are discovery topics, not claims that have been independently verified for every target school.

The product is designed to bring admissions, students, staff, academics, attendance, examinations, timetable, fees, communications, library, transport, boarding, events, inventory, reports and settings into one connected system, with access appropriate to the user's role.

Expected benefits—subject to implementation, school adoption and validation—include more consistent records, reduced duplicate entry, faster routine workflows, clearer financial visibility, better follow-up, more timely reporting and improved communication between authorised school stakeholders.

---

## 5. Current application status: what it does and does not do

### Demonstrated in the supplied prototype

The current source is a browser-only front-end demonstration. Source review confirms:

- 17 hash-routed sidebar destinations.
- Responsive navigation, global search and command navigation.
- Dashboard and reusable module layouts, tables, modal forms and toast feedback.
- Local demo data stored in browser `localStorage`.
- Demo CRUD-style flows for selected registers.
- An admissions approval demo that adds a corresponding learner to the student demo register.
- Browser-side attendance editing, class filtering, local save and CSV export.
- Demonstration payment capture that updates a local sample invoice.
- Library issue/return quantity adjustments, but not a complete loan ledger.
- Inventory quantity adjustments and a low-stock state.
- Class record create/edit, while some academic/subject content remains illustrative.
- A sample timetable with locally saved lesson additions, but no timetable conflict engine.
- CSV register exports and local JSON demo-data export; no production restore process.

### Not established by the supplied prototype

The supplied source does not establish:

- A production backend or shared database.
- Secure user authentication and server-side role/permission enforcement.
- Multi-user concurrency or cross-device data sharing.
- Production multi-school tenant isolation.
- Secure real-student document storage.
- Complete admissions, student lifecycle or guardian portal workflows.
- Full examination grading, moderation and publication.
- Conflict-aware timetable management.
- A production financial ledger, real payment reconciliation or payment gateway.
- Live SMS, email or push notification delivery.
- Complete HR/payroll, library, transport, boarding, events or procurement operations.
- Automated encrypted backups and verified restoration.
- Completed penetration/security, accessibility, load/performance or end-to-end test evidence.
- Production hosting, monitoring, support commitments or signed school UAT.

Treat any planned capability in the documents as a requirement, not as an existing feature. External integrations require provider accounts, contracts, credentials, configuration and successful tests. School-specific matters such as fee rules, grading, promotion, term dates, safeguarding, parent access and data-retention policy require approval from the school.

---

## 6. Governance: who must own the decisions

Before implementation and before launch, appoint named people for at least these responsibilities:

- Product owner/project lead — controls scope, priorities, change approvals and product acceptance.
- School sponsor/headteacher — confirms institutional outcomes and authorises readiness.
- Department owners — validate Admissions, Academics, Finance, HR, Library, Transport, Boarding and other departmental workflows.
- Development lead/architect — owns architecture, code quality, migrations and technical delivery.
- QA lead — owns test evidence, defect triage and release recommendation.
- Data owner/registrar — confirms source records, migration mapping and reconciliation.
- Finance owner/bursar — approves fee policy, payment, refund and reconciliation rules.
- Privacy/data protection owner and qualified legal reviewer — assess lawful processing, child data, notices, contracts, retention and regulatory obligations.
- Operations/hosting owner — runs environments, monitoring, backup, restore and release/rollback.

The role/access workbook is a proposed starting point, not an approved access policy. Obtain written approval before creating production accounts or exposing real records.

---

## 7. Production launch rule

Do not launch with real school data until all applicable GO-001–GO-015 gates in the QA/UAT plan have named owners and recorded evidence. At minimum, confirm:

1. Scope, workflows, business rules and role permissions have been approved.
2. Production domain, TLS/HTTPS, hosting and environment separation are configured.
3. Authentication, recovery, session security and server-side authorisation are tested.
4. Database schema, migrations, constraints and indexes are reviewed.
5. Data migration has been reconciled and accepted by school data owners.
6. Privacy notices, data processing terms, retention and incident procedures are approved.
7. Finance posting, allocations, receipts, refunds and reconciliation are signed off.
8. SMS/email/payment integrations have been tested with controlled recipients and transactions.
9. Backup automation and a successful restore rehearsal are evidenced.
10. Automated, regression, security, performance and accessibility checks have been completed.
11. Critical/high defects are closed or formally accepted by authorised risk owners.
12. Department users have completed UAT and training.
13. Monitoring, support channels, incident escalation and rollback are ready.
14. All required technical, operational, school and privacy approvals are recorded.
15. Final release authority has approved the version and launch date.

The release decision must be **Go**, **Go with explicitly approved conditions**, or **No-Go**. Any condition must have an owner, due date, mitigation and documented risk acceptance. A document checklist cannot replace technical evidence or a real restore/security/UAT test.

---

## 8. Uganda privacy and child-data review

The product is expected to process identifiable information about learners, guardians and employees, including information relating to children and potentially sensitive data. The technical specification therefore includes a privacy/security review workstream. Before production processing begins, the school and product operator should obtain qualified Uganda legal/privacy advice on their respective controller/processor roles, lawful basis, notices, consent where applicable, child-data safeguards, special personal data, retention, data-subject requests, vendor/sub-processor terms, cross-border hosting and breach response.

The relevant legal review should include the Data Protection and Privacy Act, 2019 (currently consolidated as Cap. 97), the Data Protection and Privacy Regulations, 2021, applicable Children Act provisions and current Personal Data Protection Office (PDPO) guidance. Check current legislation, amendments, registration requirements and regulator guidance directly before launch; this pack is not legal advice. The PDPO provides official information about registration and data-protection oversight. Obtain legal confirmation rather than relying on this summary.

Useful official/regulatory references:

- Uganda Data Protection and Privacy Act (ULII consolidated text): https://ulii.org/akn/ug/act/2019/9/eng@2023-12-31
- Data Protection and Privacy Regulations, 2021 (PDPO): https://pdpo.go.ug/
- Personal Data Protection Office: https://pdpo.go.ug/
- Children Act (ULII): https://ulii.org/akn/ug/act/1997/6/eng@2024-08-16

---

## 9. Document control and change management

- Keep the six Word documents editable and version-controlled.
- Record owner, reviewer, approval date and version changes.
- Maintain the workbook as the active delivery register; do not create conflicting copies in private folders.
- Every material requirement change must have a change request, impact analysis, approver and revised acceptance criteria.
- Keep implementation evidence linked to the feature ID, code change, migration, test run or signed UAT record.
- Review documentation at each release and whenever business rules, architecture, providers, law or school policy change.
- Replace draft role matrices, service levels, retention periods, RPO/RTO, support hours and performance targets with approved values before contracting or launch.
- Do not market a capability as available until it has been implemented and verified in the release offered to the customer.

---

## 10. Suggested next actions

1. Name the product owner, technical lead, QA lead, school sponsor, department owners, data owner and privacy/legal reviewer.
2. Hold a school discovery and requirements validation workshop. Confirm the problem statement with actual users rather than assuming every proposed workflow is needed.
3. Approve the first release scope, role matrix, fee rules, academic rules and data ownership.
4. Select hosting, backend, database, tenancy approach, SMS/email/payment providers and document storage.
5. Build the security, authentication, database, migration and backup foundation first.
6. Deliver core modules in the agreed phases and update the project-control workbook continuously.
7. Run data migration rehearsals, QA, department UAT, security review and restore drills.
8. Authorise a controlled pilot before a full school-wide launch.

**The project is ready for structured analysis, engineering and controlled delivery. It is not certified or ready for live school operation until implementation and all applicable launch gates have been completed and approved.**
