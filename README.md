<div align="center">

```
                        █████╗ ██╗       █████╗  ██████╗ ███████╗███╗   ██╗████████╗
                        ██╔══██╗██║      ██╔══██╗██╔════╝ ██╔════╝████╗  ██║╚══██╔══╝
                        ███████║██║      ███████║██║  ███╗█████╗  ██╔██╗ ██║   ██║   
                        ██╔══██║██║      ██╔══██║██║   ██║██╔══╝  ██║╚██╗██║   ██║   
                        ██║  ██║██║      ██║  ██║╚██████╔╝███████╗██║ ╚████║   ██║   
                        ╚═╝  ╚═╝╚═╝      ╚═╝  ╚═╝ ╚═════╝ ╚══════╝╚═╝  ╚═══╝   ╚═╝   

                       ███████╗████████╗ █████╗  ██████╗██╗  ██╗
                       ██╔════╝╚══██╔══╝██╔══██╗██╔════╝██║ ██╔╝
                       ███████╗   ██║   ███████║██║     █████╔╝ 
                       ╚════██║   ██║   ██╔══██║██║     ██╔═██╗ 
                       ███████║   ██║   ██║  ██║╚██████╗██║  ██╗
                       ╚══════╝   ╚═╝   ╚═╝  ╚═╝ ╚═════╝╚═╝  ╚═╝
```

### Curated open-source AI agent projects, frameworks, and developer tools.

`Coding Agents` &nbsp;·&nbsp; `Multi-Agent Systems` &nbsp;·&nbsp; `MCP Tooling` &nbsp;·&nbsp; `Orchestration` &nbsp;·&nbsp; `Autonomous Workflows`

<br/>

