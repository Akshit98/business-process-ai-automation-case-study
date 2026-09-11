# Workflow diagrams

The current state follows the supplied transcript. Dotted exits identify unspecified handling. The proposed future state includes new controls requiring validation.

## Current state

```mermaid
flowchart TD
  A[Lead: referral / LinkedIn / website] --> B[Discovery: partner or consultant]
  B --> C{HubSpot record captured?}
  C -->|Sometimes| D[Logged]
  C -->|Sometimes skipped| E[No CRM record yet]
  D --> F{Good fit?}
  E --> F
  F -->|Yes| G[Partner or senior consultant drafts proposal]
  F -. No: handling unspecified .-> H[Clarify follow-up / closure]
  G --> I[Send proposal]
  I --> J{Client response}
  J -->|Revisions| G
  J -->|Accepts| K[Client signs agreement]
  J -. Rejection / no response not described .-> H
  K --> L[PM normally starts Asana project + shared folders]
  L --> M{Setup finished before work?}
  M -->|Normal path| N[Setup complete before work]
  M -->|Urgent exception| O[Consultant starts while setup is incomplete]
  N --> P{Assignment path}
  O --> P
  P -->|Normal| Q[PM: availability + expertise; capacity spreadsheet]
  P -->|Some high-priority clients| R[Partner assigns directly]
  Q --> S[Delivery]
  R --> S
  S --> T{Status update channel}
  T -->|Usually expected weekly| U[Asana]
  T -->|Sometimes instead| V[Slack / email]
  U --> W[Client communication]
  V --> W
  W --> X{Format varies}
  X --> Y[Weekly meeting]
  X --> Z[Written report]
  X --> AA[Quick call]
  Y --> AB{Billing model}
  Z --> AB
  AA --> AB
  AB -->|Fixed fee| AC[Invoice generally monthly]
  AB -->|Hourly| AD{Time entries available?}
  AD -->|Submitted| AE[Accounting generates invoice]
  AD -->|Late| AF[Invoice delayed pending time]
  AF -->|When entries arrive| AE
  AC --> AG[Invoice cycle; payment / close-out not described]
  AE --> AG
```

## Proposed future state

```mermaid
flowchart TD
  A[Capture all channels; manual route for unscheduled calls] --> B[Discovery owner validates CRM record]
  B --> C[Fit decision and recorded next action]
  C --> D[Standard proposal template + named reviewer]
  D --> E{Client response}
  E -->|Revisions| D
  E -->|Accepts| F[Signed agreement + approved scope version]
  F --> G{Setup ready?}
  G -->|Yes| H[Linked Asana project + Drive folder + owner]
  G -->|No| I{Authorized urgent start?}
  I -->|No| J[Hold start and complete setup]
  J --> G
  I -->|Yes| K[Log minimum record, approver, reason and setup deadline]
  H --> L[PM or partner assigns; update shared capacity + notify PM]
  K --> L
  L --> M[Delivery with approved Asana status]
  M --> N[Optional AI draft from selected source updates]
  N --> O[Consultant reviews; client communication owner approves release]
  O --> P[Client-specific agreed format and cadence]
  P --> Q{Billing model}
  Q -->|Fixed fee| R[Contract schedule; accounting checks invoice]
  Q -->|Hourly| S[Cutoff reminders + missing-time flags]
  S --> T[Review time; accounting approves invoice]
  T --> U[Invoice cycle; confirm close-out separately]
  R --> U
```
