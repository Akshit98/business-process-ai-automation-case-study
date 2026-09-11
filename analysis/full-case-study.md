# Consulting Client Delivery Workflow Optimization & AI Automation

**Akshit Didla | Process analysis and solution design | Independent portfolio project | 2026**

## Project overview

I analyzed a consulting firm's client-delivery workflow from a supplied discovery transcript. I mapped the process from lead intake to invoicing, documented its exceptions, and developed recommendations for more consistent records, ownership and billing readiness.

## My contribution

My original assessment response covered the process summary, stakeholders, information gaps, follow-up questions, current-state diagram and improvement opportunities. This portfolio develops that analysis into a proposed future state, acceptance criteria, a KPI framework and a phased rollout plan.

Completed outputs: nine process stages, 15 follow-up discovery questions, seven issue assessments, five prioritized automation opportunities, seven proposed requirements and eight planned acceptance tests. These are artifact counts, not business outcomes.

## Central recommendation

Standardize responsibilities and required records before connecting tools. Keep authorized urgent starts and partner assignments visible. Use rules for lead capture and time reminders; use AI selectively for reviewed proposal and status drafts.

## Scope

Independent assessment-based portfolio project. I analyzed a supplied discovery transcript; I did not conduct the interview or implement changes in a production organization. The original question and my 16-page response were reviewed for this revision. No operational records, system access, timing baseline or production results are available. Company and stakeholder names are anonymized publicly. Portfolio preparation was AI-assisted.

# Evidence and source traceability

T1-T8 identify the eight topic blocks in the supplied assessment discovery transcript, in order. The response page references point to the candidate-provided 16-page answer. The raw assessment and answer are not republished here; this file contains anonymized paraphrases.

| Source ID | Topic | Transcript fact | Answer location |
| --- | --- | --- | --- |
| T1 | Lead intake and discovery | Referrals, LinkedIn and the website generate enquiries. The partner or a consultant runs discovery. HubSpot logging sometimes happens immediately and is sometimes skipped, especially for fast-moving referrals. | Original answer pp. 1-6 |
| T2 | Proposal | The partner creates most proposals; some senior consultants create their own. Formats vary and clients sometimes request revisions before acceptance. | Original answer pp. 1-5 |
| T3 | Agreement and setup | After acceptance the client signs an agreement. The PM normally creates the Asana project and shared folders. Urgent work sometimes starts before setup finishes. | Original answer pp. 2-6 |
| T4 | Work assignment | The PM normally assigns by availability and expertise using a capacity spreadsheet. The partner sometimes assigns high-priority clients directly. | Original answer pp. 1-6 |
| T5 | Delivery updates | Consultants are expected to update Asana, usually weekly. Updates are inconsistent; Slack or email sometimes substitutes for Asana. | Original answer pp. 3-6 |
| T6 | Client communication | Clients receive regular weekly meetings, written status reports or quick calls. There is no one standard format across engagements. | Original answer pp. 2-6 |
| T7 | Billing | Fixed-fee projects are generally invoiced monthly. Hourly invoices depend on submitted consultant time; late entries sometimes delay billing. | Original answer pp. 2-6 |
| T8 | Coordination | Information is spread across Asana, Google Drive, email and Slack. The partner reports extra time spent coordinating and locating information. | Original answer pp. 3-4, 14 |

## Claim boundaries

Observed: explicit scenario statements. Hypothesis: an explanation to validate. Proposed: a future control or metric. Unknown: missing rules, systems, frequency or ownership. None of these labels imply fieldwork or production validation.

# Consulting Client Delivery Workflow Optimization & AI Automation

**Akshit Didla | Process analysis and solution design | Independent portfolio project | 2026**

## Project overview

I analyzed a consulting firm's client-delivery workflow from a supplied discovery transcript. I mapped the process from lead intake to invoicing, documented its exceptions, and developed recommendations for more consistent records, ownership and billing readiness.

## My contribution

My original assessment response covered the process summary, stakeholders, information gaps, follow-up questions, current-state diagram and improvement opportunities. This portfolio develops that analysis into a proposed future state, acceptance criteria, a KPI framework and a phased rollout plan.

Completed outputs: nine process stages, 15 follow-up discovery questions, seven issue assessments, five prioritized automation opportunities, seven proposed requirements and eight planned acceptance tests. These are artifact counts, not business outcomes.

## Central recommendation

Standardize responsibilities and required records before connecting tools. Keep authorized urgent starts and partner assignments visible. Use rules for lead capture and time reminders; use AI selectively for reviewed proposal and status drafts.

