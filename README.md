# Gishiki

Gishiki is a public-interest orchestration system that helps humans receive the right guidance, service, or artifact through a trusted conversation between specialized agents and a single human-facing orchestrator.

- The human interacts with **one orchestrator** – a calm guide that reflects, synthesizes, and proposes the next move.
- Behind the orchestrator, specialized agents gather in an internal chamber – **Gishiki, the bar** – where they exchange signals, interpretations, and proposed outputs.
- A capability network connects Gishiki to real-world tools and services (from food and transport to workflows and wellbeing).

The goal is simple:

> reduce noise, increase clarity, and make technology feel more aligned with human reality.

---

## Why Gishiki exists

Digital life is fragmented.

People are surrounded by tools, assistants, recommendations, interfaces, alerts, and systems that demand attention. Most of these systems speak directly and separately to the user. Very few systems pause first, confer internally, and then return a coherent response.

Gishiki exists to reverse that pattern.

Instead of exposing the user to chaos, Gishiki organizes intelligence behind the scenes and presents only what is most relevant, useful, and aligned.

For the full mission and manifesto, see:

- [`docs/MANIFESTO.md`](docs/MANIFESTO.md)

---

## Current MVP: Wellness / Recovery Ritual v1

The current Gishiki MVP is a **Wellness / Recovery Ritual** implemented as a single static page:

- **Path**: `index.html` (served as `/`)
- **Flow**:
  - Opening card with a calm intro and **Begin / Not now** options.
  - 5 binary questions (Yes/No) about energy, body, slowing down, support, and readiness for one practical step.
  - A small internal state model that infers patterns like `depleted`, `body needs`, `needs_pause`, `wants_support`, `ready_for_step`, etc.
  - One primary result: a single next step phrased in a calm, non-bossy way.
  - One alternate result via **Show another**, which flips between rest-leaning and action-leaning suggestions.
  - A clear **Restart ritual** path that takes you back to the opening.

Everything runs on the front-end only – no backend, no partners, no accounts.

Ritual standard: [`docs/specs/ritual_standard.md`](docs/specs/ritual_standard.md)

---

## Core idea

Gishiki works through three layers:

1. **Human-facing orchestrator** – The only voice the user hears. It guides, proposes, and delivers outcomes in a simple and calm way.
2. **Internal agent chamber ("the bar")** – Specialized agents observe, interpret, and whisper signals. They never speak directly to the human.
3. **Capability network** – Connections to services, tools, and external systems that can produce outcomes in the real world.

Examples of capabilities (future work):

- ordering food
- booking transportation or lodging
- generating documents or drafts
- activating workplace tools
- adjusting connected environments
- routing toward care or wellbeing resources

---

## Interaction model

The user experience should stay simple.

Typical inputs:

- `yes` / `no`
- `not now`
- `continue`
- `show another`
- `proceed`

Behind these small inputs, Gishiki performs richer orchestration (for now within the front-end ritual, later with deeper multi-agent behavior).

The orchestrator may respond with:

- a recommendation
- a service or provider
- an action plan
- a draft or visual
- a ritual step
- a pause or reframing

---

## Principles (short version)

- **One guide, not many bots** – The human should not have to manage multiple agents.
- **Open by default** – The ecosystem remains open and accessible.
- **Trust before priority** – Reliability and alignment come before any paid placement.
- **Relevance before payment** – A paid solution must never override what is best for the user.
- **Public-interest foundation** – The system should serve humans first.

---

## Status

Gishiki is in early development, with **one working, web-verifiable ritual**:

- `/` – Wellness / Recovery Ritual v1 (static, front-end only).

Documentation:

- Mission + manifesto: `docs/MANIFESTO.md`
- Lifecycles (agents, orchestrator, user, partners): `docs/specs/lifecycles.md`
- Ritual standard: `docs/specs/ritual_standard.md`

Contributions at this stage are about **refining the ritual**, **shaping the orchestrator surface**, and **designing the internal agents and capability network that will eventually live behind this flow**.
