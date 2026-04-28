# Agent Operating System (AOS): The 5-Layer CDD Framework

## Build Any Software Project with AI Agents — One Command at a Time

---

## What This Is

A system where you type `/1` and an AI agent builds one complete, tested work package. Repeat until your product is done. No improvisation. No scope creep. No copy-pasting long prompts.

This document is a **fill-in-the-brackets template**. Replace every `[bracket]` with your project's details and you have a fully operational agent execution system.

---

## The Architecture

```
┌─────────────────────────────────────────────┐
│  Layer 5: COMMANDS         ← you type /1    │
│  Layer 4: CONTEXT          ← agent loads    │
│  Layer 3: EXECUTION        ← agent follows  │
│  Layer 2: CONSTRAINTS      ← agent obeys    │
│  Layer 1: VISION           ← agent learns   │
│  PROGRESS TRACKER          ← auto-updated   │
└─────────────────────────────────────────────┘
```

- **Layer 1** teaches the agent what the product is
- **Layer 2** gives exact rules so it never improvises
- **Layer 3** breaks the project into step-by-step tasks
- **Layer 4** tells the agent which docs to read per task
- **Layer 5** maps simple commands to full work packages
- **Progress** tracks what's done across sessions

Each layer builds on the one below. Skip a layer and the system breaks:

| Missing Layer | What Breaks |
|---|---|
| No Layer 1 | Agent doesn't understand the product |
| No Layer 2 | Different sessions produce incompatible code |
| No Layer 3 | Agent doesn't know what to do or when to stop |
| No Layer 4 | Agent loads wrong docs, skips quality gates |
| No Layer 5 | You copy-paste prompts manually every time |
| No Progress | New sessions don't know what's already built |

---

# LAYER 1: VISION — "What and Why"

**Purpose**: Give the agent deep product understanding so it builds the right thing, not random code.

**Files in this layer**: 9

---

### 01 · `01_[Project]_Complete_Spec.md` — Master Vision

The brain of your project. Agent reads this for every task.

```markdown
# [Project Name] Complete Specification

## 1. What Is [Project Name]?
[2-3 sentences. What problem does it solve? Who is it for?]

## 2. Target Users
- [User type 1 — e.g., "Saudi consumers managing multiple bank accounts"]
- [User type 2 — e.g., "University students tracking spending"]

## 3. Core Features
### 3.1 [Module Name — e.g., "Authentication"]
- [Sub-feature — e.g., "Email/password signup"]
- [Sub-feature — e.g., "JWT session management"]

### 3.2 [Module Name — e.g., "Dashboard"]
- [Sub-feature]
- [Sub-feature]
[Continue for all modules]

## 4. System Architecture
- Backend: [e.g., "FastAPI, Python 3.12"]
- Frontend: [e.g., "React, TypeScript, Vite"]
- Database: [e.g., "PostgreSQL via Supabase"]
- Cache: [e.g., "Redis via Upstash"]
- Deployment: [e.g., "Vercel + Render"]

## 5. Security Requirements
- [e.g., "Argon2id password hashing"]
- [e.g., "JWT with 30-min access tokens"]
- [e.g., "AES-256-GCM for sensitive data"]

## 6. Design Direction
- Colors: [e.g., "Deep green #0F5C4D, Sand #D6C3A1"]
- Typography: [e.g., "Manrope for English"]
- Layout: [e.g., "Mobile-first, dashboard-centric"]

## 7. Localization
- MVP: [e.g., "English only"]
- Future: [e.g., "Arabic + RTL in Phase 2"]

## 8. What This Project Is NOT
- [e.g., "Not a payment processor — read-only"]
- [e.g., "Not a banking app — aggregator only"]
```

---

### 02 · `02_[Project]_Feature_Inventory.md` — All Features

Complete feature menu across all modules.

```markdown
# [Project Name] Feature Inventory

## Module 1: [Name]
- [Feature 1.1]
- [Feature 1.2]

## Module 2: [Name]
- [Feature 2.1]
- [Feature 2.2]

[Aim for 8-15 modules]
```

---

### 03 · `03_[Project]_Scope_Map.md` — MVP vs Later

Prevents scope creep — the #1 project killer.

```markdown
# [Project Name] Scope Map

## MVP (build first)
- [Feature]
- [Feature]

## Phase 2 (after MVP works)
- [Feature]

## Future (don't build yet)
- [Feature]
```

---

### 04 · `04_[Project]_Build_Target.md` — What to Actually Build

