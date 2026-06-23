# Lesson Plan: Class 3 — Switches, Relays, and Automatic Control


* **Course:** Summer Electronics Course for Youth ([Makersmiths][05])
* **Class number:** 3 of 6
* **Phase:** 2 — Controlling Electricity
* **Date:** Tuesday, July 7, 2026, 6:00–8:00 PM
* **Experiments:** Exp 6 *Very Simple Switching* + Exp 7 *Investigating a Relay* + Exp 8 *A Relay Oscillator* (*Make: Electronics, 2nd Ed.*)
* **Prerequisites from prior classes:** Classes 1–2 (Exp 1–5) — students can use a multimeter (resistance, voltage, current, and now **continuity**), know Ohm's Law, and have built LED circuits with alligator-clip test leads. Students should have read Experiments 6–8 in the [book][01] beforehand.
* **Source of truth:** This plan implements [`syllabus.md`](syllabus.md), Class 3. Component costs and sourcing live in [`BOM.md`](BOM.md), never here.

> **About this plan.** It expands the syllabus's Class 3 outline into a minute-by-minute teaching guide. Class 3 opens **Phase 2 (Controlling Electricity)** and carries two brand-new literacy skills the book introduces here: **reading a schematic** and **using a solderless breadboard**. It weaves in the three lecture threads the syllabus calls for: a plain-language **explainer** (a relay is a switch that electricity flips by itself; feedback → oscillation), **history & application** (Scribner's jack-knife switch and the telephone switchboard; the relay in telegraph and early computing), and a real-device **theory of operation** (car starter relay; electromechanical buzzer/doorbell). Like Class 2, it is full — three experiments plus two new skills — so the plan flags exactly where to triage.


---


## 1. Class Overview


This is the first class of Phase 2, where the course shifts from *measuring and predicting* current to *controlling* it. Students start by reading and building from real schematics — wiring two switches so that either one turns an LED on or off (the same circuit as a stairway light). They then investigate a relay — a switch that an electromagnet flips automatically — using the meter's continuity mode to discover what closes inside, and (adult-supervised) cutting one open to see the coil and contacts. Finally they graduate from alligator clips to the **solderless breadboard** for the first time, building a relay circuit and then modifying it so the relay switches *itself* on and off — an oscillator that buzzes and clicks. By the end, students can read a basic schematic, explain how a small signal controls a large one through a relay, and explain how feedback makes an oscillator run on its own. This sets up Class 4, where the same breadboard, plus capacitors and transistors, turns flashing into sound.


## 2. Learning Goals


After this class, students will be able to:

* Read a basic schematic — identify the symbols for a battery, resistor, LED, switch, pushbutton, and relay, and tell connected wires (dot) from crossing wires (no dot).
* Wire two SPDT switches so either switch toggles an LED, and explain "poles" and "throws."
* Use the meter's **continuity** mode to map which contacts close inside a relay when its coil is energized.
* Build a working circuit on a **solderless breadboard** for the first time, understanding the power buses.
* Explain how a relay oscillator uses feedback to switch itself on and off — and why it keeps clicking.


## 3. Preparation Checklist


Do these before students arrive:

* **40 min before — Build all three circuits yourself.** Wire the two-switch LED circuit (Exp 6), the relay continuity test (Exp 7), and the breadboard relay oscillator (Exp 8). The breadboard oscillator is the one most likely to misbehave — get it buzzing once tonight so you know the working layout cold.
* **30 min before — Pre-strip a handful of jumper wires** in two colors (red for positive, blue/black for negative) for the breadboard build, plus a few spares. First-time breadboarders lose a lot of time stripping wire — pre-made jumpers keep momentum.
* **25 min before — Pre-open one relay yourself** (shave the plastic shell with a utility knife) so every team can see the coil, lever, and contacts without each team cutting their own. Keep it as a circulating "show" specimen.
* **20 min before — Lay out per-team workstations.** Per team: multimeter; 9-volt battery + battery connector; **2 toggle switches (SPDT or DPDT)**; **2 DPDT 9V relays** (one to investigate, one to keep intact for the oscillator); **tactile (push) switch**; 2 generic LEDs; 470 Ω resistor; **1,000 µF capacitor**; **solderless breadboard**; pre-stripped jumpers; ~5 alligator test leads; screwdriver, pliers, wire strippers/cutters.
* **15 min before — Draw the two reference diagrams** on the board: (1) the schematic symbol key (battery, resistor, LED, switch, pushbutton, relay, "dot = connected / cross = not connected"), and (2) a sketch of the breadboard showing the two power **buses** down the sides (red = +, blue = −) and that rows connect in short strips.
* **10 min before — Stage the relay-opening station** with a utility knife and cutting mat — **adult-supervised only.**
* **Have ready as spares:** extra relays (cutting one open can wreck it), extra LEDs, pre-stripped jumpers, a spare breadboard.