## Scope

Independent assessment-based portfolio project. I analyzed a supplied discovery transcript; I did not conduct the interview or implement changes in a production organization. The original question and my 16-page response were reviewed for this revision. No operational records, system access, timing baseline or production results are available. Company and stakeholder names are anonymized publicly. Portfolio preparation was AI-assisted.

## Current-state stage register

| Stage | Input | Output | Owner / uncertainty | Source |
| --- | --- | --- | --- | --- |
| Lead intake | Enquiry from referral / LinkedIn / website | Prospect ready for discovery; CRM entry may be absent | Logging owner and exact timing unclear | T1 |
| Discovery | Client needs discussed | Fit decision; good-fit prospects proceed to proposal | Partner or consultant; criteria and no-fit handling unclear | T1 |
| Proposal | Discovery information | Proposal; revisions may loop back before acceptance | Partner / senior consultant; internal approval rule unclear | T2 |
| Agreement | Accepted proposal | Client-signed agreement | Client signs; internal owner and signing tool unclear | T3 |
| Project setup | Signed engagement | Asana project and shared folders | PM normally; urgent work may start before completion | T3 |
| Work assignment | Scope, availability and expertise | Assigned consultant(s) | PM normally, or partner directly for high-priority clients; capacity spreadsheet | T4 |
| Delivery | Assigned work | Progress updates in Asana or Slack/email | Consultant; Asana updates usually expected weekly | T5 |
| Client communication | Project progress | Weekly meeting, written report or quick call | Owner and selection rule unspecified; cadence varies | T6 |
| Billing | Fixed-fee schedule OR hourly time entries | Invoice; hourly invoice delayed when time is late | Accounting for hourly invoices; fixed-fee ownership not explicitly stated | T7 |

## Stakeholders and systems

The managing partner and consultants conduct discovery; the partner and senior consultants create proposals. The PM normally sets up projects and assigns work. Consultants deliver and submit time. Accounting generates hourly invoices. Clients accept proposals, sign agreements and receive updates.

Known tools: HubSpot, Asana, Google Drive, Slack, email and a capacity spreadsheet. No contract, time-tracking or accounting product is named. The transcript does not establish a dedicated e-signature tool.

# Evidence-based issue register

Observed means stated in the supplied scenario, not independently audited in a live organization. Root causes remain hypotheses. P1/P2 are design priorities, not measured severity scores.

| ID | Area | Source | Observation | Business implication | Root-cause hypothesis | Validation | Priority |
| --- | --- | --- | --- | --- | --- | --- | --- |
| G1 | Lead capture | T1 | Some leads are not logged in HubSpot. | The CRM may omit active prospects; no missed-lead count or source-performance data is supplied. | Ownership, timing or intake rules may be unclear. | Reconcile enquiries with CRM; confirm who captures unscheduled and referral calls. | P1 |
| G2 | Proposal consistency | T2 | Proposal formats vary; revisions occur. | Handoffs may be harder to compare. The transcript does not show that format variation causes revisions or errors. | Template choice and review responsibility may be inconsistent. | Review proposal samples, revision reasons and approval practice. | P1 |
| G3 | Setup readiness | T3 | Urgent work sometimes begins before Asana and folders are ready. | Work may lack a shared location or recorded owner at the point it starts. No actual loss or unauthorized work is established. | The urgent-start path may lack a documented minimum setup rule. | Ask who authorizes early starts and how setup is completed afterward. | P1 |
| G4 | Assignment visibility | T4 | Both PM-led and direct partner assignment occur. Capacity is tracked in a spreadsheet. | An unrecorded assignment could distort the shared capacity view. Whether reconciliation already happens is unknown. | Notification and reconciliation rules may be unclear. | Confirm partner-to-PM notification, capacity updates and conflict resolution. | P1 |
| G5 | Status and documentation | T5, T8 | Slack/email can replace Asana updates; information is spread across several tools. | The partner explicitly reports extra coordination and search effort. Its frequency and cost are unmeasured. | Record ownership, tool friction or duplicate-entry effort may contribute. | Trace sample updates and ask why consultants use alternate channels. | P1 |
| G6 | Client reporting | T6 | Meetings, reports and calls vary across clients. | Variation can be appropriate. The gap is that ownership and the selection rule are not described, not that every client needs one format. | Kickoff agreements may not capture cadence, format and owner consistently. | Ask how reporting preferences are agreed and recorded. | P2 |
| G7 | Hourly billing readiness | T7 | Late time entries sometimes delay hourly invoices. | Invoice timing is affected. The size of the delay and any cash-flow impact are not quantified. | Deadlines, reminders or escalation ownership may be unclear. | Confirm time system, cutoff, approval steps and exception handling. | P1 |

