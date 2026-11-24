# DPSI School Manager

### A connected school operations platform — from admissions to analytics.

DPSI School Manager is a responsive school-management application concept designed to bring the core work of a modern school into one organised digital workspace. It brings together student administration, staff records, academic operations, attendance, fees, communication, library services, transport, boarding, events, inventory and management reporting.

The project currently ships as an **interactive front-end demonstration** built with HTML5, CSS3 and vanilla JavaScript. It is suitable for interface review, demonstrations, workflow validation and further product development. A secure server, shared database, authenticated user accounts and live third-party integrations are required before it can be used to manage real school operations.

> **Project status:** Interactive front-end demo / product prototype. The production capabilities described in the roadmap are the intended completion scope, not features that are already live in this browser-only version.

---

## Product preview

![DPSI School Manager dashboard preview](assets/dashboard-preview.png)

The interface uses a navy-and-blue school identity, a responsive sidebar, a workspace header, dashboard summaries, academic performance visualisation, operational shortcuts, notifications, events and finance snapshots. The individual modules use the same visual system for a consistent user experience.

---

## Why DPSI School Manager?

School teams often work across disconnected spreadsheets, paper registers, messaging apps and finance records. That makes it harder to find accurate information, follow up on tasks and understand what is happening across the school.

DPSI School Manager is designed around a simpler experience:

- **One organised workspace:** Keep important school records and daily workflows in a consistent interface.
- **Faster access to information:** Search records, move between departments and use quick actions without navigating unrelated tools.
- **Clearer operational visibility:** Bring enrolment, attendance, fees, events and resource information into management views.
- **Consistent record handling:** Use structured forms, searchable tables, status labels and exportable records.
- **A platform that can grow:** Extend the prototype into a multi-user application with school-specific settings, secure permissions and integrated services.

The aim is not to overwhelm staff with technology. It is to help school teams get routine work done with less friction and give management a clearer view of school operations.

---

## Modules and current demo capabilities

The sidebar links to all 17 application destinations. The table below distinguishes what can be explored in the current demo from the broader production scope.

| Module | Available in this demo | Intended production capability |
|---|---|---|
| **Dashboard** | School overview, summary cards, performance visualisation, notifications, event and finance snapshots, quick actions | Permission-aware dashboards, live operational KPIs, alerts and configurable widgets |
| **Admissions** | Application register, search/filter, create and edit records, status updates and approval workflow | Online application forms, document collection, review stages, interview scheduling, offer letters and enrolment conversion |
| **Students** | Student register, profile records, guardian/contact fields, status management and record actions | Complete student information system, documents, medical/emergency information, class history, transfers and progression |
| **Staff & Teachers** | Staff directory, department, role, contact and employment-status fields | HR records, contracts, qualifications, leave, workload, payroll integration and staff self-service |
| **Academics** | Class/stream overview, class creation and editing, curriculum/subject catalogue preview | Academic years, terms, departments, class structures, subject allocation, promotion and curriculum management |
| **Attendance** | Daily register, attendance status updates, mark-visible-learners-present action and summary | Class/lesson attendance, late/absence workflows, parent alerts, attendance history, biometric/device integrations and analytics |
| **Examinations** | Assessment register, dates, subjects, classes and assessment status | Mark entry, grading scales, moderation, report cards, transcripts, result approval and academic analytics |
| **Timetable** | Weekly timetable view and lesson creation | Conflict-aware scheduling for teachers, classes and rooms; substitutions and timetable publishing |
| **Fees & Finance** | Invoice register, invoice editing, payment capture and demo balance updates | Fee structures, billing plans, discounts, instalments, receipts, statements, reconciliations, budgets and accounting integrations |
| **Communications** | Message records, message composition interface and reusable templates | Actual SMS, email, push and in-app delivery; contact groups, delivery reports, consent and communication history |
| **Library** | Book catalogue, copy availability, issue and return actions | Member accounts, circulation rules, due dates, reservations, fines, barcode support and library reports |
| **Transport** | Route, vehicle, driver and capacity records; roster preview | Student route allocation, vehicle maintenance, trip/route management, transport fees and optional GPS integrations |
| **Boarding** | Boarding house, room, bed and occupancy records; roll-call preview | Allocation rules, check-in/out, leave requests, roll call, welfare notes and capacity reporting |
| **Events & Activities** | Event register, dates, categories, venues and statuses | Shared school calendar, event registration, trip permissions, reminders, activity scheduling and attendance |
| **Inventory** | Item register, quantities, locations, status and stock adjustments | Procurement requests, supplier records, purchase orders, asset registers, stock movement and audit history |
| **Reports & Analytics** | Supported register exports, custom data export and JSON demo backup | Scheduled reports, permission-based reporting, financial reconciliation, trend analysis and downloadable management packs |
| **Settings** | Demo school details, academic period/preferences, selected local settings, profile-name update and demo reset | School tenancy, user accounts, role permissions, integrations, security policies, retention and system administration |