[![Repos](https://img.shields.io/badge/repos_indexed-27-000000?style=for-the-badge&labelColor=111)](.)
[![PRs](https://img.shields.io/badge/PRs-welcome-22c55e?style=for-the-badge&labelColor=111)](.)
[![License](https://img.shields.io/badge/license-MIT-3b82f6?style=for-the-badge&labelColor=111)](LICENSE)
[![Updated](https://img.shields.io/badge/updated-2026-a855f7?style=for-the-badge&labelColor=111)](.)

</div>

---

## Index

A categorized index of AI agent frameworks, developer tools, orchestration systems, and learning resources. Each entry is selected for architectural relevance, active maintenance, and practical utility — not star count alone.

| | Category | Repos |
|--|--|--|
| 🛠️ | [Developer Tools & Skill Libraries](#️-developer-tools--skill-libraries) | 6 |
| 🏗️ | [Agent Frameworks & Architectures](#️-agent-frameworks--architectures) | 5 |
| 📋 | [Project & Task Management](#-project--task-management) | 2 |
| ⚡ | [Performance & Code Quality](#-performance--code-quality) | 2 |
| 🧠 | [Learning & Curricula](#-learning--curricula) | 1 |
| 🌐 | [Established & Popular Projects](#-established--popular-projects) | 11 |

---

## 🛠️ Developer Tools & Skill Libraries

<br/>

### [`openai/codex-plugin-cc`](https://github.com/openai/codex-plugin-cc)

**Codex Plugin for Claude Code** &nbsp;·&nbsp; *Uses Codex as a secondary reviewer inside Claude Code workflows*

Embeds OpenAI's Codex model directly into Anthropic's Claude Code terminal as a code review layer. The two models operate on different training assumptions, which makes Codex a useful auditor for code Claude produced.

- `/codex:review` — sends current code to OpenAI servers mid-session and returns results without interrupting the workflow
- `/codex:adversarial-review` — instructs Codex to identify design-level issues: race conditions, hidden assumptions, and architectural gaps rather than surface errors
- Reviews run asynchronously — Claude remains available during the process

> **When to use it:** Before handing off or shipping a codebase. Cross-model review catches blind spots that same-model review often misses.

<br/>

---

### [`davila7/claude-code-templates`](https://github.com/davila7/claude-code-templates)

**Claude Code Templates** &nbsp;·&nbsp; *A package manager for Claude Code integrations*

Installs MCP (Model Context Protocol) bridges to external services — GitHub, AWS, databases, APIs — through a single CLI command. Treats service integrations as versioned, swappable packages rather than manual config.

```bash
npx claude-code-templates@latest
```

- No manual config file editing — bridges install and register automatically
- Built-in analytics dashboard tracks token usage and background agent activity, accessible from a browser
- Packages are versioned and removable, same as npm dependencies

> **When to use it:** When your Claude Code workflow needs to interact with services outside the local filesystem.

<br/>

---

### [`BloopAI/vibe-kanban`](https://github.com/BloopAI/vibe-kanban)

**Vibe Kanban** &nbsp;·&nbsp; *A Kanban board where tasks are assigned to AI agents*

A visual project management interface designed for multi-agent workflows. Each task card spawns an isolated environment — dedicated git branch, terminal, and dev server — so agents work without interfering with each other.

- The running application appears in the board's built-in browser automatically when the agent completes its task
- Supports multi-model assignment: different cards can run on Claude, Copilot, or Cursor simultaneously, synchronized on the same board
- Full environment isolation per task prevents state conflicts between parallel agents

> **When to use it:** Managing multiple parallel AI tasks where terminal-based tracking becomes impractical.

<br/>

---

### [`garrytan/gstack`](https://github.com/garrytan/gstack)

**Gstack** &nbsp;·&nbsp; *Garry Tan's personal AI product development setup, open-sourced*

A product development workflow built around YC's methodology — problem validation before implementation. Published by Garry Tan as the setup he uses for rapid product iteration.

- `/office-hours` runs a structured question sequence to challenge assumptions and define the minimum viable scope before any code is written
- "Design Shotgun" generates 4–6 distinct visual directions via GPT-Image; the selected direction is converted to HTML
- Headless Chrome QA mode runs automated tests against the live site in a background browser tab

> **When to use it:** Solo founders or small teams who want to validate product direction before investing in implementation.

<br/>

---

### [`K-Dense-AI/scientific-agent-skills`](https://github.com/K-Dense-AI/scientific-agent-skills)

**Scientific Agent Skills** &nbsp;·&nbsp; *135 pre-built skills for scientific research workflows*

A modular skill library built on the open Agent Skills standard. Covers bioinformatics, drug discovery, clinical research, materials science, geospatial analysis, and data visualization — with pre-documented integrations for 100+ scientific databases and 70+ Python packages.

- **135 production-ready skills** across 15+ scientific domains with curated examples and best practices
- **Unified database access** — PubChem, ChEMBL, UniProt, AlphaFold, KEGG, ClinicalTrials.gov, FDA, USPTO, and 90+ more through a single interface
- **Open standard** — compatible with Claude Code, Cursor, Codex, Gemini CLI, and any Agent Skills-compatible agent
- 21.6k stars, 76 releases, actively maintained

> **When to use it:** Building agents for scientific research, multi-omics analysis, drug discovery, or any workflow that combines specialized databases with scientific Python packages.

<br/>

---

### [`forrestchang/andrej-karpathy-skills`](https://github.com/forrestchang/andrej-karpathy-skills)

**Karpathy-Inspired Claude Code Guidelines** &nbsp;·&nbsp; *Four coding principles derived from Andrej Karpathy's observations on LLM behavior*

A single `CLAUDE.md` file that addresses four well-documented failure modes in LLM-assisted coding: silent assumption-making, over-engineering, unintended side-effect edits, and vague task definitions. Installs as a Claude Code plugin or as a per-project guideline file.

- **Think Before Coding** — surfaces assumptions explicitly and requires clarification before implementation begins
- **Simplicity First** — prohibits speculative features, unnecessary abstractions, and unrequested error handling
- **Surgical Changes** — restricts edits to code directly related to the user's request; prevents drive-by refactoring
- **Goal-Driven Execution** — converts imperative instructions into verifiable success criteria, enabling autonomous loops

> **When to use it:** Any Claude Code or Cursor project where imprecise diffs, over-engineered output, or unintended edits have been a recurring issue.

<br/>

---

## 🏗️ Agent Frameworks & Architectures

<br/>

### [`msitarzewski/agency-agents`](https://github.com/msitarzewski/agency-agents)

**Agency Agents** &nbsp;·&nbsp; *144 role-specific agents organized across 12 departments*

A framework that replaces the "do everything" general agent model with a simulated org chart. Each agent has a defined role, success metrics, and workflow file — specialists are called explicitly rather than relying on a single model to context-switch.

- Call `@FrontendDeveloper`, `@UXResearcher`, or `@SmartContractAuditor` directly inside Cursor or Claude
- Each agent has a defined personality, explicit success metrics, and a workflow file — not just a system prompt
- Notable roles: **Evidence Collector** (requires verifiable proof of task completion), **Whimsy Injector** (micro-interactions only), **China Market SEO Specialist**, **Smart Contract Auditor**

> **When to use it:** Projects where generalist output quality degrades because the scope spans multiple distinct disciplines.

<br/>

---

### [`obra/superpowers`](https://github.com/obra/superpowers)

**Superpowers** &nbsp;·&nbsp; *Enforces structured process before and during AI coding tasks*

Addresses two common failure modes in AI-assisted coding: premature implementation without sufficient requirements gathering, and accumulated complexity from uncontrolled scope. Applies engineering process to constrain both.

- Requires a Socratic requirements session before any implementation begins
- Creates a **Git Worktree** per task automatically, isolating changes from the main branch
- Enforces **TDD**: a failing test must exist before implementation code is written (RED → GREEN → REFACTOR)
- Breaks tasks into 2–5 minute chunks to keep scope bounded and outputs verifiable

> **When to use it:** Projects where premature implementation or growing complexity has already caused rework.

<br/>

---

### [`NousResearch/hermes-agent`](https://github.com/NousResearch/hermes-agent)

**Hermes Agent** &nbsp;·&nbsp; *An agent that builds a reusable skill library from its own past solutions*

Unlike stateless agents that treat each session independently, Hermes analyzes its completed work and writes structured Skill files — so solutions to recurring problem classes become faster and more reliable over time.

- After solving a problem, Hermes distills the approach into a reusable Skill file for future sessions
- Full conversation memory via SQLite + FTS5 full-text search — state persists across sessions
- Cron support enables autonomous scheduled operation: log checks, report generation via Telegram, and scheduled hibernation without manual intervention

> **When to use it:** Long-running or recurring workflows where agent performance should improve with repeated use.

<br/>

---

### [`openclaw/openclaw`](https://github.com/openclaw/openclaw)

**OpenClaw** &nbsp;·&nbsp; *A self-hosted personal agent controlled through messaging apps*

Runs entirely on local hardware with no cloud dependency. Acts as a command gateway: incoming messages from WhatsApp, Telegram, or Discord are parsed as instructions and executed in sandboxed environments on the host machine.

- Accepts commands from WhatsApp, Telegram, and Discord as control interfaces
- All commands execute inside Docker/SSH sandboxes, isolated from the main OS
- Voice wake-word detection enables hands-free activation without a UI

> **When to use it:** Self-hosted setups where infrastructure needs to be controlled remotely without relying on a cloud provider.

<br/>

---

### [`ComposioHQ/awesome-codex-skills`](https://github.com/ComposioHQ/awesome-codex-skills)

**Awesome Codex Skills** &nbsp;·&nbsp; *Workflow templates for agents that act on external services*

A collection of agent workflow templates built on Composio's authentication infrastructure. Agents authenticate with external apps via OAuth and perform real actions — reading, writing, creating — rather than generating instructions for humans to execute.

- 1,000+ external app integrations with managed OAuth via Composio
- Example workflow: reads a meeting transcript, identifies action items per owner, creates tasks in Notion
- `brooks-lint` — detects architectural decay in codebases using principles from six foundational software engineering texts, including *The Mythical Man-Month*

> **When to use it:** Automating multi-step workflows across external services that currently require manual coordination or brittle Zapier setups.

<br/>

---

## 📋 Project & Task Management

<br/>

### [`gsd-build/get-shit-done`](https://github.com/gsd-build/get-shit-done)

**Get Shit Done** &nbsp;·&nbsp; *A structured workflow to prevent context degradation in long AI sessions*

Long AI conversations degrade: the model loses track of earlier decisions, contradicts prior output, and produces increasingly inconsistent results. GSD addresses this by splitting work into bounded sessions with persistent state files.

- Enforces four distinct phases per feature: **Discuss → Plan → Execute → Verify** — each in a separate, focused session
- `PROJECT.md` and `ROADMAP.md` are updated at each phase boundary, giving any new session accurate current-state context
- Separates Researcher, Planner, and Executor roles — the coding agent only receives the specific task it needs to complete
- A dedicated Debug agent reads logs independently and produces a structured fix plan

> **When to use it:** Multi-session projects where context loss has started affecting output consistency.

<br/>

---

### [`mksglu/context-mode`](https://github.com/mksglu/context-mode)

**Context Mode** &nbsp;·&nbsp; *Reduces context window consumption by 98% on large file operations*

When an agent attempts to read a large file directly, Context Mode intercepts the request and asks the agent to write code that extracts the relevant information instead. Only the computed result enters the context window.

- Intercepts file reads at the MCP layer before they reach the context window — returns only extracted output
- Demonstrated compression: 315 KB raw input → 5.4 KB result (98% reduction)
- Persists session state — open files, active tasks, progress — in SQLite across compaction events, preventing context loss on long sessions

> **When to use it:** Agent workflows that process large files, log archives, or any session expected to run for multiple hours.

<br/>

---

## ⚡ Performance & Code Quality

<br/>

### [`addyosmani/web-quality-skills`](https://github.com/addyosmani/web-quality-skills)

**Web Quality Skills** &nbsp;·&nbsp; *150+ Lighthouse rules applied to AI-generated web code*

Built by Google Chrome engineer Addy Osmani. Gives AI coding assistants a structured understanding of web performance, accessibility, and quality standards — so generated code is evaluated against the same criteria as a Lighthouse audit.

- Triggered by `/web-quality-audit` or natural language requests like "optimize my site"
- Framework-specific guidance for React, Next.js, Vue, and Astro
- Targets **LCP under 2.5s**, enforces JS/CSS performance budgets, and applies **WCAG 2.2** accessibility rules to generated output

> **When to use it:** Before any public launch, or after feature additions that affect rendering or accessibility.

<br/>

---

### [`thesysdev/openui`](https://github.com/thesysdev/openui)

**OpenUI** &nbsp;·&nbsp; *A compact format and render engine for AI-generated UI components*

Standard models generate UI code inside verbose JSON structures, spending tokens on formatting overhead rather than content. OpenUI replaces this with a purpose-built compact format and matching renderer.

- **67% token reduction** on UI generation compared to JSON-wrapped HTML/React output
- Streaming-first: components render incrementally as the model generates, rather than waiting for completion
- Constrains output to a defined Design System — prevents component invention and style inconsistency

> **When to use it:** Products with an established design system that need AI-generated UI at scale without token overhead.

<br/>

---

## 🧠 Learning & Curricula

<br/>

### [`microsoft/generative-ai-for-beginners`](https://github.com/microsoft/generative-ai-for-beginners)

**Generative AI for Beginners** &nbsp;·&nbsp; *21-lesson engineering curriculum for building with LLMs*

A structured curriculum written by Microsoft engineers covering the full development arc of generative AI applications — from prompt engineering to production deployment. Project-based throughout; every lesson produces working code.

- Python and TypeScript in every lesson, applied to real projects rather than isolated examples
- Covers RAG pipelines, LangChain, and vector databases through implementation, not just description
- Full arc: prompt engineering → fine-tuning → security threat modeling → LLMOps
- Includes local model deployment via Hugging Face, not only cloud API usage

> **When to use it:** Onboarding engineers to LLM application development, or building a systematic foundation before working on agent infrastructure.

<br/>

---

## 🌐 Established & Popular Projects

> Foundational projects that define the AI agent and orchestration ecosystem. Included as reference — most engineers working in this space will encounter these regardless of what else they use.

<br/>

| Repo | Focus | What it does | Stars |
|------|-------|-------------|-------|
| [**microsoft/autogen**](https://github.com/microsoft/autogen) | Multi-agent orchestration | Agents collaborate by conversing with each other — each acts as both producer and critic | `40k+` |
| [**joaomdmoura/crewAI**](https://github.com/joaomdmoura/crewAI) | Role-based agents | Define agents with explicit roles, goals, and tools; outputs chain between agents sequentially or in parallel | `25k+` |
| [**langchain-ai/langchain**](https://github.com/langchain-ai/langchain) | LLM infrastructure | The standard abstraction layer for chaining, memory, tool use, and vector DB integration | `90k+` |
| [**Significant-Gravitas/AutoGPT**](https://github.com/Significant-Gravitas/AutoGPT) | Autonomous agents | Sets its own sub-goals and executes them using web search, files, and code — without human input per step | `170k+` |
| [**geekan/MetaGPT**](https://github.com/geekan/MetaGPT) | Software company simulation | One prompt triggers a PM → Architect → Engineer → QA pipeline that produces working software | `44k+` |
| [**OpenDevin/OpenDevin**](https://github.com/OpenDevin/OpenDevin) | Autonomous dev agent | Open-source Devin alternative with a real terminal, browser, and editor for end-to-end task execution | `35k+` |
| [**princeton-nlp/SWE-agent**](https://github.com/princeton-nlp/SWE-agent) | Issue resolution | Resolves real GitHub Issues automatically; top performer on the SWE-bench benchmark | `13k+` |
| [**phidatahq/phidata**](https://github.com/phidatahq/phidata) | Agent framework | Minimal framework with built-in memory, knowledge bases, and tool use for RAG-powered assistants | `15k+` |
| [**n8n-io/n8n**](https://github.com/n8n-io/n8n) | Workflow automation | Self-hosted automation platform with 400+ integrations and a native AI Agent node | `45k+` |
| [**run-llama/llama_index**](https://github.com/run-llama/llama_index) | Data + LLM layer | Standard tooling for document ingestion, indexing, and production RAG pipeline construction | `36k+` |
| [**microsoft/semantic-kernel**](https://github.com/microsoft/semantic-kernel) | Enterprise LLM integration | C#, Python, and Java SDK for embedding AI capabilities into enterprise-scale applications | `22k+` |

---

## 🤝 Contributing

**Format:**

```markdown
### [`username/repo-name`](https://github.com/username/repo-name)

**Title** · *one-line description of what it does*

2–3 sentences explaining the problem it solves and why the approach is worth noting.

- Specific capability that matters
- Another specific capability that matters

> **When to use it:** One honest sentence about the right context.
```

**Criteria:**
- 500+ stars **or** a genuinely novel approach not duplicated elsewhere
- Active development — at least one commit in the last 6 months
- Relevant to AI agents, LLM orchestration, or developer tooling built around LLMs

Open a PR. Match the existing tone. Describe what the repo does, not how impressive it is.

---

<div align="center">

**Star it if it saved you time. PR it if you found something better.**

</div>
