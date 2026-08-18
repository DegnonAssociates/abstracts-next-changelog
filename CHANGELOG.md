# Changelog

This changelog tracks notable features, updates, fixes, tests, and maintenance work applied to the app since its creation. Entries are listed in reverse chronological order and are based on the non-merge Git history through commit `7ef3c8d`.

## 2026-08-18

- Feature: Added an Other option to Career Level author fields with required custom details and support for preserving unmatched MemberClicks values.
- Feature: Added configurable per-instance browser tab titles with a safe default when no title is configured.
- Update: Restyled Back navigation controls to use the configured primary color consistently.
- Fix: Counted historical reviewer assignments as completed when a matching reviewer response record exists, reflecting the archive's submitted-review data contract.
- Fix: Corrected historical submission and review selection responses to display configured labels and support legacy selection storage.

## 2026-08-12

- Feature: Added question duplication actions so admins can copy existing question configuration instead of rebuilding similar questions manually (`7ef3c8d`).
- Update: Added conditional navigation for submission history so users are routed through history views only when the relevant historical context exists (`53ec487`).

## 2026-08-11

- Update: Moved abstract counts under the submission heading to keep status context closer to the submission title (`4294342`).
- Update: Moved abstract length summaries into the submission overview to make length feedback easier to find during review (`cd5a265`).
- Feature: Added live abstract length counters for real-time word and character count visibility while editing (`a33f285`).

## 2026-08-10

- Feature: Added an isolated past instances archive for browsing old event instances without mixing archive workflows into current submissions (`5316dd0`).
- Feature: Added configurable MemberClicks attribute mapping for user search so lookup results can be matched to the right profile fields (`e17fc5a`).
- Fix: Normalized MemberClicks JSON during instance copy to make copied instance configuration more consistent (`a355527`).
- Update: Styled back buttons and adjusted submission headings for clearer navigation and page hierarchy (`c8b7831`).
- Update: Applied a schema update supporting the latest data model changes (`256ec03`).

## 2026-08-05

- Feature: Added checkbox any/all display logic so conditional questions can depend on whether any or all selected checkbox values match (`a3558cc`).
- Feature: Added email delivery history and resend support for tracking sent messages and replaying failed or needed deliveries (`149622f`).
- Feature: Added MemberClicks search to the add-author dialog to help populate coauthor data from MemberClicks records (`842d49c`).

## 2026-08-03

- Feature: Added configurable instance time zones so submission windows, reminders, and event timing can follow each event instance's local time (`2783540`).
- Feature: Added email delivery tracking and supporting text branding to improve communications visibility and per-instance email presentation (`001bc02`).

## 2026-08-01

- Fix: Corrected reminder worker schema resolution so scheduled email reminders can run against the expected database schema (`4ff1319`).
- Feature: Implemented scheduled email reminders, including a worker process for polling and sending reminders (`0905114`).

## 2026-07-29

- Update: Upgraded Next.js to version 15.5.21 (`99a7e0f`).
- Feature: Implemented DEG-320 NeonPay submission payments for paid submission flows (`b06d039`).
- Feature: Added a test submission cleanup workflow so admins can remove test data without affecting real submissions (`5c729d2`).
- Update: Started Neon login directly from the landing page to shorten the authentication path (`4bc7657`).

## 2026-07-28

- Fix: Preserved local author edits during MemberClicks login so imported profile data does not overwrite user-entered author changes unexpectedly (`384de69`).
- Update: Split admin configuration into collapsible sections for a more manageable administration interface (`129d837`).
- Update: Matched the login artwork background to the page styling (`0b6d565`).
- Update: Switched login artwork to a white background for cleaner visual integration (`7cbfe9b`).
- Feature: Added configurable login page artwork so each instance can customize the login visual treatment (`a43a565`).

## 2026-07-27