### Additional interface behaviour

- Sidebar navigation switches modules without a full page reload, using URL hash routes.
- Global search can find matching demo records and quick navigation can jump to modules.
- Tables provide keyword search and supported status filtering.
- Record forms provide browser-side required-field validation.
- Create, view, edit and delete actions are available for the configured record registers.
- Approving an admission adds the applicant to the demo student register.
- Recording a fee payment updates the matching demo invoice balance where a match is found.
- Library issue/return actions update the available-copy count.
- Inventory adjustments update quantities and low-stock status.
- CSV export is available for supported registers; Reports also provides JSON export/backup.
- `Ctrl + K` (or `Cmd + K` on macOS) opens quick navigation. `Esc` closes supported overlays.
- Settings provides a way to restore the original demonstration data.

---

## Technology

| Layer | Technology |
|---|---|
| Markup | HTML5 |
| Styling | CSS3, responsive layouts and CSS custom properties |
| Application logic | Vanilla JavaScript (ES6+) |
| Demo persistence | Browser `localStorage` |
| Typography | Plus Jakarta Sans via Google Fonts, with fallback fonts |
| Illustrative photography | Remote Unsplash image URLs |
| Icons | Inline SVG icons defined in the application |
| Runtime | Modern web browser; no build step required |

There is no React, Vue, Angular, jQuery, Tailwind build pipeline, npm package installation or server-side dependency in the current demonstration.

---

## Getting started

### Requirements

- A modern version of Google Chrome, Microsoft Edge, Firefox or Safari.
- Internet access for the hosted Google Font and remote demonstration photographs. The interface itself is local; those external assets may not load when offline.
- Python 3 is optional and only needed for the simple local web-server method below.

### 1. Download and extract

Download or clone the project, then extract it into a working directory. Keep the files and the `assets` directory together.

```text
dpsi-school-manager/
├── index.html
├── style.css
├── app.js
├── README.md
└── assets/
    ├── dpsi-mark.svg
    └── dashboard-preview.png
```

### 2. Run locally

**Option A — open directly**

Open `index.html` in a modern browser. This is sufficient for a quick interface preview.

**Option B — use a local web server (recommended)**

Open a terminal in the project directory and run:

```bash
python -m http.server 8000
```

Then visit:

```text
http://localhost:8000
```

Stop the server with `Ctrl + C` in the terminal.

### 3. Explore the application

Use the sidebar to open each module. Try the add, view, edit and delete actions, search the tables, approve an admission, record a sample fee payment, issue or return a library book, adjust inventory and export a report.

### 4. Reset the demonstration data

Open **Settings → Reset demo data** to restore the original sample dataset in the current browser. This removes changes saved by this demo in that browser.

---

## Where the data is stored

The current version stores its demonstration data in the browser under this local storage key:

```text
dpsi-school-manager-demo-v1
```

Changes are saved to the browser where the application is running. This is **not** a shared database:

- Data is not synchronised between staff members or devices.
- Clearing browser site data can remove the saved demo records.
- Different browsers and browser profiles maintain separate copies.
- Local storage is not an appropriate secure store for confidential student or financial information.
- The included JSON export is a convenience for demo data, not a managed or encrypted production backup service.

Use only illustrative information while testing this front-end prototype. Do not enter real student, parent, staff, medical, safeguarding or financial data.

---

## Project structure and code ownership

