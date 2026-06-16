# Lesson Plan: Class 4 — Capacitors, Transistors, Light & Sound


* **Course:** Summer Electronics Course for Youth ([Makersmiths][05])
* **Class number:** 4 of 6
* **Phase:** 2 — Controlling Electricity
* **Date:** Tuesday, July 14, 2026, 6:00–8:00 PM
* **Experiments:** Exp 9 *Time and Capacitors* + Exp 10 *Transistor Switching* + Exp 11 *Light and Sound* (*Make: Electronics, 2nd Ed.*)
* **Prerequisites from prior classes:** Classes 1–3 (Exp 1–8) — students can use a multimeter (resistance, voltage, current, continuity), know Ohm's Law, can read a basic schematic, and have built on a **breadboard** (the relay oscillator). Students should have read Experiments 9–11 in the [book][01] beforehand.
* **Source of truth:** This plan implements [`electronics-primer-syllabus.md`](../electronics-primer-syllabus.md), Class 4. Component costs and sourcing live in [`BOM.md`](../BOM.md), never here.

> **About this plan.** It expands the syllabus's Class 4 outline into a minute-by-minute teaching guide. Class 4 **closes Phase 2** with the course's first circuit that has a purpose — a flasher that speeds up into a sound synthesizer — and the **Phase 2 milestone demonstration ("Light and Sound")**. It weaves in the three lecture threads the syllabus calls for: a plain-language **explainer** (resistor-as-faucet / capacitor-as-balloon; an oscillator so fast you *hear* it), **history & application** (Faraday and the farad; Bardeen/Brattain/Shockley and the 1948 transistor; vacuum tubes → solid state), and a real-device **theory of operation** (blinking timers; how a tone is generated; transistors as the building block of all modern electronics). Like Classes 2–3, it is full — three experiments, the last one complex — so the plan flags exactly where to triage.


---


## 1. Class Overview


