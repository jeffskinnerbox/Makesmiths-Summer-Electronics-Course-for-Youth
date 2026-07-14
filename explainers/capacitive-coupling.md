# Capacitive Coupling: How a Signal Crosses a Gap That Blocks the Current
Every introductory electronics text tells you, almost on page one: **a capacitor blocks DC.** Then, in
Class 4's Experiment 9, you built the little circuit with the 1,000 µF capacitor, the LED, and the two
buttons — you pressed button A, and the LED on the *far side* of the capacitor flashed and slowly faded.
The current through that LED had to come from somewhere, and the only path runs through a component whose
two plates never touch.

What is the answer to these questions:

1. How can a pulse of current appear on the far side of a capacitor when no charge can cross the gap inside it?
1. Why did the LED flash only *once* — and why did pressing button A a second time do nothing?
1. Why did smaller capacitors (100 µF, 10 µF, 1 µF, 0.1 µF) give shorter and shorter flashes?

The short answer: a capacitor blocks *steady* DC, but it **passes a sudden change in voltage** — and when a
capacitor is placed in a circuit deliberately to do this, it is called a **coupling capacitor**. This is
one of the most-used tricks in all of electronics: it lets a *signal* (the changing part of a voltage) hop
from one part of a circuit to another while the *steady* voltages on each side stay completely separate.
Let's take it apart.


## 1. Overview
**Capacitive coupling** is the transfer of energy between two parts of a circuit through the electric field
inside a capacitor, rather than through a continuous conductive path. The core principle: current flows in
the wires *outside* a capacitor whenever the voltage across it is *changing*, because charge must pile onto
one plate and be pushed off the other — even though no charge ever crosses the insulating gap between the
plates. A steady (DC) voltage causes no such pile-up once the capacitor is charged, so steady current is
blocked; a sudden change passes through as a brief pulse; and a rapidly repeating change — which is what
alternating current (AC) and audio signals are — passes through continuously.

In Experiment 9's coupling circuit, pressing button A slammed +9 V onto the capacitor's top plate. During
the moment the capacitor charged, real current flowed around the outside of it — through the LED, lighting
it — and then died away as the capacitor filled. The result on the far side was a copy of the *change*
(a single pulse), with the *steady* 9 V that followed completely blocked.


## 2. Detailed Operation

### Step 1: The Capacitor Starts Empty and Balanced
Pressing button B shorts the capacitor's two leads together, draining any stored charge. Both plates now
sit near 0 V, with equal amounts of positive and negative charge — electrically neutral and calm. The LED
is dark because no current flows anywhere. This discharged state is essential: the whole event in the next
steps only happens when the capacitor starts empty, which is exactly what you discovered when a second press
of button A did nothing.

### Step 2: A Sudden Voltage Step Hits the Top Plate
Pressing button A connects the top plate, through the button, to the battery's +9 V. The voltage on that
plate jumps almost instantly — this is the "sudden fluctuation" the capacitor responds to. Positive charge
begins flooding onto the top plate. Crucially, that charge stops there: the gap between the plates is an
insulator, and nothing physically crosses it. What *does* cross the gap is the influence of that charge —
its electric field — which is the input to Step 3.

### Step 3: The Field Pushes Charge Off the Far Plate
The positive charge crowding the top plate attracts electrons toward the *inside face* of the bottom plate
and repels positive charge away from it. That displaced charge has to go somewhere — and its only path is
out the bottom lead, through the LED, and on to the negative side of the battery. So a real, measurable
current flows through the LED, delivered *by* the capacitor without anything passing *through* its gap. From
the outside, the circuit behaves exactly as if the pulse went straight through the capacitor. (Physicists
have a name for what is happening in the gap — see the displacement-current explainer for that story.)

### Step 4: The LED Flashes While the Charging Current Flows
The LED lights for as long as charge is being rearranged — that is, for as long as the capacitor is
charging. This is the same RC charging story as the first part of Experiment 9: the current starts at its
maximum and dies away as the capacitor's own voltage builds up and opposes the battery. With a 1,000 µF
capacitor and the 10 K resistor in the circuit, the fade takes seconds — long enough to watch. The LED's
slow fade *is* the charging curve, displayed in light instead of on a meter.

### Step 5: Fully Charged Means Fully Blocked
Once the capacitor's voltage matches the supply, the rearranging stops: no more charge flows onto the top
plate, none is pushed off the bottom plate, and the LED goes dark. The capacitor now holds a steady 9 V and
passes nothing — this is the moment the textbook rule "a capacitor blocks DC" becomes true. Press button A
again and nothing happens, because there is no *change*: the top plate is already at 9 V. Only after
button B empties the capacitor (Step 1) can the event repeat.