- Feature: Added alignment controls to admin rich text fields (`767bb4e`).
- Feature: Added rich text login copy and optional meeting details to improve configurable landing page content (`74d82c4`).
- Feature: Added selectable author profile fields for submission types (`91954fa`).
- Feature: Enabled resending saved email templates (`44d8b22`).
- Update: Included friendly submission IDs in email output (`b0a041e`).
- Update: Added the instance name to outgoing emails for clearer recipient context (`018a16c`).
- Feature: Added conflict-of-interest review emails (`e723f5a`).
- Update: Renamed a decision import column to better match import expectations (`4806b59`).
- Feature: Added heading-only questions to review forms (`b52b046`).

## 2026-07-26

- Update: Simplified decision import inputs to reduce import friction (`69237bd`).
- Feature: Added scheduler speaker conflict overrides for event scheduling exceptions (`d1ee022`).
- Feature: Added reviewer assignment exports with submission details (`375cf04`).
- Feature: Implemented audited submission decisions for traceable decision changes (`16e2b0d`).
- Feature: Added decision annotations so admins can capture context around submission decisions (`41e273a`).
- Feature: Implemented DEG-310 submission guidance (`d65d6d1`).

## 2026-07-25

- Feature: Added email preview and validation workflows (`b409011`).
- Feature: Added configurable branding and option ordering (`1a3e4fa`).
- Feature: Added managed images to email rich text content (`4437c95`).
- Feature: Added table support to rich text fields (`555c710`).

## 2026-07-24

- Feature: Added a built-in editable submission title field (`49466a5`).

## 2026-07-23

- Feature: Added an optional review conflict workflow (`3064ab1`).

## 2026-07-21

- Feature: Added reviewer assignment filtering by submission type (`02d2b5e`).
- Feature: Added user search to the admin area (`ed2c25e`).
- Update: Removed the "all" slice from dashboard pie charts to keep chart data focused (`d6e9c41`).

## 2026-07-14

- Feature: Added support for legacy Neon API credentials (`5cb08d9`).
- Fix: Corrected Neon callback cookie delivery (`63e70f7`, `68829ac`).
- Fix: Hardened the Neon CRM login flow (`5f5d614`).
- Fix: Resolved MemberClicks instances from callback hosts (`a7b1d0a`).
- Fix: Corrected MemberClicks token exchange handling (`6f50b36`).
- Feature: Added Neon CRM SSO login (`98cbb15`).

## 2026-07-06

- Update: Sent emails from `instance.contact_info` so sender identity follows instance configuration (`91672ba`).

## 2026-07-02

- Feature: Hid dashboard submission types based on configured dates (`1959c72`).
- Fix: Allowed submissions to proceed when questions use display logic (`c1c4232`).
- Feature: Added a call-for-reviewers toggle (`3220fa0`).
- Feature: Added optional selection limits for checkbox fields (`c0669ee`).

## 2026-07-01

- Fix: Resolved guidelines links from S3 so linked documents load from stored assets (`5f6bf13`).

## 2026-06-29

- Fix: Increased reliability of instance copy by addressing transaction timeouts (`ba559b9`).

## 2026-06-23

- Fix: Used SSO client names when constructing MemberClicks URLs (`2d067e7`).
- Update: Changed the submission title label (`4ed3056`).

## 2026-06-16

- Security: Rendered sanitized login page HTML to protect configurable login content (`a3262ed`).
- Fix: Bypassed the optimizer for landing hero images where direct rendering is required (`abdf8c8`).
- Security: Fixed high-risk security findings (`a9ca8ad`).

## 2026-06-15

- Security: Fixed signed authentication sessions and added stronger admin action guards (`f97502e`).

## 2026-06-12

- Infrastructure: Removed the Coolify deploy workflow (`ef7717a`).

## 2026-06-10

- Update: Made email text formatting match other rich text inputs and removed unnecessary formatting types (`8eb09ab`).
- Fix: Applied rich text fixes (`c6fce90`).
- Update: Adjusted labels and values for testing (`4d588a7`).
- Feature: Allowed admins to submit abstracts (`7cbcf1b`).
- Feature: Made submission titles editable from the submission overview (`69771f1`).

