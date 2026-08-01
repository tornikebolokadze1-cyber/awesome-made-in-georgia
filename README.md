<p align="center">
  <img src="assets/banner.svg" alt="Awesome Made in Georgia" width="100%"/>
</p>

<h1 align="center">Awesome Made in Georgia</h1>

<p align="center">
  <b>A curated list of open source software built by Georgian developers</b><br/>
  Maintained by <a href="https://aipulsegeorgia.ge">AI Pulse Georgia</a>
</p>

<p align="center">
  <a href="https://awesome.re"><img src="https://awesome.re/badge.svg" alt="Awesome"/></a>
  <img src="https://img.shields.io/badge/repos-4-00D0FF?style=flat-square&labelColor=111827" alt="Repos"/>
  <img src="https://img.shields.io/badge/categories-6-A949DA?style=flat-square&labelColor=111827" alt="Categories"/>
  <img src="https://img.shields.io/badge/made_in-Sakartvelo_%F0%9F%87%AC%F0%9F%87%AA-00D0FF?style=flat-square&labelColor=111827" alt="Made in Sakartvelo"/>
  <a href="CONTRIBUTING.md"><img src="https://img.shields.io/badge/PRs-welcome-A949DA?style=flat-square&labelColor=111827" alt="PRs welcome"/></a>
  <a href="https://aipulsegeorgia.ge"><img src="https://img.shields.io/badge/aipulsegeorgia.ge-website-A949DA?style=flat-square&labelColor=111827" alt="Website"/></a>
</p>

<p align="center"><i>Georgia here means Sakartvelo 🇬🇪 — the country in the Caucasus, not the US state.</i></p>

---

## About this list

Georgian developers write good open source, but it disappears into GitHub's millions of repositories. There has never been a single place to see what is being built in Sakartvelo. This list is that place.

Unlike most awesome lists, this one is organised by **origin rather than topic**. It does not matter whether a project is about AI, the web, or games — what matters is that a Georgian built it.

> **Sister list:** [Awesome AI Pulse Georgia](https://github.com/tornikebolokadze1-cyber/awesome-ai-pulse-georgia) — 300 international AI and developer tools, described in Georgian. The two lists point in opposite directions: that one curates *the best of the world* for a Georgian audience, this one shows *what Georgia builds* to everyone else.

**What counts as Georgian** — the exact criteria and submission rules live in [CONTRIBUTING.md](CONTRIBUTING.md).

---

## Contents

- [🤖 AI Agents & Orchestration](#-ai-agents--orchestration)
- [🛠️ Developer Tools](#️-developer-tools)
- [🔤 Georgian Language & NLP](#-georgian-language--nlp)
- [🌐 Web & Applications](#-web--applications)
- [📦 Libraries & SDKs](#-libraries--sdks)
- [🎮 Games & Graphics](#-games--graphics)

---

## 🤖 AI Agents & Orchestration

> Systems that put AI models to work on real codebases: agent orchestration, task routing, durable context, and verification of what the model produced.

| Repository | ⭐ | Description |
|---|---|---|
| [kimi-atlas](https://github.com/null0xxx/kimi-atlas) | 13 | A many-agent orchestrator for Kimi Code that ships with 115 vendored official skill packages. Its central claim is that **no LLM ever computes pass/fail** — that decision belongs to a deterministic six-lens verification harness with pure gates. The `atlas` core drives a single change through an explicit `INIT → … → OUTPUT` state machine; `ATLAS-WEAVE` decomposes a larger change into a file-disjoint plan-DAG (work split so that no two agents ever touch the same file), drains it with at most three concurrent agents, and merges through a combined-tree differential gate — degrading byte-identically to a single `atlas` run when the work does not decompose. Carries a live ContextGraph recomputed on every refine pass and two-phase forward-only rollback confined to an isolated worktree, so your real tree is never touched. Python, MIT. |
| [AIWorkHub](https://github.com/shrec/AIWorkHub) | 2 | A local-first control plane for VS Code that turns each Git repository into an isolated AI engineering workspace. It wires the models already available in your editor (Codex, Claude, DeepSeek, GLM, Copilot) to a repository-scoped task queue, a Source Graph, a session manager, durable AI memory, and a review inbox. No cloud account and no HTTP service are required, and it reuses each CLI's existing login rather than copying credentials anywhere. Two ideas carry the design: agents query the structural Source Graph instead of rescanning the tree (spending far less context), and changes are accepted only once the evidence passes. Python + VS Code extension, MIT. |

---

## 🛠️ Developer Tools

> CLIs, automation, build tooling, DevOps — anything that makes a developer's day shorter.

| Repository | ⭐ | Description |
|---|---|---|
| [claude-code-setup](https://github.com/tornikebolokadze1-cyber/claude-code-setup) | 13 | A one-command setup that turns a fresh repository into a governed Claude Code project: 17 rules, 7 hooks, 7 templates, and a `/setup` command that wires in security guardrails, automated testing, CI/CD, and secret protection from the first commit. Built for people who use AI coding agents daily and would rather install their guardrails once than re-decide them on every new project. TypeScript, MIT. |
| [georgian-payments-skills](https://github.com/erekle1/georgian-payments-skills) | 9 | Drop-in skill packages that teach an AI coding assistant the Georgian banking APIs it has never seen: TBC Bank (Checkout, TPay, and the XML CHECK/PAY billing protocol) and Bank of Georgia (iPay, the installment calculator SDK, PSD2 Open Banking). Ask for a payment flow in plain language and the skill pulls in the matching auth flow, endpoints, error codes, and code samples — instead of you reading bank PDFs at 2am. Installs into Claude Code, Cursor, Windsurf, Copilot, Zed, and 37+ other agents with a single `npx skills add`. Python, MIT. |

---

## 🔤 Georgian Language & NLP

> Technology for the Georgian language: NLP models, fonts, keyboard layouts, transliteration, TTS/STT, spell checkers, and datasets.

*Empty for now. Yours could be the first one here. [Submit it →](CONTRIBUTING.md)*

---

## 🌐 Web & Applications

> Web apps, sites, frontend and backend projects, mobile applications.

*Empty for now. Yours could be the first one here. [Submit it →](CONTRIBUTING.md)*

---

## 📦 Libraries & SDKs

> Packages other developers pull into their own projects: npm, PyPI, crates.io, Maven, and the rest.

*Empty for now. Yours could be the first one here. [Submit it →](CONTRIBUTING.md)*

---

## 🎮 Games & Graphics

> Games, graphics engines, creative coding, and visualisation.

*Empty for now. Yours could be the first one here. [Submit it →](CONTRIBUTING.md)*

---

## About

<p align="center">
  <a href="https://aipulsegeorgia.ge"><img src="https://img.shields.io/badge/AI_Pulse_Georgia-2026-00D0FF?style=for-the-badge&labelColor=111827" alt="AI Pulse Georgia 2026"/></a>
</p>

This list is maintained by **[AI Pulse Georgia](https://aipulsegeorgia.ge)** — a community focused on AI agents, automation, and the future of autonomous systems.

> *"Exploring Georgia's AI Future"*

If you build Georgian open source, or you simply want it to be more visible, star the list and pass it on.

## Contributing

Know a good repository built by a Georgian developer? Have one of your own? Open an issue or send a pull request — the full rules and the "what counts as Georgian" criteria are in **[CONTRIBUTING.md](CONTRIBUTING.md)**.

Submitting your own project is encouraged. This is not self-promotion: a list organised by authorship only works if the authors bring their own work to it.

## License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

The list is released under [CC0 1.0 Universal](LICENSE). Every repository listed keeps its own license.
