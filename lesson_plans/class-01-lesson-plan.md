# Lesson Plan: Class 1 — Electricity Is a Flow


* **Course:** Summer Electronics Course for Youth ([Makersmiths][05])
* **Class number:** 1 of 6
* **Phase:** 1 — Foundations
* **Date:** Tuesday, June 23, 2026, 6:00–8:00 PM
* **Experiments:** Exp 1 *Taste the Electricity* + Exp 2 *Let's Abuse a Battery!* (*Make: Electronics, 2nd Ed.*)
* **Prerequisites from prior classes:** None — this is the first class. Students should have read Experiments 1–2 in the [book][01] beforehand (not required to follow along).
* **Source of truth:** This plan implements [`electronics-primer-syllabus.md`](../electronics-primer-syllabus.md), Class 1. Component costs and sourcing live in [`BOM.md`](../BOM.md), never here.

> **About this plan.** It expands the syllabus's Class 1 outline into a minute-by-minute teaching guide for a volunteer instructor. It weaves in three lecture-note threads the syllabus calls for: a plain-language **explainer** (the water analogy), **history & application** (Ohm, Volta, Ampère), and a real-device **theory of operation** (the household fuse). You do not need to be a teacher to run this — say what's in the talking points, set up each build, and let teams discover.


---


## 1. Class Overview


This is the opening class of the course and of Phase 1 (Foundations). Students meet electricity for the first time as something they can *feel and measure*. In Experiment 1 they taste a 9-volt battery, then use a multimeter to measure the resistance of their tongue, skin, and water (plain vs. salty). In Experiment 2 they deliberately short out a single AA cell to feel heat being generated, then blow a 3-amp fuse and inspect the melted element under magnification. By the end, students can name the three quantities that govern every circuit in the course — **voltage, current, resistance** — explain them with the water analogy, and explain why a short circuit makes heat and why a fuse protects a circuit. This is the conceptual bedrock that Classes 2–6 build on: Ohm's Law (Class 2), controlling current (Classes 3–4), and generating it (Classes 5–6).


## 2. Learning Goals


After this class, students will be able to:

* Set up a digital multimeter (COM and VΩ sockets, dial to ohms) and measure resistance of tongue, skin, and water.
* State that lower resistance lets more current flow, and back it up with their own readings (moist tongue reads lower than dry; salt water reads lower than plain water).
* Explain electricity with the water analogy: **voltage = pressure, current = rate of flow, resistance = restriction**.
* Explain why shorting a battery makes heat, and why a fuse melts to protect the rest of a circuit.
* Record a first build-journal entry: what they built, what they observed, the physical cause, and one real-world device that uses the same idea.


## 3. Preparation Checklist


Do these before students arrive:

* **30 min before — Test every multimeter.** Confirm each team's meter powers on, has a working internal battery, and reads ohms. Set the dial to the ohm (Ω) symbol; on a manual-ranging meter pre-select the **200K** range for tongue/skin work. Verify the black lead is in **COM** and the red lead in the **VΩ** socket. (A dead meter battery is the #1 silent failure — catch it now.)
* **20 min before — Lay out per-team workstations.** Per team: one multimeter with leads, one 9-volt battery, a handful of single AA **alkaline** cells, one AA battery carrier/holder, several 3-amp fuses, a set of test leads with alligator clips, safety glasses for each person, a few tissues, and a magnifying glass.
* **20 min before — Set up the water station(s).** Three clear cups per team (or a shared station): plain tap water, salt water (stir in a heaping spoon of table salt until no more dissolves), and — if available — distilled water. Label them. Have paper towels ready.
* **15 min before — Confirm safety glasses** for every student and adult, staged at the short-circuit station for Exp 2.
* **10 min before — Pre-blow one fuse yourself** so you have a known-good "before" fuse and a blown "after" fuse to show side-by-side under the magnifier. Inspect for the S-shaped element so you can point it out.
* **5 min before — Write the three words** *VOLTAGE · CURRENT · RESISTANCE* on the whiteboard with room to add the water analogy beside each.
* **Have ready as spares:** extra AA alkaline cells (shorting drains them), extra 3-amp fuses (each team blows at least one), spare meter battery, spare alligator-clip leads.