## 2026-06-04

- Fix: Preserved reviewer roles during login (`f243e09`).
- Feature: Displayed rich text in question subheadings (`c477524`).
- Update: Replaced the single role column with multi-select user administration roles (`718b99a`).
- Fix: Cleaned up reports toolbar merge issues (`069170a`).
- Feature: Made the call-for-reviewers form assign reviewer access (`8bf13f0`).

## 2026-05-29

- Feature: Added a service-offline maintenance page (`be06e89`).

## 2026-05-21

- Feature: Added XLSX workbook exports for reports (`26f5ee4`).

## 2026-05-20

- Fix: Corrected mail API `cc` and `bcc` payload handling (`67dc31f`).

## 2026-05-01

- Feature: Added a reports-page delete button; deleted abstracts are marked inactive and hidden from app views (`866de98`).

## 2026-04-30

- Update: Showed submission content alongside review questions (`bbd5621`).
- Feature: Added reviewer PDF packet downloads (`4e90e5b`).

## 2026-04-29

- Feature: Added reviewer read-only controls (`eac95c0`).

## 2026-04-24

- Infrastructure: Added auto-deploy support for Coolify (`71f66a1`).

## 2026-04-16

- Fix: Corrected member intel activity payload parsing (`d34ea83`).
- Fix: Added a `neon_id` fallback for member intel lookup (`c5b6413`).
- Fix: Made guidelines URLs link directly to documents and only display when present (`d4f3f14`).

## 2026-04-13

- Feature: Synced admin roles from MemberClicks groups during login (`25277bc`).

## 2026-04-06

- Feature: Added initial API options (`e67ddef`).

## 2026-03-31

- Feature: Added room filtering across all calendars (`ccf3213`).

## 2026-03-23

- Update: Improved admin submission flows and author role handling (`bb60564`).
- Maintenance: Removed login and favicon debug logging (`a1d5074`).
- Feature: Added a max-authors setting to submission types (`63b7b0c`).
- Fix: Treated a zero author limit as unlimited (`13a2d34`).
- Fix: Redirected logout to the app landing page (`db579a3`).
- Fix: Corrected dynamic favicon routing for Next.js builds (`9a93c5a`).
- Fix: Applied favicon fixes (`a33af2e`).
- Feature: Added per-instance favicon metadata support (`fc78c20`).

## 2026-03-20

- Fix: Corrected login instance resolution (`3cdbc48`).
- Fix: Corrected active instance host resolution (`84ee517`).
- Feature: Resolved instances from configured host fields (`1a3d24a`).
- Feature: Resolved instances by submission URL host (`2a17262`).
- Feature: Added member-only submission type access controls (`af1ee5f`).

## 2026-03-18

- Update: Renamed the "submission questions" card to "submission info" (`40a8173`).

## 2026-03-13

- Feature: Added a meeting-day calendar and AV event access (`12e5310`).

## 2026-03-12

- Test: Added coverage for report and review utilities (`7ebee64`).

## 2026-03-10

- Feature: Added a searchable canonical organization combobox (`0ad86b6`).

## 2026-03-08

- Feature: Added Textract-based OCR suggestions for submission questions (`446cb7d`).
- Feature: Added an assignment algorithm preview workflow and related UI updates (`a8ff43f`).

## 2026-03-07

- Test: Mocked Prisma `findMany` calls in organization action tests (`e148d8e`).
- Feature: Added a submission payment flow and gateway settings (`3a6150d`).
- Feature: Added an instance copy workflow in general configuration (`058b751`).
- Feature: Added decisions and reviewer CSV import flows for admins (`5338845`).
- Feature: Included canonical organization data in preview and review author summaries (`44834e2`).

## 2026-03-06

- Fix: Removed an invalid server action directive from the organization resolution utility (`af6af19`).

## 2026-03-05

