# Root-cause hypotheses

These are hypotheses for a future discovery exercise. No stakeholder interviews or production validation were performed.

## Where work can break

Only inconsistent HubSpot logging is an explicit problem in the supplied scenario. The remaining rows are potential failure modes, not confirmed findings.

| Pain point / status | Root-cause hypothesis | Validation and proposed response |
| --- | --- | --- |
| Incomplete CRM history / supplied | No consistent entry standard or owner at the discovery handoff. | Audit recent discovery records; ask who logs each field. Require source, owner, call date, next step and due date. |
| Leads missed across channels / hypothesis | Referral and LinkedIn enquiries may stay outside a shared queue. | Compare channel records with CRM intake; introduce one capture route and an unassigned-lead queue. |
| Setup rework / hypothesis | Agreement details may be retyped into project tasks. | Trace agreement-to-project handoffs; use approved fields and a project template. |
| Assignment delays / hypothesis | Skills and availability may be checked informally. | Review assignment decisions with delivery lead; require a capacity check and named approver. |
| Unclear delivery status / hypothesis | Milestones and client updates may have different owners. | Compare project records with update cadence; assign milestone owners and review overdue items. |
| Billing delays / hypothesis | Time entries may lack project IDs or timely approval. | Trace invoice preparation; validate IDs, submission cutoffs and finance sign-off. |


### Discovery questions before building

Who owns a lead before discovery? What makes an agreement ready for delivery? Which service types need different project templates? Where are time and invoices recorded? What client-data restrictions apply? Capture answers and revise this design before a pilot.


## Validation log to collect

For each issue, record a sample record ID, observed failure, proposed cause, interview evidence, alternative explanation, owner and status. A missing CRM field alone does not prove a training problem: first check ownership, permissions, field design and duplicate records.