More specific than scope map. Includes demo flow and navigation.

```markdown
# [Project Name] Build Target

## What We're Building
[1-2 paragraphs describing the V1 product]

## Pages / Screens
1. [e.g., "Dashboard"]
2. [e.g., "Transactions"]
[All pages]

## Demo Flow
1. [e.g., "User logs in"]
2. [e.g., "Connects mock bank"]
3. [e.g., "Dashboard shows summary"]
[Full sequence]

## What To Defer
- [e.g., "Full AI chat — just insight cards"]
```

---

### 05 · `05_[Project]_Build_Order.md` — Implementation Sequence

Ensures dependencies are built before features that need them.

```markdown
# [Project Name] Build Order

## Phase 1: Foundation
- Project scaffold
- Authentication

## Phase 2: Data Layer
- Database schema
- Data ingestion

## Phase 3: Core Features
- [Feature that others depend on]

## Phase 4: Business Logic
- [Advanced feature]

## Phase 5: Frontend
- App shell → pages → UI components

## Phase 6: Polish
- Security → UX → Demo prep
```

---

### 06 · `06_[Project]_System_Parts.md` — Architecture Explained

Plain-language module descriptions. Non-technical stakeholders can read this too.

```markdown
# [Project Name] System Parts Explained

## [Module 1 — e.g., "Frontend"]
**What it does**: [1-2 sentences]
**Talks to**: [which other modules it connects to]
**Key technology**: [e.g., "React + Vite"]

## [Module 2 — e.g., "Backend API"]
**What it does**: [1-2 sentences]
**Talks to**: [which other modules]
**Key technology**: [e.g., "FastAPI"]

## [Module 3 — e.g., "Database"]
**What it does**: [1-2 sentences]
**Talks to**: [which other modules]
**Key technology**: [e.g., "PostgreSQL"]

[Continue for all modules — aim for 6-12 modules]
```

---

### 07 · `07_[Project]_Stack_Cost.md` — Tech Choices + Pricing

What it costs to run your product.

```markdown
# [Project Name] Stack, Cost, and Capacity

## Technology Stack
| Layer | Technology | Why |
|---|---|---|
| Backend | [e.g., "FastAPI"] | [e.g., "Async, auto-docs, Pydantic"] |
| Frontend | [e.g., "React + Vite"] | [e.g., "SPA, fast dev server"] |
| Database | [e.g., "PostgreSQL"] | [e.g., "ACID, decimal precision"] |
| Hosting | [e.g., "Render + Vercel"] | [e.g., "Free tiers, auto-deploy"] |

## Monthly Cost Estimate
| Service | Free Tier | Paid Tier |
|---|---|---|
| [e.g., "Supabase"] | [e.g., "500 MB, 50K requests"] | [e.g., "$25/mo"] |
| [e.g., "Render"] | [e.g., "750 hours"] | [e.g., "$7/mo"] |
| **Total** | **$0** | **$[X]/mo** |

## Capacity
- [e.g., "Free tier supports ~100 daily active users"]
- [e.g., "Bottleneck: database connections at 20 concurrent"]
```

---

### 10 · `10_[Project]_Risk_Register.md` — What Can Go Wrong

```markdown
# [Project Name] Risk Register

## R-01: [e.g., "Scope Creep"]
- Likelihood: [High/Medium/Low]
- Impact: [High/Medium/Low]
- Mitigation: [e.g., "Strict in/out scope per WP"]

## R-02: [Risk]
- Likelihood:
- Impact:
- Mitigation:

[5-15 risks]
```

---

### 11 · `11_[Project]_Agent_Workflows.md` — Agent Operating Rules

```markdown
# [Project Name] Agent Workflow System

## Workflow Types

### /feature (default)
- Read: MVP context + constraint docs
- Do: implement one WP
- Output: code + tests + summary

### /fix
- Read: relevant source files only
- Do: fix one bug
- Output: cause + fix + verification

### /review
- Read: spec + WBS + risk register
- Do: review one completed WP
- Output: findings by severity

## Session Rules
- One WP per session (recommended)
- Always read PROGRESS.md first
- Never start the next WP without being asked
```

---

# LAYER 2: CONSTRAINTS — "The Exact Rules"

**Purpose**: Remove ALL ambiguity. Agent never improvises database tables, API shapes, or test approaches. This makes different agent sessions produce compatible output.

**Files in this layer**: 7

---

### 16 · `16_[Project]_ERD.md` — Database Schema