## 4. Materials & Components


Names and quantities only — see [`BOM.md`](../BOM.md) for costs and sourcing. Only items used *this* class are listed.

| Item | Per team | Shared / notes |
|:-----|:--------:|:---------------|
| Digital multimeter with leads | 1 | Provided by Makersmiths; measures resistance + continuity today |
| 9-volt battery | 1 | For the Exp 1 tongue test |
| AA alkaline cells (single 1.5 V) | 3–4 | Exp 2 short circuit; **alkaline only, never rechargeable/lithium** |
| AA battery carrier/holder | 1 | Holds the cell for the short-circuit build |
| 3-amp fuse | 2–3 | Exp 2 fuse-blowing; teams will sacrifice these |
| Test leads with alligator clips | 1 set | From Pack 1 |
| Safety glasses | 1 per person | Worn for Exp 2 |
| Magnifying glass | 1 | Inspect the blown fuse element |
| Tissues / paper towels | a few | Dry tongue between readings; water station |
| Clear cups — plain water, salt water, (distilled) | 3 | Shared water station; table salt to mix |
| Build journal + pencil | 1 per student | Student-provided; primary record |


## 5. Class Timeline


Follows the standard 2-hour session from the syllabus. Time checks tell you when to move on even if a team isn't finished.

| Segment | Clock | Duration |
|:--------|:------|:--------:|
| 5a. Welcome, Safety & Setup | 0:00–0:15 | 15 min |
| 5b. Mini-Lecture (story first) | 0:15–0:35 | 20 min |
| 5c. Guided Builds (Exp 1 + Exp 2) | 0:35–1:30 | 55 min |
| 5d. "Explain It" Peer Share + Journal | 1:30–1:45 | 15 min |
| 5e. Wrap-Up & Next-Class Preview | 1:45–2:00 | 15 min |


### 5a. Welcome, Safety & Setup — 0:00–0:15 (15 min)


This class has no prior session to recap, so use this slot to set the tone, the safety ground rules, and the meter setup.

**What to do**

* Welcome everyone; introduce yourself and the adult helpers. State the one rule that defines the course: **"We build first and figure out why afterward. Mistakes — even burning out a part — are how we learn here, not something to be embarrassed about."**
* Hand out / confirm each team's workstation and journals.
* Walk through today's two safety rules out loud, because Exp 2 involves real heat:
  * For the tongue test (Exp 1): **only the 9-volt battery, never anything bigger, and never on broken skin.** If you have metal braces, keep the battery off them.
  * For the short circuit (Exp 2): **safety glasses on, single AA alkaline cell only.** Never short a wall outlet, a car battery, or a lithium/rechargeable battery — those are genuinely dangerous (loud bang, flying molten metal, fire).
* Have every team set up their meter together: black lead → **COM**, red lead → **VΩ**, dial → ohm (Ω) symbol.

**What to say**

* "Today you're going to *taste* electricity, then *feel* it make heat. Both are things most people are told never to do — done safely, they teach you more than any lecture."
* "The meter is your sense organ for electricity. You can't see volts or amps, but this tool lets you read them."

**What to watch for**

* Meters with leads in the wrong sockets (current sockets instead of VΩ) — this is the most common setup error. Check each one.
* A student wanting to jump ahead to the short circuit before the safety briefing — hold them.

**Time check:** Meters set up and safety covered by 0:15. Move on even if a meter is acting up — swap in a spare.


### 5b. Mini-Lecture (story first) — 0:15–0:35 (20 min)


Keep this to 20 minutes. It exists to set up the builds, not to replace them. Tell it as a story.

**Key concept 1 — Electricity is electrons flowing, like water in pipes (the explainer).**
Draw or point to the water-tank picture. A battery is like two water tanks, one full and one empty, joined by a pipe with a valve (*Make: Electronics* Fig. 1-25). Open the valve and water flows until the levels equalize. Open an electrical path between a battery's two terminals and electrons flow the same way — even if the only "pipe" is the moisture on your tongue.

