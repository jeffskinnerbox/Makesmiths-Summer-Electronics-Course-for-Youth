# Lesson Plan: Class 6 — Generating Your Own Power


* **Course:** Summer Electronics Course for Youth ([Makersmiths][05])
* **Class number:** 6 of 6
* **Phase:** 3 — Magnetism, Generation & the KidWind Capstone
* **Date:** Tuesday, July 28, 2026, 6:00–8:00 PM
* **Experiments:** Exp 26 *Tabletop Power Generation* + course Wrap-Up (*Make: Electronics, 2nd Ed.*)
* **Prerequisites from prior classes:** Classes 1–5 (Exp 1–11, 25, 28) — students can use a multimeter (including **AC volts** and **millivolts**), know Ohm's Law, read a schematic, build on a breadboard, and — most importantly from Class 5 — know that **current creates a magnetic field** and that a coil stores energy in that field. They also saw in Class 2 that a lemon can make electricity chemically. Students should have read Experiment 26 in the [book][01] beforehand.
* **Source of truth:** This plan implements [`electronics-primer-syllabus.md`](../electronics-primer-syllabus.md), Class 6. Component costs and sourcing live in [`BOM.md`](../BOM.md), never here.

> **About this plan.** It expands the syllabus's Class 6 outline into a minute-by-minute teaching guide. Class 6 is the **finale of the course** and the **Phase 3 / KidWind capstone**. Students complete the two-way street they started in Class 5: there they made *magnetism from current*; here they make **current from a moving magnet** — electromagnetic induction — and light an LED with electricity they generated, no battery. It carries the three lecture threads the syllabus calls for: a plain-language **explainer** (a moving magnet pushes electrons in a coil; faster motion / more turns / stronger magnet → more output), **history & application** (Faraday and Henry independently discovering induction in 1831; the rise of electric power), and a real-device **theory of operation** (generators and alternators; hydro, diesel, and **wind** turbines; bicycle dynamos and hand-crank flashlights). The class ends with the **"Make Power" milestone**, an explicit KidWind discussion, a recap of the whole six-week arc, and a preview of where the path could go next. Per the syllabus *(Appendix A, Q3)*, which offers a whole-class spinning-generator rig only "if time and prep allow," this course runs the **per-team hand-generator** path: every team shuttles a strong magnet through its own coil to light an LED — no spinning rig and no drilling this year.


---


## 1. Class Overview


This is the last class, and it's the payoff of everything. In Class 5 students proved that running current through a coil makes a magnet. Today they run it backwards: they move a magnet through a coil and watch electricity appear — first as millivolts on the multimeter, then, with a bigger coil and a stronger magnet, as a real flicker of light from a low-current LED powered by nothing but their own hand motion. That's **electromagnetic induction**, and it's the single most important idea in the course, because nearly every watt of electricity on the grid — hydro, coal, gas, nuclear, and **wind** — is made exactly this way: something spins a magnet past a coil. Teams discover that moving the magnet *faster*, using *more* turns of wire, or a *stronger* magnet all make more electricity. They complete the **Phase 3 "Make Power" milestone** by lighting an LED from a moving magnet and explaining how this is the same principle a KidWind wind turbine uses. The class — and the course — closes with a recap of the whole six-week journey from "what is electricity?" to "I generated my own," an explicit KidWind connection, and a look at what a future Intermediate course could add.


## 2. Learning Goals


After this class, students will be able to:

* Move a magnet through a coil and measure the induced voltage on a multimeter (AC millivolts), demonstrating that a moving magnet generates electricity.
* Light a low-current LED using only a hand-moved magnet and a coil — no battery.
* Explain that faster motion, more turns of wire, and a stronger magnet all increase the generated output.
* Compare two coils wound from different wire (thin magnet wire vs. thick hookup wire) and explain why the coil with more turns generates more — and why real generators are wound with magnet wire.
* Explain the complete two-way relationship: current makes magnetism (Class 5) **and** a moving magnet makes current (today).
* Explain how a wind turbine — including a KidWind turbine — uses this exact principle: spinning blades turn a magnet-and-coil generator into electricity.


## 3. Preparation Checklist