## 4. Materials & Components


Names and quantities only — see [`BOM.md`](BOM.md) for costs and sourcing. Only items used *this* class are listed.

| Item | Per team | Shared / notes |
|:-----|:--------:|:---------------|
| Digital multimeter with leads | 1 | Used in **continuity** mode today |
| 9-volt battery | 1 | Powers all three experiments |
| 9-volt battery connector | 1 | Connects battery to the breadboard (Exp 8) |
| Toggle switches, SPDT or DPDT | 2 | Exp 6 two-switch circuit |
| DPDT 9V relay | 2 | One to investigate/cut open (Exp 7); one kept intact for the oscillator (Exp 8) |
| Tactile (push) switch | 1 | Exp 7 + Exp 8 |
| Generic LEDs | 2 | Exp 6 + Exp 8 |
| Resistor 470 Ω (yellow-violet-brown) | 1 | Protects the LED(s) |
| Capacitor, 1,000 µF electrolytic | 1 | Slows the Exp 8 oscillator to an audible click `[VERIFY]` exact placement |
| Solderless breadboard | 1 | First breadboard use of the course (Exp 8) |
| Hookup wire / pre-stripped jumpers, 22-gauge | a few | Breadboard connections; two colors |
| Test leads with alligator clips | ~5 | Exp 6 + Exp 7 |
| Screwdriver, pliers, wire strippers/cutters | 1 set | From Pack 1 |
| Utility knife | shared | Adult-supervised; cutting a relay open (Exp 7) |
| Build journal + pencil | 1 per student | Student-provided; primary record |


## 5. Class Timeline


Follows the standard 2-hour session from the syllabus. **This class is full** (three experiments + two new skills) — keep the time checks. Triage guidance is in §9.

| Segment | Clock | Duration |
|:--------|:------|:--------:|
| 5a. Review & Q&A (Class 2 recap) | 0:00–0:10 | 10 min |
| 5b. Mini-Lecture (story + reading schematics) | 0:10–0:30 | 20 min |
| 5c. Guided Builds (Exp 6 + Exp 7 + Exp 8) | 0:30–1:30 | 60 min |
| 5d. "Explain It" Peer Share + Journal | 1:30–1:45 | 15 min |
| 5e. Wrap-Up & Next-Class Preview | 1:45–2:00 | 15 min |


### 5a. Review & Q&A — 0:00–0:10 (10 min)


**What to do**

* Recap Phase 1 in one question: *"What's Ohm's Law, and what does it tell you?"* (V = I × R; it predicts current/resistor values.) If the Phase 1 "Explain the LED" milestone got squeezed at the end of Class 2, run it now — 60 seconds per team.
* Frame the shift: "For two weeks we measured and predicted electricity. Starting today we *control* it — turning it on and off, and getting circuits to control themselves."
* Confirm meters can do **continuity** (set to the sound-wave/diode symbol; touch the two probes together — it should beep).

**Time check:** Done by 0:10. The builds and the new schematic skill need every minute.


### 5b. Mini-Lecture (story + reading schematics) — 0:10–0:30 (20 min)


Keep to 20 minutes. Two jobs: hook interest with the relay story, and teach enough schematic-reading to build from a diagram.

**Key concept 1 — Reading a schematic (the new literacy skill).** "Up to now you built from pictures of alligator clips. Real electronics uses schematics — a cleaner map. The map doesn't tell you *where* to put parts, only *how they connect*." Point at the symbol key on the board:

* **Battery** = long line (+) and short line (−). **Resistor** = zigzag. **LED** = triangle with two little arrows (triangle points the way conventional current flows, + to −; long lead is +). **Switch** = a pole and a contact. **Pushbutton** = normally-open momentary contact. **Relay** = a switch drawn next to a coil.
* **The crossover rule (say it twice):** wires that simply cross are **not** connected; a **fat dot** means they *are* connected.
* Mention the book's color help: red wires = positive, blue = negative/ground (a book convention, not universal). Positive runs along the top, negative along the bottom.

**Key concept 2 — Poles and throws (explainer).** A toggle switch's lever connects a center **pole** to one **throw** (contact) or the other. SPST = simple on/off (single-pole, single-throw). SPDT = single-pole, double-throw — flips between two contacts. "Two SPDT switches wired together give you the stairway-light trick: either switch flips the light, no matter what the other one is doing."