Every table, column, FK, and index. Agent reads this whenever it touches the database.

```markdown
# [Project Name] ERD

## Tables

### users
| Column | Type | Constraints |
|---|---|---|
| id | uuid | PK |
| email | string | unique, not null |
| password_hash | string | not null |
| created_at | timestamp | not null |

### [next table]
| Column | Type | Constraints |
|---|---|---|
| id | uuid | PK |
| user_id | uuid | FK → users.id |
[Continue for all tables]

## Indexes
- [table(column)]

## Unique Constraints
- [table(column)]
```

**Without this**: WP-05 creates `accounts`, WP-09 creates `user_accounts`. With this: same names everywhere.

---

### 17 · `17_[Project]_API_Contracts.md` — API Shapes

Exact JSON for every endpoint. Backend and frontend both read this.

```markdown
# [Project Name] API Contracts

## POST /api/v1/[endpoint]
Request: { "[field]": "[type]" }
Response 201: { "[field]": "[type]" }
Errors: [status codes]

## GET /api/v1/[endpoint]
Response 200: { "[field]": "[type]" }

[Every endpoint]

## Standard Error Shape
{ "detail": "message", "error_code": "CODE" }
```

**Without this**: Backend returns `user_name`, frontend expects `full_name`. With this: perfect sync.

---

### 18 · `18_[Project]_Testing_Strategy.md` — Test Plan

What to test per WP, tools, minimum counts.

```markdown
# [Project Name] Testing Strategy

## Tools
- Backend: [e.g., "pytest"]
- Frontend: [e.g., "Vitest + React Testing Library"]

## Test Matrix
| WP | Unit | Integration | Frontend |
|---|---|---|---|
| WP-01 | - | - | - |
| WP-02 | - | Auth flow | Protected routes |
| WP-03 | Interface contract | - | - |
[All WPs]

## Minimum Counts
- [Complex WP]: at least [N] tests

## Rule
No tests = NOT complete.
```

---

### 19 · `19_[Project]_Test_Data.md` — Realistic Domain Data

Makes demos look real, not fake.

```markdown
# [Project Name] Test Data Corpus

## [Domain Objects — e.g., "Merchants"]
| Raw Input | Clean Output | Category |
|---|---|---|
| [noisy data] | [clean] | [category] |

## Demo User
| Field | Value |
|---|---|
| Name | [e.g., "Ahmed Al-Rashid"] |
| Email | [e.g., "ahmed@demo.app"] |

## Timeline
- Month 1: [normal activity]
- Month 2: [variation]
- Month 3: [current, upcoming bills]
```

---

### 20 · `20_[Project]_Security.md` — Security Rules

```markdown
# [Project Name] Security

## Authentication
- Hashing: [e.g., "Argon2id"]
- Access token: [e.g., "30 min"]
- Refresh token: [e.g., "7 days, rotation"]

## Encryption
- [What]: [e.g., "AES-256-GCM"]

## Rate Limiting
| Endpoint | Limit |
|---|---|
| Auth | [e.g., "5/min"] |
| API | [e.g., "60/min"] |

## Env Variables
| Variable | Purpose |
|---|---|
| DATABASE_URL | DB connection |
| JWT_SECRET_KEY | Token signing |
```

---

### 21 · `21_[Project]_ADR_Register.md` — Tech Decisions

Why each technology was chosen. Essential for evaluators.

```markdown
# [Project Name] Architectural Decision Records

## ADR-01: [Decision — e.g., "Use FastAPI for Backend"]
- **Status**: Accepted
- **Context**: [Why this decision was needed]
- **Decision**: [What was chosen]
- **Alternatives Considered**:
  - [Alternative 1 — e.g., "Django"] — rejected because [reason]
  - [Alternative 2 — e.g., "Express.js"] — rejected because [reason]
- **Consequences**: [What this means for the project]

## ADR-02: [Decision — e.g., "Use PostgreSQL for Database"]
- **Status**: Accepted
- **Context**: [Why]
- **Decision**: [What]
- **Alternatives Considered**:
  - [Alternative] — rejected because [reason]
- **Consequences**: [What this means]

[Aim for 5-12 ADRs covering all major tech choices]
```

---

### 22 · `22_[Project]_CI_CD.md` — Git + CI + Deploy