Do these before students arrive. **Magnet and coil prep is the make-or-break item** — induction demos fail quietly when the coil is too small or the magnet too weak.

* **Before class day — Wind one generator coil per team, on identical short 3/4″ ID PVC tubes** (bore sized so the strong 3/4″ × 1″ magnet slides straight through). **Wind two coils from 26-ga magnet wire and one from 22-ga hookup wire**, building each to about the same physical size on the tube — so the thin magnet-wire coils end up with **many more turns** than the bulky hookup-wire coil. This is deliberate: the class compares the two wire types' output in §5c. Winding takes ~10 min per coil — start during Class 5 (recruit older students/parents), and keep the **same team on 22-ga hookup** as in Class 5. Leave ~6 in of stripped lead per end, tape the winding, scrape the enamel off magnet-wire ends, and confirm a low end-to-end resistance (not open).
* **Per-team hand generators — no rig, no drilling this year** *(syllabus Appendix A, Q3 fallback)*. There is no plywood spool, dowel handle, or hole-saw work: a team simply shuttles the magnet through the PVC-tube coil by hand (or drops it in and rattles it). This removes the rig's drilling-safety burden entirely.
* **25 min before — Build and TEST a working generator yourself.** Clip a meter set to **AC volts (~2 V range)** across a coil and shuttle the **3/4″ × 1″** magnet through the PVC tube — you should see tenths of a volt; the peaks are higher than the averaged reading. Then attach a **low-current LED** in place of the meter and move the magnet *vigorously* — confirm a visible flicker. **If the LED won't light, flip the magnet end-for-end and try again.** Know the motion that works before class.
* **20 min before — Lay out workstations.** Per team: the PVC-tube generator coil; a **strong 3/4″ × 1″ neodymium magnet** (staged carefully — see safety). If you have only one strong magnet, plan for teams to **rotate through it** for the LED moment. Plus: multimeter with alligator leads; **low-current LEDs** (have spares — pulses can be rough on them); optional **1N4001 diode** + **1,000 µF capacitor** for the charge-a-capacitor extension; and the lemon battery from Class 2 if you want the callback prop.
* **15 min before — Whiteboard the capstone picture:** the two-way street completed (*current → magnetism* | *moving magnet → current*), and a simple sketch: **wind → blades spin → magnet spins past coils → electricity** = a wind turbine = KidWind.
* **10 min before — Magnet safety station.** Set the ground rules you'll repeat (below). Keep a clear, nonmagnetic work area; keep magnets away from phones, cards, and the multimeter.

> **Neodymium magnet safety — say this out loud and enforce it** *(syllabus Safety Notes)*: these magnets are extremely strong. They **pinch hard enough to blood-blister** when they snap together or to steel — keep fingers out of the gap. They are **brittle and can shatter** (eye protection when slamming is possible). They **wreck phones, credit/transit cards, and hard drives**, and can interfere with pacemakers — keep them well away from devices and pockets. Never put a magnet near the mouth (serious swallowing hazard). Handle one at a time on a clear surface.


## 4. Materials & Components


Names and quantities only — see [`BOM.md`](../BOM.md) for costs and sourcing. Only items used *this* class are listed.

| Item | Per team | Shared / notes |
|:-----|:--------:|:---------------|
| Generator coil on a short 3/4″ ID PVC tube | 1 | **Wound before class** (see §3): **two teams use 26-ga magnet wire, one uses 22-ga hookup wire** on identical tubes, so the class can compare. The more turns, the more output. PVC bore sized so the strong magnet slides through |
| Neodymium cylinder magnet, 3/4″ × 1″ axially magnetized | 1 | The strong magnet each team shuttles through its coil; **rotate one shared magnet** if only one is available |
| Low-current LEDs | 1–2 | The thing you light with generated power; spares — pulses can be rough |
| Digital multimeter with alligator leads | 1 | Set to **AC volts / millivolts** to read the induced voltage |
| 1N4001 diode + 1,000 µF capacitor | optional | Older-student extension: rectify the AC pulses and read DC volts on the capacitor |
| Build journal + pencil | 1 per student | Student-provided; primary record + course keepsake |

