# Lesson Plan: Class 5 — Magnetism and Coils


* **Course:** Summer Electronics Course for Youth ([Makersmiths][05])
* **Class number:** 5 of 6
* **Phase:** 3 — Magnetism, Generation & the KidWind Capstone
* **Date:** Tuesday, July 21, 2026, 6:00–8:00 PM
* **Experiments:** Exp 25 *Magnetism* + Exp 28 *Making a Coil React* (*Make: Electronics, 2nd Ed.*)
* **Prerequisites from prior classes:** Classes 1–4 (Exp 1–11) — students can use a multimeter, know Ohm's Law, read a basic schematic, build on a **breadboard**, and have met resistors, LEDs, switches, relays, capacitors, and transistors. Crucially, they know from Class 3 that a **relay** uses a coil to switch contacts, and from Class 4 that a **capacitor** stores energy and charges on an RC curve. Students should have read Experiments 25 and 28 in the [book][01] beforehand.
* **Source of truth:** This plan implements [`syllabus.md`](syllabus.md), Class 5. Component costs and sourcing live in [`BOM.md`](BOM.md), never here.

> **About this plan.** It expands the syllabus's Class 5 outline into a minute-by-minute teaching guide. Class 5 **opens Phase 3** and crosses the bridge the whole course has been building toward: **electricity and magnetism are the same two-way street.** Students wind an electromagnet that picks up a paper clip (Exp 25), then build a breadboard circuit where one LED flashes as a coil's magnetic field *builds* and a second LED flashes as that field *collapses* (Exp 28) — seeing **self-inductance** ("electrical inertia") and the **collapsing-field pulse** with their own eyes. It weaves in the three lecture threads the syllabus calls for: a plain-language **explainer** (current makes magnetism; a coil is a flywheel for current; energy is stored *in the field*), **history & application** (Joseph Henry, the self-taught American who discovered self-inductance and got the *henry* named after him, working in parallel with Michael Faraday), and a real-device **theory of operation** (electromagnets in motors, speakers, and door locks; the flyback spark from a switched coil; why a diode sits across a relay coil — the very thing they saw inside the relay in Class 3). This class sets up Class 6, where the coil becomes half of a generator.


---


## 1. Class Overview


This is the first class of Phase 3, and it turns the course toward magnetism and power generation. Students start with the simplest, most satisfying build in the book: wind about 100 turns of wire onto a steel screwdriver, touch it to a 9-volt battery, and watch it pick up a paper clip — they've made an electromagnet, and proved that **electric current creates a magnetic field.** Then they move to the breadboard for a circuit that looks impossible at first: a coil, a small resistor, and an LED. Press the button and the LED flashes — even though current "should" just take the easy path through the coil. Add a second LED facing the other way, and now one LED flashes when you *press* the button and the other flashes when you *release* it. The release-flash is the payoff of the whole class: the coil's collapsing magnetic field dumps its stored energy back out as a brief pulse of electricity. That's **self-inductance**, the third and last basic property of passive components (after resistance and capacitance), and it's the reason a diode sits across the relay coil they cut open in Class 3. By the end, each team can explain why the second LED flashes *after* the button is released and name a real device that uses an electromagnet. Next week the same coil-and-magnet physics becomes a generator.


## 2. Learning Goals


After this class, students will be able to:

* Wind a coil on a steel core, energize it from a 9-volt battery, and use it to pick up a paper clip — demonstrating that current creates a magnetic field.
* Explain that coiling the wire and adding an iron core concentrate the magnetic field, and that more turns make a stronger magnet.
* Build the Exp 28 breadboard circuit and observe one LED flash as the field builds and a second LED flash as the field collapses.
* Explain **self-inductance** in plain language — a coil resists a *change* in current ("electrical inertia"), and stores energy in its magnetic field.
* Explain why the second LED flashes when the button is *released* (the collapsing field releases stored energy) and connect this to the diode across a relay coil from Class 3.


## 3. Preparation Checklist


Do these before students arrive:

* **The night before — Pre-wind the Exp 28 coils (critical, do not skip).** Per the syllabus, Class 5 does **not** depend on the long generator coil made in Class 6. Wind **one coil per team, ~100 ft of wire (≈300+ turns)** on identical forms (a film canister, marker, or short dowel) so the coils are comparable; secure with tape; leave ~6 in of stripped lead per end and label them. **Use 26-ga magnet wire for two teams and 22-ga hookup wire for the third** — same form, so the thin magnet-wire coils pack in noticeably more turns. (Scrape the enamel off magnet-wire ends; verify a low resistance end-to-end on the meter.) Keep the same team on **22-ga hookup wire** in Class 6, so they carry the "thick wire" side of the comparison through both experiments. Winding 300 turns takes real time — doing it live would eat the class.
* **45 min before — Build and test the Exp 28 circuit yourself.** Confirm the press-flash on the first LED and, with the second LED added the other way round, the release-flash. Know which orientation gives which behavior so you can coach it. Confirm with the **47 Ω** resistor (not a bigger one — see §9).
* **30 min before — Lay out the Exp 25 electromagnet kits.** Per team: one **large steel screwdriver** (Makersmiths-supplied; magnetic steel shaft, smooth so a clip can slide), a **9-volt battery + connector**, ~**6 ft of 22-gauge hookup wire**, a few **paper clips**, and a small piece of tape. Test that at least one of your screwdrivers actually works as a core before class — some stainless shafts are weakly magnetic.
* **25 min before — Lay out per-team Exp 28 workstations.** Per team: breadboard; the **pre-wound coil**; **47 Ω** resistor; **two low-current LEDs**; one **tactile (push) switch**; 9-volt battery + connector; pre-stripped jumpers (two colors); multimeter; small tools.
* **15 min before — Whiteboard two anchors:** (1) the two-way street — *"current → magnetism"* and *"moving magnet → current"* (today is the first; next week is the second); and (2) the coil-as-flywheel idea — a coil resists a *change* in current, builds a field slowly, and gives that energy back when the field collapses.
* **10 min before — Stage the Class 3 callback.** Have the cut-open relay (or its photo) from Class 3 handy: "Remember the coil inside this? Today is *why* that coil behaves the way it does, and why a diode lives next to it."
* **Have ready as spares:** extra low-current LEDs (the release-pulse can be rough on them if the coil is wound), extra pre-wound coils, extra 47 Ω resistors, spare screwdrivers/paper clips, pre-stripped jumpers.

> **Looking ahead to Class 6 (do this now):** Class 6 runs **per-team hand generators** — each team needs its own **~200-ft coil of 22-gauge hookup wire** wound on a short **3/4″ ID PVC tube** (so the strong 3/4″ × 1″ magnet can shuttle straight through it). No spinning rig, no plywood, no drilling this year. Winding 200 ft takes ~10 minutes per coil — start it tonight or recruit early-arriving parents to wind during *this* class so Class 6 isn't lost to coil-winding. Keep the **neodymium magnets** in your pocket/box until Class 6; they pinch hard (see §6 safety).


## 4. Materials & Components


Names and quantities only — see [`BOM.md`](BOM.md) for costs and sourcing. Only items used *this* class are listed.

| Item | Per team | Shared / notes |
|:-----|:--------:|:---------------|
| Large steel screwdriver | 1 | Exp 25 — the iron core of the electromagnet (Makersmiths-supplied) |
| 22-gauge hookup wire (for Exp 25 winding) | ~6 ft | Exp 25 — wound fresh on the screwdriver in class |
| Paper clip | 1–2 | Exp 25 — the thing the electromagnet picks up |
| Pre-wound coil, ≈100 ft / 300+ turns | 1 | Exp 28 — **wound before class** (see §3): two teams 26-ga magnet wire, one team 22-ga hookup (for the wire-type comparison) |
| 47 Ω resistor | 1 | Exp 28 — deliberately small so the brief LED flash is visible (see §9) |
| Low-current LEDs | 2 | Exp 28 — one for the build-up flash, one (reversed) for the collapse flash |
| Tactile (push) switch | 1 | Exp 28 — press to energize the coil, release to collapse the field |
| Solderless breadboard | 1 | Exp 28 |
| 9-volt battery + connector | 1 | Powers both experiments |
| Digital multimeter with leads | 1 | Check coil continuity / resistance; troubleshooting |
| Pre-stripped jumpers, 22-gauge | a few | Breadboard connections; two colors |
| Small screwdriver, pliers, wire strippers/cutters | 1 set | From Pack 1 |
| Build journal + pencil | 1 per student | Student-provided; primary record |

> **Capstone parts (neodymium magnets, the long generator coil) are NOT used this class** — they belong to Class 6. Keep them staged but out of reach.


## 5. Class Timeline


Follows the standard 2-hour session from the syllabus. This class is **lighter on build complexity than Class 4** (two short experiments, no dense multi-transistor circuit), which leaves room for the "why" to land — protect the discussion time, especially the collapsing-field reveal.