* **Analogy to write on the board:**
  * **Voltage = water pressure** (how hard it's pushed) — measured in **volts**, named after **Volta**.
  * **Current = rate of flow** (how much per second) — measured in **amps**, named after **Ampère**.
  * **Resistance = how narrow the pipe is** (how much it restricts flow) — measured in **ohms**, named after **Ohm**.
* **Question to ask:** "If I make the pipe narrower — more resistance — does more or less water flow?" (Less.) "Hold that thought — you're about to prove it with your own tongue."

**Key concept 2 — Lower resistance → more current → more heat.**
That's the through-line connecting both of today's experiments. A tongue has *high* resistance, so only a tiny current flows — you feel a tingle, no heat. A wire has *very low* resistance, so a lot of current flows — enough to get hot. Same battery idea, wildly different result, purely because of resistance.

**Key concept 3 — A quick history hook (history & application).** Three people whose names we now use as units:

* **Georg Ohm** (Bavaria, 1787) worked in obscurity, making his own wire, and showed in 1827 that current is proportional to voltage and inversely related to resistance. We'll use his law next week.
* **Alessandro Volta** (Italy, 1745) built the first real battery in 1800 — the "voltaic pile," stacked copper and zinc discs in salt water. We'll build our own version in Class 2.
* **André-Marie Ampère** (France, 1775) showed that current creates magnetism — the seed of Classes 5–6 and of every KidWind generator.

**Key concept 4 — DC vs. AC (brief).** A battery pushes current steadily in one direction — **direct current (DC)**, which is what this whole course uses. A wall outlet **alternates** direction 60 times a second — **AC**. Mention it, don't dwell.

**Common misconception to address:** Students often think voltage and current are the same thing ("more volts = more power = more dangerous"). Use the water analogy: high pressure behind a closed/narrow path moves almost nothing; it's the *flow* (current) that does work and makes heat. The 9 V on the tongue (high-ish pressure, tiny flow) is harmless; a 1.5 V cell shorted (low pressure, big flow) gets hot.

**Time check:** Wrap the story by 0:35. If you're running long, cut the history to just the three names and move to building.


### 5c. Guided Builds — 0:35–1:30 (55 min)


Two experiments. Aim ~25 min on Exp 1, ~25 min on Exp 2, with a 5 min buffer. Helpers circulate and **ask questions rather than fix** — let teams reason out their own readings.

---


#### Experiment 1 — *Taste the Electricity* (≈25 min)


**Step 1 — Taste it.** Moisten the tongue, touch it to **both terminals** of the 9-volt battery. Feel the tingle. Then dry the tongue thoroughly with a tissue and touch again — the tingle is weaker. Ask: *"Why weaker when dry?"*

**Step 2 — Measure the tongue.** With the meter on ohms, touch the two probes **gently** to the tongue about an inch apart (never jab them in). Read the value — expect roughly **50K** (50,000 ohms). Record it. Dry the tongue, measure again — the reading rises. *The moisture lowered the resistance.*

> **Reading the display:** "K" after the number means thousands of ohms (50K = 50,000 Ω); "M" means millions. An autoranging meter picks the range itself; on a manual meter, if you see "1" or "OL" alone the value is off-scale — turn to a higher range (e.g., 200K).

**Step 3 — Vary the probe distance.** Hold the probes ¼″ apart on the tongue, then 1″ apart. *Shorter distance → less resistance → lower reading.* This previews how resistance depends on the path.

**Step 4 — Measure skin and water.**

* **Skin:** probes on a dry forearm — likely too high to read (shows "OL"/"1"). Moisten the skin and try again. Tie it to the real world: this is exactly how a **lie detector** works — stress makes you perspire, which lowers skin resistance.
* **Water:** dip the probes (about an inch apart) into plain water, then salt water, then distilled if available. Rank the readings: **salt water conducts best (lowest ohms), plain water next, distilled highest.** The dissolved salt — not the water itself — carries the current.

**Checkpoint — Exp 1 "done" looks like:** each team has written down tongue (wet vs. dry), skin, and the three water readings, and can say in one sentence *why salt water conducts better than plain water.*

---


#### Experiment 2 — *Let's Abuse a Battery!* (≈25 min)


**Safety glasses on before this starts.** Single AA **alkaline** cell only.

**Step 1 — Short the cell.** Put one AA alkaline cell in the carrier. Twist the two bare carrier wire-ends together (or join them with a short alligator lead). At first nothing seems to happen. **Wait about a minute** — the wires warm up; wait another minute and the cell itself gets warm. Have students cautiously touch the wire (not the cell terminals directly) to feel the heat. Then disconnect.

* **Ask:** *"The tongue had 9 volts and barely tingled. This is only 1.5 volts — why does it get hot?"* (The wire's resistance is tiny, so a large current flows; current makes heat. Lower resistance → more current → more heat — the same rule from the lecture.)
* **Analogy:** like a bicycle pump getting warm as you force air through it — pushing a lot of flow generates heat.

**Step 2 — Blow a fuse.** This shows what protects a real circuit from that runaway current.

* First, inspect a fresh 3-amp fuse under the magnifier — point out the thin **S-shaped element** (automotive) or thin wire (glass cartridge). That thin metal is the sacrificial part.
* Remove the cell from the carrier and set it aside (it's spent — recycle it). Connect the carrier to the fuse using two test leads (clip a lead to each end of the fuse). Now insert a **fresh** AA cell.
* Watch the fuse: a break appears in the center of the element where the metal **melts**. If nothing happens after a few seconds with a fresh cell, apply the leads directly, or the fuse may simply be a slow one — try another.
* Inspect the blown fuse under the magnifier next to a fresh one. The tiny gap is now an open circuit — **no current can flow.**

**Theory of operation — the household fuse (real-device hook).** A fuse is a deliberate weak link: a thin metal strip sized to melt when current exceeds its rating (here, 3 amps). When a fault lets too much current flow, the strip melts *first*, opening the circuit before the wiring overheats and starts a fire. A circuit breaker does the same job with a spring/electromagnet instead of melting metal, so it can be reset. The same reason a toaster's thin nichrome wire glows hot — thin, higher-resistance metal heats up — is why a fuse's thin element is the part that melts.

**Checkpoint — Exp 2 "done" looks like:** each team has felt the shorted wire get warm, blown at least one fuse, and can explain in a sentence that *the fuse melted to stop too much current from flowing.*

**Time check:** Both experiments wrapped by 1:30. If a team is behind, the fuse-blow is the must-do — the heat demo can be a quick feel.


### 5d. "Explain It" Peer Share + Journal — 1:30–1:45 (15 min)


**What to do**

* Pick one team to explain to the others **what physically happened** when they shorted the cell and blew the fuse — in their own words. Then a second team explains the water/salt-water readings. Coach with questions, don't correct hard.
* Everyone writes their first **build-journal** entry. Put the four-part template on the board:
    1. **What I built / did** — sketch or note (e.g., "shorted an AA cell; blew a 3-amp fuse").
    2. **What I observed** — the actual result (e.g., "wires got hot; fuse showed a melted gap").
    3. **What's physically happening** — one sentence on the cause (e.g., "low resistance let a big current flow → heat; the fuse melted to stop it").
    4. **Real-world link** — one device (e.g., "the fuse box / breaker panel in my house").

**What to watch for**

* Journal entries that only describe ("it got hot") without the *why*. Nudge with: "And why did it get hot?" Younger students may keep #3 to one short clause; that's fine.

**Time check:** Journals started by 1:45 — they can finish #4 at home.


### 5e. Wrap-Up & Next-Class Preview — 1:45–2:00 (15 min)


**What to do — restate what they should have learned:**

* Electricity is electrons flowing; **voltage = pressure, current = flow, resistance = restriction.**
* **Lower resistance → more current → more heat** — proven twice today (tongue/skin/water, then the shorted cell).
* A fuse is a planned weak link that melts to protect everything downstream.

**KidWind tie-in (say this every class):** "Every wind-turbine circuit obeys these same volts, amps, and ohms. When a generator actually delivers power, protecting the circuit — fuses and breakers — matters for real. You just met the rules the whole course, and every turbine, runs on."

**Preview Class 2 — Resistance and Ohm's Law (Experiments 3–5):** "Next week we put resistance to work: you'll light an LED, use different resistors to change its brightness, dim it with a knob, and even build a battery out of a lemon. We'll turn today's three words into one short equation — Ohm's Law."

**Assignment:** Read **Experiments 3–5** in *Make: Electronics* before next class. Finish today's journal entry (all four parts). Optional: notice where fuses or breakers live in your home.


## 6. Troubleshooting Guide


| Problem | Likely cause | Fix |
|:--------|:-------------|:----|
| Meter shows nothing at all | Dead/missing meter battery, or meter off | Swap meter battery or use a spare meter; confirm dial is on a function, not OFF |
| Tongue/skin reads "1", "OL", or "L" | Resistance above the selected range, or dry contact | On a manual meter pick a higher range (200K); moisten the contact point; hold probes closer together |
| Tongue reading wildly inconsistent | Probe distance/pressure varying between tries | Keep probes a fixed ~1″ apart, gentle even pressure — this is the experiment's lesson about uncontrolled variables |
| Plain and salt water read nearly the same | Salt not fully dissolved, or probes touching cup/each other | Stir salt until no more dissolves; keep probes ~1″ apart and off the cup walls |
| Shorted cell never gets warm | Weak/old cell, or wires not actually touching | Use a fresh AA alkaline cell; ensure bare wire ends are firmly twisted/clipped; wait the full 1–2 minutes |
| Fuse won't blow | Slow fuse, weak cell, or poor lead contact | Use a fresh AA cell; clip leads firmly to fuse ends; try a different fuse; as a last resort touch the carrier wires directly to the fuse |
| Meter reads ohms wrong on everything | Leads in the wrong sockets | Black → COM, red → VΩ; current (mA/10A) sockets won't measure resistance |
| Student feels a strong shock / pain | (Should not happen at these voltages) Broken skin contact with 9 V | Stop; never apply the battery across broken skin; reassure — at 9 V across intact skin there is no hazard |


## 7. Age Differentiation Notes


**Younger students (12–14):**

* Pair them with a buddy or an adult helper for the meter setup (socket + dial). Pre-set their meter to the 200K range so they don't chase ranges.
* For the journal, accept a short cause sentence ("less resistance, more current, so heat") and a simple sketch.
* Let them focus on the *qualitative* result: which reading is bigger, which water conducts best — no numbers required beyond reading the display.

**Older students (15+) and adults (challenge extensions, no scores):**

* Have them **test whether doubling the probe distance doubles the resistance** on the forearm (measure at ¼″, ½″, ¾″, 1″ and look for the pattern) — a first taste of a controlled experiment and uncontrolled variables.
* Ask them to record actual ohm values for all five readings (tongue wet/dry, skin, 3 waters) and rank-order them, then predict and explain the ranking.
* Challenge: estimate roughly how much current flowed in the short circuit versus the tongue, using the resistance they measured — sets up next week's Ohm's Law.


## 8. Assessment


No grades, no quizzes. Class 1 has **no milestone demonstration** of its own — the Phase 1 milestone ("Explain the LED") comes after Class 2. Progress today is shown by:

* **Completion:** every team took the five resistance readings, shorted a cell, and blew a fuse.
* **Build journal:** a first four-part entry exists (what / observed / why / real-world link). It does not need to be polished — it needs to capture the team's own observation and a plausible cause.
* **Verbal explanation:** at least one student can say, out loud, why salt water conducts better and why the fuse blew.

Give feedback as questions, not scores: *"What would happen to the reading if your tongue were drier?"* Celebrate a good blown-fuse inspection or a sharp water-ranking explanation.


## 9. Instructor Tips


* **The fuse-blow is the showstopper — protect time for it.** It's the most memorable moment of Class 1 and the cleanest "theory of operation" payoff. If you're running behind, trim the lecture history and the probe-distance extension, not the fuse.
* **Pre-blow a fuse before class** so you always have a clear before/after pair under the magnifier, even if a team's fuse is stubborn.
* **Stock extra AA alkaline cells.** Shorting and fuse-blowing each drain a cell; teams will go through several. Running out mid-class kills momentum.
* **Let the tongue test be a little silly.** The laughter is the hook. Then immediately turn it into measurement — that pivot from "gross/funny" to "huh, I can measure that" is the whole pedagogy of the course.
* **"Ask, don't fix" in practice:** when a team's reading looks wrong, resist grabbing the probes. Ask "are the probes the same distance apart as last time?" and let them find it. This is the instructor habit the syllabus is built around.
* **Recovery if meters misbehave:** you can run all of Exp 1's lessons on a single shared "demo meter" at the front if several team meters fail — the qualitative result (wet < dry, salt < plain < distilled) shows clearly to the whole room.
* **Watch the clock at 0:35.** First-time hands-on always runs long. If the room isn't building by 0:35, stop talking and start them on Exp 1.


## 10. Resources & References

**Course text (students should have read Exp 1–2):**

* *Make: Electronics, 2nd Edition*, Charles Platt — [print][01] / free [PDF][02]. Class 1 covers Experiments 1–2.

**Instructor prep / background:**
* [Circuit Canvas][09] — makes it quick and easy to draw schematics and wiring diagrams.
* [The Electronics Club][12] — friendly entry-level explanations of voltage, current, resistance.
* [Electronics Tutorials][13] — a little more theory if you want depth on Ohms/Volts/Amps before class.
* [Electrical Engineering Basics][03]

**Student-facing enrichment (optional, after class):**
* [Best Explanation of Alternating Current Vs Direct Current](https://www.youtube.com/watch?v=CCHGatqIkAI&t=138s)
* [Electricity Water Analogy](https://www.mathsisfun.com/physics/electricity-water-analogy.html)
* [An intuitive approach for understanding electricity](https://www.youtube.com/watch?v=X_crwFuPht4)
* [Understanding the basics of electricity by thinking of it as water](https://www.freeingenergy.com/understanding-the-basics-of-electricity-by-thinking-of-it-as-water/)
* [Voltage, Current & Resistance: Electricity Explained Finally! (The Water Analogy)](https://www.youtube.com/watch?v=3qz1SVk1sRc)
* [Every Basic Electronic Component Explained in 21 Minutes](https://www.youtube.com/watch?v=HGNKhLActDo) — good overview as the course builds; resistors and fuses appear early.
* [Shock and Awe: The Story of Electricity -- Jim Al-Khalili BBC Horizon](https://www.youtube.com/watch?v=Gtp51eZkwoI)
* [Zap, Crackle and Pop: The Story of Electricity](https://www.youtube.com/watch?v=Ch6jti8i6u4)

For the Mathematically prepared:
* [Maxwell's Equations - The Ultimate Beginner's Guide](https://www.youtube.com/watch?v=F3QHUvr8d8I)
* [How Divergence and Curl Were Invented](https://www.youtube.com/watch?v=11QvV18JGQM)
* [Circuit Analysis Using Kirchhoff's Laws](https://www.youtube.com/watch?v=kZvhNDmLjEU)

**Course context:**
* [Makersmiths][05] — the makerspace hosting the course.
* [KidWind][04] — the wind-energy program this course connects to; today's volts/amps/ohms underlie every turbine generator.


---


[01]:https://www.amazon.com/Make-Electronics-Learning-Through-Discovery/dp/1680450263/
[02]:https://someplace-else.neocities.org/books/Make%20Electronics%202nd%20Edition.pdf
[03]:https://www.youtube.com/playlist?list=PLWv9VM947MKi_7yJ0_FCfzTBXpQU-Qd3K
[04]:https://kidwind.org/
[05]:https://makersmiths.org/event-6729146
[09]:https://circuitcanvas.com/
[12]:https://electronicsclub.info
[13]:https://www.electronics-tutorials.ws