**Key concept 3 — A relay is a switch electricity flips by itself.** Inside a relay is an electromagnet (a coil). Send a small current through the coil and its magnetic field physically yanks a switch closed — which can control a *much* bigger current. "A small signal controls big power, with no finger on the switch. That's the seed of all automatic control."

* **Theory of operation (real device):** when you turn your car key, a tiny switch sends a small current to a relay; the relay closes a fat connection that feeds the starter motor *hundreds* of amps. The key never carries that current. Old top-loading washing machines did the same with the lid switch.

**Key concept 4 — Feedback makes an oscillator (history & application).** "What if a relay is wired so that closing it cuts off its own coil? It clicks open — which powers the coil again — which clicks it closed... forever. That self-cycling is **oscillation**, and you'll hear it buzz today." History hook: telephone switchboards were once patched by hand with Charles Scribner's 1878 "jack-knife switch" (that's why we still call audio plugs "jacks"); operators were replaced by **relays**, and relays later by transistors (next class). Relays ran the first automatic telephone exchanges and early computers.

**Common misconception:** students think a relay is just a fancy switch. Stress the leverage: the control side and the switched side are *electrically separate* — a weak circuit commands a strong one. That separation is the whole point.

**Time check:** Wrap by 0:30. If long, cut the history aside; the schematic key and poles/throws are the must-teach.


### 5c. Guided Builds — 0:30–1:30 (60 min)


Three experiments, ~60 minutes. Suggested split: **Exp 6 ~15 min · Exp 7 ~22 min · Exp 8 ~23 min.** Exp 8 (first breadboard) is the marquee build — protect its time. Helpers circulate and **ask questions rather than fix.**

---


#### Experiment 6 — *Very Simple Switching* (≈15 min)


**Step 1 — Build from the schematic.** Hand each team the two-switch schematic (book Fig. 2-37/2-38). Using alligator leads, wire: 9V → switch 1 → switch 2 → 470 Ω → LED → back to battery, with the two SPDT switches cross-wired so either can break or complete the path. **Long lead of the LED toward positive.**

**Step 2 — Discover the stairway behavior.** Flip either switch. Whatever state the LED is in, *either* switch changes it. Ask: *"This is the circuit for a light at the top and bottom of a staircase — why does that need two switches that each work?"*

**Checkpoint — Exp 6 "done":** the LED toggles from *either* switch, and the team can point to the pole and the two throws on a switch.

---


#### Experiment 7 — *Investigating a Relay* (≈22 min)


**Step 1 — Hear the click.** Wire the tactile switch so pressing it sends 9V to the relay's two **coil** pins (the isolated pair). Press — you'll hear/feel a faint click as the internal switch moves. (Touch the relay to feel the vibration if the room is noisy.)

**Step 2 — Map the contacts with continuity.** Set the meter to continuity. Clip the probes (use test leads for hands-free) across a pair of the relay's switch pins. Press the coil button and listen:

* With the coil **off** (relaxed), one pair of contacts is connected (beeps) — the "normally closed" pair.
* Press the button (coil **on**) and a *different* pair connects instead. The magnetic field threw the internal switch from one contact to the other.
* Move a probe to the neighboring pin and the behavior reverses. Let teams reason out the internal wiring by elimination.

**Step 3 — Look inside (adult-supervised).** Bring the **pre-opened relay** around (or, if a team is fast and an adult is free, let them shave one open with the utility knife — **cut away from the body, downward, on the mat**). Point out the **coil** (electromagnet), the **lever/armature** it pulls, and the **contacts** the lever moves between. Connect it back to what the continuity test proved.

* **Safety:** the utility knife is adult-only. Most teams should learn from the shared pre-opened specimen, not cut their own.

**Checkpoint — Exp 7 "done":** team can state which contacts close when the coil is energized and has seen the coil + contacts inside.

---


#### Experiment 8 — *A Relay Oscillator* — first breadboard (≈23 min)


The marquee build: the course's first **solderless breadboard** circuit, and a relay that switches *itself*.

**Step 1 — Meet the breadboard.** Show the board: the two long strips down the sides are the power **buses** (rails) — positive on the left, negative on the right; the short rows in the middle each connect a handful of holes. "Push a component leg into a hole and it's electrically joined to everything else in that strip — no clips, no solder." Note the buses may have a **gap/break** in the middle that sometimes needs a jumper to bridge.

**Step 2 — Build the relay circuit (book Fig. 2-62).** Plug in the relay (coil pins toward the bottom), two LEDs (long leg toward +), the 470 Ω resistor, the tactile switch, and jumpers per the diagram. Connect the battery via its connector to the buses. **Power on:** one LED lights. **Press the button:** the relay closes and the second LED lights. "Congratulations — your first breadboarded circuit."

