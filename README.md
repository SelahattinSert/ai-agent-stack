<div align="center">

```
                           █████╗  ██████╗ ███████╗███╗   ██╗████████╗
                          ██╔══██╗██╔════╝ ██╔════╝████╗  ██║╚══██╔══╝
                          ███████║██║  ███╗█████╗  ██╔██╗ ██║   ██║   
                          ██╔══██║██║   ██║██╔══╝  ██║╚██╗██║   ██║   
                          ██║  ██║╚██████╔╝███████╗██║ ╚████║   ██║   
                          ╚═╝  ╚═╝ ╚═════╝ ╚══════╝╚═╝  ╚═══╝   ╚═╝  
                           █████╗ ██████╗ ███████╗███████╗███╗   ██╗ █████╗ ██╗     
                          ██╔══██╗██╔══██╗██╔════╝██╔════╝████╗  ██║██╔══██╗██║     
                          ███████║██████╔╝███████╗█████╗  ██╔██╗ ██║███████║██║     
                          ██╔══██║██╔══██╗╚════██║██╔══╝  ██║╚██╗██║██╔══██║██║     
                          ██║  ██║██║  ██║███████║███████╗██║ ╚████║██║  ██║███████╗
                          ╚═╝  ╚═╝╚═╝  ╚═╝╚══════╝╚══════╝╚═╝  ╚═══╝╚═╝  ╚═╝╚══════╝
```

### The no-fluff, no-filler index of AI agent repos that actually matter.

<br/>