- Feature: Added an organization resolution workflow and admin queue (`679bee9`).
- Maintenance: Removed instance lookup debug logging (`3da6d93`).
- Update: Switched submission window datetimes to Luxon time-zone-aware handling (`f227bfe`).
- Test: Added more unit tests (`b23de20`).

## 2026-03-03

- Maintenance: Removed old logging (`cc29a9a`).
- Test: Added a test coverage alias (`d2e0ed6`).

## 2026-03-02

- Documentation: Added initial admin documentation (`0c4954e`).

## 2026-02-27

- Feature: Added JSON output for the program builder and changed friendly IDs to start at 1000 (`519d145`).

## 2026-02-26

- Feature: Added initial journal output (`0207273`).

## 2026-02-25

- Feature: Added an "included in journal" option (`8371345`).
- Feature: Added an "included in word/char count" option (`e37b1f3`).
- Feature: Added initial program and instance copy links (`fd66cea`).
- Feature: Added User Administration and Individual Email sections to admin (`7daef18`).

## 2026-02-24

- Test: Added unit tests and verified they passed at the time (`dd33997`).

## 2026-02-23

- Feature: Completed the speaker section pending entry-point wiring (`4811076`).
- Feature: Added city and country dropdown question fields (`6dc25a5`).
- Feature: Added question show/hide logic (`e9e79c1`).
- Feature: Added "Other" and heading-only options to question creation (`8f0022d`).
- Feature: Expanded speaker functionality (`80ab5c4`).

## 2026-02-17

- Feature: Added the initial presentation room (`7586635`).
- Update: Polished materials upload (`ae6db5e`).
- Feature: Added the initial materials upload section (`c85dbc5`).

## 2026-02-13

- Fix: Resolved linting errors (`eae7f44`).
- Feature: Added confirmation merge fields and questions (`6d60018`).
- Feature: Added presentation confirmation questions (`adfc24c`).
- Feature: Added call-for-reviewers sections (`3653c71`).
- Feature: Added event import category colors (`da06017`).

## 2026-02-12

- Feature: Added the initial event import workflow (`46b768a`).

## 2026-02-10

- Feature: Added manual event scheduling with a color picker (`b6978d0`).
- Update: Removed color from the acceptance types section (`5ca244c`).

## 2026-02-06

- Feature: Added the initial acceptance types section (`7891348`).
- Fix: Resolved TypeScript errors (`5138eb3`).

## 2026-02-04

- Feature: Added symposium functionality and a speaker wireframe (`8c8312a`).

## 2026-01-28

- Update: Removed page-based behavior that was too complex for the abstracts workflow (`8400112`).
- Feature: Added initial symposium setup (`9a91795`).
- Fix: Reinforced dynamic paragraph height (`3d4704e`).

## 2026-01-26

- Feature: Added rich text editing (`3b2fe25`).
- Maintenance: Updated `package.json` dependencies or scripts (`c224f9f`).

## 2025-12-05

- Update: Updated the Next.js version (`1c97a97`).

## 2025-11-04

- Feature: Added rich text editor components (`824cb9a`).

## 2025-11-01

- Fix: Resolved remaining TypeScript errors known at the time (`379f6df`).

## 2025-10-31

- Fix: Fixed TypeScript build errors (`89f94d6`).

## 2025-10-30

- Feature: Added a submission preview option (`3e4c81d`).
- Feature: Added coauthor functionality (`849dee1`).

## 2025-10-29

- Feature: Added general configuration and author options to submission types (`ee7ac03`).

## 2025-10-28

- Update: Updated the login page to show instance dates, location, and a create-account button placeholder (`30ca22e`).
- Fix: Fixed Prisma build errors (`2bf764c`).

## 2025-10-27

- Fix: Fixed Prisma dotenv handling (`9ff20e1`).
- Feature: Added `.env`, Prisma, and updated database calls (`c09e690`).
- Foundation: Created the initial app commit (`57e22e0`).