**Step 3 — Make it oscillate (book Fig. 2-69/2-70).** Rewire so the pushbutton draws its power *through the relay's own contact* (rotate the tactile switch and add the one extra jumper shown). Now press the button: the relay **buzzes**. Why? In its relaxed state the contact feeds power to the coil's control path; energizing the coil throws the switch, which *cuts* that feed; the switch falls back, which reconnects the feed — and it cycles, fast, on its own. That self-feeding loop is feedback-driven oscillation.

> **The capacitor:** wiring the **1,000 µF capacitor** into the circuit slows the buzz into a slower, audible *click-click-click* by storing and releasing charge each cycle — a preview of the capacitor timing you'll measure next class. `[VERIFY]` exact capacitor placement against your pre-built circuit before class.

**Checkpoint — Exp 8 "done":** the relay oscillates (buzz or click) on its own while powered/pressed, and the team can say in a sentence why it keeps going.

**Time check:** all three wrapped by 1:30. If behind, the oscillator is the must-finish; Exp 6 and the continuity map can be trimmed (see §9).


### 5d. "Explain It" Peer Share + Journal — 1:30–1:45 (15 min)


**What to do**

* Pick one team to explain **what's inside the relay** (coil → magnetic field → moves the switch), pointing at the opened specimen. Pick a second team to explain **why the oscillator keeps clicking by itself.**
* Everyone writes their journal entry. The syllabus sets this class's **journal milestone**: *sketch the relay's inside and explain in one or two sentences why the oscillator keeps clicking by itself.* Four-part template:
    1. **What I built** — two-switch LED circuit; relay continuity test; breadboard relay oscillator.
    2. **What I observed** — either switch toggles the LED; contacts that close on the coil; the relay buzzing/clicking on its own.
    3. **What's physically happening** — "the coil's magnetic field throws the switch, which cuts its own power, so it cycles."
    4. **Real-world link** — car starter relay; doorbell/buzzer; stairway light.

**What to watch for**

* "It just buzzes" with no mechanism. Nudge: "What happens to the coil's power the instant the switch closes?"

**Time check:** journals under way by 1:45.


### 5e. Wrap-Up & Next-Class Preview — 1:45–2:00 (15 min)


**Restate what they should have learned:**

* A schematic is a connection map — symbols and dots, not positions.
* A relay lets a small current switch a much bigger one, with the two sides electrically separate — the basis of automatic control.
* Wire a relay to cut its own coil and it oscillates — feedback makes it run by itself.
* A breadboard joins parts through hidden strips; the side rails are the power buses.

**KidWind tie-in:** "A wind turbine needs control and protection circuitry — something that lets a small sensor signal switch real generated power on or off, or disconnect a fault. A relay is the simplest version of exactly that: a small signal commanding big power. You just built the idea every turbine controller is based on."

**Preview Class 4 — Capacitors, Transistors, Light & Sound (Experiments 9–11):** "Today a relay clicked because of feedback. Next week you'll do it with no moving parts at all — capacitors that store charge and time things, and transistors that switch and amplify. You'll build a circuit that flashes a light, then speeds up until you *hear* it as a tone through a speaker."

**Assignment:** Read **Experiments 9–11** before next class. Finish the journal milestone (relay sketch + why the oscillator clicks). Optional: spot a relay or a two-switch stairway light in your home.


## 6. Troubleshooting Guide


| Problem | Likely cause | Fix |
|:--------|:-------------|:----|
| LED won't toggle from both switches | One switch mis-wired (using throws as poles) | Center terminal is the pole; the two outer terminals are the throws — re-check against the schematic |
| Relay makes no click when button pressed | Power not reaching the **coil** pins | Identify the isolated pair (the coil); confirm 9V across them; check the tactile switch is actually closing |
| Continuity meter never beeps on relay pins | Wrong pin pair, or meter not in continuity | Touch probes together to confirm continuity mode beeps; try other pin pairs by elimination |
| Breadboard circuit completely dead | Battery not on the buses, or a bus gap not bridged | Confirm + and − reach the side rails; jumper across any mid-board bus break |
| One section of the board has no power | Bus has a break in the middle | Add a jumper bridging the gap in that rail |
| LED on breadboard won't light | LED reversed, or leg in the wrong strip | Long leg toward +; make sure each leg is in a different strip (not shorted in one row) |
| Relay won't oscillate (just sits) | Feedback jumper missing/mis-placed | The pushbutton must draw power *through* the relay contact — re-check the extra jumper |
| Oscillator buzzes too fast to hear distinct clicks | That's normal without the capacitor | Add the 1,000 µF capacitor to slow it to an audible click |
| Relay cracked/dead after cutting | Knife went too deep | Use the spare relay; only shave the shell, stop at a hair-thin opening |


