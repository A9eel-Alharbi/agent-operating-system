# Agent Operating System (AOS): The 5-Layer CDD Framework

> Stop writing prompts. Start building an Agent Operating System.

Welcome to the **Agent Operating System (AOS)**. This is a reusable, **5-Layer Execution Architecture** that implements **Constraint-Driven Development (CDD)**—turning any software idea into an airtight, highly disciplined project vault that AI coding agents (like Cursor, Claude, Codex, or Gemini) can execute **flawlessly**.

If you've ever asked an AI to build a feature, only to have it hallucinate database schemas, skip tests, or break existing code, this is for you.

## 🌟 Why This Exists

Most developers treat AI agents like junior devs: they chat with them, give them vague instructions, and hope for the best. This leads to:
- **Scope Creep**: The agent builds too much or guesses what you want.
- **Inconsistencies**: Session 1 creates `users` table; Session 2 queries `user_accounts`.
- **"Done" without Verification**: The agent writes code but skips writing or running tests.
- **Context Loss**: You run out of tokens, start a new chat, and the agent forgets your architecture.

**The Solution? Constraint-Driven Development (CDD).** Don't write a single prompt. Build a 5-layer vault of constraints. 

With this system, you type one command (like `/1`) and the agent reads your exact schema, your exact API contracts, and your exact test requirements before writing a single line of code.

## 🏗️ The 5 Layers

```text
┌─────────────────────────────────────────────┐
│  Layer 5: COMMANDS         ← you type /1    │
│  Layer 4: CONTEXT          ← agent loads    │
│  Layer 3: EXECUTION        ← agent follows  │
│  Layer 2: CONSTRAINTS      ← agent obeys    │
│  Layer 1: VISION           ← agent learns   │
│  PROGRESS TRACKER          ← auto-updated   │
└─────────────────────────────────────────────┘
```

1. **Layer 1: Vision (What & Why)**: Teaches the agent about the product, users, features, and MVP boundaries. 
2. **Layer 2: Constraints (The Rules)**: Hard-coded database ERD, API JSON contracts, testing strategies, and security rules. **The agent cannot improvise.**
3. **Layer 3: Execution (Step-by-Step)**: Breaks the project into 10-30 atomic work packages with strict "in scope" and "out of scope" boundaries.
4. **Layer 4: Context (What to Load)**: Tells the agent exactly which docs to read depending on the task. Includes the **Done Criteria** quality gate.
5. **Layer 5: Commands (Frictionless)**: Maps your execution steps to simple commands.

## 🚀 How to Use This Scaffold

This repository is already pre-built with the 29 files you need.

1. **Clone this repository** (or click "Use this template" if viewing on GitHub).
2. Look at the files: you will see `01_[Project]_Complete_Spec.md`, `16_[Project]_ERD.md`, etc.
3. Open each file and replace every `[bracket]` with your project's specific details.
4. Work through Layer 1, then Layer 2, until you reach Layer 5.
5. Open your IDE with an AI agent (Cursor, Claude Code, Gemini, etc).
6. Type `/1`. Watch the magic happen.

*(Note: The full `PROMPT_ENGINEERING_BLUEPRINT.md` is included in the root folder as a master reference manual.)*

## 💡 Example Execution Flow

When you type `/7` into your agent, here is what happens under the hood:

1. **Layer 5**: Agent reads `AGENTS.md`, finds the command, and sees the scope.
2. **Layer 4**: Agent loads the specific context pack and the "Done Criteria" checklist.
3. **Layer 1**: Agent reads your spec to understand the business logic.
4. **Layer 2**: Agent reads `16_ERD.md` to get exact table names. It reads `17_API_Contracts.md` to get exact JSON return shapes. It reads `18_Testing_Strategy.md` to know it needs to write 15 unit tests.
5. **Layer 3**: Agent follows the specific prompt in `14_Runbook.md` and stops exactly at the "out of scope" boundary.
6. **Result**: Agent writes the code, runs the tests, summarizes the changes, and automatically updates `PROGRESS.md`.

## 🤝 Contribution

This is an open-source template. Have ideas on how to improve the constraints or the agent syntax? Open an issue or submit a PR!
