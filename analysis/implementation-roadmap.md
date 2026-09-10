## A staged, reversible rollout

Illustrative eight-week plan. Timing depends on access, staffing, approved tools and sufficient pilot volume; roles below are proposed responsibilities, not actual collaborators.

| Phase | Work and accountable owner | Exit gate |
| --- | --- | --- |
| Weeks 1-2
Validate + baseline | Operations owner interviews sales, delivery and finance; audits records; confirms fields, data access and current metrics. | Stakeholders approve process map, baseline method and data contract. |
| Week 3
Standardize | Sales owner introduces required fields; delivery lead approves project templates and ownership; finance confirms billing controls. | Manual handoff passes readiness checklist on sample cases. |
| Week 4
Configure + test | Authorized system administrator builds a sandbox handoff and exception log; operations tests recovery; security reviews access. | All critical acceptance tests pass; rollback and manual fallback rehearsed. |
| Weeks 5-8
Pilot + decide | Delivery lead pilots one service type; operations reviews exceptions weekly. Optional AI drafts stay in a separate review queue. | Compare baseline and pilot; resolve critical defects; process owners approve expansion or extend pilot. |


### Planned acceptance tests - not executed

Valid signed handoff creates one linked project. Missing scope blocks creation. Replayed event creates no duplicate. Permission failure produces an actionable exception. Scope change requests review. Unsupported AI date is rejected. Missing project ID blocks billing approval. Restore manual processing after disabling the automation.


### Rollout decision

Expand only when the agreed KPI gates are met and there are no unresolved critical data, duplicate-project or unauthorized-message defects. Otherwise keep the manual checklist, fix the failure mode and rerun the affected tests. Preserve logs and identifiers during rollback to avoid duplicate recovery work.

