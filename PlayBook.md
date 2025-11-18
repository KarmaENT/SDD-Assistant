# SDD PlayBook 

Nominate a Pilot (tech lead) who owns the spec/plan quality bar

Collect non-functional requirements (security, compliance, design tokens, latency/SLOs)

Define interfaces & data contracts early (types, schemas, events)



## Phase gates



### Specify



Problem statement + who it’s for

Primary flows (happy + edge cases)

Success criteria (KPIs, budgets, SLOs)

Add UX guardrails: authentication, empty states, accessibility



### Plan



Stack, architecture diagrams, service boundaries

Data model + migrations; API contracts

Security and compliance rules as executable checks where possible



### Tasks



Break into ≤90-minute units; each with Definition of Done and tests

Sequence for fast feedback (vertical slices > horizontal layers)

Implement

Run tasks in parallel where safe

Enforce review gates (tests, static analysis, performance checks)



### After each phase



Reflect → refine → regenerate (don’t be precious; iterate the spec)





### 6.2 What to put in the spec (and what to keep out)



Must include



Auth & roles (e.g., HR login, admin toggles)

Data sources & schemas (PII rules, retention, lineage)

UX rules (empty/loading/error states, a11y constraints)

Performance budgets (e.g., p95 < 300ms) and observability (logs/metrics)

Keep out



Low-level code style—let the formatter/linter handle it

Over-detailing trivialities that stall the team



### 6.3 SDD “Gotchas” checklist



Does every primary flow have required auth and role-based screens?

Are edge cases (empty data, timeouts, retries) explicitly covered?

Are events & contracts versioned (compatibility plan)?

Will the agent seed data for demos/tests?

Do tasks encode tests up front (TDD bias)?

Are design tokens and components specified (not just “use our DS”)?
