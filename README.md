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
  <img src="https://img.shields.io/badge/repos-8-00D0FF?style=flat-square&labelColor=111827" alt="Repos"/>
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
| [awesome-ai-pulse-georgia](https://github.com/tornikebolokadze1-cyber/awesome-ai-pulse-georgia) | 130 | The sister list of this one, and a tool in its own right: 300 curated AI agent frameworks, coding agents, and automation resources, every entry described in Georgian rather than copied from its README. The collection ships as more than a page — an MCP server and an `aipulse` CLI let you query all 300 entries in natural language from inside Claude Code, Cursor, Codex, or any MCP client, so you can ask which repo fits the job instead of scrolling a 280 KB README. Maintained by the same people who maintain this list. TypeScript, CC0. |
| [georgian-payments-skills](https://github.com/erekle1/georgian-payments-skills) | 9 | Drop-in skill packages that teach an AI coding assistant the Georgian banking APIs it has never seen: TBC Bank (Checkout, TPay, and the XML CHECK/PAY billing protocol) and Bank of Georgia (iPay, the installment calculator SDK, PSD2 Open Banking). Ask for a payment flow in plain language and the skill pulls in the matching auth flow, endpoints, error codes, and code samples — instead of you reading bank PDFs at 2am. Installs into Claude Code, Cursor, Windsurf, Copilot, Zed, and 37+ other agents with a single `npx skills add`. Python, MIT. |
| [rs-mcp](https://github.com/Parsa-29/rs-mcp) | 8 | An MCP server and CLI that put Georgia's Revenue Service (rs.ge) inside an AI assistant. It wraps the WayBill, Invoice (NTOS), and TaxPayer SOAP endpoints as 85 callable tools, building the SOAP envelopes and parsing the XML replies for you, so an agent can look up a taxpayer, issue a waybill, or close an invoice from a plain-language request. Every destructive operation is gated behind a human-in-the-loop confirmation, and the CLI asks `[y/N]` before doing anything irreversible. The same 85 operations ship three ways: as an MCP server, as `rs-cli` subcommands with JSON output, and as a Claude Skill folder. TypeScript. No license declared yet — ask the author before reusing. |
| [flitt-payments-skill](https://github.com/Parsa-29/flitt-payments-skill) | 5 | A Claude Code and Cursor skill covering the Flitt payment API end to end: SHA1 request signing, hosted checkout in both redirect and server-to-server variants, direct card payments with the two-step 3DS flow, saved-card charges and tokenisation, subscriptions, captures, reversals, webhook validation with idempotency, and how to read the response codes. Mention Flitt in a prompt and the assistant pulls in the matching parameter reference instead of guessing at it. Thirteen reference documents plus a Python signature helper; one `git clone` into the skills folder installs it in either editor. Markdown + Python. No license declared yet — ask the author before reusing. |
| [loop-config](https://github.com/Parsa-29/loop-config) | 0 | An agent-neutral working setup built around a single `AGENTS.md` as the source of truth, bridged to whichever AI coding tool you happen to be in: Codex, Cursor, Copilot, Windsurf, and Cline read `AGENTS.md` directly, while Claude Code gets it copied or symlinked to `CLAUDE.md`. What it encodes is an Observe → Decide → Act → Verify → Learn loop, and the repo ships each tool's approval-gate settings next to it, so the same guardrails follow you between editors instead of being rebuilt per project. Python and shell. No license declared yet — ask the author before reusing. |

---

## 🔤 Georgian Language & NLP

> Technology for the Georgian language: NLP models, fonts, keyboard layouts, transliteration, TTS/STT, spell checkers, and datasets.

| Repository | ⭐ | Description |
|---|---|---|
| [ka-to-lat](https://github.com/Parsa-29/ka-to-lat) | 3 | A small library that transliterates Georgian into Latin and back: `georgianToLatin("ლორემ იპსუმ")` returns `"Lorem ipsum"`, and the reverse direction works too. Built for the places where Georgian script needs an ASCII form that people can still type and read — search indexing, URL slugs, sortable identifiers. Published on npm as `ka-to-lat`, and it optionally extends `String.prototype` so `"Gamarjoba!".latinToGeorgian()` works inline. The README is refreshingly honest about its one rough edge: some digraphs in the Latin→Georgian direction need specific casing (`gverDZe`, not `gverdze`) to resolve correctly. TypeScript, MIT. |

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
