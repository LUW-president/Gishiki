# Gishiki Ritual Standard (v1)

This document defines the minimum structure and acceptance criteria for a Gishiki ritual.
The first implementation is the **Wellness / Recovery Ritual v1** in `index.html`.

---

## 1. Ritual structure

Every ritual in Gishiki must have at least:

1. **Opening**
   - A short calm intro (1–2 sentences).
   - Clear CTA to begin.
   - A secondary option to defer ("Not now" / "Later").

2. **Binary question flow**
   - Between **3 and 7** questions.
   - Each question:
     - is a single, clear sentence.
     - accepts **Yes** / **No** answers (optionally mapped to buttons and keyboard shortcuts).
   - Notes/hints under each question should be gentle, not prescriptive.

3. **Internal state / scoring**
   - A simple, front-end only scoring or state mechanism (no backend required for Sprint 01).
   - Each question contributes to 1..N internal dimensions (e.g., `depleted`, `needs_pause`, `wants_support`).
   - After the last question, the ritual chooses a **primary state** (and may compute supporting states).

4. **Primary result**
   - The orchestrator surfaces **one main proposition** based on the primary state:
     - e.g., a small next step, a pause, a reach-out, or a reframing.
   - The tone must be:
     - calm,
     - non-bossy,
     - non-generic,
     - aligned with Gishiki's mission.

5. **Alternate result**
   - A "Show another" path must exist.
   - The alternate result should be **meaningfully different** (e.g., lean more toward rest vs action), not a random variant.

6. **Restart path**
   - A clear "Restart ritual" or equivalent control.
   - Restart must:
     - reset internal state/scoring,
     - return the user to the opening section,
     - work reliably in a simple refresh-free way.

---

## 2. Web-verifiable acceptance criteria

A ritual is considered **DONE (v1)** when a human tester can:

1. Open the ritual page (for now: `/`).

2. See an opening card that:
   - invites a small, calm check-in,
   - offers **Begin** and **Not now**.

3. Click **Begin** and:
   - see the opening section disappear,
   - see the first question appear,
   - see Yes/No buttons,
   - answer through the entire flow without errors.

4. At the end of the questions, see:
   - a **Next step** section,
   - one clear suggestion (sentence) and a short explanatory tagline,
   - optional tags or small indicators of internal state (limited and non-diagnostic in tone).

5. Use the result controls:
   - Click **Yes, I'll do this** → nothing breaks, ritual remains stable.
   - Click **Show another** → a different suggestion appears, matching a different balance (e.g., more rest vs more action).

6. Restart:
   - Click **Restart ritual** → returns cleanly to the opening screen.
   - Running the ritual again behaves the same way (idempotent, no hidden broken state).

Everything above must work in a normal browser (mobile or desktop) with no console errors.

---

## 3. Implementation constraints (Sprint 01)

For Sprint 01 (Wellness / Recovery Ritual v1):

- **No backend** – all scoring and logic live in the browser.
- **No partners** – suggestions are self-contained; no external services are called.
- **No auth / accounts** – purely session-based, ephemeral usage.
- **No heavy frameworks** – plain HTML/CSS/JS only.
- **No dashboards / analytics** – beyond what the human can see on screen.

---

## 4. Style and tone

Ritual copy should:

- feel like a calm friend or wise peer,
- avoid clinical or diagnostic language,
- avoid wellness clichés ("optimize", "hack", "hustle"),
- avoid moral judgement (no "should" unless very carefully scoped),
- keep the surface simple: one question, one answer, one next move.

---

## 5. Extensibility

Future rituals (e.g., movement, sleep, founder focus, travel reset) should reuse the same pattern:

- Opening → 3–7 binary questions → scoring → primary result → alternate result → restart.
- The internal state model can be extended with new dimensions per ritual.
- The orchestrator's outward voice should stay consistent across rituals.