> The **multimeter and batteries are Makersmiths-supplied**; the **magnets and coil wire are shared capstone purchases**, and a short **3/4″ ID PVC tube** per team is pulled from the makerspace stock as the coil form (see BOM). No spinning rig is built this year, so no drill is needed. No 9-volt battery is needed to *generate* power today — that's the whole point.


## 5. Class Timeline


Follows the standard 2-hour session from the syllabus. The build is short and dramatic; the **milestone, recap, and KidWind close get a full half-hour** because this is the last class.

| Segment | Clock | Duration |
|:--------|:------|:--------:|
| 5a. Review & Q&A (Class 5 recap + the big flip) | 0:00–0:15 | 15 min |
| 5b. Mini-Lecture (story first) | 0:15–0:35 | 20 min |
| 5c. Guided Build (Exp 26 per-team generators) | 0:35–1:25 | 50 min |
| 5d. "Make Power" Milestone + Journal | 1:25–1:45 | 20 min |
| 5e. Course Wrap-Up & What Comes Next | 1:45–2:00 | 15 min |


### 5a. Review & Q&A — 0:00–0:15 (15 min)


**What to do**

* Recap Class 5 in one question: *"What did the coil do when you switched it off?"* (Its collapsing magnetic field pushed out a pulse of electricity — the second LED flashed.) Then make the flip explicit: "Last week, *current* made a magnetic field. Today we do the reverse — we'll *move a magnet* and let it make current. That completes the two-way street."
* Connect back further: in Class 2 they made electricity *chemically* (the lemon battery). "Today is the other way humans make electricity — and it's the way almost all of it is actually made."
* Surface pre-reading questions (Exp 26). Set the stakes: "By the end of class you'll light a light with electricity you generated with your own hand. Then we'll talk about how that's exactly what a wind turbine does."

**Time check:** Done by 0:15.


### 5b. Mini-Lecture (story first) — 0:15–0:35 (20 min)


Keep to 20 minutes — they need bench time to feel it.

**Key concept 1 — A moving magnet pushes electrons: induction (explainer).** "A magnet sitting still next to a coil does nothing. But *move* it — change the magnetic field through the coil — and it shoves the electrons in the wire, making them flow. That flow is electricity you generated." Stress the word **change**: it's the *motion*, the changing field, that does it. Stop moving and the current stops.

**Key concept 2 — More motion, more turns, more magnet → more power (explainer).** Three knobs, and students will test all three: move the magnet **faster**; use **more turns** of wire; use a **stronger magnet**. Each one increases the voltage. "This is why a real generator spins fast, has big coils, and uses powerful magnets." Today the "more turns" knob is built right into the coils: the teams with thin **magnet-wire** coils packed in many more turns than the team with thick **hookup wire** — and you'll see it in the output.

**Key concept 3 — This is how the world makes electricity (theory of operation).** "Almost every power plant is the same trick at huge scale: *something* spins a magnet past coils. In a hydro dam, falling water spins it. In a coal or gas or nuclear plant, steam spins it. In a **wind turbine**, the wind spins it. The only big exception is solar panels." Everyday versions: a bicycle dynamo lighting a headlamp, a hand-crank flashlight, the alternator charging a car battery.

**Key concept 4 — History hook (history & application).** In **1831**, **Michael Faraday** in England and **Joseph Henry** in America (the *henry*, from Class 5) independently discovered electromagnetic induction — that a moving magnet makes current. Within a few decades this one discovery grew into the entire electric-power industry and rewired civilization. "You're about to repeat their experiment by hand."

**Common misconception:** students think the coil or magnet is "full of electricity" that gets released. Correct it: nothing is stored — the magnet's *motion* (your muscle energy) is what's converted into electrical energy, moment by moment. Stop moving, no power. A generator is an energy *converter*, not an energy *container*.

**Time check:** Wrap by 0:35.


### 5c. Guided Build — 0:35–1:25 (50 min)


One core experiment, with a measurement stage and a light-it stage, plus an optional capacitor extension. Helpers circulate and **ask questions rather than fix.**

---


#### Experiment 26 — *Tabletop Power Generation* (≈40 min)