## 7. Age Differentiation Notes


**Younger students (12–14):**

* Give them the pre-stripped jumpers and a labeled copy of the breadboard layout (which hole gets which part). The breadboard's hidden connections are the hardest new idea — a picture helps.
* For schematics, focus on recognizing four symbols (battery, resistor, LED, switch) and the dot-vs-cross rule; skip the relay symbol's internals.
* Pair with a buddy or adult for the continuity mapping in Exp 7.

**Older students (15+) and adults (challenge extensions, no scores):**

* **Challenge (from the syllabus):** make the relay oscillator click as **fast** as possible — experiment with what changes the rhythm (and predict what the capacitor will do before adding it).
* Have them fully map the relay's internal wiring from continuity alone, then check it against the opened specimen.
* Ask them to redraw the breadboard circuit as a clean schematic, or vice versa — translating between the two representations.


## 8. Assessment


No grades, no quizzes. This class has **no phase milestone** (the Phase 2 milestone, "Light and Sound," comes after Class 4). Progress shows through:

* **Completion:** each team toggled the two-switch circuit, mapped the relay contacts with continuity, and got the breadboard oscillator running.
* **Journal milestone (this class):** a sketch of the relay's interior plus one–two sentences on why the oscillator self-clicks. Completion-based — the mechanism matters more than artistry.
* **Verbal explanation:** at least one student can explain how the coil throws the switch and why that creates oscillation. Give feedback as questions: *"What cuts the coil's power the moment it pulls the switch over?"*


## 9. Instructor Tips


* **Triage if you fall behind (you might — three experiments + two new skills):** the breadboard oscillator (Exp 8) is the centerpiece — protect it. If short on time, (1) keep Exp 6 to a single quick "either switch works" demonstration, (2) use only the shared pre-opened relay instead of teams cutting their own, and (3) shorten the continuity mapping to one pin pair. Never cut Exp 8.
* **Pre-strip jumpers and pre-open a relay.** These two prep steps save the most time. First breadboarding plus wire-stripping plus knife work would otherwise eat the whole hour.
* **The breadboard's hidden connections are the #1 confusion.** Before teams build, hold up the board and trace one row and one bus with your finger. Many "dead circuit" problems are just two legs sharing one strip (a short) or a leg one hole off.
* **Mind the bus gap.** The single-bus boards have mid-rail breaks. When the bottom half of a circuit has no power, it's almost always a missing jumper across that gap — check it first.
* **Let the buzz be the payoff.** The self-oscillating relay is genuinely delightful — a machine that runs itself. Let teams enjoy it before you explain the feedback; the explanation lands better after the grin.
* **"Ask, don't fix":** for a dead relay circuit, resist re-seating parts yourself. Ask "is power actually getting to the coil?" and hand them the meter. Continuity tracing is the diagnostic skill of the day.
* **Safety on the knife:** keep the relay-opening to an adult-run station, cutting away from the body and down toward the mat. It only takes one careless slip.


## 10. Resources & References


**Course text (students should have read Exp 6–8):**

* *Make: Electronics, 2nd Edition*, Charles Platt — [print][01] / free [PDF][02]. Class 3 covers Experiments 6–8.

**Instructor prep / background:**

* [Doctronics][11] — especially good for **schematic symbols and breadboard layout** illustrations; review before teaching 5b.
* [The Electronics Club][12] — friendly explanations of switches, relays, and reading circuit diagrams.
* [Electronics Tutorials][13] — deeper background on relays and electromagnetic switching.

**Student-facing enrichment (optional, after class):**

* [Every Basic Electronic Component Explained in 21 Minutes][08] — covers switches, relays, and the breadboard.

**Course context:**

* [Makersmiths][05] — the makerspace hosting the course.
* [KidWind][04] — the wind-energy program this course connects to; turbines need relay-style control and protection.


---


[01]:https://www.amazon.com/Make-Electronics-Learning-Through-Discovery/dp/1680450263/
[02]:https://someplace-else.neocities.org/books/Make%20Electronics%202nd%20Edition.pdf
[04]:https://kidwind.org/
[05]:https://makersmiths.org/
[08]:https://www.youtube.com/watch?v=HGNKhLActDo
[11]:http://www.doctronics.co.uk
[12]:https://electronicsclub.info
[13]:https://www.electronics-tutorials.ws
