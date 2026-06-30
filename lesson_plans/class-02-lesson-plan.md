# Lesson Plan: Class 2 — Resistance and Ohm's Law


* **Course:** Summer Electronics Course for Youth ([Makersmiths][05])
* **Class number:** 2 of 6
* **Phase:** 1 — Foundations
* **Date:** Tuesday, June 30, 2026, 6:00–8:00 PM
* **Experiments:** Exp 3 *Your First Circuit* + Exp 4 *Varying the Voltage* + Exp 5 *Let's Make a Battery* (*Make: Electronics, 2nd Ed.*)
* **Prerequisites from prior classes:** Class 1 (Exp 1–2) — students have used a multimeter to measure resistance and know the words **voltage, current, resistance** and the water analogy. Students should have read Experiments 3–5 in the [book][01] beforehand.
* **Source of truth:** This plan implements [`syllabus.md`](syllabus.md), Class 2. Component costs and sourcing live in [`BOM.md`](BOM.md), never here.

> **About this plan.** It expands the syllabus's Class 2 outline into a minute-by-minute teaching guide for a volunteer instructor. It weaves in the three lecture-note threads the syllabus calls for: a plain-language **explainer** (resistor-as-restriction, the brightness ladder), **history & application** (Ohm, Volta's pile, Watt, the positive/negative naming convention), and a real-device **theory of operation** (how a chemical battery liberates electrons; how a dimmer works). **This is the busiest class of the course** — three experiments in one session — so the plan tells you exactly where to triage if time runs short.


---


## 1. Class Overview


This is the second and final class of Phase 1 (Foundations), and it turns last week's three words into a working law. Students build their first real circuit — lighting an LED — and discover that a bigger resistor means a dimmer LED. They read resistor color codes and verify values with the meter. Then they use a potentiometer (a knob-controlled variable resistor) to dim an LED smoothly, measure current with the meter in series, and from their own readings *derive Ohm's Law* (V = I × R) — the most fundamental rule in electronics. They finish by building a battery out of lemons, pennies, and galvanized brackets, lighting an LED with chemistry alone. By the end, each team can explain what controls an LED's brightness, which is exactly the **Phase 1 milestone demonstration ("Explain the LED")** that follows this class. This closes Foundations and sets up Phase 2 (Classes 3–4), where students start *controlling* current with switches, relays, capacitors, and transistors.


## 2. Learning Goals


After this class, students will be able to:

* Read a resistor's value from its color stripes and confirm it with the meter set to ohms.
* Build an LED circuit and explain why a higher-value resistor makes the LED dimmer (more resistance → less current).
* Use a potentiometer to vary an LED's brightness, and measure current by putting the meter **in series**.
* State **Ohm's Law (V = I × R)** and use it (with a calculator) to find the right resistor for an LED.
* Build a lemon battery and explain that a chemical reaction between two different metals liberates electrons.


## 3. Preparation Checklist


Do these before students arrive:

* **30 min before — Build and test one of each circuit yourself.** Wire the Exp 3 LED circuit, the Exp 4 potentiometer dimmer (with its protective 470 Ω resistor), and one lemon cell. Confirm your meter reads current in mA when inserted in series. Catching a dead meter or a backwards LED now saves chaos later.
* **25 min before — Pre-cut the lemons** (one half per cell, ~3 halves per team) and have pennies + galvanized brackets sorted. **Use bright, shiny pennies** — dull/oxidized copper won't work. This prep is the single biggest time-saver for the packed schedule.
* **20 min before — Lay out per-team workstations.** Per team: multimeter with leads; 9-volt battery; **generic LEDs (several — a few will get sacrificed)**; one **low-current LED** (for the lemon battery); resistors **470 Ω (yellow-violet-brown), 1K (brown-black-red), 2.2K (red-red-red)**; one **1K potentiometer**; ~5 test leads with alligator clips; calculator.
* **15 min before — Set the meters to ohms**, black lead in **COM**, red lead in **VΩ** — same as last week. Have a note card at each station showing the three resistor color codes.
* **10 min before — Write the brightness ladder on the board:** `470Ω → 1K → 2.2K` with arrows showing brighter → dimmer, and leave space to build the Ohm's Law table (`9mA @ 1K · 6mA @ 1.5K · 4.5mA @ 2K`).
* **5 min before — Stage the lemon-battery station** with lemon halves, bright pennies, brackets, and paper towels (juice is messy).
* **Have ready as spares:** extra generic LEDs (the dimming demo burns some out), spare potentiometer per couple of teams, calculator, paper towels.