**Step 1 — Measure the induced voltage.** Set the meter to **AC volts / millivolts** and clip it across the two ends of the generator coil. Shuttle the **3/4″ × 1″** magnet quickly back and forth through the PVC-tube coil. The meter shows tenths of a volt. "That number is electricity you just made — and it's *averaging* the pulses, so the peaks are actually higher."

* **Why AC:** as the magnet goes in, current flows one way; as it comes out, it flows the other way — alternating current. (Tie-in to Class 5: each LED flashed for one direction of current.)

**Step 2 — Test the three knobs.** Have teams move the magnet **faster** (bigger reading), then reason about the other two knobs — **more turns** and a **stronger magnet** — using their own coil as the baseline. Let them see speed move the number in real time.

**Step 3 — Light the LED (the moment).** Replace the meter with a **low-current LED** clipped across the coil. Move the magnet **vigorously** — the LED flickers. "No battery. That light is you." If it won't light, **flip the magnet end-for-end** (an LED only passes current one way, so it lights on one stroke direction).

* It must be a **low-current LED** — a generic LED needs too much current to light from a hand-moved generator.
* If the class shares one strong magnet, run Steps 1–2 on whatever magnet each team has, then **rotate the strong 3/4″ × 1″ magnet** team-to-team for the LED flash so everyone gets the moment.

**Step 4 — Compare the wire types (whole-class observation).** Line up the coils: two are wound from thin **26-ga magnet wire**, one from thick **22-ga hookup wire**, on identical tubes. Using the **same magnet and the same brisk motion**, read the meter for each coil (swap coils around the room). The magnet-wire coils — many more turns in the same space — generate **more voltage** and light the LED more easily. Ask: *"Same magnet, same motion — why does one coil make more electricity?"* (More turns; thin wire fits more of them.) Land the payoff: **this is exactly why generators and wind-turbine coils are wound with fine magnet wire, not fat hookup wire** — and it's the "more turns" knob from the mini-lecture, made real.

**Checkpoint — Exp 26 "done":** the team has made the meter read a generated voltage, lit a low-current LED by moving a magnet (no battery), and seen that the higher-turn magnet-wire coil out-generates the thick hookup-wire coil.

---


#### Optional extension (older students): rectify to DC and charge a capacitor


Insert a **1N4001 diode** in series and a **1,000 µF capacitor** across the output; switch the meter to **DC volts**. The diode passes only one direction of the AC pulses, charging the capacitor to a small steady DC voltage — a hand-cranked version of how generated AC is turned into usable DC. Two opposed LEDs also nicely show the current reversing on the in-stroke vs. the out-stroke.

**Time check:** every team should have lit an LED by ~1:20 so the milestone can start on time.


### 5d. "Make Power" Milestone + Journal — 1:25–1:45 (20 min)


This is the final phase milestone, so it gets the full 20 minutes — make it celebratory.

**Phase 3 Milestone — "Make Power" (completion-based, no scores).** Each team **lights an LED from a moving magnet** and explains, in their own words, **how this is the same principle a KidWind wind turbine uses** — wind spins blades, blades spin a magnet past coils, the coils make electricity. 60–90 seconds per team, applause for each. Every team that can generate the light and draw the turbine connection has completed Phase 3 — and the course. (If teams shared one strong magnet, just queue the demos so each team lights its own coil.)

**Journal milestone (this class).** The syllabus asks each student to: *explain how moving the magnet made the LED light, and describe how a wind turbine uses the same idea.* Four-part template:

1. **What I built** — a magnet-and-coil generator (a magnet shuttled through a coil on a tube).
2. **What I observed** — the meter read a voltage only while the magnet moved; faster motion and more turns gave more; the **thin magnet-wire coil out-generated the thick hookup-wire coil**; the LED lit with no battery.
3. **What's physically happening** — "a moving magnet changes the field through the coil and pushes electrons through the wire" (electromagnetic induction).
4. **Real-world link** — a generator that uses this: wind turbine (KidWind!), hydro dam, bicycle dynamo, hand-crank flashlight, car alternator.


### 5e. Course Wrap-Up & What Comes Next — 1:45–2:00 (15 min)


