## Abraham Robison

**Applied AI engineer with deep finance roots.** I design and ship agentic, full-stack AI
systems — autonomous, judge-gated, cost-aware — and ground them in real financial work:
treasury, forecasting, portfolio, risk, and valuation.

Currently an **Applied AI Scientist (contract) at FEV**, building AI and data tooling for
private-asset valuation. Previously **Senior Quantitative Analyst, Treasury at Google** and
**Senior Quantitative Research Analyst at Russell Investments**, shipping applied-ML and
forecasting systems into large-scale finance operations.

### What I build

- **Agentic systems & LLM orchestration** — autonomous, judge-gated pipelines with cost ledgers and audit trails
- **Applied ML & forecasting** — self-improving models, closed-loop learning, decision systems
- **End to end** — research → models → data pipelines → UI → production
- **Cost-aware AI** — local-model routing with fail-safe fallback; distillation and efficiency

### Latest release: Skill Mesh v2

[Skill Mesh v2.0.0](https://github.com/aberson/skill-mesh/releases/tag/v2.0.0) is out:
57 skills for Claude Code, with 54 also packaged for GitHub Copilot and OpenAI Codex.
Shared behavior contracts connect planning, implementation, independent review, and
session continuity. Separate utility projects support retrieval, evidence, and validation.

[Explore all 57 workflows](https://github.com/aberson/skill-mesh/tree/main/docs/workflows)
· [Skill reference](https://github.com/aberson/skill-mesh/blob/main/documentation/skill-reference.md)
· [Install v2](https://github.com/aberson/skill-mesh#install-or-upgrade)
· [Portfolio case study](https://aberson.github.io/work/skill-mesh/)

### Selected projects

- **[Skill Mesh v2](https://github.com/aberson/skill-mesh)** — a released catalog of 57 agent skills for planning, building, reviewing, and shipping software. Shared contracts and host adapters package 54 portable skills for Claude Code, GitHub Copilot, and OpenAI Codex; three remain Claude-native. Required independent-review capabilities stay explicit. *Markdown contracts; Python + PowerShell tooling.*
- **[Alpha4Gate](https://github.com/aberson/Alpha4Gate)** — a self-improving StarCraft II bot: a Claude-advised loop that reads its own telemetry and auto-commits fixes (gated by tests + validation games), plus a self-play arena with an Elo ladder. *Python, PyTorch/SB3, FastAPI, React.*
- **[toybox](https://github.com/aberson/toybox)** — a local-first home AI: passive listening (VAD + Whisper) → intent detection → a branching activity engine → parent-approval UI → a kids' PWA with generated sprites and on-device TTS. Runs fully offline. *Python/FastAPI + React/TypeScript.*
- **[pta_finance](https://github.com/aberson/pta_finance)** — a production finance toolkit for small nonprofits: Google Sheets as system-of-record, canonical ledger normalization, budget-vs-actual analytics, automated monthly reports. *Python, `mypy --strict`, GitHub Actions.*
- **[measure-twice](https://github.com/aberson/measure-twice)** — a local benchmarking toolkit for deciding which model should do which job with measurements instead of assertions: author suites, sweep them across a model roster, score through calibrated instruments, and keep an evidence ledger that ties every routing claim to the run behind it — or honestly marks it `ASSERTED`. *Python, stdlib-only core, `mypy --strict`.*
- **[citation-needed](https://github.com/aberson/citation-needed)** — gives every design choice buried in an LLM-facing file (skills, rules, `CLAUDE.md`, plans) a citation trail — research literature first, workspace provenance second — plus an anchored 0–100 score and a corpus that compounds across reviews. Reviews are read-only toward their targets; the CLI never calls an LLM. *Python, SQLite/FTS5.*
- **Pipeline utilities** — separate local-first tools for inspection and coordination: [tripwire](https://github.com/aberson/tripwire), [changed-check](https://github.com/aberson/changed-check), [heads-up](https://github.com/aberson/heads-up), [paper-trail](https://github.com/aberson/paper-trail), [find-again](https://github.com/aberson/find-again), [same-page](https://github.com/aberson/same-page), and [mesh-lens](https://github.com/aberson/mesh-lens). The [v2 integration table](https://github.com/aberson/skill-mesh#how-utility-projects-are-used) distinguishes actual callers, optional helpers, and deferred hookups; not every utility is installed or wired by the skill release. *Python.*
- **[shake_spear](https://github.com/aberson/shake_spear)** — a markdown-first creative-writing workshop: a stdlib-only `ss` CLI that scaffolds and manages independent story projects, with AI as coach and continuity assistant. The product is plain-markdown files on disk — no web app, no database, no API. *Python.*
- **[applied_learning](https://github.com/aberson/applied_learning)** — hands-on ML ramps (diffusion, knowledge distillation) with runnable notebooks; distillation tied to real cost reduction. *Jupyter.*
- **[walkies](https://github.com/aberson/walkies)** — a native dog-walking decision app fusing weather, air quality, and pavement temperature into a go/no-go verdict. *React Native, TypeScript.*

### Writing

- **[What My StarCraft II Bot Taught Me About Contract Drift](https://medium.com/@aberobison/what-my-starcraft-ii-bot-taught-me-about-contract-drift-9e3b368152cf)** — a postmortem from Alpha4Gate: the bot's trained network won an evaluation game against the built-in Easy AI, and its own evaluator logged the win as a crash. The bug lived in the handoff between two correct components (a changed ID shape); the lesson is to test the round trip end to end. *Medium, Oct 2026.*
- **[A StarCraft II bot, now with more Jev](https://medium.com/@aberobison/my-starcraft-ii-bot-now-with-more-jev-5581c1ff03d2)** — a proof of concept: Typesafe's hosted Jev decision model answered in a median ~0.53 s, versus a median ~6.2 s for my April 2026 Claude advisor run as a CLI subprocess — fast enough to make strategic calls in a live real-time game while a local decision graph (~300 nodes, nine lanes) issues every command. *Medium, Oct 2026.*

### How I build with AI

I treat agent work as a **pipeline with quality gates**: plan one step at a time, build each in
isolation, review with independent adversarial passes, and only then ship. Much of it runs as a
provider-neutral collection of agent skills I use daily — open-sourced as skill-mesh.

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/core-pipeline-dark.svg">
  <img alt="Plan, review, redline and wrap; sync issues and save a durable handoff; build-phase runs each build-step with its own checks, selected review lane and landing gates; acceptance and repository publishing follow." src="assets/core-pipeline-light.svg">
</picture>

Several skills use multi-agent fan-out — parallel reviewers, judge panels, and generate-then-grade
loops — so a change clears independent scrutiny before it lands.

→ **[github.com/aberson/skill-mesh](https://github.com/aberson/skill-mesh)** — the full
collection, now released as v2 with installation guidance and source-linked diagrams
generated through [Show Your Work](https://github.com/aberson/show-your-work).
Portable skills share behavior contracts across three host adapters; native capabilities
and external dependencies remain explicit. [Drift Ranger](https://github.com/aberson/drift-ranger)
tracks intended outcomes, Find Again supports prior-work retrieval, and Citation Needed
owns evidence records for the citation workflows. These tools support the gates;
they do not replace independent review.

### GitHub activity

![Abraham Robison — top languages and recent GitHub activity](./github-metrics.svg)

### Background

10+ years across Google Treasury, Russell Investments, and BlackRock. MA Economics + Graduate
Certificate in Computational Finance (University of Washington); BS Computer Science + BA
Mathematics. Google Cloud Certified — Generative AI Leader.

**Stack:** Python · R · SQL · PyTorch · GCP/Vertex AI · BigQuery · FastAPI · React/TypeScript · Docker

*Bay Area · open to remote and relocation.*
