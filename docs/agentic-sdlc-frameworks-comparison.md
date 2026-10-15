# Agentic & AI-Driven SDLC Frameworks: Landscape Comparison

> **Snapshot Date:** October 2026  
> **Scope:** A comparative analysis of leading **Agentic Software Development Life Cycle (ASDLC)**, **Spec-Driven Development (SDD)**, and **AI-Driven Development Life Cycle (AI-DLC)** frameworks, toolkits, and reference architectures.

---

## 1. Executive Summary & Live GitHub Adoption Matrix

As software engineering transitions from unstructured "vibe coding" to disciplined agentic workflows, a clear split has emerged in the ecosystem between:
1. **Executable Workflow & Skill Frameworks** (which give developers immediate slash commands, subagent orchestrators, steering files, and CLIs),
2. **Enterprise Lifecycle Methodologies** (which restructure team rituals, sprints, and role handoffs around AI), and
3. **Reference Taxonomies & Pattern Languages** (which codify shared architectural vocabulary and mental models).

| Framework / Repo | GitHub Stars | Forks | Category / Layer | Architectural Approach | Primary Strength / Trade-off |
| :--- | :---: | :---: | :--- | :--- | :--- |
| **[Superpowers](https://github.com/obra/superpowers)** (`obra/superpowers`) | **299,284** | 26,735 | **Execution & TDD Skill Framework** | Behavioral skills & strict implementation loop (*Brainstorm $\rightarrow$ Plan $\rightarrow$ Subagent TDD*) | **Strength:** Zero-ceremony install as an agent skill; enforces "no production code before a failing test" and subagent reviews.<br>**Trade-off:** Adds verification latency to every task. |
| **[GitHub Spec Kit](https://github.com/github/spec-kit)** (`github/spec-kit`) | **141,322** | 12,651 | **Spec-Driven CLI Pipeline** | Agent-agnostic `.specify/` constitution & gated pipeline (`/specify` $\rightarrow$ `/plan` $\rightarrow$ `/tasks` $\rightarrow$ `/implement`) | **Strength:** Official GitHub backing; portable across Claude Code, Copilot, Cursor, etc.; low adoption friction.<br>**Trade-off:** Primarily a specification layer rather than an execution engine; can cause markdown bloat on legacy repos. |
| **[OpenSpec](https://github.com/Fission-AI/OpenSpec)** (`Fission-AI/OpenSpec`) | **71,984** | 4,919 | **Brownfield Delta-Spec Toolkit** | Lightweight, change-scoped delta proposals & automated spec archiving | **Strength:** Purpose-built for existing/brownfield codebases; avoids monolithic spec maintenance.<br>**Trade-off:** Less suited for greenfield macro-architecture design. |
| **[GSD (Get Shit Done)](https://github.com/glittercowboy/get-shit-done)** (`open-gsd`) | **~64,500+** | ~5,500+ | **Subagent Execution Engine** | Wave-based parallel task execution, fresh subagent context isolation, and atomic git commits | **Strength:** Prevents context-window rot on long sessions; optimizes for raw shipping velocity and clean git history.<br>**Trade-off:** High token consumption from frequent subagent context hydration. |
| **[BMAD Method](https://github.com/bmad-code-org/BMAD-METHOD)** (`bmad-code-org/BMAD-METHOD`) | **54,155** | 6,088 | **Multi-Persona Agile Org Simulator** | Simulates a 21+ persona software house (PM, Architect, Scrum Master, Developer, QA) | **Strength:** Exhaustive PRD-to-Epic-to-Story traceability for complex greenfield systems.<br>**Trade-off:** Heavy ceremony and file-handoff overhead for small iterative changes. |
| **[Amazon AI-DLC](https://github.com/awslabs/aidlc-workflows)** (`awslabs/aidlc-workflows`) | **5,204** | 948 | **Enterprise AI-Native Lifecycle & Steering** | 3-phase adaptive lifecycle (*Inception $\rightarrow$ Construction $\rightarrow$ Operations*), **Bolts**, and **Mob Elaboration/Construction** | **Strength:** Backed by AWS (native to **Kiro** & harness-neutral across Claude Code/Cursor); adapts depth by task risk and replaces 2-week sprints with hours/days "Bolts."<br>**Trade-off:** Requires cultural buy-in to shift team rituals (Mob sessions). |
| **[ASDLC.io](https://github.com/villetakanen/asdlc-io)** (`villetakanen/asdlc-io`) | **42** | 6 | **Reference Pattern Encyclopedia & MCP** | Pattern language for the "Agentic Software Factory" + live MCP server (`https://asdlc.io/mcp`) | **Strength:** Exceptional conceptual clarity (*Adversarial Code Review*, *Context Gates*, *AGENTS.md* spec, *"Optionality is a feature"*).<br>**Trade-off:** Reference textbook rather than an executable CLI orchestrator. |

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

### 2.4 GSD — Get Shit Done (`glittercowboy/get-shit-done` / `open-gsd`)
* **Repository:** [https://github.com/glittercowboy/get-shit-done](https://github.com/glittercowboy/get-shit-done)
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

---

## 3. Architectural Positioning Map

Each framework occupies a distinct layer of the Agentic SDLC stack, which is why many mature engineering organizations **combine** them rather than treating them as mutually exclusive:

```
┌─────────────────────────────────────────────────────────────────────────────┐
│ 1. MENTAL MODELS & PATTERN TAXONOMY (The "Why" & Vocabulary)                │
│    • ASDLC.io (Factory Architecture, Context Gates, Adversarial Review)     │
├─────────────────────────────────────────────────────────────────────────────┤
│ 2. ENTERPRISE LIFECYCLE & ORG OPERATING MODEL (Team Rituals & Cadence)      │
│    • Amazon AI-DLC (Inception/Construction/Ops, Bolts, Mob Elaboration)     │
│    • BMAD Method (21+ Agile Persona Simulation, PRD-to-Story Sharding)      │
├─────────────────────────────────────────────────────────────────────────────┤
│ 3. SPECIFICATION & CHANGE MANAGEMENT LAYER (The Contract)                   │
│    • GitHub Spec Kit (Greenfield & cross-agent .specify/ + constitution.md) │
│    • OpenSpec (Brownfield delta-specs & change proposals)                   │
├─────────────────────────────────────────────────────────────────────────────┤
│ 4. EXECUTION, CONTEXT ISOLATION & TDD ENFORCEMENT (The Engine)              │
│    • Superpowers (Mandatory TDD, Brainstorm -> Plan -> Subagent Review)     │
│    • GSD / Get Shit Done (Wave-based parallel subagents & atomic commits)   │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Common Production Combinations
* **GitHub Spec Kit + GSD:** Use Spec Kit's constitution and specification pipeline to lock down *what* to build, then hand off to GSD's wave-based subagent engine to execute tasks in isolated contexts.
* **OpenSpec + Superpowers:** The pragmatic brownfield stack—use OpenSpec to scope a lightweight delta proposal on an existing repo, and Superpowers to enforce strict test-first implementation and subagent code review.
* **Amazon AI-DLC / BMAD + Superpowers:** Use AI-DLC's *Mob Elaboration* (or BMAD's Architect/PM personas) for upfront system decomposition and enterprise governance, paired with Superpowers as the developer-level TDD guardrail during construction.
