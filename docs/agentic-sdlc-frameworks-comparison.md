# Agentic & AI-Driven SDLC Frameworks: Landscape Comparison

> **Snapshot Date:** October 2026  
> **Scope:** A comparative analysis of leading **Agentic Software Development Life Cycle (ASDLC)**, **Spec-Driven Development (SDD)**, **Brownfield Knowledge Substrates**, and **AI-Driven Development Life Cycle (AI-DLC)** frameworks, toolkits, and reference architectures.  
> **Companion Execution Guide:** For the executive summary of Levels 1–5 (Light/Twilight/Dark Factories) and step-by-step blueprints for Application Modernization, Brownfield Bugfixing, and Greenfield Engineering, see **[The Practical Agentic SDLC Playbook](./practical-agentic-sdlc-playbook.md)**.

---

## 1. Executive Summary & Live GitHub Adoption Matrix

As software engineering transitions from unstructured "vibe coding" to disciplined agentic workflows, five distinct architectural layers have emerged:
1. **Mental Models & Pattern Taxonomy** (levels of autonomy, Light/Twilight/Dark factories, Elephants vs. Goldfish context isolation, and quality gates),
2. **Enterprise Lifecycle & Fleet Methodologies** (adaptive rituals, background fleet agents, and dark-factory pipelines),
3. **Brownfield Truth & System-1 Decision Substrates** (Code Property + Intent graphs, attested git-native knowledge, and calibrated 100ms System-1 decision models),
4. **Specification & Change Management Layer** (greenfield constitutions, task DAGs, and brownfield delta-specs),
5. **Execution Harnesses, Context Isolation & TDD Enforcement** (CLI/SDK state machines, worktree wave runners, Stop hooks, and TDD skills).