# Follow-up discovery guide

These 15 questions are proposed for a next session; no follow-up interview has been conducted.

| No. | Theme | Question | Decision enabled |
| --- | --- | --- | --- |
| 1 | Workflow | What internal review occurs before a proposal is sent, and what commonly drives revisions? | Proposal approval and rework rules |
| 2 | Workflow | How is the agreement signed, who owns it internally, and who reviews terms? | Contract owner, tool and approval |
| 3 | Workflow | What happens after delivery: client acceptance, close-out, offboarding or renewal? | Boundary beyond the described billing cycle |
| 4 | Ownership | Who logs a referral that was not entered immediately, and by when? | CRM accountability and capture timing |
| 5 | Ownership | Who can authorize work before setup finishes, and what minimum information is required? | Urgent-start rule |
| 6 | Ownership | When the partner assigns directly, how is the PM notified and capacity updated? | Assignment reconciliation |
| 7 | Rules | What defines a high-priority client, and how are conflicting assignments resolved? | Exception criteria and authority |
| 8 | Rules | How are reporting format, cadence and owner agreed with each client? | Client communication agreement |
| 9 | Rules | What is the fixed-fee/hourly mix, and which contractual events trigger invoices? | Billing branches and population definitions |
| 10 | Exceptions | How often do Slack/email updates replace Asana, and why does this happen? | Frequency and root-cause evidence |
| 11 | Exceptions | How late are time entries, what is the cutoff, and how are missing or disputed entries handled? | Billing delay and escalation |
| 12 | Exceptions | What happens when a prospect is not a fit, rejects a proposal or stops responding? | Unspecified commercial exits |
| 13 | Documentation | Which tool is authoritative for status, scope, documents and billing respectively? | Record-level sources of truth |
| 14 | Documentation | What onboarding or operating checklist do new consultants use today? | Existing controls and adoption needs |
| 15 | Documentation | Has standardization been attempted before, and what made it difficult to sustain? | Practical rollout constraints |

# Automation and AI opportunities

I retained the five opportunities in my original answer and refined where AI is appropriate. P1 prioritizes capture, assignment visibility and the explicitly reported hourly billing delay. Proposal and status AI follow the basic controls. This order is design judgment, subject to volumes, risk and effort validation.

| ID | Opportunity | Issue | Proposed solution | Method | Human control | Dependencies | Expected impact | Priority |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| A1 | Lead capture | G1 | A scheduled discovery event or approved intake form creates or matches a CRM record. Manual intake covers unscheduled calls and referrals. | Rules first; AI is unnecessary for basic record creation. | Capture source, owner and next action; review duplicate matches. | A reliable scheduling/intake trigger, CRM access and a capture owner must be confirmed. | More complete lead records; benefit unmeasured. | P1 |
| A2 | Proposal drafting | G2 | Use a standardized proposal template, optionally prefilled from reviewed discovery notes. AI may draft narrative sections. | Template + optional AI draft. | Named reviewer approves scope, dates and pricing before sending; unsupported fields stay blank. | Approved template, source notes, access restrictions and review ownership. | Less formatting variation and potentially less drafting effort; unmeasured. | P2 |
| A3 | Status consolidation | G5, G6 | From explicitly selected Slack/email updates, AI drafts an Asana update and client summary for review. | AI draft; deterministic project-ID routing. | Consultant checks source, project and status; communication owner approves release. No unrestricted mailbox ingestion. | Approved access, project mapping, data retention and evidence that consolidation reduces total effort. | Less duplicate entry and easier status retrieval, if review time permits. | P2 |
| A4 | Time-entry reminders | G7 | Send reminders before the agreed hourly billing cutoff. Flag missing submissions and active hourly projects with no time for review. | Rules; no AI needed. | Consultant resolves entries; PM/authorized reviewer checks them; accounting controls invoicing. Zero hours is a review flag, not proof of error. | Time system, expected submission roster, cutoff, billing model and approver must be confirmed. | Fewer late-entry delays; no measured improvement. | P1 |
| A5 | Resourcing visibility | G4 | Keep a shared capacity view that the PM and partner update for both assignment paths. Add direct-assignment notifications. | Process + shared tooling; no AI required. | PM reconciles capacity; the partner retains an explicit, logged exception path. | Confirm the existing spreadsheet structure and update practice before replacing it. | Better visibility of assignments; no proven conflict reduction. | P1 |

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