| File | Purpose |
|---|---|
| `index.html` | Application shell, metadata, sidebar/header containers, modal roots and script/style references |
| `style.css` | Colour system, typography, layout, navigation, cards, tables, forms, modals, breakpoints and print styles |
| `app.js` | Navigation, seeded demo data, module configuration, render functions, forms, record actions, local persistence, exports and event handling |
| `assets/dpsi-mark.svg` | Application mark/favicon |
| `assets/dashboard-preview.png` | Dashboard preview used in this README |
| `README.md` | Product overview, setup guide, current functionality, limitations and production roadmap |

### Customisation guide

- **School name, logo and brand:** Update the identity in `index.html`, the `seed.meta` / `seed.settings` values in `app.js`, and replace `assets/dpsi-mark.svg` with an approved mark.
- **Sidebar labels and order:** Update the `navigation` array near the beginning of `app.js`.
- **Module titles and descriptions:** Update `moduleDescriptions` and `moduleNames` derived from the navigation configuration in `app.js`.
- **Sample records:** Update the `seed` object in `app.js`. All sample names, counts, dates and values should be replaced with approved demo content before presenting the product as a live school deployment.
- **Record forms and table columns:** Update the `configs` object in `app.js` and the related render/action functions.
- **Colours, spacing and responsive behaviour:** Update the CSS custom properties and component rules in `style.css`.
- **Photography:** Replace remote Unsplash URLs in `index.html` and `app.js` with properly licensed school photography or locally hosted assets.
- **Search engine indexing:** `index.html` currently contains `noindex, nofollow`, which is appropriate for a private/demo application. Keep the application private or behind authentication in production. Publish a separate public product/marketing page if search visibility and lead generation are required.

---

## Production completion roadmap

The interface is a starting point. To turn it into a dependable school information system for daily use, the following work is required.

### Phase 1 — Backend and database

- Build a documented API and connect the existing front end to server-side data services.
- Implement a relational database with migrations, indexes, validation constraints and referential integrity.
- Define the core data model for schools, academic years, terms, users, roles, students, guardians, staff, classes, subjects, attendance, assessments, invoices, payments, books, loans, routes, boarding allocations, events, assets and audit events.
- Add server-side validation and consistent error handling.
- Support import/migration from the school's existing spreadsheets and systems.

### Phase 2 — Authentication, permissions and privacy

- Implement secure sign-in, sign-out, password reset, session expiry and optional multi-factor authentication.
- Enforce role-based access control on the server, not only by hiding interface elements.
- Define separate permissions for school administrators, admissions staff, teachers, bursars, librarians, transport staff, boarding staff, parents/guardians and students.
- Add an audit trail for sensitive record views, edits, approvals, exports and financial actions.
- Protect personal information with encryption in transit, appropriate encryption at rest, secure file handling, access logging and retention controls.
- Establish privacy notices, consent processes and data-handling procedures that meet applicable data-protection requirements.

### Phase 3 — Complete school workflows

- Complete academic setup, class/subject allocation, grading, mark entry, result approval, report cards and transcripts.
- Add student progression, transfers, withdrawals, document management and guardian relationship handling.
- Add staff leave, contracts, payroll/accounting integration and workload management where required.
- Implement timetable conflict checks and substitution workflows.
- Add complete financial controls: fee structures, discounts, invoices, receipts, payment reconciliation, arrears follow-up and financial reports.
- Add real parent/student/teacher portals with individual accounts and data permissions.
- Implement communication delivery through approved SMS, email and push notification providers.
- Add full boarding, library, transport, events, procurement and asset-management workflows according to school requirements.

### Phase 4 — Reliability, deployment and support

- Create automated unit, integration, end-to-end, security and acceptance tests.
- Configure production hosting, HTTPS, domain, secrets management and environment-specific settings.
- Establish encrypted backups, restore drills, monitoring, logging and incident-response procedures.
- Test performance, accessibility, mobile usability, browser compatibility and high-volume data scenarios.
- Provide administrator training, user guides, onboarding and a support process.
- Pilot with a controlled group of users, resolve issues and obtain school sign-off before full rollout.

---

## Security and production-readiness notice

