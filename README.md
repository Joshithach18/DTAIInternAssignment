# The Daily Reflection Tree

> A deterministic end-of-day reflection tool. No LLM at runtime — just a well-designed tree, walked by simple code.

---

## Quick Start

```bash
# Part B — run the web UI
open agent/index.html
# or
python3 -m http.server 8080 --directory agent/
# then visit http://localhost:8080
```

No dependencies. No build step. Pure HTML + JS.

---

## Repository Structure

```
/tree/
  reflection-tree.json     ← Part A: full tree data (29 nodes, JSON format)
  tree-diagram.md          ← Part A: Mermaid diagram + path documentation

/agent/
  index.html               ← Part B: runnable web UI (single file, no deps)

/transcripts/
  persona-1-transcript.md  ← Victor/Contributor/Altrocentric persona
  persona-2-transcript.md  ← Victim/Entitlement/Self-Centric persona

write-up.md                ← Design rationale (2 pages)
README.md                  ← This file
```

---

## The Three Axes

| Axis | Spectrum | Psychology |
|------|----------|------------|
| **Locus** | Victim ↔ Victor | Rotter (1954) Locus of Control + Dweck (2006) Growth Mindset |
| **Orientation** | Entitlement ↔ Contribution | Campbell et al. (2004) + Organ (1988) OCB |
| **Radius** | Self-Centric ↔ Altrocentric | Maslow (1969) Self-Transcendence + Batson (2011) |

---

## Node Inventory

| Type | Count | IDs |
|------|-------|-----|
| start | 1 | START |
| question | 11 | A1_OPEN, A1_Q_AGENCY_HIGH, A1_Q_AGENCY_LOW, A1_Q2_INTERNAL, A1_Q2_EXTERNAL, A2_OPEN, A2_Q_CONTRIBUTION, A2_Q_ENTITLEMENT, A2_Q2, A3_OPEN, A3_Q_SELF, A3_Q_OTHER |
| decision | 7 | A1_D1, A1_D2, A1_D3, A2_D1, A2_D2, A3_D1, A3_D2 |
| reflection | 6 | A1_R_INTERNAL, A1_R_EXTERNAL, A2_R_CONTRIBUTION, A2_R_ENTITLEMENT, A3_R_SELF, A3_R_OTHER |
| bridge | 2 | BRIDGE_1_2, BRIDGE_2_3 |
| summary | 1 | SUMMARY |
| end | 1 | END |
| **TOTAL** | **29** | |

---

## How the Tree Works

### State
The agent maintains a `state` object:
```js
{
  answers: { "A1_OPEN": "stormy", "A1_Q_AGENCY_LOW": "stuck", ... },
  signals: { "axis1:external": 1, "axis2:entitlement": 1, ... },
  history: ["START", "A1_OPEN", "A1_D1", ...]
}
```

### Routing
- **Question nodes** wait for user selection, store `answers[nodeId] = value`
- **Decision nodes** run condition functions against state, route to matching target
- **Signal nodes** increment `signals[key]` when reached
- **Reflection/Bridge/Summary nodes** interpolate `{nodeId}` placeholders from stored answers

### Signal Model (not per-question branching)
Each axis accumulates signals across its 2 question nodes. At the end of each axis, a decision node routes to the appropriate reflection based on whichever signal pole has `count > 0`. This makes the tree resilient to mixed answers within an axis.

### Determinism
Same answers → same signals → same routing → same reflections. Every time. No randomness, no API calls, no external dependencies.

---

## Possible Paths

There are **8 unique conversation paths** (2 routing outcomes per axis × 3 axes):

| Path | Axis 1 | Axis 2 | Axis 3 | Profile |
|------|--------|--------|--------|---------|
| 1 | Internal | Contribution | Other | Victor + Giver + Altrocentric |
| 2 | Internal | Contribution | Self | Victor + Giver + Self-focused |
| 3 | Internal | Entitlement | Other | Victor + Taker + Altrocentric |
| 4 | Internal | Entitlement | Self | Victor + Taker + Self-focused |
| 5 | External | Contribution | Other | Victim + Giver + Altrocentric |
| 6 | External | Contribution | Self | Victim + Giver + Self-focused |
| 7 | External | Entitlement | Other | Victim + Taker + Altrocentric |
| 8 | External | Entitlement | Self | Victim + Taker + Self-focused |

---

## Reading the Tree Data (reflection-tree.json)

```json
{
  "id": "A1_Q2_INTERNAL",
  "type": "question",
  "axis": 1,
  "signal": "axis1:internal",
  "text": "There's something that didn't go the way you hoped today...",
  "options": [...],
  "next": "A1_D3"
}
```

Every node has `id`, `type`, and routing info (`next` or `routes`). Decision nodes contain an array of `routes` with conditions and targets. This file is the single source of truth — the agent in `index.html` loads its logic from an embedded equivalent of this structure.

---

## Design Principles

1. **No LLM at runtime.** The tool runs entirely offline. No API keys, no network calls.
2. **Fixed options only.** No free text. The hard work is designing options that honestly capture the spectrum.
3. **No moralizing.** Every reflection acknowledges the reality before offering a reframe. The tone is a wise colleague, not a manager.
4. **The axes connect.** The insight from each axis is designed to build toward the next. Agency → Contribution → Transcendence is a coherent psychological arc, not three quizzes.

---

## Built With

- Vanilla HTML, CSS, JavaScript
- Google Fonts (DM Serif Display + DM Sans)
- Zero runtime dependencies
- Zero LLM calls

---

*DT Fellowship Assignment — The Daily Reflection Tree*