# KPI framework

No baseline or measured improvement is available. Numerical gates below are illustrative proposed pilot thresholds. Agree them after a two-week baseline, then compare a four-week pilot for the same service type. Report denominator, sample size, exclusions and complexity.

| KPI | Definition | Data / owner | Cadence | Proposed gate | Control |
| --- | --- | --- | --- | --- | --- |
| CRM capture completeness | Captured eligible enquiries / all enquiries found in reconciled channel records x 100 | Intake/channel records + HubSpot; discovery owner | Weekly | At least 95% | Do not use CRM records alone as the denominator; that hides unlogged leads. |
| Standard-start readiness | Standard project starts with the full checklist completed before work / all standard starts x 100 | Asana/Drive links + start times; PM | Weekly | At least 95% | Report urgent starts separately, including approval and setup-completion timeliness. |
| Assignment reconciliation | Assignments entered in the shared capacity view within the agreed window / all assignments x 100 | PM and partner assignment log + capacity tracker; PM | Weekly | 100% within 1 business day | Include both assignment paths; measure any conflicts separately. |
| On-time status update | Active projects with an approved update by the agreed weekly cutoff / active projects due an update x 100 | Asana and project roster; PM | Weekly | At least 95% | A Slack message alone does not count until reflected in the approved record. |
| Time-related invoice delay | Hourly invoices due but delayed because time is missing / hourly invoices due x 100 | Time records + invoice schedule + reason log; accounting | Billing cycle | At most 5% | Exclude fixed-fee invoices; report delay days and other delay reasons separately. |
| Net coordination effort | Median total minutes per comparable project-week spent collecting, reviewing, correcting and locating updates | Short activity log; PM and consultants | Weekly | Set after baseline | Compare the same service type and report sample size; do not count draft time alone. |

## AI and reliability guardrails

All client-facing AI drafts require approval; release no unsupported commitments. Count logical handoffs rather than retry attempts; tolerate zero duplicate project creations. Record failures and recovery time. These are proposed control gates, not achieved performance.

# Proposed implementation roadmap

An illustrative eight-week plan; dependent on access, staffing, approved tooling and adequate case volume. No stage has been implemented in a production organization.

| Timing | Phase | Work | Exit gate |
| --- | --- | --- | --- |
| Weeks 1-2 | Validate rules and collect a baseline | PM coordinates a follow-up with the partner, consultants and accounting. Sample enquiries, proposals, assignments, updates and invoice delays. | Agree record owners, unknowns, definitions and access. |
| Week 3 | Standardize before automation | Introduce a proposal template, normal/urgent setup checklist, shared assignment record, reporting agreement and hourly time cutoff. | Manual trial passes the approved checklists. |
| Week 4 | Configure and test a sandbox | An authorized administrator configures agreed rule-based handoffs and reminders. Test billing branches, replay handling and recovery. | Critical tests pass; owners can use the manual fallback. |
| Weeks 5-8 | Pilot and evaluate | Pilot one service type, review exceptions weekly, and compare with baseline. Trial optional AI drafts separately with full review. | Expand only after agreed gates are met; otherwise fix and extend the pilot. |

## Go / no-go

Do not expand with unresolved critical data exposure, duplicate-project, unauthorized-release or billing-branch errors. If gates are missed, retain the manual checklist, correct the failure and extend the pilot. Preserve IDs and logs during rollback.

# Risks and controls

| Risk | Proposed control | Owner |
| --- | --- | --- |
| Confidential source material | Use only project-scoped, approved inputs; minimize personal data and confirm retention before connecting Slack/email or AI. | Security/process owner |
| Unsupported AI scope or status | Require source excerpts and human review. Notes are untrusted data; they cannot instruct the system to change prices, dates or permissions. | Proposal reviewer / consultant |
| Early-start or assignment bypass | Keep an authorized urgent path, log the reason and owner, and require PM reconciliation instead of hiding exceptions. | Partner + PM |
| Wrong billing rule | Separate fixed-fee and hourly readiness. Flag zero time for review; accounting retains invoice approval. | Accounting |
| Duplicate or partial project creation | Use a unique handoff key, bounded retries, source/destination reconciliation and a manual recovery log. | System/operations owner |
| Administrative burden | Measure review and correction effort; keep the existing capacity spreadsheet if it meets the shared-view requirement. | PM |
