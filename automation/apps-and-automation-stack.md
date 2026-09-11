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

## Platform alternatives

Choose one central automation platform. These recommendations are design judgments, not measured comparisons.

### Make

Recommended pilot for this multi-branch process. Visual routing across the existing stack; configure incomplete executions and retries for supported temporary failures. A workflow owner still maintains mappings, credentials, exception routing and usage limits.

[Official reference](https://help.make.com/automatic-retry-of-incomplete-executions)

### Zapier

Alternative for simpler, operations-owned handoffs. Evaluate when the required triggers/actions are available and simpler setup matters most. Autoreplay and Human in the Loop support recovery and approvals. Confirm plan eligibility, task consumption and replay behavior. Complex branches still need careful design.

[Official reference](https://help.zapier.com/hc/en-us/articles/19220226086797-What-is-replay)

### n8n Cloud

Alternative for custom logic with a technical owner. Evaluate for API-heavy integrations and more tailored processing. An Error Trigger can start an exception workflow. Managed hosting reduces infrastructure work; workflow logic, credentials, error handling and data quality still need ownership.

[Official reference](https://n8n.io/integrations/error-trigger/)

### n8n self-hosted

Only with an accountable technical operator. Consider when infrastructure control is a real requirement and the team can operate it. Highest maintenance burden in this shortlist: upgrades, backups, security, availability and recovery become team responsibilities.

[Official reference](https://github.com/n8n-io/n8n-docs/blob/main/docs/deploy/host-n8n/README.md)

### Power Automate

Conditional alternative for a Microsoft-centered firm. Evaluate if the organization already works mainly in Microsoft 365 and has Power Platform administration. Check the exact third-party connectors and licensing. It is not the default choice for the supplied HubSpot/Asana/Drive stack.

[Official reference](https://learn.microsoft.com/en-us/power-automate/getting-started)

## Lower-oversight operating model

Keep Make for the proposed pilot; evaluate Zapier for simpler handoffs or n8n Cloud for technical customization. Prefer self-hosting only when a technical owner can maintain the infrastructure. Verify the exact connectors, licenses, workload costs and recovery behavior before selection.

Validated capture, approved project setup, linking, reminders and draft preparation can run unattended after testing. Pricing, scope, urgent starts, resource conflicts, AI client content and invoice release retain approval.

Enable bounded retries for temporary errors, prevent duplicates with event/deal/version identifiers, persist created IDs, reconcile eligible signed deals against project/folder records daily, and send exception alerts plus a daily summary. Give each exception an owner and backup. During the pilot, review exceptions daily and failure patterns weekly.

Test duplicate events, missing fields, expired connections, outages, version changes and delayed approvals before reducing oversight. Measure successful eligible runs without manual intervention / all eligible runs, excluding approval-required decisions. Track exception age, duplicate records and reconciliation mismatches separately. No unattended completion rate is claimed.