| Framework / Repo | GitHub Stars / Scale | Forks | Category / Layer | Architectural Approach | Primary Strength / Trade-off |
| :--- | :---: | :---: | :--- | :--- | :--- |
| **[Superpowers](https://github.com/obra/superpowers)** (`obra/superpowers`) | **299,284** | 26,735 | **Execution & TDD Skill Framework** | Behavioral skills & strict implementation loop (*Brainstorm $\rightarrow$ Plan $\rightarrow$ Subagent TDD*) | **Strength:** Zero-ceremony install as an agent skill; enforces "no production code before a failing test" and subagent reviews.<br>**Trade-off:** Adds verification latency to every task. |
| **[GitHub Spec Kit](https://github.com/github/spec-kit)** (`github/spec-kit`) | **141,322** | 12,651 | **Spec-Driven CLI Pipeline** | Agent-agnostic `.specify/` constitution & gated pipeline (`/specify` $\rightarrow$ `/plan` $\rightarrow$ `/tasks` $\rightarrow$ `/implement`) | **Strength:** Official GitHub backing; portable across Claude Code, Copilot, Cursor, Antigravity; low adoption friction.<br>**Trade-off:** Primarily a specification layer rather than an execution engine; can cause markdown bloat on legacy repos. |
| **[OpenSpec](https://github.com/Fission-AI/OpenSpec)** (`Fission-AI/OpenSpec`) | **71,984** | 4,919 | **Brownfield Delta-Spec Toolkit** | Lightweight, change-scoped delta proposals (`ADDED / MODIFIED / REMOVED`) & automated spec archiving | **Strength:** Purpose-built for existing/brownfield codebases; avoids monolithic spec maintenance.<br>**Trade-off:** Less suited for greenfield macro-architecture design. |
| **[GSD (Get Shit Done)](https://github.com/gsd-build/get-shit-done)** (`gsd-build/get-shit-done`) | **~64,500+** | ~5,500+ | **Subagent Execution Engine** | Wave-based parallel task execution, fresh subagent context isolation, and atomic git commits | **Strength:** Prevents context-window rot on long sessions; optimizes for raw shipping velocity and clean git history.<br>**Trade-off:** High token consumption from frequent subagent context hydration. |
| **[BMAD Method](https://github.com/bmad-code-org/BMAD-METHOD)** (`bmad-code-org/BMAD-METHOD`) | **54,155** | 6,088 | **Multi-Persona Agile Org Simulator** | Simulates a 21+ persona software house (PM, Architect, Scrum Master, Developer, QA) | **Strength:** Exhaustive PRD-to-Epic-to-Story traceability for complex greenfield systems.<br>**Trade-off:** Heavy ceremony and file-handoff overhead; prone to telephone-game drift. |
| **[Amazon AI-DLC v2.0](https://github.com/awslabs/aidlc-workflows)** (`awslabs/aidlc-workflows`) | **5,204** | 948 | **Enterprise AI-Native Lifecycle & CLI Engine** | Deterministic TS/Bun CLI (93 tools, 11 adaptive profiles), **Bolts**, **Mob Elaboration**, and `codekb` brownfield scan | **Strength:** Backed by AWS (native to **Kiro** & harness-neutral); v2.0 replaced specialist chains with *"Small Mob, Broad Agents"* and 6 Brownfield Safeguards.<br>**Trade-off:** Avoid the 33-stage default profile for routine edits—use `bugfix` (9 stages) or `express` (10 stages). |
| **[Spotify Honk & Fleetshift](https://engineering.atspotify.com/2025/11/spotifys-background-coding-agent-part-1)** (Internal Fleet) | **1,500+ PRs / 1,800+ migrations** | — | **Level 4 Fleet Background Agent** | Ephemeral K8s pod agent triggered via Fleetshift campaigns or `@Honk` in Slack; single `verify()` MCP tool + LLM Judge | **Strength:** Solves the "30% semantic tail" where deterministic AST codemods (OpenRewrite) fail; cuts fleet migration time by 60–90%.<br>**Trade-off:** Requires strict tool minimalism and independent LLM-as-a-Judge to prevent test deletion. |
| **[StrongDM Attractor](https://github.com/strongdm/attractor)** (`strongdm/attractor`) | **[Factory Report](https://factory.strongdm.ai/)** | — | **Level 5 "Dark Factory" Engine** | `.dot` graph pipeline orchestrator + NLSpecs + External Holdout Scenarios + Digital Twin Universe (DTU) | **Strength:** Proves Level 5 lights-out engineering (*"no human writes or reviews code"*) is possible with external holdouts and simulated twins.<br>**Trade-off:** High compute cost (~$1k/day/engineer) and legal/provenance barriers for typical brownfield enterprises. |
| **[ASDLC.io](https://github.com/villetakanen/asdlc-io)** (`villetakanen/asdlc-io`) | **42** | 6 | **Reference Pattern Encyclopedia & MCP** | Pattern language for Levels 1–5, Light/Twilight/Dark Factories, Context Gates, Ralph Loop, and `AGENTS.md` spec | **Strength:** Exceptional conceptual clarity and empirical citations (InfiAgent context rotation, ETH Zurich `AGENTS.md` study).<br>**Trade-off:** Reference architecture rather than an executable CLI orchestrator. |
| **[OKF v0.2](https://github.com/GoogleCloudPlatform/knowledge-catalog/blob/main/okf/SPEC.md) + [GraphDB](https://github.com/jjdelorme/graphdb-skill/blob/main/GRAPHDB_OVERVIEW.md) + [Jev](https://typesafe.ai/blog/introducing-system-one-models-and-jev)** | **Google Cloud / TypeSafe AI** | — | **Brownfield Truth & System-1 Decision Stack** | Neo4j CPG+RPG (`graphdb`) + Git-native attested knowledge (`OKF`) + 100ms calibrated `noul`/`choice`/`score` decisions (`Jev`) | **Strength:** Eliminates legacy guesswork: GraphDB maps seams/blast radius, OKF attests SQL/reporting parity, and Jev enforces 100ms calibrated gates.<br>**Trade-off:** Requires upfront graph indexing (`graphdb build-all`) and OKF schema adoption. |

---

## 2. Deep-Dive Comparison by Framework

### 2.1 Superpowers (`obra/superpowers`)
* **Repository:** [https://github.com/obra/superpowers](https://github.com/obra/superpowers)
* **Core Philosophy:** Enforce uncompromising engineering discipline at the implementation layer through composable agent skills and mandatory Test-Driven Development (TDD).
* **How It Works:** Operates directly inside the coding agent's skill/rule system. Before writing code, the agent is forced through a structured sequence: interactive brainstorming/design refinement, granular implementation planning, and subagent-driven execution where **no production code is permitted before a failing test is written and verified**.
* **Why It Leads in Stars (~299k):** Developers can drop it into their existing agent harness immediately without restructuring their project management or adopting enterprise ceremony, seeing an immediate jump in code reliability.

### 2.2 GitHub Spec Kit (`github/spec-kit`)
* **Repository:** [https://github.com/github/spec-kit](https://github.com/github/spec-kit)
* **Core Philosophy:** Stop ad-hoc "vibe coding" by treating structured specifications and a project-wide `constitution.md` as the primary source of truth.
* **How It Works:** Provides a lightweight CLI (`specify`) and slash-command workflow (`/specify` $\rightarrow$ `/clarify` $\rightarrow$ `/plan` $\rightarrow$ `/tasks` $\rightarrow$ `/implement`) that generates a standardized `.specify/` directory.
* **Positioning:** The de facto baseline standard for **Spec-Driven Development (SDD)**. Because it is vendor-neutral and backed by GitHub, it serves as the common entry point for teams standardizing across Copilot, Claude Code, Cursor, and Windsurf.

### 2.3 OpenSpec (`Fission-AI/OpenSpec`)
* **Repository:** [https://github.com/Fission-AI/OpenSpec](https://github.com/Fission-AI/OpenSpec)
* **Core Philosophy:** Spec-Driven Development tailored specifically for **brownfield (existing) codebases** via delta-specs.
* **How It Works:** Rather than attempting to capture an entire legacy repository in a static specification, OpenSpec scopes each change into an isolated proposal folder containing only the delta requirements, design, and task checklist. Once implemented and verified, the delta merges into the living spec and archives itself.
* **Positioning:** The preferred alternative to GitHub Spec Kit for senior engineers working in large, mature production repositories where full-repo spec generation creates too much noise.

### 2.4 GSD — Get Shit Done (`gsd-build/get-shit-done`)
* **Repository:** [https://github.com/gsd-build/get-shit-done](https://github.com/gsd-build/get-shit-done) (formerly `glittercowboy/get-shit-done`)
* **Core Philosophy:** Solve "context rot" (the degradation of LLM reasoning as the context window fills up) through wave-based subagent isolation and atomic commits.
* **How It Works:** Breaks implementation plans into parallelizable waves of atomic tasks. Each task is dispatched to a fresh subagent with a clean context window and results in an atomic git commit, making `git bisect` and rollbacks trivial.
* **Positioning:** The high-velocity execution engine of the ecosystem—frequently paired downstream of Spec Kit or OpenSpec.

### 2.5 BMAD Method (`bmad-code-org/BMAD-METHOD`)
* **Repository:** [https://github.com/bmad-code-org/BMAD-METHOD](https://github.com/bmad-code-org/BMAD-METHOD)
* **Core Philosophy:** *Breakthrough Method for Agile AI-Driven Development*—simulate an entire agile software organization using 21+ specialized AI personas.
* **How It Works:** Orchestrates explicit handoffs between role-specific agents (Analyst, Product Manager, System Architect, Scrum Master, Developer, QA, UX Designer). Context is sharded across detailed PRDs, architecture documents, epics, and story files before code is written.
* **Positioning:** Heavily favored by enterprise architects and teams building large greenfield systems that require exhaustive documentation and audit trails, though often considered too bureaucratic for small bug fixes or rapid iteration.

### 2.6 Amazon's AI-DLC (`awslabs/aidlc-workflows`)
* **Repository:** [https://github.com/awslabs/aidlc-workflows](https://github.com/awslabs/aidlc-workflows)
* **Documentation & Announcements:**
  * [AI-Driven Development Life Cycle (AI-DLC) Method Definition Site](https://awslabs.github.io/aidlc-workflows/)
  * [AWS DevOps Blog: AI-Driven Development Life Cycle — Reimagining Software Engineering](https://aws.amazon.com/blogs/devops/ai-driven-development-life-cycle/)
  * [AWS DevOps Blog: Open-Sourcing Adaptive Workflows for AI-DLC](https://aws.amazon.com/blogs/devops/open-sourcing-adaptive-workflows-for-ai-driven-development-life-cycle-ai-dlc/)
* **Core Philosophy:** Rather than retrofitting AI assistants onto human-paced Agile Scrum, **AI-DLC** reimagines the entire software engineering operating model around AI as a central collaborator that initiates plans, decomposes work, and drafts artifacts while humans govern critical decision gates.
* **Three Adaptive Phases & Rituals:**
  1. **Inception ("What & Why"):** Workspace/brownfield reverse-engineering, requirements elaboration, and decomposing high-level *Intent* into **Units of Work** via synchronous team + AI **"Mob Elaboration"** sessions.
  2. **Construction ("How"):** Per-unit domain modeling, functional/NFR design, and automated code + test generation via **"Mob Construction"**, executed in rapid cycles called **"Bolts"** (measured in hours or days rather than 2-week sprints).
  3. **Operations ("Deploy & Monitor"):** Infrastructure-as-code generation, CI/CD readiness, and telemetry feedback loops.
* **How Amazon AI-DLC Compares to BMAD, Spec Kit, and ASDLC.io:**
  * **vs. BMAD:** Both target enterprise-grade rigor across the full lifecycle. However, whereas **BMAD** simulates an entire Agile team *inside* the AI via 21+ role-playing personas (which can create heavy markdown handoff ceremony), **Amazon AI-DLC** focuses on **adaptive workflow depth** (scaling ceremony up or down based on task complexity/risk) and **human-AI "Mob" rituals** (*Mob Elaboration* and *Mob Construction*) that compress 2-week Scrum sprints into hours-long **Bolts**.
  * **vs. GitHub Spec Kit & Kiro:** AWS baked AI-DLC's spec-driven core (`requirements.md` $\rightarrow$ `design.md` $\rightarrow$ `tasks.md`) directly into its agentic IDE **[Kiro](https://kiro.dev/)**, and open-sourced `awslabs/aidlc-workflows` as a harness-neutral steering package that runs in Claude Code, Cursor, GitHub Copilot, and Kiro.
  * **vs. ASDLC.io:** Amazon's AI-DLC and Ville Takanen's ASDLC.io share nearly identical philosophical DNA (moving from human-artisan craft to an AI-driven industrial operating model with strict human-in-the-loop governance gates). The difference is scale and packaging: AWS delivers AI-DLC as an **executable set of adaptive steering workflows** (`awslabs/aidlc-workflows`, ~5.2k stars) plus enterprise methodology training, whereas `asdlc.io` serves as an **independent pattern encyclopedia**.

### 2.7 ASDLC.io (`villetakanen/asdlc-io`)
* **Website:** [https://asdlc.io/](https://asdlc.io/)
* **Repository:** [https://github.com/villetakanen/asdlc-io](https://github.com/villetakanen/asdlc-io)
* **Core Philosophy:** Document the **"Pattern Language" for the Agentic Software Factory**—moving software engineering from a 50-year artisan craft to an industrial discipline where agents form the architecture of labor and humans govern the system via schemas, `AGENTS.md`, and deterministic verification gates.
* **How It Fares in the Ecosystem:**
  * With **42 GitHub stars**, `asdlc.io` is a boutique reference library rather than a mass-market runtime tool.
  * However, it punches above its weight as a **canonical lexicon and citation source**. Tool authors and researchers frequently cite specific `asdlc.io` pattern definitions—such as **[Adversarial Code Review](https://asdlc.io/patterns/adversarial-code-review/)** (Critic-Builder separation), **[The Ralph Loop](https://asdlc.io/patterns/ralph-loop/)** (continuous autonomous execution loops), **[AGENTS.md Spec](https://asdlc.io/practices/agents-md-spec)**, and **[Context Gates](https://asdlc.io/patterns/context-gates/)**—and it provides a live MCP server (`https://asdlc.io/mcp`) for agents to query those patterns on demand.

### 2.8 Spotify Honk & StrongDM Attractor (Level 4 Fleet & Level 5 Dark Factories)
* **Spotify Honk & Fleetshift:** ([Spotify Engineering Blog Series, Parts 1–4](https://engineering.atspotify.com/2025/11/spotifys-background-coding-agent-part-1))
  * **Core Philosophy:** Combine deterministic AST codemods (OpenRewrite/ErrorProne, which handle ~70% of mechanical fleet upgrades) with ephemeral background coding agents (Claude Code in isolated Kubernetes pods) to solve the **30% semantic tail** across thousands of microservices.
  * **Key Mechanics:** Enforces **Tool Minimalism** (replacing raw git/bash/Maven/Docker CLI access with a single `verify()` MCP tool that returns only concise errors) and an **Independent LLM-as-a-Judge** that blocks PR creation if tests are deleted or scope is exceeded.
* **StrongDM Attractor:** ([https://github.com/strongdm/attractor](https://github.com/strongdm/attractor) | [Factory Report](https://factory.strongdm.ai/))
  * **Core Philosophy:** Reference implementation of a **Level 5 Dark Software Factory** (*"No human writes code. No human reviews code."*).
  * **Key Mechanics:** Orchestrates multi-agent state graphs defined in Graphviz `.dot` files against Markdown `NLSpecs`, verifying outputs exclusively via **External Holdout Scenarios** stored outside the repository and a **Digital Twin Universe (DTU)** that simulates third-party SaaS dependencies (Okta, Jira, Slack).

### 2.9 The Brownfield Truth & System-1 Decision Stack (`GraphDB` + `OKF v0.2` + `System One Jev`)
* **GraphDB Skill (`jjdelorme/graphdb-skill`):** ([GRAPHDB_OVERVIEW.md](https://github.com/jjdelorme/graphdb-skill/blob/main/GRAPHDB_OVERVIEW.md)) Fuses a deterministic Tree-sitter AST Code Property Graph (CPG) in Neo4j with a Gemini 768d semantic **Repository Planning Graph (RPG)** (`graphdb build-all`) to automate Michael Feathers' legacy analysis (`hotspots`, `impact`, `what-if`, `seams`, `semantic-seams`).
* **Open Knowledge Format (`OKF v0.2`):** ([GoogleCloudPlatform/knowledge-catalog](https://github.com/GoogleCloudPlatform/knowledge-catalog/blob/main/okf/SPEC.md)) Git-native Markdown + YAML frontmatter specification featuring `[^id]` line-level provenance footnotes, 3 derived trust tiers (*Unverified*, *Machine-confirmed*, *Human-reviewed*), `stale_after` expiration, and `type: Attested Computation` for zero-LLM SQL/reporting parity verification (`sql_equality.py`).
* **System One Models & Jev (`typesafe.ai`):** ([Introducing System One Models and Jev](https://typesafe.ai/blog/introducing-system-one-models-and-jev)) A non-generative System-1 decision model (`jev-1.14.0`, trained via RLCD) that evaluates dozens of typed primitives (`jev.noul` Bernoulli Yes/No probability, `jev.choice` categorical routing, `jev.score` rubric rating) in a **single 100ms forward pass** across 262k tokens at **$0.042/MTok input and $0 output**.

---

## 3. Architectural Positioning Map

Each framework occupies a distinct layer of the Agentic SDLC stack, which is why mature engineering organizations **combine** them rather than treating them as mutually exclusive:

```
┌─────────────────────────────────────────────────────────────────────────────┐
│ 1. MENTAL MODELS & PATTERN TAXONOMY (The "Why" & Vocabulary)                │
│    • ASDLC.io (Levels 1-5, Light/Twilight/Dark Factories, Ralph Loop)       │
│    • Dave Rensin (Elephants vs. Goldfish & Zero-Context Spec Blind-Spot Check)│
├─────────────────────────────────────────────────────────────────────────────┤
│ 2. ENTERPRISE LIFECYCLE & FLEET OPERATING MODEL (Cadence & Campaigns)       │
│    • Amazon AI-DLC v2.0 (Inception/Construction/Ops, Bolts, 6 Safeguards)   │
│    • Spotify Honk & Fleetshift (70% AST Codemod + 30% Pod Agent + verify()) │
│    • StrongDM Attractor (Level 5 .dot Pipelines + Holdouts + Digital Twins) │
├─────────────────────────────────────────────────────────────────────────────┤
│ 3. BROWNFIELD TRUTH & SYSTEM-1 DECISION SUBSTRATE (External Memory & Gates) │
│    • GraphDB Skill (Neo4j AST CPG + 768d Semantic RPG + Pinch-Point Seams)  │
│    • Open Knowledge Format v0.2 (Provenance Footnotes + Attested SQL)       │
│    • TypeSafe System One Jev (100ms Single-Pass noul/choice/score Gates)    │
├─────────────────────────────────────────────────────────────────────────────┤
│ 4. SPECIFICATION & CHANGE MANAGEMENT LAYER (The Contract)                   │
│    • GitHub Spec Kit (Greenfield & cross-agent .specify/ + constitution.md) │
│    • OpenSpec (Brownfield ADDED/MODIFIED/REMOVED delta-specs)               │
├─────────────────────────────────────────────────────────────────────────────┤
│ 5. EXECUTION HARNESSES, CONTEXT ISOLATION & TDD ENFORCEMENT (The Engine)    │
│    • Google Antigravity CLI (agy) & Python SDK (google-antigravity)         │
│    • Claude Code Dynamic Workflows (.claude/workflows/*.js / ultracode)     │
│    • Superpowers (Mandatory TDD) & GSD (Wave-based worktree subagents)      │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Common Production Combinations
* **Modernization Stack (Level 4 Twilight Factory):** **GraphDB + OKF v0.2 + Jev + Antigravity Python SDK** — Extract legacy structure and SQL contracts into Neo4j and OKF, block builders from reading legacy source code, execute parallel wave builds via the SDK, and verify cutover parity with OKF attesters and 100ms Jev gates.
* **Brownfield Feature / Bugfix Stack (Level 3 Light Factory):** **GraphDB + OpenSpec + Superpowers + Antigravity CLI (`agy`)** — Query blast radius in GraphDB, draft a 1-page OpenSpec delta via `/grill-me` $\rightarrow$ `/plan`, and execute test-first fixes in a worktree using `/boost` or `/goal`.
* **Greenfield Engineering Stack (Level 3 $\rightarrow$ 4):** **Spec Kit / `agy /plan` + External `.holdouts/` + `agy /teamwork-preview`** — Lock domain contracts and hidden holdout scenarios at Gate 0, build Unit 1 (Walking Skeleton) sequentially, and fan out parallel Goldfish workers under `Integrity Mode: development`.

