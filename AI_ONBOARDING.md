# AI Onboarding: Agent Operating System (AOS)

Hello! You are an AI assistant operating within the **Agent Operating System (AOS)** using **Constraint-Driven Development (CDD)**.

## How You Must Operate
You are not allowed to hallucinate architectures, database schemas, or API contracts. This repository contains an `.aos/` vault that provides your constraints. 

When the user asks you to build something, you must obey the constraints in the vault.

### The 5 Layers You Must Respect
1. **Layer 1 (Vision)**: `.aos/01` to `.aos/11`. Read these to understand the business logic and project scope.
2. **Layer 2 (Constraints)**: `.aos/16` to `.aos/22`. This is your absolute source of truth for schemas, API shapes, and security. **Do not invent your own table names or endpoints.**
3. **Layer 3 (Execution)**: You execute atomic Work Packages defined in `.aos/14_[Project]_Runbook.md`. You must never exceed the "out of scope" boundary.
4. **Layer 4 (Context)**: You must follow the Done Criteria (`.aos/agent-contexts/done-criteria.md`) before marking a task complete. This includes writing and passing tests.
5. **Layer 5 (Commands)**: `AGENTS.md` (in the root directory) defines the shorthand commands the user will send you (e.g., `/1`).

## Your Execution Flow
When the user types a command like `/1`:
1. Check `AGENTS.md` to see the scope of WP-01.
2. Read the required constraint files in `.aos/`.
3. Write the code and the tests.
4. Report the changed files and any blockers.
5. Update `PROGRESS.md` in the root directory by checking the `[ ]` box.

You are a professional, highly disciplined agent. Acknowledge this document and wait for the user's first command.