| Segment | Clock | Duration |
|:--------|:------|:--------:|
| 5a. Review & Q&A (Class 4 recap + phase pivot) | 0:00–0:15 | 15 min |
| 5b. Mini-Lecture (story first) | 0:15–0:35 | 20 min |
| 5c. Guided Builds (Exp 25 + Exp 28) | 0:35–1:30 | 55 min |
| 5d. "Explain It" Peer Share + Journal | 1:30–1:45 | 15 min |
| 5e. Wrap-Up & Next-Class Preview | 1:45–2:00 | 15 min |


### 5a. Review & Q&A — 0:00–0:15 (15 min)


**What to do**

* Recap Phase 2 in one line: "You've now controlled electricity with switches, relays, capacitors, and transistors — light *and* sound." Then pivot: "Every way we've controlled electricity so far, we've left out one big thing: **magnetism**. That's the whole rest of the course."
* Make the Class 3 callback concrete. Hold up the cut-open relay: "What made the contacts move?" (The coil — current through it became a magnet.) "Today we find out exactly how that works, and next week we run it *backwards* to make electricity."
* Surface pre-reading questions (Exp 25 and 28). Flag the one genuinely surprising result coming up: *a coil can make an LED flash after you stop pressing the button.* Plant it now so they watch for it.

**Time check:** Done by 0:15 — the builds are short, so a slightly longer review is fine here.


### 5b. Mini-Lecture (story first) — 0:15–0:35 (20 min)


Keep to 20 minutes. The builds are quick; the *understanding* is the work today.

**Key concept 1 — Current makes magnetism; a coil concentrates it (explainer).** "Run current through any wire and it becomes a (very weak) magnet — there's an invisible magnetic field wrapped around it." Draw the field looping around a straight wire. "Bend the wire into a loop and the field from each part adds up through the middle. Stack 100 loops into a coil and the field gets strong. Drop a steel screwdriver down the middle and it gets stronger still, because iron *concentrates* the field." That's all an electromagnet is — and it's the same coil that's inside the relay from Class 3 and inside every electric motor.

**Key concept 2 — A coil has "electrical inertia": self-inductance (explainer).** "A coil doesn't like to *change* what it's doing. When you first push current into it, it pushes back while it builds its magnetic field — so current rises *slowly*, not instantly." Use the flywheel/heavy-door analogy: hard to get moving, then hard to stop. "And here's the magic part: the energy you spent building that field is **stored in the field**. When you cut the power, the field collapses — and it shoves that stored energy back out as a brief pulse of electricity." This is **self-inductance**, the third basic property of components after resistance (Class 2) and capacitance (Class 4).

**Key concept 3 — What you'll see, and why it's the point (the payoff).** "In the breadboard circuit, you'll press a button and one LED flashes as the field builds. Add a second LED facing the other way, and when you *release* the button, *that* LED flashes — powered by the collapsing field, with the battery already disconnected." Tell them straight: "Electricity coming out of a coil *after* you turned off the power surprises everyone the first time. Watch for it." Then close the loop: "That after-pulse is exactly why a diode sits across a relay's coil (Class 3) — to safely soak up that pulse instead of letting it spark."

**Key concept 4 — History hook (history & application).** The unit of inductance, the **henry**, is named for **Joseph Henry** (1797–1878) — the son of a day laborer in Albany, New York, who called himself "principally self-educated," built the first powerful electromagnets, and discovered self-inductance. He later ran the brand-new **Smithsonian Institution**. An Englishman named **Michael Faraday** (the *farad*, from Class 4) was discovering the same magnetic ideas at the same time, each unaware of the other. *Theory of operation:* this one principle runs every electric motor, every loudspeaker, every solenoid door lock, the ignition coil that sparks a gasoline engine, and — next week — every generator.

**Common misconception:** students think the coil "stores electricity like a little battery." Correct it: the coil stores energy in its **magnetic field**, only while current is flowing, and only for a split second after — it's a flywheel, not a battery. (Contrast with the capacitor from Class 4, which stores charge on its plates and can hold it.)

**Time check:** Wrap by 0:35. If long, cut the Faraday aside; keep the collapsing-field setup.


### 5c. Guided Builds — 0:35–1:30 (55 min)


Two experiments, ~55 minutes. Suggested split: **Exp 25 ~15 min · Exp 28 ~40 min.** Exp 28 (the collapsing-field circuit) is the heart of the class — protect its time. Helpers circulate and **ask questions rather than fix.**