## 4. Materials & Components


Names and quantities only — see [`BOM.md`](BOM.md) for costs and sourcing. Only items used *this* class are listed.

| Item | Per team | Shared / notes |
|:-----|:--------:|:---------------|
| Digital multimeter with leads | 1 | Measures ohms, volts DC, and mA today |
| 9-volt battery | 1 | Powers Exp 3 and Exp 4 |
| Generic LEDs | 3–4 | Exp 3 + Exp 4; expect to sacrifice one or two in the dimming demo |
| Low-current LED | 1 | Exp 5 lemon battery (lights on very little current) |
| Resistor 470 Ω (yellow-violet-brown) | 1 | Exp 3 brightness ladder; Exp 4 protective resistor |
| Resistor 1K (brown-black-red) | 1 | Exp 3 ladder; Exp 4 Ohm's Law table |
| Resistor 2.2K (red-red-red) | 1 | Exp 3 brightness ladder |
| Potentiometer, 1K linear | 1 | Exp 4 variable resistance / dimmer |
| Test leads with alligator clips | ~5 | From Pack 1 |
| Calculator | 1 | Student-provided; for Ohm's Law |
| Lemon halves | ~3 | Shared station; pre-cut. Exp 5 electrolyte |
| Copper-plated coins (bright pennies) | ~3–4 | Shared; copper electrode. Must be shiny |
| Galvanized (zinc-plated) steel brackets | ~3–4 | Shared; zinc electrode |
| Build journal + pencil | 1 per student | Student-provided; primary record |


## 5. Class Timeline


Follows the standard 2-hour session from the syllabus. **This class is tight** — the time checks are not optional. If you fall behind, see the triage note in §9.

| Segment | Clock | Duration |
|:--------|:------|:--------:|
| 5a. Review & Q&A (Class 1 recap) | 0:00–0:10 | 10 min |
| 5b. Mini-Lecture (story first) | 0:10–0:30 | 20 min |
| 5c. Guided Builds (Exp 3 + Exp 4 + Exp 5) | 0:30–1:30 | 60 min |
| 5d. "Explain It" Peer Share + Journal | 1:30–1:45 | 15 min |
| 5e. Wrap-Up + Phase 1 Milestone | 1:45–2:00 | 15 min |


### 5a. Review & Q&A — 0:00–0:10 (10 min)


**What to do**

* Recap Class 1 in two questions: *"What three things govern every circuit?"* (voltage, current, resistance) and *"What did lower resistance do?"* (let more current flow → more heat). Tie the new word **current** to today: last week you measured resistance; today you'll measure current too.
* Surface any questions from the pre-reading (Exp 3–5). Acknowledge the big one coming: "Today we get an actual formula — and you'll discover it yourselves, not just be told it."
* Confirm meters still read ohms (black → COM, red → VΩ).

**What to watch for**

* Students who missed Class 1 — pair them with a buddy; the meter-setup and water-analogy recap gets them up to speed fast.

**Time check:** Done by 0:10. Keep it brisk — the builds need the time.


### 5b. Mini-Lecture (story first) — 0:10–0:30 (20 min)


Keep to 20 minutes. The goal is to set up three builds, not teach the law outright — they'll derive it with their hands.

**Key concept 1 — A resistor is a deliberate restriction (explainer).** Back to the water pipe: a resistor is a narrowed section that limits flow. The narrower it is (more ohms), the less current gets through. "Today you'll light an LED through three different resistors and watch it get dimmer as resistance goes up. Same battery, same LED — only the restriction changes."

**Key concept 2 — Reading resistor color codes.** Most resistors are striped, not labeled. Show the rule on the board:

* First two stripes = the first two digits.
* Third stripe = how many zeros follow.
* The gold/silver stripe (tolerance) goes on the **right**; ignore the body color.
* Worked examples for today's three: **470 Ω** = yellow(4) violet(7) brown(1 zero); **1K** = brown(1) black(0) red(2 zeros) = 1,000; **2.2K** = red(2) red(2) red(2 zeros) = 2,200.
* **Question to ask:** "Why 2.2K and not a round 2.0K?" (Historical: old resistors were ±20%, so values were spaced so their ranges just met — 1.0, 1.5, 2.2, 3.3, 4.7, 6.8. The odd numbers are a fossil of that.)