[![Repos](https://img.shields.io/badge/repos_indexed-27-000000?style=for-the-badge&labelColor=111)](.)
[![PRs](https://img.shields.io/badge/PRs-welcome-22c55e?style=for-the-badge&labelColor=111)](.)
[![License](https://img.shields.io/badge/license-MIT-3b82f6?style=for-the-badge&labelColor=111)](LICENSE)
[![Updated](https://img.shields.io/badge/updated-2026-a855f7?style=for-the-badge&labelColor=111)](.)

</div>

## What's in here

Six categories. Twenty-five repos. Zero filler.

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

**Codex Plugin for Claude Code** &nbsp;·&nbsp; *Let your AI's rival review its code*

The premise is beautifully adversarial: OpenAI's Codex, embedded inside Anthropic's Claude Code terminal, auditing whatever Claude just wrote. Two competing labs, one workflow.

- `/codex:review` — ships your current code to OpenAI servers mid-session, results come back without breaking your flow
- `/codex:adversarial-review` — the interesting one. Codex doesn't look for typos. It's asked to find design philosophy failures, race conditions, and hidden assumptions the original author wouldn't catch
- Everything runs async in the background — you keep writing

> **When to use it:** Any codebase you're about to hand off or ship. Having a second model rip into your architecture before a human does is underrated.

<br/>

---

### [`davila7/claude-code-templates`](https://github.com/davila7/claude-code-templates)

**Claude Code Templates** &nbsp;·&nbsp; *npm install for your AI's superpowers*

If Claude Code is the agent, this is the package manager for everything it can connect to. GitHub, AWS, databases, external APIs — installed in one command.

```bash
npx claude-code-templates@latest
```

- Installs MCP (Model Context Protocol) bridges without touching a config file
- Analytics dashboard shows token spend and background activity — accessible from your phone
- Treats service integrations like packages: versioned, swappable, removable

> **When to use it:** The moment you want your AI talking to anything outside the local filesystem.

<br/>

---

### [`BloopAI/vibe-kanban`](https://github.com/BloopAI/vibe-kanban)

**Vibe Kanban** &nbsp;·&nbsp; *Project management where the workers are AI agents*

Jira, except the assignees are LLMs. You open a card, an isolated environment (branch + terminal + dev server) spins up automatically, and the agent works it. No tab-switching, no copy-pasting from terminal to browser.

- The running app appears in the board's built-in browser the moment the agent ships code
- Multi-model: assign one card to Claude, the next to Copilot, another to Cursor — synchronized on the same board
- Full isolation per task — agents can't accidentally step on each other

> **When to use it:** Running more than one AI task in parallel and tired of losing track of what's where.

<br/>

---

### [`garrytan/gstack`](https://github.com/garrytan/gstack)

**Gstack** &nbsp;·&nbsp; *Garry Tan's personal AI product factory, open-sourced*

YC's CEO built this for himself and then published it. The philosophy is baked in from line one: don't start with code, start with the right question.

- `/office-hours` — the AI plays YC mentor. It interrogates your assumptions, kills the bad ideas, and surfaces the actual MVP before a line of code is written
- "Design Shotgun" generates 4–6 fully divergent visual directions via GPT-Image — pick one, it becomes clean HTML
- Headless Chrome QA mode: a hidden browser tab runs automated tests against your live site like a real QA engineer

> **When to use it:** Solo founder or small team trying to compress weeks of product work into days.

<br/>

---

### [`K-Dense-AI/scientific-agent-skills`](https://github.com/K-Dense-AI/scientific-agent-skills)
 
**Scientific Agent Skills** &nbsp;·&nbsp; *135 pre-built skills that transform agents into AI scientists*
 
A modular skill library built on the open Agent Skills standard. Pre-documented integrations to 100+ scientific databases and 70+ Python packages — covering bioinformatics, drug discovery, clinical research, materials science, geospatial analysis, data visualization, and more. Drop in, pick the skills you need, start running complex multi-step scientific workflows immediately.
 
- **135 production-ready skills** organized across 15+ scientific domains with curated examples and best practices
- **100+ unified database access** — PubChem, ChEMBL, UniProt, AlphaFold, KEGG, Reactome, ClinicalTrials.gov, COSMIC, FDA, USPTO, FRED, and dozens more via a single interface
- **Open standard** — works with any agent that supports Agent Skills (Claude Code, Cursor, Codex, Gemini CLI)
- **Actively maintained**: 21.6k stars, 76 releases, continuous updates with new databases and packages

> **When to use it:** Building agents for scientific research, multi-omics analysis, drug discovery, clinical trials, materials science, or any workflow combining specialized databases with scientific Python packages.

<br/>

---

### [`forrestchang/andrej-karpathy-skills`](https://github.com/forrestchang/andrej-karpathy-skills)

**Karpathy-Inspired Claude Code Guidelines** &nbsp;·&nbsp; *Four principles that stop LLMs from making costly mistakes*

A single `CLAUDE.md` file — grounded in Andrej Karpathy's observations on LLM coding pitfalls — that transforms how Claude Code (and Cursor) behaves. Four explicit principles: Think Before Coding, Simplicity First, Surgical Changes, and Goal-Driven Execution. Installs as a Claude Code plugin or as a per-project guideline file.

- **Think Before Coding** — forces the model to surface assumptions, ask for clarification, and present tradeoffs instead of guessing silently
- **Simplicity First** — eliminates the tendency to overcomplicate; no speculative features, abstractions, or premature error handling
- **Surgical Changes** — guarantees only requested code is touched; prevents drive-by refactoring of unrelated code
- **Goal-Driven Execution** — converts vague tasks into verifiable success criteria, letting the model loop independently

> **When to use it:** Every Claude Code or Cursor project where you want fewer unnecessary rewrites, fewer overengineered solutions, and more precise diffs.

<br/>

---

## 🏗️ Agent Frameworks & Architectures

<br/>

### [`msitarzewski/agency-agents`](https://github.com/msitarzewski/agency-agents)

**Agency Agents** &nbsp;·&nbsp; *144 virtual employees. 12 departments. One codebase.*

The insight: "build me a website" is a terrible prompt because it asks a generalist to do specialist work. This framework solves it by giving your AI an org chart.

- Call `@FrontendDeveloper`, `@UXResearcher`, or `@SmartContractAuditor` directly inside Cursor or Claude
- Each agent has a defined personality, explicit success metrics, and a workflow file — not just a system prompt
- Standout roles: **Evidence Collector** (won't accept "it works" without proof), **Whimsy Injector** (micro-interactions and easter eggs only), **China Market SEO Specialist**

> **When to use it:** Complex projects where one AI playing all roles produces mediocre output on every front.

<br/>

---

### [`obra/superpowers`](https://github.com/obra/superpowers)

**Superpowers** &nbsp;·&nbsp; *Forces your AI to slow down and think before it ships*

AI coding agents share two predictable failure modes: they dive straight into implementation, and they produce tangled code nobody can maintain. Superpowers treats both as engineering problems and solves them with process.

- No immediate coding — the agent runs a Socratic session first, gathering requirements before touching a file
- Auto-creates a **Git Worktree** per task, keeping main branch clean regardless of what the agent does
- Enforces strict **TDD**: failing test must exist before any implementation code is written (RED → GREEN → REFACTOR)
- Tasks are time-boxed to 2–5 minutes — small enough that hallucination has nowhere to hide

> **When to use it:** Any project where "vibe coding" has already caused you pain.

<br/>

---

### [`NousResearch/hermes-agent`](https://github.com/NousResearch/hermes-agent)

**Hermes Agent** &nbsp;·&nbsp; *An agent that gets better at its job the longer it runs*

Most agents are stateless amnesiacs. Hermes isn't. Every problem it solves gets analyzed, distilled, and written into a Skill file — a reusable solution the agent pulls from next time the same class of problem appears.

- Self-improving: it builds its own toolbox as it works
- Full conversation memory via SQLite + FTS5 — nothing is forgotten between sessions
- Cron support: wakes up autonomously, checks your logs, sends a Telegram report, goes back to sleep — no human required

> **When to use it:** Long-running, recurring workflows where you want the agent to stop asking the same questions.

<br/>

---

### [`openclaw/openclaw`](https://github.com/openclaw/openclaw)

**OpenClaw** &nbsp;·&nbsp; *Your home server, controlled via WhatsApp*

A personal agent backbone that runs on your own hardware and takes orders from your messaging apps. No cloud dashboard. No subscription. Your infrastructure, your rules.

- Connects to WhatsApp, Telegram, and Discord as command interfaces
- Text "restart the nginx container" from your phone → it happens at home
- Commands execute inside **Docker/SSH sandboxes**, isolated from your main OS
- Voice wake-word support — speak a trigger phrase, it responds

> **When to use it:** Self-hosters and homelab enthusiasts who want an AI that lives where their servers do.

<br/>

---

### [`ComposioHQ/awesome-codex-skills`](https://github.com/ComposioHQ/awesome-codex-skills)

**Awesome Codex Skills** &nbsp;·&nbsp; *The gap between "AI that talks" and "AI that does"*

An archive of workflow templates that give agents hands. Real OAuth into real apps. Not simulated — the agent is actually logged in and clicking on your behalf.

- 1,000+ external app integrations via Composio's auth layer
- Meeting transcript → parsed action items → Notion tasks, automatically
- `brooks-lint`: uses six canonical software engineering books (including *The Mythical Man-Month*) to detect architectural decay in your code

> **When to use it:** Automating multi-app workflows that used to require Zapier plus a lot of manual glue.

<br/>

---

## 📋 Project & Task Management

<br/>

### [`gsd-build/get-shit-done`](https://github.com/gsd-build/get-shit-done)

**Get Shit Done** &nbsp;·&nbsp; *The antidote to context rot*

Context rot is real: long AI conversations degrade. The model forgets what it built, contradicts its earlier decisions, and starts producing soup. GSD treats this as a systems problem.

- Enforces four distinct phases per feature: **Discuss → Plan → Execute → Verify** — each in a fresh, focused session
- `PROJECT.md` and `ROADMAP.md` are updated at every step, giving any future session an accurate picture of current state
- Three separate agents: Researcher, Planner, Executor — the coder only ever sees its small task
- Dedicated Debug agent that reads logs and writes the fix plan itself

> **When to use it:** Projects longer than a few hours where you've already noticed the AI forgetting things it knew earlier.

<br/>

---

### [`mksglu/context-mode`](https://github.com/mksglu/context-mode)

**Context Mode** &nbsp;·&nbsp; *98% less context. 100% of the information.*

Instead of feeding the AI a 315 KB log file and watching the context window evaporate, Context Mode intercepts the request and asks the agent to write code that extracts what it needs. The AI gets a 5.4 KB summary. The token budget survives.

- Intercepts file reads before they hit the context window — returns only computed results
- Persists open files, active tasks, and session state in SQLite across compaction events — the AI never loses the thread
- Works at the MCP layer, so it's compatible with any client that supports Model Context Protocol

> **When to use it:** Any agent workflow involving large files, long logs, or multi-hour sessions.

<br/>

---

## ⚡ Performance & Code Quality

<br/>

### [`addyosmani/web-quality-skills`](https://github.com/addyosmani/web-quality-skills)

**Web Quality Skills** &nbsp;·&nbsp; *150+ Lighthouse rules, taught to your AI*

AI writes code. It doesn't always write *fast, accessible, correct* code. Google Chrome engineer Addy Osmani built this to close that gap — a skill set that makes your assistant reason about web quality the way a performance engineer would.

- Trigger: `/web-quality-audit` or "optimize my site"
- Framework-aware: React, Next.js, Vue, Astro each get tailored recommendations
- Targets **LCP under 2.5s**, enforces JS/CSS performance budgets, applies **WCAG 2.2** accessibility rules to generated code

> **When to use it:** Before any public launch. After any major feature addition that touched rendering.

<br/>

---

### [`thesysdev/openui`](https://github.com/thesysdev/openui)

**OpenUI** &nbsp;·&nbsp; *67% fewer tokens. UI that renders before it's finished.*

The core problem: models generate UI components as verbose JSON, burning tokens on structure instead of content. OpenUI replaces that with a compact custom format and a purpose-built render engine.

- **67% token reduction** on UI generation tasks
- Streaming-first: components appear on screen as the model generates, not after
- Locks the AI to your Design System — no invented components, no style drift

> **When to use it:** Any product with a design system that needs AI-generated UI at scale.

<br/>

---

## 🧠 Learning & Curricula

<br/>

### [`microsoft/generative-ai-for-beginners`](https://github.com/microsoft/generative-ai-for-beginners)

**Generative AI for Beginners** &nbsp;·&nbsp; *21 lessons. No handwaving.*

Written by Microsoft engineers. The difference between this and most AI tutorials is that it teaches you to build real things — not just call an API and print the response.

- Python and TypeScript throughout, real projects in every lesson
- Covers RAG pipelines, LangChain, vector databases by doing, not describing
- Arc: prompt engineering → fine-tuning on your own data → security threat modeling → LLMOps
- Local model deployment on Hugging Face, not just cloud APIs

> **When to use it:** Onboarding engineers into LLM development, or filling your own gaps systematically.

<br/>

---

## 🌐 Established & Popular Projects

> The bedrock. These weren't on the original list, but any serious index of the space has to include them.

<br/>

| Repo | What it is | Stars | Stack |
|------|-----------|-------|-------|
| [**microsoft/autogen**](https://github.com/microsoft/autogen) | Multi-agent framework from Microsoft Research. Agents solve problems by talking to each other — each acts as both producer and critic | `40k+` | Python |
| [**joaomdmoura/crewAI**](https://github.com/joaomdmoura/crewAI) | Define agents as crew members with roles, goals, and tools. Sequential or parallel execution, outputs chain between agents | `25k+` | Python |
| [**langchain-ai/langchain**](https://github.com/langchain-ai/langchain) | The de facto standard. Chains, memory, tool use, vector DB integration — the vocabulary the whole ecosystem speaks | `90k+` | Python / TS |
| [**Significant-Gravitas/AutoGPT**](https://github.com/Significant-Gravitas/AutoGPT) | The one that started it all. Sets its own sub-goals and works toward them with web search, files, and code execution — no human in the loop | `170k+` | Python |
| [**geekan/MetaGPT**](https://github.com/geekan/MetaGPT) | One prompt → a simulated software company. PM → Architect → Engineer → QA agents collaborate to ship actual software | `44k+` | Python |
| [**OpenDevin/OpenDevin**](https://github.com/OpenDevin/OpenDevin) | Open-source Devin. Real terminal, real browser, real editor. Full-stack tasks executed end-to-end | `35k+` | Python |
| [**princeton-nlp/SWE-agent**](https://github.com/princeton-nlp/SWE-agent) | Resolves real GitHub Issues automatically. Top SWE-bench performer. The methodology is fully open | `13k+` | Python |
| [**phidatahq/phidata**](https://github.com/phidatahq/phidata) | Minimal agent framework with built-in memory, knowledge bases, and tool use. RAG assistants in minimal code | `15k+` | Python |
| [**n8n-io/n8n**](https://github.com/n8n-io/n8n) | Self-hosted workflow automation with 400+ integrations and a native AI Agent node. LLM pipelines without a backend | `45k+` | TypeScript |
| [**run-llama/llama_index**](https://github.com/run-llama/llama_index) | Standard for LLM + your data. Document ingestion, indexing, querying, RAG pipelines — production-grade | `36k+` | Python |
| [**microsoft/semantic-kernel**](https://github.com/microsoft/semantic-kernel) | Enterprise LLM integration from Microsoft. C#, Python, and Java. The serious choice for org-scale deployments | `22k+` | C# / Python |

---

## 🤝 Contributing

The bar for inclusion is quality, not quantity.

**Format:**
```markdown
### [`username/repo-name`](https://github.com/username/repo-name)

**Title** · *one-line hook*

2–3 sentences: what it does, what's clever about it, what problem it actually solves.

- Specific feature that matters
- Another specific feature that matters

> **When to use it:** One honest sentence about the right context.
```

**Criteria:**
- 500+ stars **or** a genuinely novel idea that isn't duplicated elsewhere
- Active development — at least one commit in the last 6 months
- Fits: AI agents, LLM orchestration, or developer tooling built around LLMs

Open a PR. Keep the voice consistent. Don't pad.

---

<div align="center">

<br/>

<br/>

**Star it if it saved you time. PR it if you found something better.**

</div>