---


#### Experiment 25 — *Magnetism* (≈15 min)


**Step 1 — Wind the coil.** Wind about **100 turns** of 22-gauge wire neatly around the screwdriver shaft, near the tip, within about a 2-inch length — you'll have to wind over previous turns to fit them. Tape the last turn so it can't unravel. Leave a few inches of lead at each end.

**Step 2 — Pick up a paper clip.** Touch the two wire ends to the 9-volt battery terminals and bring the screwdriver tip near a paper clip lying on a smooth surface — the clip jumps to the tip. Let go of one wire and the clip drops (if the screwdriver isn't permanently magnetized).

* **Safety / heat:** a coil across a 9-volt battery is *close to a short circuit* (like Exp 2 in Class 1) — the wire and battery get **warm**. Connect only for a few seconds at a time; don't leave it hooked up. This is also why we use a 9-V, not a big battery.
* If a screwdriver is *already* slightly magnetic and grabs the clip with no power, slide the clip just out of reach first, then apply power so the jump is unmistakable.

**Step 3 — Make it stronger (optional/older students).** More turns = stronger magnet. Have them add turns and feel the difference, or pick up two clips.

**Checkpoint — Exp 25 "done":** team has lifted a paper clip with the powered screwdriver and can say "current through the coil made the iron a magnet; no current, no magnet."

---


#### Experiment 28 — *Making a Coil React* (≈40 min)


The heart of the class: see self-inductance and the collapsing field with two LEDs. Build from the schematic (book Fig. 5-34) / breadboard (Fig. 5-35).

**Step 1 — Build the one-LED version.** Wire it up: 9 V → **tactile switch** → **47 Ω** resistor → then the line splits in parallel into (a) the **coil** and (b) **one low-current LED** → back to negative. The puzzle to pose first: *"Current can flow straight through the coil — so why would the LED ever light?"*

**Step 2 — Press and observe.** Press the button. The LED **flashes briefly**, then goes dark even while the button is held. Why? *(explainer):* at the instant of switch-on, the coil's self-inductance momentarily *blocks* current (it's building its field), so current detours through the LED. Once the field is established, current takes the easy path through the coil and the LED goes out.

**Step 3 — Add the second LED for the collapse (the reveal).** Add a **second low-current LED in parallel, facing the opposite direction** (book Fig. 5-36/5-37). Press the button — first LED flashes as before. **Release** the button — now the **second LED flashes**, powered by the coil's collapsing field after the battery path is broken. Let every team see this. This is the moment of the class.

* **Don't run it without the coil:** with the coil removed, the 47 Ω won't protect the LEDs and you'll pop them. The coil is doing real work even when it looks idle.
* **Why 47 Ω (not 470 Ω):** the pulse is brief; the small resistor keeps the flash bright enough to see. (See §9.)

**Step 4 — Tie it back (say this out loud).** "The release-flash is the surge a coil makes whenever you switch it off. In Class 3 we put a diode across the relay coil — *this* pulse is what that diode tames. Same physics, on your breadboard."

**Checkpoint — Exp 28 "done":** the circuit flashes one LED on press and the other on release, and the team can say the release-flash is the collapsing magnetic field giving its stored energy back.

**Time check:** the two-LED version should be working for every team by ~1:25 so the peer share has something to show.


### 5d. "Explain It" Peer Share + Journal — 1:30–1:45 (15 min)