This is the final class of Phase 2, and it brings together everything so far into a circuit that does something genuinely fun. Students first time a capacitor charging through a resistor, discovering the RC time constant — why a capacitor fills up fast at first and then ever more slowly. They meet the transistor with a memorable "finger test" (their own skin's tiny current, amplified, lights an LED) and learn it acts as both a switch and an amplifier. Then they build the marquee project: a two-transistor astable multivibrator that flashes an LED about once a second — and by swapping in smaller capacitors, they speed the oscillation up until the flashing becomes too fast to see and instead becomes an audible **tone** through a loudspeaker. By the end, each team can demonstrate the **Phase 2 milestone ("Light and Sound")** — light, then sound, from one circuit — and explain what the capacitor and transistor are each doing. This is the bridge to Phase 3 (Classes 5–6), where the course turns to magnetism and generating electricity.


## 2. Learning Goals


After this class, students will be able to:

* Charge a capacitor through a resistor and explain why it fills quickly at first, then slowly (the RC time constant, T = R × C).
* Explain a capacitor with the balloon analogy and state that it stores charge and blocks DC but passes a sudden change (AC).
* Demonstrate that a transistor uses a tiny base current to control a much larger current — acting as both a **switch** and an **amplifier**.
* Build a two-transistor oscillator that flashes an LED, and change components to change the flash rate.
* Speed the oscillator up until the flashing becomes an audible tone, and change its pitch — the Phase 2 "Light and Sound" demonstration.


## 3. Preparation Checklist


Do these before students arrive:

* **45 min before — Build the Exp 11 flasher yourself and get it making sound.** This is the most complex circuit of the whole course (two-transistor astable multivibrator + a third transistor driving the LED, plus the speaker). Build it once tonight, confirm it flashes ~1 Hz, then confirm that swapping the timing capacitors speeds it into an audible tone. Know the working layout cold.
* **35 min before — Pre-strip a generous set of jumpers** (red = +, blue/black = −) plus spares — the flasher is crowded and first-timers lose big time stripping wire mid-build.
* **30 min before — Sort and label the capacitors** into a tray: the Exp 9 set (0.1 µF, 1 µF, 10 µF, 100 µF, 1,000 µF) and the Exp 11 timing set (notably **3.3 µF** for the ~1 Hz flash, plus smaller values like 0.1 µF / 0.01 µF for the tone). Electrolytics have **polarity** — point out the minus stripe / short lead now.
* **25 min before — Lay out per-team workstations.** Per team: breadboard; multimeter; 9-volt battery + connector; **2 tactile switches**; **2N2222 transistors (several — they're fragile; have spares)**; **500 K trimmer potentiometer**; generic LEDs; **8-ohm loudspeaker (1″–2″)**; the sorted resistor set (470 Ω, 1 K, 4.7 K, 100 K, 220 K, 470 K) and capacitor set; small screwdriver; pliers; wire strippers/cutters; pre-stripped jumpers.
* **15 min before — Draw two boards' worth of reference on the whiteboard:** (1) the RC idea (`T = R × C`; capacitor = balloon, resistor = faucet; "63% per time constant"); and (2) the transistor pinout (collector / base / emitter) with "tiny base current controls big collector current."
* **10 min before — Pre-build a spare Exp 11 flasher** to keep as a known-good reference/loaner — if a team's build won't run, they can still see and hear the goal and do the milestone.
* **Have ready as spares:** extra 2N2222 transistors (fragile, easily damaged), extra electrolytic capacitors, extra LEDs, pre-stripped jumpers, the spare pre-built flasher.


## 4. Materials & Components


Names and quantities only — see [`BOM.md`](../BOM.md) for costs and sourcing. Only items used *this* class are listed.

| Item | Per team | Shared / notes |
|:-----|:--------:|:---------------|
| Solderless breadboard | 1 | All three experiments |
| Digital multimeter with leads | 1 | Times the capacitor charge (volts DC) in Exp 9 |
| 9-volt battery + connector | 1 | Powers all three experiments |
| Tactile (push) switches | 2 | Exp 9 charge (A) / discharge (B) |
| 2N2222 transistor | several | Exp 10 (1) + Exp 11 (needs **6**); fragile — keep spares. **Not** P2N2222 |
| 500 K trimmer potentiometer | 1 | Exp 10 — control the transistor's base voltage |
| Generic LEDs | 1–2 | Exp 9, 10, 11 |
| 8-ohm loudspeaker, 1″–2″ | 1 | Exp 11 — turns the fast oscillation into sound |
| Resistors: 470 Ω, 1 K, 4.7 K, 100 K, 220 K, 470 K | assorted set | Exp 9–11 (the 4.7 K + 470 K set the flash timing) |
| Capacitors: 0.01–1,000 µF assortment (incl. **3.3 µF**, 1,000 µF) | assorted set | Exp 9 RC timing; Exp 11 flash rate / pitch. Electrolytics have polarity |
| Small screwdriver, pliers, wire strippers/cutters | 1 set | From Pack 1 |
| Hookup wire / pre-stripped jumpers, 22-gauge | a few | Breadboard connections; two colors |
| Build journal + pencil | 1 per student | Student-provided; primary record |


## 5. Class Timeline


Follows the standard 2-hour session from the syllabus. **This class is full and the last build is complex** — keep the time checks. Triage guidance is in §9.

| Segment | Clock | Duration |
|:--------|:------|:--------:|
| 5a. Review & Q&A (Class 3 recap) | 0:00–0:10 | 10 min |
| 5b. Mini-Lecture (story first) | 0:10–0:30 | 20 min |
| 5c. Guided Builds (Exp 9 + Exp 10 + Exp 11) | 0:30–1:30 | 60 min |
| 5d. "Light and Sound" Milestone + Journal | 1:30–1:50 | 20 min |
| 5e. Wrap-Up & Next-Class Preview | 1:50–2:00 | 10 min |


### 5a. Review & Q&A — 0:00–0:10 (10 min)


**What to do**

* Recap Class 3 in one question: *"Why did the relay oscillator keep clicking by itself?"* (Feedback — closing it cut its own power, so it cycled.) Connect forward: "Today we make something oscillate with no moving parts at all, and speed it up until you *hear* it."
* Surface pre-reading questions (Exp 9–11). Flag the new components: capacitor (stores charge) and transistor (the heart of all modern electronics).
* Confirm boards/meters are ready; remind teams electrolytic capacitors and transistors have a right way round.

**Time check:** Done by 0:10 — the complex Exp 11 build needs the hour.


### 5b. Mini-Lecture (story first) — 0:10–0:30 (20 min)


Keep to 20 minutes. Set up three builds; the flasher will teach itself once it's running.

**Key concept 1 — A capacitor stores charge; the balloon analogy (explainer).** "A capacitor is two metal plates with a gap — it can't pass steady DC, but it can store charge." Use the board picture: the resistor is a faucet, the capacitor is a balloon you're filling. Open the faucet a little (big resistor) and the balloon fills slowly; open it more (small resistor) and it fills faster. And as the balloon fills, it pushes back — so filling **slows down** as it goes. That's the RC time constant: **T = R × C**. Each time constant adds 63% of the *remaining* gap, so it never quite "finishes" — like a greedy guy who always eats 63% of the cake that's left.

**Key concept 2 — The transistor: a tiny current controls a big one (explainer).** "Today's other new part is the most important component ever invented." A transistor has three legs — collector, base, emitter. A *tiny* current into the base controls a *much* larger current through the other two. That makes it two things at once: a **switch** (base current on/off → main current on/off) and an **amplifier** (small base change → big output change). You'll prove it by letting the trickle of current through your own finger light an LED.

**Key concept 3 — Flashing vs. hearing: an oscillator's speed (the payoff).** "Combine capacitors (for timing) and transistors (for switching) and you get an oscillator with no moving parts — like last week's relay, but solid-state." If it cycles about once a second, you *see* an LED flash. Speed it up past ~20 times a second and your eye can't follow it — but a speaker turns those fast pulses into a **tone you hear**. "Same circuit. The only difference between a blinking light and a musical note is *speed*." Smaller timing capacitors = faster = higher pitch.

**Key concept 4 — History hook (history & application).** The **farad** is named for **Michael Faraday** (1791–1867), a bookbinder's apprentice who taught himself science and discovered electromagnetic induction — the idea behind Classes 5–6. The **transistor** was invented at Bell Labs in **1948** by Bardeen, Brattain, and Shockley (Nobel Prize 1956); Shockley's company seeded **Silicon Valley**. Transistors replaced bulky, hot vacuum tubes and made it possible to shrink electronics from room-sized to pocket-sized. *Theory of operation:* every blinking timer, every tone generator, and effectively every modern gadget is built from exactly these two parts.

**Common misconception:** students think a transistor "makes electricity bigger." Correct it: a transistor doesn't create energy — it *controls* a larger current from the battery using a small one (it amplifies **current**, not voltage). The battery still supplies the power; the transistor is the valve.

**Time check:** Wrap by 0:30. If long, cut the history aside and move to building.


### 5c. Guided Builds — 0:30–1:30 (60 min)


Three experiments, ~60 minutes. Suggested split: **Exp 9 ~18 min · Exp 10 ~17 min · Exp 11 ~25 min.** Exp 11 (the flasher → sound) is the marquee build and the Phase 2 milestone — protect its time. Helpers circulate and **ask questions rather than fix.**

---


#### Experiment 9 — *Time and Capacitors* (≈18 min)


**Step 1 — Time a charge.** Build the simple RC circuit (book Fig. 2-79): a **1,000 µF** capacitor charged through a **1 K** resistor, with button A to charge and button B to discharge (B shorts the capacitor). Clip the meter (volts DC) across the capacitor. Press B to discharge to ~0 V, then hold A and time how long it takes to reach ~9 V — about **3 seconds**.

* **Electrolytic polarity:** the capacitor's short lead / minus stripe goes to negative. Wrong way round, it won't work (and can pop) — check before powering.

**Step 2 — Change the resistor.** Swap the 1 K for a **10 K**. Discharge, then time the charge again — now it takes roughly **10× longer**. "Bigger resistor = slower fill, exactly like a more closed faucet." That's `T = R × C`.

**Step 3 — Watch the curve.** Have them notice the voltage climbs fast at first, then crawls toward 9 V — the charge never *quite* reaches the full supply.

**Checkpoint — Exp 9 "done":** team has timed two charges (1 K vs 10 K) and can say the bigger resistor made it slower, and that charging slows as the capacitor fills.

---


#### Experiment 10 — *Transistor Switching* (≈17 min)


**Step 1 — The finger test (the hook).** Build the little transistor circuit (book Fig. 2-93): 2N2222 + LED + 470 Ω, with two stripped jumpers left exposed. Press a fingertip across both exposed jumpers — the LED lights. Press harder / moisten the finger — it gets brighter. "The transistor is amplifying the tiny current leaking through your skin."

* **Safety:** touch only **one hand** — never bridge the two jumpers with fingers of *different* hands (don't route current hand-to-hand), and never with broken skin. At 9 V through one fingertip it's harmless and you won't even feel it.

**Step 2 — Replace the finger with control.** Swap in the **500 K trimmer** as a voltage divider feeding the base; turn the screw and watch the LED brighten smoothly. Point out the base must get about **0.7 V** above the emitter before the transistor turns on at all.

**Step 3 — Switch and amplifier.** Frame what they saw: a minuscule base current controlled a much bigger LED current — that's *amplifying*. Turn the base fully off and on and the LED goes off and on — that's *switching*. Same part, both jobs.

**Checkpoint — Exp 10 "done":** team has lit the LED via their finger (or the trimmer) and can say the transistor lets a small current control a big one — switch and amplifier.

---


#### Experiment 11 — *Light and Sound* — the modular project (≈25 min)


The marquee build and Phase 2 capstone: a two-transistor **astable multivibrator** that flashes, then sings.

**Step 1 — Build the flasher (book Fig. 2-108/2-109).** It's crowded — install with pliers and count holes carefully. Core parts: two **2N2222** transistors (Q1, Q2) cross-coupled, two **4.7 K** and two **470 K** resistors, two **3.3 µF** capacitors (the timing pair), a **100 K**, a **1 K**, a third 2N2222 driving the **generic LED**. Apply 9 V: the LED should flash roughly **one second on, one second off.**

> **Why it flashes (explainer):** the two halves take turns. While one transistor is off, its timing capacitor charges through a 470 K resistor; when the voltage builds enough, that transistor flips on — and through its capacitor it kicks the *other* half off. Then they swap. The 470 K + 3.3 µF set how long each half waits — i.e., the flash rate. It's last week's feedback oscillation, done with no moving parts.

**Step 2 — Turn light into sound.** Swap the timing capacitors for **much smaller** values (e.g., 0.1 µF or 0.01 µF) so the circuit oscillates *hundreds* of times a second — far too fast to see as flashing. Connect the **8-ohm loudspeaker** to the output: now you **hear a tone**. Smaller capacitor → faster oscillation → **higher pitch**. Let teams swap values and hear the pitch change. `[VERIFY]` exact speaker-connection point and the best capacitor values for an audible tone against your bench build before class.

**Checkpoint — Exp 11 "done":** the circuit visibly flashes the LED, and (with smaller capacitors + speaker) makes an audible tone whose pitch changes when components change.

**Time check:** the flasher should be running by ~1:20 so every team can do the milestone. If a team's build won't run, lend the pre-built spare so they can still demonstrate and explain (see §9).


### 5d. "Light and Sound" Milestone + Journal — 1:30–1:50 (20 min)


This class ends Phase 2, so the milestone gets its own slot (20 min instead of the usual 15).

**Phase 2 Milestone — "Light and Sound" (completion-based, no scores).** Each team, in turn, demonstrates their modular project: first the **flashing light**, then the **tone** through the speaker, and explains **what the capacitor and the transistor are each doing** (the capacitor times the oscillation; the transistor switches/amplifies). 60–90 seconds per team, celebratory. Every team that can show light, show sound, and explain the two parts has completed Phase 2. (If a team's own build failed, they may demonstrate on the loaner and still explain — completion is about understanding, not a flawless solder-free build.)

**Journal milestone (this class).** The syllabus asks each student to: *note how changing capacitor values changed the flash rate / pitch, and explain why a transistor is called a "switch" and an "amplifier."* Four-part template:

1. **What I built** — RC charging circuit; transistor finger test; the two-transistor flasher → sound.
2. **What I observed** — charge time vs resistor; LED brightness vs finger pressure; flash rate and pitch vs capacitor value.
3. **What's physically happening** — "smaller capacitor charges faster → faster oscillation → higher pitch"; "a small base current controls a big collector current."
4. **Real-world link** — blinking timer / turn-signal; a buzzer or tone generator; "transistors are inside everything."

**Time check:** milestone + journals wrapped by 1:50.


### 5e. Wrap-Up & Next-Class Preview — 1:50–2:00 (10 min)


**Restate what they should have learned:**

* A capacitor stores charge and fills on an RC timetable (T = R × C) — fast at first, then slow.
* A transistor lets a tiny current control a big one — it's both a switch and an amplifier, and it's the building block of all modern electronics.
* An oscillator's *speed* is the only difference between a flashing light and a musical tone.

**KidWind tie-in:** "The same capacitors and transistors you used today are exactly what goes into the electronics that take a generator's raw output and turn it into something useful — smoothing it, switching it, measuring it. When your KidWind turbine makes electricity, parts like these are what condition and control it."

**Preview Class 5 — Magnetism and Coils (Experiments 25 + 28):** "We've now controlled electricity every way short of magnetism. Next week we cross the bridge: electric current makes a magnetic field. You'll wind a coil and build an electromagnet strong enough to pick up a paper clip, and watch an LED flash from a magnetic field *collapsing*. That's the doorway to making your own power in the final class."

**Assignment:** Read **Experiments 25 and 28** before next class. Finish the journal milestone (flash rate/pitch + switch vs amplifier). Optional enrichment that pairs with today: [Every Basic Electronic Component Explained in 21 Minutes][08].


## 6. Troubleshooting Guide


| Problem | Likely cause | Fix |
|:--------|:-------------|:----|
| Capacitor never reaches ~9 V | Electrolytic reversed, or button A not making contact | Check polarity (short lead/minus stripe to −); confirm button A closes; discharge with B and retry |
| Capacitor charges instantly (no timing) | Resistor shorted or wrong value, or cap value too small | Use the specified resistor + 1,000 µF; make sure the resistor is actually in series |
| Finger test does nothing | Skin too dry, or jumpers not actually exposed/bridged | Moisten the fingertip; ensure both jumper ends are stripped and you're touching both |
| Transistor circuit dead after wiring | Transistor in wrong orientation or damaged | Check flat side / pin order (collector-base-emitter); swap in a fresh 2N2222 (they're fragile) |
| Flasher won't flash | A cross-coupling wire, capacitor, or transistor misplaced | Compare carefully to the layout; reseat the two timing caps; verify both transistors' orientation |
| One half flashes, other half dead | A resistor or capacitor missing on one side | The circuit is symmetric — check the dead side against the working side, part by part |
| Flashes but no sound when sped up | Speaker not connected at the output, or caps still too large | Connect the 8 Ω speaker at the output point; use much smaller timing caps for an audible rate |
| Tone is there but won't change pitch | Same capacitors left in | Pitch tracks the timing capacitor — swap to a different value to shift it |
| Whole board intermittently dead | Bus gap not bridged, or a leg one hole off | Jumper the mid-board bus gap; trace each leg's strip; nothing should share a strip unintentionally |


## 7. Age Differentiation Notes


**Younger students (12–14):**

* Give them a pre-stripped jumper kit and a labeled copy of the Exp 11 layout (which part in which hole). The flasher is the densest build of the course — a picture prevents most errors.
* For Exp 9, focus on the qualitative result (bigger resistor = slower charge) rather than computing T = R × C.
* Let the finger test and the sound be the wins; pair with a buddy or adult for the dense flasher wiring.

**Older students (15+) and adults (challenge extensions, no scores):**

* Compute the RC time constant for the 1 K and 10 K cases (T = R × C with farads) and compare to their measured times.
* **Challenge (from the syllabus):** tune the modular project's oscillator from a visible flash all the way **up past the edge of hearing** — find the capacitor values for the lowest audible note and the highest they can still hear.
* Have them trace the flasher as a schematic and explain, with the snapshots in mind, how one half shutting off kicks the other half on.


## 8. Assessment


No grades, no quizzes. This class carries the **Phase 2 milestone**:

* **Phase 2 Milestone — "Light and Sound":** each team demonstrates the modular project producing a flashing light, then a tone, and explains what the capacitor and transistor are doing (see §5d). Completion-based, celebratory — not scored. A team may demonstrate on the loaner if their own build failed; understanding is the bar.
* **Journal milestone (this class):** a note on how capacitor value changed flash rate / pitch, plus an explanation of why a transistor is both a "switch" and an "amplifier." Give feedback as questions: *"What would a smaller timing capacitor do to the pitch — and why?"* Celebrate teams that successfully tuned a flash into a tone.


## 9. Instructor Tips


* **Triage if you fall behind (likely — three experiments, the last one dense):** the Exp 11 flasher → sound is the centerpiece and the Phase 2 milestone — protect it. If time is short, (1) keep Exp 9 to a single timed charge (1 K only, skip the 10 K comparison or make it a demo), (2) keep Exp 10 to just the finger test (skip the trimmer), and (3) start Exp 11 by 0:55 at the latest. Never cut the flasher or the milestone.
* **Build and pre-test the flasher tonight, and keep a spare running.** This is the one circuit most likely to defeat a team in the time available. A known-good loaner means every team can still hear the result and do the milestone even if their own build stalls.
* **Pre-strip jumpers and pre-sort capacitors.** The flasher is crowded with small parts; stripping wire and hunting for the right capacitor mid-build is where the hour disappears.
* **Make the finger test theatrical.** "Your body is completing the circuit — you're part of the electronics." It's the most memorable 3 minutes of the class and sells what a transistor does better than any explanation.
* **Let the flash-to-tone moment land.** Build the flasher first so they *see* the ~1 Hz blink, then swap capacitors so the *same* circuit suddenly sings. The "wait — it's the same thing, just faster?" realization is the whole point of Phase 2.
* **Mind the fragile parts.** 2N2222 transistors damage easily (wrong orientation, too much current) and electrolytic capacitors can pop if reversed. Keep spares within reach and check orientation before powering.
* **"Ask, don't fix":** for a dead flasher, resist rebuilding it yourself. The circuit is symmetric — hand them the meter and ask "does the working half look exactly like the dead half?" Comparing the two sides is the diagnostic skill of the day.


## 10. Resources & References


**Course text (students should have read Exp 9–11):**

* *Make: Electronics, 2nd Edition*, Charles Platt — [print][01] / free [PDF][02]. Class 4 covers Experiments 9–11.

**Instructor prep / background:**

* [Doctronics][11] — clear breadboard and schematic illustrations for the capacitor/transistor circuits.
* [The Electronics Club][12] — friendly explanations of capacitors, transistors, and oscillators.
* [Electronics Tutorials][13] — deeper background on the RC time constant and transistor biasing if you want it.

**Student-facing enrichment (optional, after class):**

* [Every Basic Electronic Component Explained in 21 Minutes][08] — covers capacitors and transistors; a good recap after this class.

**Course context:**

* [Makersmiths][05] — the makerspace hosting the course.
* [KidWind][04] — the wind-energy program this course connects to; capacitors and transistors condition a generator's output.


---


[01]:https://www.amazon.com/Make-Electronics-Learning-Through-Discovery/dp/1680450263/
[02]:https://someplace-else.neocities.org/books/Make%20Electronics%202nd%20Edition.pdf
[04]:https://kidwind.org/
[05]:https://makersmiths.org/
[08]:https://www.youtube.com/watch?v=HGNKhLActDo
[11]:http://www.doctronics.co.uk
[12]:https://electronicsclub.info
[13]:https://www.electronics-tutorials.ws