```markdown
# [Project Name] CI/CD

## Branches
- main: always deployable
- feat/wp-XX-description: feature branches

## Commits
- feat: new feature
- fix: bug fix
- test: tests

## CI Pipeline
[GitHub Actions or equivalent — what runs on push/PR]

## Deployment
- Frontend: [e.g., "Vercel"]
- Backend: [e.g., "Render"]
- Database: [e.g., "Supabase"]
```

---

# LAYER 3: EXECUTION — "Step-by-Step Prompts"

**Purpose**: Break the project into atomic work packages with clear boundaries. Each has "in scope" and "out of scope" so the agent never builds too much.

**Files in this layer**: 5

---

### 08 · `08_[Project]_WBS.md` — Work Breakdown Structure

All WPs with objectives, tasks, dependencies.

```markdown
# [Project Name] WBS

## WP-01 [Name]
**Objective**: [1 sentence]
**Tasks**: [bulleted list]
**Dependencies**: None

## WP-02 [Name]
**Objective**: [1 sentence]
**Tasks**: [bulleted list]
**Dependencies**: WP-01

[10-30 WPs]
```

---

### 12 · `12_[Project]_Prompt_Templates.md` — Reusable Patterns

```markdown
# [Project Name] Prompt Templates

## Feature Implementation Template
"Implement WP-[XX]. Read [source files]. Build [scope]. Write tests per [testing doc]. Match API contracts from [API doc]. Match schema from [ERD doc]. Do not start WP-[XX+1]."

## Bug Fix Template
"Fix: [description]. Find root cause. Fix only the root cause. Do not refactor unrelated code. Report: cause, fix, verification."

## Review Template
"Review WP-[XX] against [spec], [WBS], and [risk register]. Prioritize: bugs > regressions > testing gaps > architecture drift. If no issues found, say so clearly."
```

---

### 13 · `13_[Project]_Playbook.md` — Operating Guide

```markdown
# [Project Name] Agent Playbook

## Before Starting
1. Ensure PROGRESS.md is up to date
2. Verify previous WP's tests still pass
3. Start a fresh agent session for each WP

## Common Mistakes
- Starting the next WP without being asked → prevented by "out of scope"
- Skipping tests → prevented by done criteria
- Inventing table names → prevented by ERD
- Wrong API shapes → prevented by API contracts

## Tips
- Use /review on complex WPs (see Operational Guidance below)
- If agent runs out of tokens, say "continue WP-XX"
- If something breaks, use /fix before moving on
```

---

### 14 · `14_[Project]_Runbook.md` — MVP Execution (Primary File)

Shared preamble + one prompt per WP.

```markdown
# [Project Name] Runbook

## Shared Preamble
[Copy this, then append the WP prompt]

Source of truth:
- 01_[Project]_Complete_Spec.md
- 04_[Project]_Build_Target.md
- 08_[Project]_WBS.md
- 10_[Project]_Risk_Register.md
- agent-contexts/done-criteria.md

Implementation references:
- 16_[Project]_ERD.md
- 17_[Project]_API_Contracts.md
- 18_[Project]_Testing_Strategy.md
- 19_[Project]_Test_Data.md
- 20_[Project]_Security.md
- 22_[Project]_CI_CD.md

Requirements:
- match schema, match API contracts, write tests
- do not start the next WP
- summarize files, report tests, report blockers

---

## WP-01 [Name]
Target: WP-01 [Name]
In scope:
- [task 1]
- [task 2]
Out of scope:
- do not start [next thing]

## WP-02 [Name]
Target: WP-02 [Name]
In scope:
- [task 1]
Out of scope:
- do not start [next thing]

[Continue for all MVP WPs]
```

**How it works**: Preamble (same every time) + WP prompt (unique). Saves tokens, ensures consistency.

---

### 15 · `15_[Project]_Full_Runbook.md` — Post-MVP Execution

Same pattern, different preamble. Adds "preserve MVP compatibility."

```markdown
# [Project Name] Full Project Runbook

## Shared Preamble (Full Project)

Source of truth:
- 01_[Project]_Complete_Spec.md
- 02_[Project]_Feature_Inventory.md
- 09_[Project]_Full_WBS.md
- agent-contexts/full-context.md
- agent-contexts/done-criteria.md

Implementation references:
- 16-22 (same as MVP)

Requirements:
- preserve MVP compatibility
- extend schema/API if needed, document additions
- write tests, summarize files, report blockers
- update PROGRESS.md

---

## [Post-MVP Package 1]
Target: [Name]
In scope: [tasks]
Out of scope: [boundaries]

[Continue for all post-MVP packages]
```