**Do not deploy this current front-end demo as the live system of record for a school.** It has no server-side authentication, database, enforced permissions, protected API, encrypted backup service or real integrations. The administrator profile and sign-out interactions are demonstration behaviours, not account security. Messages are not delivered to real recipients, and fee payment capture does not process money through a payment gateway.

Before go-live, the production implementation must be independently tested and reviewed for security, privacy, operational resilience and compliance with the requirements that apply to the deploying school. A production release should also include a documented backup-and-restore process, support ownership and a user acceptance sign-off.

---

## Product positioning for schools

### A single view of the school. A smoother day for every team.

DPSI School Manager is designed for schools that want to bring administration and daily operations into one connected platform. Instead of searching through separate files for admissions, attendance, student details, fee balances and school activities, staff can work from a consistent digital workspace.

**A good fit for:**

- Nursery, primary and secondary schools.
- International and mixed-curriculum schools.
- Day and boarding schools.
- Schools moving from paper registers and disconnected spreadsheets to structured digital records.
- School groups that need a platform that can be configured around their own departments and processes.

**Value to school leadership:** better visibility of key operations and more consistent management information.

**Value to administrators:** centralised records, structured workflows and easier follow-up.

**Value to teachers and staff:** clearer access to the information and tools relevant to their responsibilities.

**Value to parents and learners:** a foundation for secure parent and student portals, timely notices and transparent school processes once those production services are implemented.

---

## Request a demo or a school-specific solution

Are you a school owner, director, headteacher or administrator looking to modernise school operations?

Arrange a product walkthrough to discuss your current processes, the modules your school needs, data migration, integrations, implementation and ongoing support. The system can be scoped around the school's size, curriculum, day/boarding model and administrative workflow.

### Start a conversation

Before publishing this README or sharing it with prospective clients, replace the contact placeholders below with your verified business details:

- **Product / implementation contact:** Kisakye Paul
- **Email:** `YOUR_BUSINESS_EMAIL`
- **WhatsApp / telephone:** `YOUR_BUSINESS_PHONE`
- **Portfolio / company website:** `YOUR_WEBSITE_OR_PORTFOLIO_URL`
- **Demo booking link:** `YOUR_DEMO_BOOKING_URL`

**Suggested call to action:** *Book a personalised demo — see how your school can manage admissions, students, academics, attendance, fees and daily operations from one connected platform.*

### Suggested enquiry questions

When a school requests a demo, collect only the details needed to understand its requirements:

1. What is the school's name, location and type (primary, secondary, international, day or boarding)?
2. Approximately how many students, staff members and campuses does it have?
3. Which processes are currently managed manually or across separate systems?
4. Which modules are the highest priority for the first rollout?
5. Does the school need migration from spreadsheets or an existing school system?
6. Which communication, payment, accounting or identity integrations are required?
7. Who will approve the project, and what is the preferred implementation timeline?

These questions help prepare a relevant demonstration and a realistic implementation proposal rather than offering a generic software tour.

---

## Search and marketing phrases

For a public product page, portfolio case study or sales landing page, relevant search themes include:

- School management system in Uganda
- School management software in Kampala
- School ERP and school administration software
- Student information system for schools
- School fees and finance management system
- Student attendance and academic management software
- Admissions and enrolment management for schools
- Digital school administration platform

Use these phrases naturally in a dedicated public landing page, page title, meta description, case study and useful articles. Keep the actual application behind authentication and do not expose student records or internal dashboards to search engines.

### Short promotional copy

> **Run your school from one connected workspace.** Bring admissions, student records, staff, academics, attendance, fees, communication and school operations into a platform designed around the way your school works. Book a personalised demo and explore a practical path from scattered records to organised school management.

---

## Licence, branding and demo content

This repository is a project demonstration. Confirm ownership and permissions for all school names, logos, photographs, fonts and third-party assets before redistribution or commercial deployment. Replace sample data and branding with approved material for each client deployment. Add an explicit software licence and commercial-use terms before publishing the source code as an open-source or paid product.

---

## Acknowledgement

**Product concept and front-end implementation:** Kisakye Paul  
**Interface stack:** HTML5 · CSS3 · Vanilla JavaScript  
**Current release:** Browser-based demonstration prototype
