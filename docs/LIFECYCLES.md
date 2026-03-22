# Gishiki Lifecycles

This document defines the lifecycle of the four core actors in the ecosystem:

- agents
- the orchestrator
- the user
- the partner

---

## 1. Agent lifecycle

### 1. Created
An agent is defined with a role, boundaries, confidence rules, and an observation domain.

### 2. Tuned
The agent learns what signals it may interpret, when it should defer, and what kinds of mistakes are unacceptable.

### 3. Activated
The agent is called into a session only when relevant.
It is not always active.

### 4. Observe
The agent receives user signals, context, recent history, and possibly hints from other agents.

### 5. Interpret
The agent forms a narrow internal view.
It does not decide the whole truth.
It contributes its disciplined perspective.

### 6. Contribute
The agent sends hints, warnings, scores, hypotheses, and confidence levels into the chamber.

### 7. Challenged
Other agents or the orchestrator may challenge or weaken that contribution.

### 8. Weighted
The system decides how much weight the agent should have in the current session.

### 9. Learn
The agent receives outcome feedback and calibrates over time.

### 10. Upgrade, pause, or retire
An agent may evolve, split, be demoted, paused, or removed.

---

## 2. Orchestrator lifecycle

### 1. Initialize session
The orchestrator gathers context, recent history, session goal, and available capabilities.

### 2. Frame the interaction
The orchestrator decides what mode the session is in: decision, execution, routing, support, or recovery.

### 3. Invite signal
The orchestrator asks the human for simple input.

### 4. Convene Gishiki
The orchestrator summons the relevant agents into the chamber.

### 5. Synthesize
The orchestrator combines user signals, agent output, memory, partner options, and confidence levels into one coherent reading.

### 6. Surface the next move
The orchestrator chooses whether to present a recommendation, artifact, question, redirect, service, or pause.

### 7. Stage delivery
The orchestrator adjusts tone and pacing according to the user's state.

### 8. Trigger action
If accepted, the orchestrator launches an internal workflow or external partner action.

### 9. Observe outcome
The orchestrator checks whether the recommendation was accepted and whether the action succeeded.

### 10. Remember
The orchestrator stores session memory for future improvement.

---

## 3. User lifecycle

### 1. Discovery
The user encounters Gishiki as a calm guided system rather than a swarm of bots.

### 2. Onboarding
The user learns the basic interaction pattern and what kind of guidance Gishiki can provide.

### 3. First signal
The user submits an initial need, question, or state.

### 4. Guided interaction
The user responds in lightweight binary or near-binary ways.

### 5. Proposition
The user receives a recommendation, action path, artifact, or reframing.

### 6. Accept or reject
The user confirms or declines.

### 7. Outcome
A workflow, recommendation, booking, draft, or other action happens.

### 8. Trust formation
With repeated useful sessions, the user begins to rely on the orchestrator.

### 9. Personalization
The system becomes more adapted to the user's patterns, pacing, and preferences.

### 10. Advocacy
The user returns often, recommends Gishiki, and uses it as a front door to action.

---

## 4. Partner lifecycle

### 1. Open entry
A service or company enters the network as an open solution.

### 2. Technical integration
The partner's capabilities, metadata, and action schemas are connected to the system.

### 3. Observation period
The partner is measured in real usage for reliability, latency, fulfillment quality, and relevance.

### 4. Qualification review
Gishiki evaluates whether the partner deserves premium status.

### 5. Premium solution status
The partner earns trust through strong quality, low error rates, and stable integration.

### 6. Priority access
Only after becoming premium may the partner pay for priority placement within relevant contexts.

### 7. Active participation
The partner becomes a living node in the ecosystem and is surfaced, selected, and measured.

### 8. Governance
Premium and priority status are continuously reviewed and may be downgraded or revoked.

### 9. Expansion
A strong partner may deepen integration, enter more categories, or support the public-interest layer.

### 10. Renewal or exit
The partner renews, downgrades, exits, or is removed.

---

## Shared rule

All four lifecycles obey one principle:

> the system becomes more powerful only if it becomes more trustworthy.