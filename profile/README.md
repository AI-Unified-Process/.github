<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://unifiedprocess.ai/images/logo-white.svg">
  <img src="https://unifiedprocess.ai/images/logo.svg" alt="AI Unified Process" width="360">
</picture>

### Requirements-driven, AI-native software development.

**Specs at the center. AI handles the rest.**

[unifiedprocess.ai](https://unifiedprocess.ai) · [Methodology](https://unifiedprocess.ai/methodology.html) · [Tools](https://unifiedprocess.ai/tools.html) · [Tutorial](https://unifiedprocess.ai/tutorial.html) · [Articles](https://unifiedprocess.ai/articles.html) · [Deutsch](https://unifiedprocess.ai/de/)

</div>

---

## What is the AI Unified Process?

The **AI Unified Process (AIUP)** is a spec-driven development methodology in which requirements —
not code — are the source of truth. Every project starts with a written vision and proceeds through a
requirements catalog, an entity model, and use case specifications before a single line of code is
written. Code, tests, and documentation are then generated, regenerated, and refactored around those
specs by AI.

The phases follow the [Rational Unified Process](https://en.wikipedia.org/wiki/Rational_unified_process)
— Inception, Elaboration, Construction, Transition — adapted for AI-driven workflows.

**How this differs from other spec-driven tools.** In most of them, a developer writes a spec to
describe the code they are about to write: an elaborate prompt for one feature, effectively discarded
once the code ships. AIUP specs describe the *behavior of the system* — what it must do, not how the
code does it. They are living artifacts owned by requirements engineers (or by developers deliberately
doing requirements engineering), and they outlive any implementation.

> Nothing gets built without a use case. Nothing reaches production without tests traceable to requirements.

## The workflow

```
Inception          Elaboration                           Construction
─────────────────  ───────────────────────────────────   ──────────────────────────────────
/requirements  →  /entity-model  →  /use-case-diagram  →  /use-case-spec  →  /flyway-migration
                                                                          ↘  /implement
                                                                          ↘  /browserless-test
                                                                          ↘  /playwright-test
```

Each step picks up the files the previous one produced — `docs/vision.md`, `docs/requirements.md`,
`docs/entity_model.md`, `docs/use_cases.puml`, `docs/use_cases/UC-*.md`, `docs/test_cases/TC-*.md` —
and you can inspect or edit any of them before continuing.

Inheriting a legacy codebase? `/reverse-engineer` walks the existing code, configuration, and schema
and produces the same artifacts the forward workflow would have, giving you a documented baseline.

## Tools

| | |
|---|---|
| **[marketplace](https://github.com/AI-Unified-Process/marketplace)** | Claude Code plugins that drive the workflow end to end: the stack-agnostic `aiup-core` plus `aiup-vaadin-jooq` (Vaadin + jOOQ) and `aiup-angular-jpa` (Angular + Spring Boot JPA). Also installable on Codex CLI, Cursor, Copilot, Gemini CLI, and OpenCode. |
| **[intellij-plugin](https://github.com/AI-Unified-Process/intellij-plugin)** · **[vscode-plugin](https://github.com/AI-Unified-Process/vscode-plugin)** | *AI Unified Process Navigator* — jumps between `@UseCase`-annotated test methods and their Markdown specs, and renders a live activity diagram of the spec you are editing. Install from the [JetBrains Marketplace](https://plugins.jetbrains.com/plugin/31481-ai-unified-process-navigator/) or the [VS Code Marketplace](https://marketplace.visualstudio.com/items?itemName=aiup.aiup-navigator). |
| **[AIUP Studio](https://unifiedprocess.ai/studio.html)** | A web workspace giving every stakeholder one view of the project: structured editors for requirements, entity models, and use cases, with ER and activity diagrams generated automatically — read from and written straight to your Git repository. Currently in private beta. |

## Example projects

| | |
|---|---|
| **[book-library](https://github.com/AI-Unified-Process/book-library)** | The reference project for the [tutorial](https://unifiedprocess.ai/tutorial.html), built step by step with Vaadin, jOOQ, Spring Boot, and PostgreSQL. |
| **[task-manager](https://github.com/AI-Unified-Process/task-manager)** | The case study from the book *Spec-driven Development with the AI Unified Process*, showing how specs, code, and tests stay in sync as requirements change. |

## Getting started

1. Write a `docs/vision.md` describing the product, its users, and its goals — the richer it is, the better everything downstream.
2. Install the plugins in [Claude Code](https://claude.ai/code):

   ```
   /plugin marketplace add ai-unified-process/marketplace
   /plugin install aiup-core
   /plugin install aiup-vaadin-jooq        # for a Vaadin + jOOQ project
   /plugin install aiup-angular-jpa        # for an Angular + JPA project
   ```

   Using a different stack? Install `aiup-core` on its own — the methodology skills are stack-agnostic.
   On another AI coding agent, install via [Tessl](https://tessl.io) instead: `tessl install aiup/aiup-core`.
3. Run `/requirements` and let the workflow carry you from there.

The [tutorial](https://unifiedprocess.ai/tutorial.html) walks through the whole chain on a real
application, and the [videos](https://unifiedprocess.ai/videos.html) show it in motion.

## Adopting AIUP in your organization

Workshops, coaching, and enterprise rollout support are available — see
[Enterprise](https://unifiedprocess.ai/enterprise.html) or
[get in touch](https://unifiedprocess.ai/#contact).

<div align="center">

---

Created by [Simon Martinelli](https://martinelli.ch) · [unifiedprocess.ai](https://unifiedprocess.ai)

</div>