**Key concept 3 — An LED is fussy and has a direction.** Unlike a resistor, an LED has **polarity**: the longer leg is positive (connect it toward the battery's +). It has a maximum **forward voltage** (~2V) and **forward current** (~20mA); exceed them and it burns out — permanently. "You'll see an LED die today. That's a planned lesson, not a failure — it's *why* we put a resistor in series with it."

**Key concept 4 — The punchline they'll derive: Ohm's Law (history & application).** Georg Ohm (whom we met last week) showed current is proportional to voltage and inversely proportional to resistance. Written as a formula: **V = I × R** (volts = amps × ohms). "I'm not going to prove this on the board. You're going to measure current through different resistances and discover the pattern yourselves." Mention the family of names becoming units: Ohm (ohms), Volta and his copper-zinc "voltaic pile" (volts — you'll rebuild it with lemons today), Watt (power).

**Common misconception to address:** Students think the battery "pushes a fixed amount of electricity into" the LED. Reframe: the battery supplies *voltage* (pressure); how much *current* flows depends on the total resistance in the loop. Change the resistance, change the current, change the brightness.

**Time check:** Wrap by 0:30. If running long, cut the color-code history aside and move to building — they can read codes from the note cards.


### 5c. Guided Builds — 0:30–1:30 (60 min)


Three experiments, ~60 minutes. Suggested split: **Exp 3 ~18 min · Exp 4 ~28 min · Exp 5 ~14 min.** Exp 4 is the heart of the class (Ohm's Law) — protect its time. Helpers circulate and **ask questions rather than fix.**

---


#### Experiment 3 — *Your First Circuit* (≈18 min)


**Step 1 — Read and verify a resistor.** Have each team identify the **2.2K** resistor by its stripes (red-red-red), then check it with the meter on ohms (disconnected from everything, probes pressed on the leads). The reading may be slightly off the marked value — that's normal (tolerance + meter accuracy). Do the same for 1K and 470 Ω.

> **Tip:** rest the resistor on a non-metal surface and hold the probes by their plastic handles — if you pinch the resistor and probes in your fingers, you measure your body's resistance too.

**Step 2 — Light the LED (the brightness ladder).** Build the circuit from *Make: Electronics* Fig. 1-45: 9V battery → resistor → LED → back to battery. **Long leg of the LED toward battery +.** Start with the **2.2K** resistor — the LED glows dimly. Swap to **1K** — brighter. Swap to **470 Ω** — brightest. Make sure no alligator clips touch each other.

* **Ask:** "The resistor went *down* and the LED got *brighter* — why?" (Lower resistance → more current flows → brighter LED.)

**Checkpoint — Exp 3 "done":** team has verified a resistor's value with the meter and can state, from their own observation, that a higher-value resistor makes the LED dimmer because it lets less current through.

---


#### Experiment 4 — *Varying the Voltage* → deriving Ohm's Law (≈28 min)


This is the centerpiece. A potentiometer ("pot") is a knob-controlled variable resistor: a circular resistive track with a wiper that slides along it. The center terminal is the wiper; the two outer terminals are the ends of the track. It has **no polarity**.

**Step 1 — Dim an LED with the pot (and protect it).** Wire the pot in place of the fixed resistor, **with a 470 Ω resistor in series** to protect the LED (Fig. 1-53). Turn the shaft and watch the LED smoothly brighten and dim. *This is exactly how a light dimmer works.*

> **Optional, instructor-run demonstration (destructive):** wire one LED to the pot **without** the protective resistor, start fully counterclockwise (max resistance), and turn slowly toward minimum — the LED gets brighter, then suddenly dies. It makes the "always protect an LED" lesson unforgettable. Do this once at the front so teams don't burn their own LEDs. (Safety glasses optional; an LED rarely cracks.)

**Step 2 — Measure current in series (new meter skill).** Set the meter to **mA**. Current measurement is different from resistance/voltage: the meter must be **inserted into the circuit so current flows through it** (in series), not touched across two points.

* **Safety — Meter Overload:** never touch the mA probes straight across the battery — that's a short through the meter and it blows the meter's internal fuse. Always have a resistor in the circuit. If your meter has a separate mA socket, move the red lead there only while measuring current, then move it back.

**Step 3 — The Ohm's Law discovery.** Remove the LED. Put the meter in series with the **1K resistor + 1K pot**. Measure the current at three settings and record total resistance vs. current:

| Pot setting | Total resistance | Current (≈) |
|:------------|:----------------:|:-----------:|
| Fully clockwise (~0 Ω) | 1K | 9 mA |
| Halfway (~500 Ω) | 1.5K | 6 mA |
| Fully counterclockwise (1K) | 2K | 4.5 mA |

* **Ask the magic question:** "Multiply the milliamps by the kilohms on each row. What do you get?" (9 every time.) "And what's the battery voltage?" (9 volts!)
* That's the discovery: **volts = milliamps × kilohms**, which in base units is **V = I × R** — **Ohm's Law.** Write its three forms: `V = I × R`, `I = V / R`, `R = V / I`.

**Step 4 — Use the law (challenge / older students).** "An LED wants 2V at 20mA. The battery is 9V, so the resistor must drop 7V. What resistor?" Walk it: I = 20mA = 0.02A; R = V/I = 7 / 0.02 = **350Ω**, round up to the standard **470Ω** — *which is why Exp 3 used 470Ω.* The math closes the loop on the whole class.

**Checkpoint — Exp 4 "done":** team has a filled-in current-vs-resistance table and can show that volts ≈ amps × ohms using their own numbers.

---


#### Experiment 5 — *Let's Make a Battery* (≈14 min)
A fun, hands-on closer that makes "a battery liberates electrons by chemistry" concrete.

**Recommended LED Specifications:**
To maximize your chances of success without needing a massive chain of lemons:
* **Color:** Choose a standard Red LED, with ong lead wire = Anode, short lead wire = Cathode.
  Red LEDs have the lowest forward voltage requirements (typically 2.0 V to 2.2 V, 20mA),
  making them the easiest to light up with the limited power a fruit battery provides.
* **Avoid:** Do not use Blue, White, or Green LEDs if possible.
  These colors are built with different semiconductor materials that require a higher forward voltage (often 3.0 V or more),
  which will be much harder to achieve with a simple fruit-based setup.

**Key Tips for Success:**
* **Type:** Look for a standard through-hole (THT) LED (typically 3mm or 5mm).
  Avoid LEDs labeled as "high power," "flashing," or "multi-color," as these require significantly more current and voltage to function.
* **Series Connection:** You will likely need to connect 3 to 6 lemon cells in series
  (connecting the zinc nail, aka galvanized nail, of one lemon to the copper wire/penny of the next) to reach the required voltage threshold.
* **Polarity:** LEDs are diodes, meaning they only allow current to flow in one direction. If the LED doesn't light up,
  simply rotate it 180 degrees—the longer leg is the positive (+) anode, and the shorter leg is the negative (-) cathode.
* **Low Current Efficiency:** While most standard LEDs are rated for 20mA (milliamperes),
  they will often produce a faint, visible glow at much lower currents (often in the microampere range),
  which is perfect for a lemon battery.

**Step 1 — One lemon cell.** Push a **bright penny** (copper) and a **galvanized bracket** (zinc) into a lemon half, close together but **not touching**. Set the meter to volts DC (2V range) and measure between penny and bracket — expect **~0.8–1V**. One cell isn't enough to light an LED.

**Step 2 — Cells in series.** Link three lemon cells in series with test leads — always **bracket → penny → bracket → penny** (never penny-to-penny or bracket-to-bracket). Connect the chain to a **low-current LED**. With three cells (~3V total) the LED glows.

* **Ask:** "Where's the electricity coming from? There's no battery in the kit here." (A chemical reaction between two different metals — copper and zinc — in the lemon's acid. The metals + electrolyte liberate electrons.) This is exactly Volta's "voltaic pile" from 1800, just with lemons instead of brine-soaked cardboard.

**Checkpoint — Exp 5 "done":** team has measured a single cell's voltage and lit the low-current LED with cells in series, and can name the two metals doing the work.

**Time check:** All three wrapped by 1:30. If behind, Exp 5 can be a quick whole-room demo at one station (see §9 triage).


### 5d. "Explain It" Peer Share + Journal — 1:30–1:45 (15 min)


**What to do**

* Pick one team to explain **what controls the LED's brightness** (resistance/current) pointing at their brightness ladder. Pick a second team to explain the **Ohm's Law table** — why milliamps × kilohms equaled the battery voltage.
* Everyone writes a journal entry. The syllabus sets this class's **journal milestone**: record current vs. total resistance from the pot test and show that **volts ≈ amps × ohms**, plus name one real device that uses a variable resistor (dimmer, volume knob, fan-speed control). Use the four-part template:
    1. **What I built** — LED + resistor ladder; pot dimmer; lemon battery.
    2. **What I observed** — brightness vs. resistor; the current/resistance numbers; lemon-cell voltage.
    3. **What's physically happening** — "lower resistance → more current → brighter," and "V = I × R."
    4. **Real-world link** — a dimmer/volume knob (pot); a lemon/chemical battery.

**What to watch for**

* Journal entries that copy the formula without the team's own numbers. Nudge: "Put your three current readings in — does the pattern hold?"

**Time check:** Journals under way by 1:45.


### 5e. Wrap-Up + Phase 1 Milestone — 1:45–2:00 (15 min)


**Restate what they should have learned:**

* A resistor restricts current; higher ohms → less current → dimmer LED. Color stripes tell you the value.
* **Ohm's Law: V = I × R** — you derived it from your own current measurements. It predicts exactly what resistor an LED needs.
* A battery makes electricity from a chemical reaction between two metals — you built one from lemons.

**Phase 1 Milestone — "Explain the LED" (completion-based, no scores).** This is the demonstration the syllabus places after Class 2. Have each team, in turn, show their working LED circuit and explain in their own words **what sets its brightness** (the resistor/current relationship), pointing to their journal numbers. It's a 60-second show-and-tell per team, celebratory, not graded — every team that can explain it has completed Phase 1. (If time is tight, fold this into the peer-share in 5d or carry it to the start of Class 3.)

**KidWind tie-in:** "A turbine's output has to be matched to whatever it's powering — Ohm's Law is exactly how you reason about that. And a battery is one way to store the energy a turbine makes. You now have the one equation that every part of a wind-energy system obeys."

**Preview Class 3 — Switches, Relays, and Automatic Control (Experiments 6–8):** "We've measured and predicted current. Next week we start *controlling* it — reading real schematics, switching circuits on and off, and meeting the relay: a switch that electricity flips by itself. We'll even make one buzz."

**Assignment:** Read **Experiments 6–8** before next class. Finish the journal milestone (current/resistance table + V = I × R + one variable-resistor device). Optional enrichment that pairs with today: [Every Type of Battery Explained][10] and [Every Basic Electronic Component Explained in 21 Minutes][08].


## 6. Troubleshooting Guide


| Problem | Likely cause | Fix |
|:--------|:-------------|:----|
| LED won't light at all | LED in backwards (polarity) | Flip the LED — long leg toward battery + |
| LED flashed bright then went dark forever | Burned out (too much current, no/low resistance) | Replace LED; ensure a resistor is in series; for the pot, start at max resistance |
| All three resistors give the same brightness | LED reversed, or a clip shorting across the resistor | Check LED direction; make sure alligator clips aren't touching each other |
| Resistor reads wildly wrong on the meter | Fingers pinching the leads (measuring your body too) | Rest resistor on a non-metal surface; hold probes by the plastic handles |
| Meter reads 0 or won't show current | Meter not in series, or wrong socket | Insert meter *into* the loop (in series); move red lead to the mA socket if separate |
| Meter went dead / blank when measuring current | Internal fuse blown (mA probes shorted across battery) | Replace the meter's fuse or swap meters; never put mA probes straight across a battery |
| Pot does nothing when turned | Using the two end terminals, not wiper + one end | Use the **center** (wiper) terminal and one outer terminal |
| Lemon cell reads near 0V | Penny oxidized, electrodes touching, or dry contact | Use a bright penny; keep penny and bracket close but not touching; push electrodes in firmly |
| Lemon LED won't light | Too few cells, or a generic (not low-current) LED | Use 3 cells in series and the **low-current** LED; check bracket→penny→bracket order |


## 7. Age Differentiation Notes


**Younger students (12–14):**

* Give them the color-code note card and let them focus on the *qualitative* brightness ladder (which resistor is brightest/dimmest) rather than memorizing codes.
* For Ohm's Law, it's enough to fill in the current/resistance table and notice the pattern (milliamps × kilohms = 9). Skip the unit-conversion algebra.
* Pair with a buddy or adult for the in-series current measurement — it's the trickiest meter move of the course so far.

**Older students (15+) and adults (challenge extensions, no scores):**

* Do the full Ohm's Law calculation in §5c Step 4 (R = V/I) and confirm it predicts the 470Ω from Exp 3.
* **Challenge (from the syllabus):** use Ohm's Law to predict and then build the **dimmest LED that still visibly glows** — pick the resistor, calculate the current, test it.
* Add the lemon cells one at a time and record how the voltage stacks (≈0.9V, ≈1.8V, ≈2.7V) — a concrete demonstration that series sources add.
* Optional: pry open the spare potentiometer (adult-supervised) to see the track and wiper that make the variable resistance.


## 8. Assessment


No grades, no quizzes. Two things land this class:

* **Journal milestone (this class):** the current-vs-total-resistance table from the pot test, a line showing **volts ≈ amps × ohms**, and one named device that uses a variable resistor. Completion-based — it needs the team's own numbers, not perfection.
* **Phase 1 Milestone — "Explain the LED":** each team shows a working LED circuit and explains what sets its brightness (resistance/current). This is a completion demonstration, not a scored test (see §5e). Give feedback as questions: *"What would happen to the current if you doubled the resistor?"* Celebrate clear explanations and good color-code reading.


## 9. Instructor Tips


* **Triage plan if you fall behind (you might — this is the fullest class):** Exp 4's Ohm's Law table is the non-negotiable centerpiece — protect it. If time is short, (1) skip the destructive LED-burnout demo, (2) run Exp 5 as a single front-of-room demo instead of per-team, and (3) move the "Explain the LED" milestone to the top of Class 3. Never cut the current-measurement / Ohm's Law derivation.
* **Pre-cut the lemons and use shiny pennies.** Oxidized pennies are the #1 reason the lemon battery "doesn't work." Bright copper is essential.
* **The in-series current measurement trips people up.** Demo it once at the front: physically break the loop and put the meter *in* the gap. Emphasize "current flows THROUGH the meter; voltage is measured ACROSS two points" — that distinction recurs all course.
* **Let the discovery be a discovery.** Don't write V = I × R on the board first. Let teams fill the table, then ask them to multiply the columns. The "oh — it's always 9!" moment is the best teaching of the day; the formula lands because they found it.
* **Stock spare LEDs.** Between the dimming demo and the occasional backwards wiring, LEDs die. Running out stalls the room.
* **"Ask, don't fix":** when an LED won't light, resist flipping it yourself — ask "which leg is longer, and where should it go?" Polarity is a lesson they should own.
* **Watch the clock at 0:30.** If the room isn't building by 0:30, stop the lecture; teams can read color codes from the cards as they go.


## 10. Resources & References


**Course text (students should have read Exp 3–5):**

* *Make: Electronics, 2nd Edition*, Charles Platt — [print][01] / free [PDF][02]. Class 2 covers Experiments 3–5.

**Instructor prep / background:**

* [Doctronics][11] — clear breadboard/schematic and resistor illustrations.
* [The Electronics Club][12] — friendly explanations of resistors, LEDs, and Ohm's Law.
* [Electronics Tutorials][13] — deeper treatment of Ohm's Law and series/parallel if you want it.

**Student-facing enrichment (optional, after class):**

* [Every Type of Battery Explained][10] — pairs directly with the Exp 5 lemon battery.
* [Every Basic Electronic Component Explained in 21 Minutes][08] — great overview of resistors, LEDs, and potentiometers.

**Course context:**

* [Makersmiths][05] — the makerspace hosting the course.
* [KidWind][04] — the wind-energy program this course connects to; Ohm's Law underlies matching a turbine to its load.


---


[01]:https://www.amazon.com/Make-Electronics-Learning-Through-Discovery/dp/1680450263/
[02]:https://someplace-else.neocities.org/books/Make%20Electronics%202nd%20Edition.pdf
[04]:https://kidwind.org/
[05]:https://makersmiths.org/
[08]:https://www.youtube.com/watch?v=HGNKhLActDo
[10]:https://www.youtube.com/watch?v=2G6Rn99sVmM
[11]:http://www.doctronics.co.uk
[12]:https://electronicsclub.info
[13]:https://www.electronics-tutorials.ws