This is the close of the whole course — slow down and make it land.

**Recap the six-week arc (let students do it).** Ask the room to rebuild the journey: *electricity is a flow* (Class 1) → *resistance & Ohm's Law, and making a battery* (Class 2) → *switches, relays, automatic control* (Class 3) → *capacitors, transistors, light & sound* (Class 4) → *current makes magnetism* (Class 5) → *a moving magnet makes electricity* (Class 6). "You went from 'what *is* electricity?' to generating your own. That's a real arc."

**KidWind connection (the capstone point).** "Everything pointed here. A KidWind turbine is a generator with blades on it: wind turns the rotor, the rotor spins magnets past coils, and out comes the electricity — the exact thing you just did by hand. Every choice in turbine design (more turns, stronger magnets, faster spin, matching the load with Ohm's Law) is something you now understand from the inside."

**What comes next** *(syllabus Appendix A, Q8).* This was the **Primer**, the first of a possible three-part path (Primer / Intermediate / Advanced). A future **Intermediate** course would add **soldering**, **integrated circuits**, the **555 timer**, and **digital logic** — building permanent projects instead of breadboard experiments. Students who want to keep going can get their own kit (see the BOM) and keep their build journals as a record.

**Final word.** Thank the students, the parents/helpers, and the teams. Encourage them to keep the journal and keep asking "what's physically happening?" — the habit that matters more than any one circuit.

**Optional enrichment:** [Every Type of Electric Generator Explained][09] — a perfect after-course watch now that they've built one.


## 6. Troubleshooting Guide


| Problem | Likely cause | Fix |
|:--------|:-------------|:----|
| Meter reads ~0 while moving the magnet | Meter on DC (induced output is AC), or lead not clipped to bare wire | Switch to **AC volts/mV**; confirm both coil ends are stripped/clean and clipped |
| Tiny reading, magnet barely does anything | Too few turns or slow motion | Use the full ~200-ft coil and the strong 3/4″ × 1″ magnet; move faster; magnet must pass *through* the coil, not just near it |
| LED won't light at all | Generic (not low-current) LED, or too little generated current | Use a **low-current LED**; move the magnet vigorously through the tube; make sure it's the strong magnet |
| LED still won't light, meter shows voltage | LED passes current only one way; wrong stroke direction | **Flip the magnet end-for-end** and try again; try clipping the LED the other way |
| Coil reads "open" on the meter | A lead isn't stripped to bare copper | Re-strip the last 1/2 in of each lead until the meter reads a low resistance |
| Magnet jams / won't slide in the PVC tube | Magnet diameter too close to the tube bore, or burrs at the ends | Use a tube whose bore clears the magnet; deburr the ends; a hair of clearance is enough |
| Magnet suddenly slams to something steel | Neodymium magnets grab hard from a distance | Keep a clear nonmagnetic area; keep tools, the meter, and other magnets clear; warn before handing one over |
| Capacitor extension shows no DC | Diode backwards, or capacitor polarity reversed | Flip the 1N4001; confirm the capacitor's + lead toward the diode; keep moving the magnet to keep charging |


## 7. Age Differentiation Notes


**Younger students (12–14):**

* Lead with the magic, keep the words simple: "moving the magnet pushes the electricity; stop moving and it stops." The lit LED is the whole win.
* Make sure they get a turn with the strong 3/4″ × 1″ magnet so the effect is obvious and not fiddly — the lit LED is the whole win.
* Pair with a buddy or adult for clipping the meter/LED leads; let them own the *moving the magnet* part.

**Older students (15+) and adults (challenge extensions, no scores):**

* Do the **rectify-and-charge-a-capacitor** extension (1N4001 + 1,000 µF, meter on DC) and explain why a diode turns AC pulses into usable DC.
* Quantify the three knobs: record voltage vs. speed, vs. number of turns (and **wire gauge** — magnet wire vs. hookup wire), vs. magnet — and connect it to the syllabus challenge ("wind a coil that lights the LED most brightly, and explain what you changed").
* Use two opposed LEDs to show current reverses with stroke direction, and relate it to the Class 5 two-LED collapsing-field circuit and to AC.
* Discuss the load/Ohm's-Law angle: why a turbine's output must be matched to what it's driving.


