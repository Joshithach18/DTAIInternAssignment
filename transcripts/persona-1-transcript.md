# Transcript — Persona 1: Victor / Contributing / Altrocentric

**Persona:** Priya, Senior Product Manager. Finished a difficult sprint review where one feature was cut. Stayed calm, helped a junior dev reframe the setback, and thought a lot about the user experience downstream.

---

**[SESSION START]**

> Good evening. Glad you're here.
> This is your space — no performance, no right answers. We're just going to look honestly at your day together.
> It takes about 5 minutes. Let's begin.

---

**Node: A1_OPEN**
> Let's start simply. If today were a weather report, what would it be?

**Priya selects:** ☁️ Overcast — steady, but low energy.

*→ Routes to A1_D1: answer=overcast → A1_Q_AGENCY_HIGH*

---

**Node: A1_Q_AGENCY_HIGH**
> You said "overcast" — sounds like a relatively workable day. When something went well, what made it happen?

**Priya selects:** I adapted when the original plan changed.

*→ Signal: (not yet — routes to A1_D2: answer=adapted → A1_Q2_INTERNAL)*

---

**Node: A1_Q2_INTERNAL**
> There's something that didn't go the way you hoped today. When you picture that moment — where do you place the cause?

**Priya selects:** Mostly on me — I could have done something differently.

*→ Signal: axis1:internal*
*→ Routes to A1_D3: axis1:internal > 0 → A1_R_INTERNAL*

---

**Node: A1_R_INTERNAL** *(Reflection)*
> You see your hand in what happened today — not perfectly, maybe not completely, but you're not pointing only outward.
>
> That's agency. It doesn't mean you controlled everything. It means you stayed in the driver's seat even when the road was rough.
>
> Hold that.

**Priya clicks Continue →**

---

**Node: BRIDGE_1_2**
> Now let's shift from how you handled things — to what you gave.

---

**Node: A2_OPEN**
> Think about one meaningful interaction you had today — with a colleague, a client, your manager, anyone. What was the energy of it?

**Priya selects:** I gave something — time, effort, perspective.

*→ Routes to A2_D1: answer=gave → A2_Q_CONTRIBUTION*

---

**Node: A2_Q_CONTRIBUTION**
> You said you gave something today. What was the nature of that giving?

**Priya selects:** I helped someone with something outside my job description.

*→ Signal: axis2:contribution*

---

**Node: A2_Q2**
> One more lens. Was there a moment today where you went beyond what was asked — where no one would have noticed if you hadn't?

**Priya selects:** Yes — I did something extra, unprompted.

*→ Routes to A2_D2: axis2:contribution > 0 → A2_R_CONTRIBUTION*

---

**Node: A2_R_CONTRIBUTION** *(Reflection)*
> You gave today. That's not nothing — it's the quiet engine of functional teams.
>
> The best organizations run on discretionary effort: the help no one asked for, the knowledge shared without keeping score, the work done even when it's invisible.
>
> You added something to the system today. Notice that.

**Priya clicks Continue →**

---

**Node: BRIDGE_2_3**
> Now let's zoom out from what you gave — to who you were thinking about.

---

**Node: A3_OPEN**
> When you replay today's biggest challenge right now — who's in the frame?

**Priya selects:** The customer or end user we ultimately serve.

*→ Routes to A3_D1: answer=customer → A3_Q_OTHER*

---

**Node: A3_Q_OTHER**
> You're already holding others in the frame — that's meaningful. Did you act on that awareness at any point today?

**Priya selects:** Yes — I checked in or adjusted based on their needs.

*→ Signal: axis3:other*
*→ Routes to A3_D2: axis3:other > 0 → A3_R_OTHER*

---

**Node: A3_R_OTHER** *(Reflection)*
> Your frame includes others — their needs, their experience, the bigger mission. That's perspective-taking in practice.
>
> This isn't altruism for its own sake. Research consistently shows that people who orient beyond themselves at work report more meaning, more resilience, and more satisfaction — not because life gets easier, but because it gets larger.
>
> You're already doing it.

**Priya clicks Continue →**

---

**Node: SUMMARY**

> **Here's what your day looked like through the tree:**
>
> **Agency (Axis 1):** Today you leaned toward internal locus. You located your choices even when things were hard.
>
> **Contribution (Axis 2):** On orientation, you were more contribution-oriented. You added to the system without being asked.
>
> **Radius (Axis 3):** Your frame of concern today was wider — others were in it. You held others in the frame — that widens everything.
>
> ---
> You described today as "overcast". Whatever that meant — you showed up, you reflected, and you looked at it honestly.
>
> That's not a small thing.

---

**Node: END**
> Rest well. See you tomorrow.

---

## Path Taken
```
START → A1_OPEN(overcast) → A1_D1 → A1_Q_AGENCY_HIGH(adapted) → A1_D2 → 
A1_Q2_INTERNAL(self) → A1_D3 → A1_R_INTERNAL → BRIDGE_1_2 →
A2_OPEN(gave) → A2_D1 → A2_Q_CONTRIBUTION(beyond) → A2_Q2(yes_extra) → A2_D2 →
A2_R_CONTRIBUTION → BRIDGE_2_3 →
A3_OPEN(customer) → A3_D1 → A3_Q_OTHER(acted) → A3_D2 → A3_R_OTHER →
SUMMARY → END
```

**Signals accumulated:**
- axis1:internal: 1
- axis2:contribution: 1
- axis3:other: 1

**Profile:** Victor + Contributor + Altrocentric — the ideal trajectory the tree is designed to surface and reinforce.
