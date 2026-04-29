# Write-Up: Design Rationale for the Daily Reflection Tree

*Max 2 pages — as specified*

---

## Why These Questions?

The most dangerous trap in designing reflection questions is writing what you *want* people to say, not what they might actually think at 7pm after a hard day. Every question in this tree started with a single test: *"Would a real person, tired and slightly guarded, pause at this?"*

The opening question — "If today were a weather report, what would it be?" — is deliberately soft. It uses metaphor to lower the threat level before the tree moves toward attribution and agency. People answer weather questions before they've raised their guard. By the time the tree asks *"where do you place the cause?"*, they've already committed to a frame.

**Axis 1 (Locus)** draws directly from Rotter's Internal-External Scale (1966) and Dweck's Fixed vs Growth Mindset work. The key insight was that most people with external locus don't *know* they have it — they experience external attribution as accurate description, not protective fiction. So the questions don't ask "do you blame others?" — they ask "what was your first instinct?" and "where do you place the cause?" Subtle difference. The first sounds like a character test; the second sounds like a memory exercise.

**Axis 2 (Orientation)** was the hardest to design. Entitlement, as Campbell et al. (2004) describe it, is invisible to its holder. Directly asking "were you entitled today?" would be useless — no one says yes. Instead, the questions surface the *behavioral signature* of entitlement: tracking recognition, monitoring others' effort, measuring fairness. The options are written to be honest rather than leading — option D in A2_Q_ENTITLEMENT ("I was just surviving") is intentionally offered as a non-judgmental escape hatch, because sometimes surviving is accurate.

**Axis 3 (Radius)** rests on two bodies of work: Maslow's 1969 paper "Theory Z" (where self-transcendence appears as a developmental stage beyond self-actualization) and Batson's empathy-altruism hypothesis (2011). The weather-to-frame progression by Axis 3 isn't accidental — by the time someone reaches "who's in the frame?", they've already done two rounds of honest self-examination, which makes widening the lens feel natural rather than preachy.

---

## How I Designed the Branching

The core trade-off in any decision tree is **fidelity vs complexity**. You can branch at every question and produce a tree with hundreds of paths — or you can use signals (tallied scores) that route at the end of each axis rather than at each question. I chose the signal approach for three reasons:

1. **Resilience:** Real human answers are messy. Someone might show internal locus in one question and external in another. A per-question branch would route them into a contradictory path. A signal tally at the axis end produces a *dominant* pattern that's more honest about the whole.

2. **Conversation flow:** If every question branches into a completely different sub-tree, the tool starts to feel like a choose-your-own-adventure game. Using bridging questions (the second question per axis) that don't branch, but add nuance, keeps the conversation feeling linear while the routing stays sensitive.

3. **Maintainability:** A tree with 8 question nodes × 4 options × 3 axes = 64+ possible paths is unmaintainable as data. The signal model reduces this to 2^3 = 8 effective summary profiles, all from the same nodes.

**The decision nodes are invisible to the user.** This is critical. The employee never sees "routing based on answer=Tough|Frustrating." They just experience a conversation that somehow *fits* — their opening answer shows up interpolated in the next question, the reflection they receive feels earned. The seam between determinism and warmth is what determines whether the tool feels like a form or a colleague.

---

## What I'd Improve With More Time

1. **Per-combination summary templates.** The current summary synthesizes three axes independently. A more nuanced version would have 8 distinct summary paragraphs for each Victor/Victim × Contribution/Entitlement × Altrocentric/Selfcentric combination — e.g., a "Victor + Entitlement + Self" combination has a very specific psychological texture (high agency, low generosity) that deserves its own reframe.

2. **A fourth optional node type: `probe`** — a single follow-up question that appears only when a user's signal pattern is ambiguous (e.g., split between internal and external). The probe would add one more data point before routing to a reflection.

3. **Longitudinal state.** The tree currently treats every session as independent. A real product would persist signals across 30 days and surface patterns: "For the third week in a row, your Axis 2 signal is entitlement-dominant. Here's what that usually means..." That's knowledge engineering at the system level, not just the session level.

4. **Options calibration.** The options were designed through research and persona-testing with LLM simulations, but real empirical calibration — running the tree with 50 real employees and checking whether options cleanly distinguish signal poles — would sharpen the branching accuracy significantly.

---

## Sources

- Rotter, J.B. (1966). *Generalized expectancies for internal versus external control of reinforcement.* Psychological Monographs.
- Dweck, C. (2006). *Mindset: The New Psychology of Success.* Random House.
- Campbell, W.K. et al. (2004). *Psychological entitlement: Interpersonal consequences and validation of a self-report measure.* Journal of Personality Assessment.
- Organ, D.W. (1988). *Organizational Citizenship Behavior: The Good Soldier Syndrome.* Lexington Books.
- Maslow, A. (1969). *Theory Z.* Journal of Transpersonal Psychology.
- Batson, C.D. (2011). *Altruism in Humans.* Oxford University Press.