## 8. Assessment


No grades, no quizzes. This class carries the **final phase milestone** and closes the course:

* **Phase 3 Milestone — "Make Power":** each team lights an LED from a moving magnet and explains how it's the same principle a KidWind turbine uses (see §5d). Completion-based, celebratory — not scored. If teams share one strong magnet, queue the demos so each lights its own coil; the bar is generating power and explaining it.
* **Journal milestone (this class):** how moving the magnet lit the LED, plus a wind-turbine (or other generator) real-world link. Give feedback as questions: *"What would happen to the LED if the blades spun faster — and why?"* Celebrate the completed six-week journal as the record of the whole course.


## 9. Instructor Tips


* **Test a working generator before class — twice.** Induction demos fail silently when the coil is too small or the magnet too weak. Confirm both the meter reading and a visibly flickering low-current LED at the bench (with the strong 3/4″ × 1″ magnet through the PVC-tube coil), and memorize the motion that works.
* **Wind the per-team coils ahead of time.** ~10 minutes per coil; do it during Class 5 with helpers, on identical short 3/4″ ID PVC tubes — **two coils from 26-ga magnet wire, one from 22-ga hookup wire** so the class can compare wire types. Don't lose the finale to coil-winding.
* **"Flip the magnet" is your most common fix.** A low-current LED only lights on one current direction; half the "it doesn't work" cases are solved by reversing the magnet. Teach helpers this first.
* **If you have only one strong magnet, plan the rotation.** Have every team get its meter reading on whatever magnet it has, then pass the strong 3/4″ × 1″ magnet team-to-team for the LED flash and the milestone — a quick queue, not a bottleneck.
* **No rig, no drill this year.** The per-team hand generators need no plywood spool and no hole-saw work, which removes the rig's drilling-safety burden entirely — keep it simple.
* **Respect the magnets out loud, every time you hand one over.** The strong magnets pinch hard, can shatter, and kill phones/cards. Clear nonmagnetic area, one magnet at a time, away from devices.
* **Let the recap be theirs.** In the wrap-up, ask the students to reconstruct the six-week arc rather than reciting it yourself — it's the best evidence (and feeling) that they learned it.
* **End on the KidWind sentence.** "Wind spins a magnet past a coil, and that's electricity" should be the last technical thing they hear — it ties the capstone to the program several of them are in.


## 10. Resources & References


**Course text (students should have read Exp 26):**

* *Make: Electronics, 2nd Edition*, Charles Platt — [print][01] / free [PDF][02]. Class 6 covers Experiment 26 (and completes the induction story begun in Exp 25/28).

**Instructor prep / background:**

* [Doctronics][11] — clear schematics and breadboard illustrations.
* [The Electronics Club][12] — friendly explanations of coils, magnets, and generators.
* [Electronics Tutorials][13] — deeper background on electromagnetic induction if you want it.

**Student-facing enrichment (optional, after the course):**

* [Every Type of Electric Generator Explained][09] — pairs directly with this capstone; how the magnet-and-coil idea scales up to real power plants and wind turbines.
* [Every Type of Battery Explained][10] — a callback to the Class 2 lemon battery, the *other* way to make electricity.

**Course context & where this leads:**

* [Makersmiths][05] — the makerspace hosting the course.
* [KidWind][04] — the wind-energy program this course's capstone connects to; a turbine is a magnet-and-coil generator with blades. A future Intermediate Makersmiths course (soldering, ICs, 555 timer, logic) would extend the path.


---


[01]:https://www.amazon.com/Make-Electronics-Learning-Through-Discovery/dp/1680450263/
[02]:https://someplace-else.neocities.org/books/Make%20Electronics%202nd%20Edition.pdf
[04]:https://kidwind.org/
[05]:https://makersmiths.org/
[09]:https://www.youtube.com/watch?v=-7CyYxqIacg
[10]:https://www.youtube.com/watch?v=2G6Rn99sVmM
[11]:http://www.doctronics.co.uk
[12]:https://electronicsclub.info
[13]:https://www.electronics-tutorials.ws
