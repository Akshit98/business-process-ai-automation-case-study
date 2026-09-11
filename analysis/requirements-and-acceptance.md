# Proposed requirements and acceptance tests

Requirements are design artifacts. Tests below are planned and have not been executed in HubSpot, Asana or a billing system.

| ID | Requirement | Acceptance condition | Proposed owner |
| --- | --- | --- | --- |
| R1 | Lead record | At the agreed capture point, each enquiry has an owner, source, contact, discovery status and next action. An unscheduled call can be logged manually. | Sales/discovery owner |
| R2 | Proposal release | A proposal uses the approved template and has a named reviewer. Client revisions return to the author; approval applies to the final version. | Proposal author + reviewer |
| R3 | Project readiness | Normal work starts after agreement, project, shared folder and owner are linked. An urgent start requires a recorded approver, minimum record and setup-completion deadline. | PM + authorized partner |
| R4 | Assignment reconciliation | Both PM and partner assignments enter the shared capacity record. The PM receives a direct-assignment notice and resolves capacity conflicts. | PM + partner |
| R5 | Status and communication | Asana holds approved delivery status; Drive holds approved documents. Each project records its client communication owner, cadence and format. | Consultant + PM |
| R6 | Billing branches | Hourly invoice readiness depends on complete, approved time. Fixed-fee invoice timing follows the contract, generally monthly in the scenario; hourly time rules do not block it. | Accounting + reviewer |
| R7 | Automation recovery | A deal ID + agreement version identifies a project handoff. Replays retrieve the same project; failures retain logs and route to a named owner. | Operations/system owner |

## Planned tests

| ID | Scenario | Expected result |
| --- | --- | --- |
| U1 | Unscheduled referral | A manual intake creates a record and owner without requiring a calendar trigger. |
| U2 | Proposal revision | A revised scope returns to the author/reviewer; the earlier approval does not release the new version. |
| U3 | Urgent project start | An incomplete setup cannot follow the normal path; an approved exception records an owner and deadline. |
| U4 | Direct partner assignment | The shared capacity view is updated and the PM receives a notice. |
| U5 | Off-system status | An approved draft is linked to the correct project; unapproved text cannot replace Asana status. |
| U6 | Hourly vs fixed-fee | Missing hourly time flags an invoice delay; a fixed-fee invoice uses its contractual schedule. |
| U7 | Replayed / failed event | Replay creates no duplicate; a failed write produces a recoverable exception. |
| U8 | Unsupported AI statement | An invented date or unsupported completion claim is rejected before approval. |
