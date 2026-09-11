# Apps and automation stack

Independent proposed implementation design. No connected production workflow or measured results.

## Current systems

- **HubSpot** — Named in the scenario. CRM, lead and discovery records; logging is inconsistent.
- **Asana** — Named in the scenario. Project setup, assigned work and expected delivery updates.
- **Google Drive** — Named in the supplied answer. Shared folders and project documentation.
- **Slack** — Named in the scenario. Internal updates; sometimes used instead of Asana.
- **Email** — Provider unspecified. Client communication and internal updates. Do not assume Gmail or Outlook.
- **Capacity spreadsheet** — App unspecified. Availability and allocation tracking. Excel or Google Sheets is not confirmed.
- **Agreement / e-signature tool** — Tool unspecified. The client signs an agreement; the signing platform is not identified.
- **Time tracking / accounting** — Tools unspecified. Hourly time entries feed accounting invoicing. These may be separate systems.
- **LinkedIn, website, referrals** — Lead sources. LinkedIn is a named channel; the website platform and form tool are unknown. Referrals are a source, not an app.

## Recommended pilot stack

### HubSpot

Retain · CRM. Store lead source, discovery owner, fit outcome, deal ID and agreement reference. Use a form or manual capture for referral and LinkedIn enquiries.

[Official documentation](https://apps.make.com/hubspotcrm)

### Make

Add · Workflow automation. Connect events and scheduled checks across apps. Apply filters, duplicate checks, error handling and a named exception owner.

[Official documentation](https://help.make.com/whats-a-scenario-and-which-type-should-you-use)

### PandaDoc

Candidate · Proposals & signatures. Prepare proposals from approved templates, obtain review, and track agreement signatures. Evaluate its HubSpot integration.

[Official documentation](https://www.pandadoc.com/integrations/crm/hubspot/)

### Asana

Retain · Delivery & review. Create project tasks, record the accountable owner, track readiness and hold approval tasks. Approval fields and automation must be configured.

[Official documentation](https://apps.make.com/asana)

### Google Drive

Retain · Documents. Create the engagement folder and link approved scope, signed agreement and deliverables. Preserve access by project.

[Official documentation](https://apps.make.com/google-drive)

### Google Sheets

Candidate · Capacity register. Use a shared allocation register for the pilot if the existing spreadsheet cannot be shared reliably. PM and partner assignments enter the same record.

[Official documentation](https://apps.make.com/google-sheets)

### Slack + existing email

Retain · Notifications & communication. Send internal reminders and links to review tasks. Keep the existing approved email provider for client messages; its exact connector needs confirmation.

[Official documentation](https://apps.make.com/slack)

### Harvest

Candidate · Time tracking. Evaluate time capture alongside Asana. Confirm approval, billing exports and compatibility with the existing accounting system before choosing it.

[Official documentation](https://www.getharvest.com/integrations/asana)

### Existing accounting system

Retain pending discovery · Billing. Remain the authoritative invoice record. Confirm its name and connector/API; use a reviewed import if direct integration is unavailable.

### Make AI Toolkit

Optional · AI summaries. Draft discovery or progress summaries from selected text. A person checks facts and approves the content before it becomes an official update.

[Official documentation](https://www.make.com/en/integrations/ai-tools)

## Proposed automations

### 01 · Lead capture

Trigger: Website form, or a person logs a referral / LinkedIn enquiry.

Apps: HubSpot → Make → HubSpot.

Automatic action: Find an existing contact, create or update the enquiry, assign an owner and flag missing fields.

Human checkpoint: Discovery owner confirms fit and next action. No LinkedIn scraping or automated outreach is assumed.

### 02 · Proposal preparation

Trigger: Discovery marked ready with required fields complete.

Apps: HubSpot → Make → PandaDoc.

Automatic action: Create a draft from an approved template and notify the reviewer. Record the document ID and scope version.

Human checkpoint: Author/reviewer approves content and price before sending. Client revisions reset approval.

### 03 · Signed agreement handoff

Trigger: Signing service reports a completed agreement.

Apps: PandaDoc → Make → HubSpot + Asana + Drive.

Automatic action: Verify signature status and approved scope; create or retrieve the project and folder, then write their links back to the deal.

Human checkpoint: PM checks readiness. An urgent start needs a recorded approver and setup deadline.

### 04 · Consultant assignment

Trigger: PM or partner submits an allocation.

Apps: Asana + Google Sheets → Make → Slack.

Automatic action: Record the assignment in the shared capacity register, notify the PM and flag possible overlaps.

Human checkpoint: PM or partner chooses the consultant; PM resolves conflicts. Capacity logic is configured, not provided automatically by the sheet.

### 05 · Progress and client reporting

Trigger: Scheduled status check for an active project.

Apps: Asana + selected Slack/email text → Make AI Toolkit → Asana.

Automatic action: Flag overdue updates; optionally prepare a summary with source links in a review task.

Human checkpoint: Consultant checks accuracy; communication owner authorizes client release. No unrestricted inbox or Slack collection.

### 06 · Hourly billing readiness

Trigger: Agreed time-entry cutoff approaches.

Apps: Harvest or existing tracker → Make → Asana / Slack → Accounting.

Automatic action: Identify missing time for active hourly projects, remind owners, then prepare approved time for a draft invoice or reviewed import.

Human checkpoint: Time reviewer and accounting approve. Missing time delays hourly billing; no final invoice is automatically issued.

### 07 · Fixed-fee billing

Trigger: Contract billing date arrives.

Apps: HubSpot contract schedule → Make → Accounting.

Automatic action: Prepare an invoice request or draft from the approved fixed-fee schedule.

Human checkpoint: Accounting checks scope and amount. Hourly time-entry rules do not block this branch.

## Build sequence and controls

Start with capture and setup, then reminders and billing readiness. Add AI last. Verify tool editions, permissions, connector events, API limits and usage costs. Identify the existing accounting tool before automating invoices. Use deal ID plus agreement version for duplicate prevention; persist created IDs, assign failures to an Asana exception queue and retry only failed actions. Give either native integration or Make ownership of each write. Review every external proposal, client message and final invoice.

Product references checked 11 September 2026.