---

# LAYER 4: CONTEXT — "What the Agent Loads"

**Purpose**: Different work types load different document sets. Done criteria is the quality gate.

**Files in this layer**: 4

---

### `agent-contexts/mvp-context.md`

What to read during MVP work.

```markdown
# MVP Context

Primary: 01, 04, 05, 08, 10
References: 16, 17, 18, 19, 20, 22

Rules:
- stay in MVP scope
- one WP at a time
- match API contracts and schema
- write tests
```

---

### `agent-contexts/full-context.md`

What to read during post-MVP work.

```markdown
# Full Project Context

Use this only for post-MVP expansion work.

Primary source files:
- 01_[Project]_Complete_Spec.md
- 02_[Project]_Feature_Inventory.md
- 09_[Project]_Full_WBS.md

Implementation references:
- 16_[Project]_ERD.md
- 17_[Project]_API_Contracts.md
- 18_[Project]_Testing_Strategy.md
- 20_[Project]_Security.md
- 22_[Project]_CI_CD.md

Rules:
- preserve MVP compatibility
- extend schema/contracts if needed
- write tests
```

---

### `agent-contexts/done-criteria.md`

**The quality gate.** Without this, agents say "done" when code is written. With this, they must prove it works.

```markdown
# Done Criteria

A package is only done if:
- implementation is complete for the scoped package
- code runs without errors
- tests are written per testing strategy
- tests pass
- API contracts match (if endpoints created)
- schema matches ERD (if tables created)
- changed files are summarized
- blockers are reported
```

---

### `agent-contexts/work-package-template.md`

Execution checklist the agent follows.

```markdown
# WP Execution Template

When executing a work package, follow this structure:

1. **Read** PROGRESS.md to see what's done
2. **Read** all source files listed in the preamble
3. **Read** constraint docs (ERD, API, testing, security)
4. **Implement** only what's in scope
5. **Stop** at the out-of-scope boundary
6. **Write tests** per testing strategy
7. **Run tests** and verify they pass
8. **Report**: changed files, test results, blockers
9. **Update** PROGRESS.md
```

---

# LAYER 5: COMMANDS — "Type /1 and It Builds"

**Purpose**: Zero friction. One command = one work package executed.

**Files in this layer**: 3

---

### `AGENTS.md` — Command Map (project root)

AI agents auto-read this file on session start.

```markdown
# [Project Name] Agent Instructions

## Command System
When the user types /1, /2, etc., execute that work package.

### Rules
1. Read ALL source files before starting
1b. Read PROGRESS.md first
2. Implement ONLY the specified WP
3. Match schema from 16_[Project]_ERD.md
4. Match API from 17_[Project]_API_Contracts.md
5. Write tests per 18_[Project]_Testing_Strategy.md
6. Use test data from 19_[Project]_Test_Data.md
7. Follow security from 20_[Project]_Security.md
8. Follow CI/CD from 22_[Project]_CI_CD.md
9. Report: files, tests, blockers
10. Update PROGRESS.md — mark WP as [x]

### /1 — WP-01 [Name]
[In scope + out of scope]

### /2 — WP-02 [Name]
[In scope + out of scope]

[All WPs]

### /review [number]
Review completed WP for bugs and gaps.

### /fix
Fix specific bug. Root cause only.

### /status
Report what's done and what's left.
```

**Copy as `CLAUDE.md` too** for Claude Code compatibility.

---

### `PROGRESS.md` — Build Tracker (project root)

Agent auto-updates after each WP. New sessions read this first.

```markdown
# [Project Name] Progress

## MVP
- [ ] WP-01 [Name]
- [ ] WP-02 [Name]
- [ ] WP-03 [Name]
[All WPs]

**Progress: 0 / [total]**
```

---

# AGENT SYNTAX

| Agent | Where | You Type | It Reads |
|---|---|---|---|
| **Gemini** | VS Code sidebar | `/1` | AGENTS.md |
| **Codex** | VS Code terminal | `WP-01` | AGENTS.md |
| **Claude Code** | Terminal | `/1` | CLAUDE.md |
| **Cursor** | IDE | `/1` | .cursor/rules (copy content) |

**Note**: Codex reserves `/` for system commands. Use `WP-01` syntax instead.

---

# HOW LAYERS CONNECT

When you type `/1`:

```
/1
 ▼
Layer 5 → Finds "/1 — WP-01" with scope + rules
 ▼
Layer 4 → Loads MVP context + done criteria
 ▼
Layer 1 → Reads spec, build target, risks → understands product
 ▼
Layer 2 → Reads ERD (tables) + API (shapes) + tests (requirements)
           + test data (values) + security (rules)
 ▼
Layer 3 → Follows WP-01 prompt, stops at "out of scope"
 ▼
Output  → Code + tests + summary → PROGRESS.md updated
```

*(Note: The layers are processed in 5 → 4 → 1 → 2 → 3 order. You build the architecture from 1 to 5, but the AI executes it top-down starting from the command.)*

---

# OPERATIONAL GUIDANCE

## Error Recovery

| Situation | Do This |
|---|---|
| Agent runs out of tokens | "continue WP-XX" in new session |
| Agent built wrong thing | `/fix [description]` |
| Previous WP code breaks | `/fix` then `/review [number]` |
| Major architecture mistake | Stop → update constraint docs → redo WP |
| Tests fail on old WP | Fix BEFORE moving forward |

**Golden rule**: Never advance if current WP has failing tests.

## WP Weight (Token Planning)

| Weight | Characteristics | Runs Needed | Example |
|---|---|---|---|
| 🟢 Light | Scaffolding, schemas, simple CRUD, config | 1 run | Project setup, DB migrations, simple modules |
| 🟡 Medium | Real business logic, API endpoints, moderate tests | 1 run | Auth, dashboard, budgets, most features |
| 🔴 Heavy | Complex algorithms, many test cases, multiple files | 1-2 runs | Normalization, BNPL detection, full frontend |

**Tip**: If tokens are tight, do heavy WPs in the agent with the most generous limits.

## When to `/review`

Don't review every WP. Review the ones where mistakes are expensive:

| ✅ Review | ❌ Skip Review |
|---|---|
| Complex algorithms (10+ tests) | Simple scaffolding |
| Security hardening WP | Config/schema only |
| Final demo/presentation WP | Light CRUD endpoints |
| Frontend ↔ backend connection | Single-module work |

---

# COMPLETE FILE TREE

```
your-project/
├── .aos/                                ← The AOS methodology vault
│   ├── 01_[Project]_Complete_Spec.md    Layer 1: Master vision
│   ├── 02_[Project]_Feature_Inventory.md
│   ├── 03_[Project]_Scope_Map.md
│   ├── 04_[Project]_Build_Target.md
│   ├── 05_[Project]_Build_Order.md
│   ├── 06_[Project]_System_Parts.md
│   ├── 07_[Project]_Stack_Cost.md
│   ├── 08_[Project]_WBS.md              Layer 3: Work packages
│   ├── 10_[Project]_Risk_Register.md
│   ├── 11_[Project]_Agent_Workflows.md
│   ├── 12_[Project]_Prompt_Templates.md
│   ├── 13_[Project]_Playbook.md
│   ├── 14_[Project]_Runbook.md          Layer 3: MVP execution ★
│   ├── 15_[Project]_Full_Runbook.md
│   ├── 16_[Project]_ERD.md              Layer 2: DB schema
│   ├── 17_[Project]_API_Contracts.md
│   ├── 18_[Project]_Testing_Strategy.md
│   ├── 19_[Project]_Test_Data.md
│   ├── 20_[Project]_Security.md
│   ├── 21_[Project]_ADR_Register.md
│   ├── 22_[Project]_CI_CD.md
│   └── agent-contexts/                  Layer 4: Context blocks
│       ├── mvp-context.md
│       ├── full-context.md
│       ├── done-criteria.md
│       └── work-package-template.md
├── src/                                 ← Your actual app code goes here
├── AGENTS.md                            Layer 5: Commands
├── AI_ONBOARDING.md                     System guide for AI agents
├── CLAUDE.md                            Layer 5: Commands (Claude)
├── PROGRESS.md                          Progress tracker
├── PROMPT_ENGINEERING_BLUEPRINT.md      Master reference manual
└── README.md
```

**30 files. 5 layers. 1 command per work package.**

---

# QUICK START

1. Clone this repository (it comes with the `.aos/` vault pre-built)
2. Replace all `[brackets]` with your project details
3. Start with **Layer 1** — write the spec and features
4. Then **Layer 2** — define ERD, API contracts, tests, security
5. Then **Layer 3** — break into WPs, write the runbook
6. Then **Layer 4** — create context packs and done criteria
7. Then **Layer 5** — create AGENTS.md command map
8. Type **`/1`** and start building
