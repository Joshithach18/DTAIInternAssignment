# Transcript — Persona 2: Victim / Entitlement / Self-Centric

**Persona:** Rajan, Senior Software Engineer. Had a code review where his PR was rejected with terse comments. Spent the afternoon frustrated, feeling the reviewer was unfair, and left without completing anything notable. Tired, resentful, unseen.

---

**[SESSION START]**

> Good evening. Glad you're here.
> This is your space — no performance, no right answers. We're just going to look honestly at your day together.
> It takes about 5 minutes. Let's begin.

---

**Node: A1_OPEN**
> Let's start simply. If today were a weather report, what would it be?

**Rajan selects:** ⛈ Stormy — rough patches, maybe conflict.

*→ Routes to A1_D1: answer=stormy → A1_Q_AGENCY_LOW*

---

**Node: A1_Q_AGENCY_LOW**
> You said "stormy" — sounds like it wasn't easy. When things got hard, what was your first instinct?

**Rajan selects:** Feel stuck — not sure what to do.

*→ Routes to A1_D2: answer=stuck → A1_Q2_EXTERNAL*

---

**Node: A1_Q2_EXTERNAL**
> Even on a tough, foggy, or stormy day — somewhere in it, you made a decision. Which of these feels closest?

**Rajan selects:** I'm honestly not sure I made any meaningful choice.

*→ Signal: axis1:external*
*→ Routes to A1_D3: axis1:internal = 0 → A1_R_EXTERNAL*

---

**Node: A1_R_EXTERNAL** *(Reflection)*
> Hard days pull attention outward — toward what others did, what didn't work, what you couldn't change. That's a very human response.
>
> But even in those moments, there's usually one small decision that was yours. Asking for help. Taking a breath. Staying in the room.
>
> That's where your agency lives. Even when it's quiet.

**Rajan clicks Continue →**

---

**Node: BRIDGE_1_2**
> Now let's shift from how you handled things — to what you gave.

---

**Node: A2_OPEN**
> Think about one meaningful interaction you had today — with a colleague, a client, your manager, anyone. What was the energy of it?

**Rajan selects:** I received something — help, feedback, credit.

*→ Routes to A2_D1: answer=received → A2_Q_ENTITLEMENT*

---

**Node: A2_Q_ENTITLEMENT**
> Sometimes we track what we're getting — recognition, fairness, credit. Which of these sounds most familiar today?

**Rajan selects:** I felt my effort wasn't noticed or appreciated.

*→ Signal: axis2:entitlement*

---

**Node: A2_Q2**
> One more lens. Was there a moment today where you went beyond what was asked — where no one would have noticed if you hadn't?

**Rajan selects:** Not today — I gave what was expected.

*→ Routes to A2_D2: axis2:entitlement > 0 → A2_R_ENTITLEMENT*

---

**Node: A2_R_ENTITLEMENT** *(Reflection)*
> Today you were tracking what you were getting — recognition, fairness, effort from others. That's natural. It's also a signal worth sitting with.
>
> Entitlement isn't a character flaw. It's usually a gap between expectation and reality. The question is: whose job is it to close that gap?
>
> Sometimes the answer is 'the organization.' Sometimes it's you — by shifting from what you're owed to what you can give.

**Rajan clicks Continue →**

---

**Node: BRIDGE_2_3**
> Now let's zoom out from what you gave — to who you were thinking about.

---

**Node: A3_OPEN**
> When you replay today's biggest challenge right now — who's in the frame?

**Rajan selects:** Just me — it was my problem to solve.

*→ Routes to A3_D1: answer=just_me → A3_Q_SELF*

---

**Node: A3_Q_SELF**
> It's okay to be focused inward — especially on hard days. But let's stretch the frame a little. Was there anyone today who was affected by your work, even indirectly?

**Rajan selects:** My work today felt pretty isolated from others.

*→ Signal: axis3:self*
*→ Routes to A3_D2: axis3:self > 0 → A3_R_SELF*

---

**Node: A3_R_SELF** *(Reflection)*
> Today your attention stayed close — on your own work, your own stress, your own outcomes. That's not wrong. Focused days are real.
>
> But here's something worth knowing: Maslow's most underappreciated insight was that the healthiest humans eventually orient outward — not because they've fixed themselves, but because they've expanded what 'self' even means.
>
> Tomorrow: one moment. One glance at how your work lands in someone else's world.

**Rajan clicks Continue →**

---

**Node: SUMMARY**

> **Here's what your day looked like through the tree:**
>
> **Agency (Axis 1):** Today you leaned toward external attribution. Tomorrow: find the one small decision that was yours.
>
> **Contribution (Axis 2):** On orientation, you were more entitlement-oriented. Tomorrow: one act of giving before counting what you're owed.
>
> **Radius (Axis 3):** Your frame of concern today was close to yourself. Tomorrow: one moment of imagining how your work lands for someone else.
>
> ---
> You described today as "stormy". Whatever that meant — you showed up, you reflected, and you looked at it honestly.
>
> That's not a small thing.

---

**Node: END**
> Rest well. See you tomorrow.

---

## Path Taken
```
START → A1_OPEN(stormy) → A1_D1 → A1_Q_AGENCY_LOW(stuck) → A1_D2 → 
A1_Q2_EXTERNAL(none) → A1_D3 → A1_R_EXTERNAL → BRIDGE_1_2 →
A2_OPEN(received) → A2_D1 → A2_Q_ENTITLEMENT(unnoticed) → A2_Q2(expected_only) → A2_D2 →
A2_R_ENTITLEMENT → BRIDGE_2_3 →
A3_OPEN(just_me) → A3_D1 → A3_Q_SELF(isolated) → A3_D2 → A3_R_SELF →
SUMMARY → END
```

**Signals accumulated:**
- axis1:external: 1
- axis2:entitlement: 1
- axis3:self: 1

**Profile:** Victim + Entitlement + Self-Centric — the opposite trajectory. Notice the tree doesn't shame Rajan. Each reflection acknowledges the reality ("hard days pull attention outward", "entitlement isn't a character flaw") and offers a single actionable reframe — not a lecture. The same warm colleague tone persists. The tree's value is surfacing the pattern, not judging it.