**Peer share.** One or two teams demonstrate the two-LED circuit and answer the key question aloud: *"Why does the second LED flash after you let go of the button?"* (The magnetic field built up in the coil collapses and pushes its stored energy back out as a brief pulse.) Celebrate good reasoning, not just a working board. This is the standard syllabus "Explain It" share; there is **no phase milestone this class** (Phase 3's "Make Power" milestone is in Class 6).

**Wire-type teaser (sets up Class 6).** Two teams' coils are wound with thin **26-ga magnet wire** and one with thick **22-ga hookup wire**. Hold them side by side: same ~100 ft, but the thin wire packs more turns into the same space. Plant the question — *does more turns make a stronger effect?* — which they'll **measure directly** with the hand generators next week.

**Journal milestone (this class).** The syllabus asks each student to: *explain why the second LED flashes after the button is released (collapsing field) and name a device that uses an electromagnet.* Four-part template:

1. **What I built** — a screwdriver electromagnet; a coil-and-two-LED breadboard circuit.
2. **What I observed** — the electromagnet lifted a paper clip only with power on; one LED flashed on press, the other on release.
3. **What's physically happening** — "current makes the coil a magnet; the field stores energy; when current stops, the collapsing field pushes a pulse back out and lights the second LED" (self-inductance).
4. **Real-world link** — an electromagnet device: electric motor, loudspeaker, relay, solenoid door lock, or junkyard crane magnet.

**Time check:** share + journals wrapped by 1:45.


### 5e. Wrap-Up & Next-Class Preview — 1:45–2:00 (15 min)


**Restate what they should have learned:**

* Electric current creates a magnetic field; coiling the wire and adding an iron core concentrate it into a usable electromagnet.
* A coil has "electrical inertia" (self-inductance): it resists a change in current and stores energy in its magnetic field.
* When the current stops, the field collapses and gives that energy back as a brief pulse — the reason the second LED flashes and the reason a diode guards a relay coil.

**KidWind tie-in (build the bridge to Class 6):** "Today you saw the first half of the two-way street: **current makes magnetism**. A coil and a magnetic field belong together. Next week we run it the *other* way — move a magnet through a coil and the coil makes electricity. That's exactly what the heart of a KidWind wind turbine does: the wind spins magnets past coils, and out comes power. You've just built and understood *half* of a generator."

**Preview Class 6 — Generating Your Own Power (Experiment 26 + Wrap-Up):** "Next week is the payoff of the whole course. You'll move a powerful magnet through a big coil and light an LED with electricity *you* generated — no battery. Then we connect the entire course to KidWind and look at where this path could go next."

**Assignment:** Read **Experiment 26** before next class. Finish the journal milestone (collapsing-field explanation + an electromagnet device). Optional enrichment that pairs with next week: [Every Type of Electric Generator Explained][09].

**Safety heads-up for next class:** "Next week we use **neodymium magnets** — they're incredibly strong, they pinch hard enough to blister, and they can wreck phones and cards. We'll handle them carefully and keep them away from your devices."


## 6. Troubleshooting Guide


| Problem | Likely cause | Fix |
|:--------|:-------------|:----|
| Electromagnet won't pick up the clip | Battery contact not solid, or screwdriver shaft is non-magnetic stainless | Press leads firmly to the battery terminals; try a known-magnetic steel screwdriver; make sure ~100 turns are wound |
| Clip sticks even with power off | Screwdriver became (or already was) permanently magnetized | Slide the clip out of range first, then power on so the jump is clearly from the current |
| Electromagnet wire/battery getting hot | Normal — a coil across 9 V is near-short | Connect only a few seconds at a time; don't leave it powered |
| Exp 28: no LED flash at all on press | LED reversed, coil lead not seated, or switch not closing | Check LED polarity (long lead = +); reseat both coil leads; confirm the tactile switch actually closes |
| Press-flash works, but no flash on release | Second LED missing, same-direction, or its leg is loose | The second LED must face the **opposite** direction from the first; reseat it; verify with the meter |
| Both LEDs glow steadily (don't flash) | A wire is bypassing the coil, or the coil is open/broken | Trace the circuit against Fig. 5-34; meter the coil end-to-end (should read a low resistance, not open) |
| LEDs are very dim / hard to see the flash | Resistor too large, or coil has too few turns | Use the **47 Ω** (not 470 Ω); use the full pre-wound ~100-ft coil — more turns store more energy |
| LED popped / went dark permanently | Circuit was run with the coil removed, so nothing limited current | Replace the LED; never run this circuit without the coil in place |
| Coil reads "open" on the meter | Magnet-wire ends not scraped clean of enamel | Scrape/sand the enamel off the last 1/2 in of each lead until the meter reads < ~100 Ω |


## 7. Age Differentiation Notes


**Younger students (12–14):**

* Let the wins be physical and obvious: the paper-clip jump and the surprise release-flash. Keep the "why" to one sentence — "the magnet's energy comes back out when it disappears."
* Provide the coil already wound (everyone gets this) and a labeled copy of the Fig. 5-35 breadboard layout showing exactly which hole each leg goes in.
* Pair with a buddy or adult for the two-LED orientation step — facing the LEDs the right way is the one fiddly part.

**Older students (15+) and adults (challenge extensions, no scores):**

* Meter the coil's resistance and reason about why a low-resistance coil still "blocks" the initial current (it's the *changing* current it resists, not steady current).
* Try the book's variation (Fig. 5-38/5-39): swap the coil for a **1,000 µF capacitor** (mind polarity) and a 470 Ω resistor and compare — the capacitor does the *opposite* of the coil, lighting on press and fading, which sharpens the resistor/capacitor/coil comparison.
* Have them wind extra turns on the Exp 25 electromagnet and quantify the effect (how many clips? at what distance?), then predict what a Class 6 generator coil will need.
* Recruit them to help wind the **Class 6 per-team generator coils** (~200 ft each, on 3/4″ ID PVC tubes) — a genuine contribution that also previews next week.


## 8. Assessment


No grades, no quizzes. **There is no phase milestone in Class 5** — Phase 3's "Make Power" demonstration happens in Class 6. This class uses the standard ongoing assessment:

* **"Explain It" peer share (see §5d):** a team explains why the second LED flashes on release. Give feedback as questions: *"Where did that pulse of electricity come from, if the battery was already disconnected?"*
* **Journal milestone (this class):** the collapsing-field explanation plus one real device that uses an electromagnet. Completion-based. Celebrate clear reasoning and good real-world examples (motor, speaker, relay, door lock, crane magnet).


## 9. Instructor Tips


* **Pre-wind the Exp 28 coils — this is the single most important prep item.** A live 300-turn wind would consume the class. Hand teams a finished coil and spend the time on the physics. (Also start the **Class 6** per-team ~200-ft generator coils now; they're even longer.)
* **Make the release-flash a moment.** Build the one-LED version first so they see the press-flash and wonder about it; *then* add the reversed LED and have everyone press-and-release together. The "wait — it lit up *after* I let go?!" reaction is the emotional core of Phase 3. Don't rush past it.
* **Keep the 47 Ω resistor.** It looks too small to protect an LED, and that's the point: the inductive pulse is brief, so the small resistor keeps the flash visible. A 470 Ω makes the flash too faint to see. Never run the circuit *without* the coil, though — then nothing limits the current and the LEDs pop.
* **Use the cut-open relay from Class 3 as your spine.** Open on it ("what moved the contacts?"), and close on it ("this pulse is why the relay has a diode"). It ties Phase 3 directly back to something they already built, and makes self-inductance feel like an answer rather than a new topic.
* **Watch for stainless screwdrivers.** Some shafts are weakly magnetic and the electromagnet fizzles. Test your screwdrivers beforehand and set aside the ones that work as cores.
* **Mind the heat on Exp 25.** The coil-across-9V is essentially a short; tell teams to tap power for a few seconds, not hold it. Warm wire is expected; hot is the cue to disconnect.
* **"Ask, don't fix":** for a circuit that flashes on press but not release, resist rewiring it. Ask: "Which way is each LED facing?" Comparing the two LED orientations is the reasoning win of the day.
* **Don't let neodymium magnets out early.** Keep them staged for Class 6. If a student finds them, you'll spend the class on magnet play (and pinched fingers).


## 10. Resources & References


**Course text (students should have read Exp 25 and 28):**

* *Make: Electronics, 2nd Edition*, Charles Platt — [print][01] / free [PDF][02]. Class 5 covers Experiments 25 and 28. (Exp 25 introduces Joseph Henry and the two-way relationship; Exp 28 demonstrates self-inductance and the collapsing field.)

**Instructor prep / background:**

* [Doctronics][11] — clear breadboard and schematic illustrations for coil/inductor circuits.
* [The Electronics Club][12] — friendly explanations of electromagnets, coils, and relays.
* [Electronics Tutorials][13] — deeper background on inductance and self-inductance if you want it.

**Student-facing enrichment (optional, points toward Class 6):**

* [Every Type of Electric Generator Explained][09] — sets up the Class 6 generator capstone; the coil they built today becomes half of a generator next week.

**Course context:**

* [Makersmiths][05] — the makerspace hosting the course.
* [KidWind][04] — the wind-energy program this course connects to; a turbine's generator is a magnet spinning past coils, the principle this class begins and Class 6 completes.


---


[01]:https://www.amazon.com/Make-Electronics-Learning-Through-Discovery/dp/1680450263/
[02]:https://someplace-else.neocities.org/books/Make%20Electronics%202nd%20Edition.pdf
[04]:https://kidwind.org/
[05]:https://makersmiths.org/
[09]:https://www.youtube.com/watch?v=-7CyYxqIacg
[11]:http://www.doctronics.co.uk
[12]:https://electronicsclub.info
[13]:https://www.electronics-tutorials.ws