### Step 6: Capacitor Size Sets How Much Change Gets Through
Substitute smaller capacitors — 100 µF, 10 µF, 1 µF, 0.1 µF — and the flash gets briefer each time, until
the LED barely flickers. A smaller capacitor fills almost instantly, so it can only sustain the coupled
pulse for a moment. Run the pulses *repeatedly* and this becomes a frequency rule: **a small capacitor
passes fast (high-frequency) fluctuations but blocks slow (low-frequency) ones**, while a large capacitor
passes both. Because alternating current is nothing but a rapid series of alternating pulses — and audio
signals are a form of AC — a capacitor sized for the job will pass a signal continuously while still
blocking DC completely. Reversing the circuit's polarity works just as well: the coupling effect passes a
brief fluctuation *regardless of which way the current flows*.


## 3. Block Diagram

```text
                     the "signal" (a change)  ────────  crosses via the field
                                                │
9V step ──> Button A ──> ┌── top plate ──┐   electric   ┌── bottom plate ──┐ ──> LED ──> flash!
(sudden change)          │   charge piles │    field    │  charge pushed   │    (then fades as
                         │   up here      │   in gap    │  out here        │     capacitor fills)
                         └────────────────┘             └──────────────────┘
                                        no charge crosses the gap;
                              steady DC (no change) couples nothing at all
```


## 4. Key Parameters

| Parameter | Value | Notes |
| :---------- | :------ | :------ |
| Coupled event | A *change* in voltage | Steady DC couples nothing once charged |
| Flash duration, 1,000 µF | Seconds (visible fade) | Set by the RC charging time |
| Flash duration, 0.1 µF | Barely a flicker | 10,000× less capacitance, far briefer pulse |
| Small capacitor passes | High-frequency fluctuations | Blocks low frequencies — the basis of filters |
| Large capacitor passes | Low *and* high frequencies | Fills slowly, sustains longer pulses |
| Direction dependence | None | A brief fluctuation passes either way — this is why capacitors pass AC |


## 5. Common Misconceptions
- **Misconception:** "The pulse means electrons jumped across the capacitor's gap."
  **Reality:** No charge ever crosses the gap. Charge piling onto one plate pushes, through the electric
  field, an equal charge off the other plate. Current flows in the external circuit on both sides — the
  middle is bridged by a field, not by moving charge.

- **Misconception:** "The LED flashed, so 'a capacitor blocks DC' must be false."
  **Reality:** The rule is about *steady* DC. The flash happened only during the change — the instant of
  switching on — and stopped the moment the voltage became steady. Both facts are true at once: blocks
  steady DC, passes sudden fluctuations.

- **Misconception:** "A bigger capacitor is always better at passing signals."
  **Reality:** It depends on the frequency. A big capacitor passes slow and fast changes alike; a small one
  passes only fast changes. Engineers *choose* the capacitance to select which frequencies couple through —
  that is the starting point of every audio filter and crossover.

- **Misconception:** "Coupling is a rare special effect."
  **Reality:** It is everywhere — sometimes unwanted. Any two conductors near each other form an accidental
  capacitor, which is why signals can "leak" between neighboring wires. Deliberate coupling capacitors and
  accidental coupling are the same physics.


## 6. Why this matters everywhere: joining circuits without merging them
The coupling capacitor solves a problem every multi-stage circuit has: different stages need to *talk*
(pass signals to each other) but often must not *share* their steady DC voltages. Place a capacitor between
them, and the changing signal hops across while each side keeps its own DC level — the stages are
**coupled** for AC and **isolated** for DC, simultaneously.

You will use exactly this in Class 4's marquee build, **Experiment 11**: the two 3.3 µF capacitors in the
flasher couple each transistor's sudden output swing across to the *other* transistor's input — each half
kicks the other through a capacitor — while keeping the two halves' DC operating points separate. That
cross-coupling is what makes the circuit oscillate at all. The same trick sits inside virtually every audio
device: a microphone's tiny AC wiggle is coupled from amplifier stage to amplifier stage through capacitors,
while each stage's different DC bias voltage stays put (the book returns to this in Experiment 29). Your
guitar amp, your phone's headphone circuit, and radio receivers passing a station's signal between stages
all lean on the same two-plate gap: block the steady, pass the change.


## Bottom line
A capacitor blocks steady DC — but a *sudden change* in voltage on one plate pushes a matching pulse of
current out of the other plate, through the electric field in the gap, without any charge crossing it. That
is why your LED flashed once (the change), faded (the capacitor filling), and refused to flash again (no
change left to couple) until you discharged and reset. Sized small, a capacitor passes only fast
fluctuations; and since AC and audio are nothing but fast fluctuations, a well-placed **coupling capacitor**
lets signals travel between circuit stages while their DC voltages stay strangers — the trick that makes
Experiment 11's flasher oscillate and that threads through every amplifier you own. For more, see
[Capacitive coupling][01], [Capacitor][02], and [High-pass filter][03].



[01]:https://en.wikipedia.org/wiki/Capacitive_coupling
[02]:https://en.wikipedia.org/wiki/Capacitor
[03]:https://en.wikipedia.org/wiki/High-pass_filter
