# Displacement Current: The Current That Isn't There
In the last part of Class 4's Experiment 9, you swapped the LED for your multimeter and pressed button A
while watching the display. The voltage on the *far side* of the capacitor jumped almost instantly, then
drained slowly away. On an oscilloscope, the book reports, the rise looks vertical — effectively instant.
Yet inside that capacitor sit two metal plates separated by an insulator. Nothing touches. Nothing *can*
carry charge across.

What is the answer to these questions:

1. How does a pulse get across a gap that no electron ever crosses?
1. What exactly is "displacement current," and is it a *real* current?
1. Why did this puzzle, of all things, lead one physicist to predict radio and explain light itself?

The short answer: the thing that crosses the gap is a **changing electric field**, and in the 1860s the
Scottish physicist **James Clerk Maxwell** showed that a changing electric field acts exactly like a
current — it even produces a magnetic field, just as current in a wire does. He named this ghostly
stand-in the **displacement current**. It completes the circuit through your capacitor, and — far beyond
your breadboard — it is the mechanism that lets electromagnetic waves, from radio to light, travel through
empty space. Let's take it apart.


## 1. Overview
**Displacement current** is not a flow of charge. It is the name for the way a **changing electric field**
behaves like a current: wherever an electric field is growing or shrinking — such as in the gap of a
charging capacitor — the changing field produces a magnetic field and "carries" the circuit's current
across, exactly as if a wire were there. In Experiment 9's circuit, pressing button A drives real
(conduction) current onto the capacitor's top plate; the electric field in the gap grows; and that growing
field induces an equal current flowing away from the bottom plate. The current is continuous around the
whole loop, even though no charge crosses the gap — the changing field is the missing link.

Once the capacitor finishes charging, the field stops changing, the displacement current stops with it,
and the capacitor goes back to blocking DC. That is the whole rule of thumb in one mechanism: *steady*
field, no current — *changing* field, current flows. Maxwell added this one term to the equations of
electricity in the 1860s, and the completed equations predicted self-propagating electromagnetic waves
moving at the speed of light.


## 2. Detailed Operation

### Step 1: The Charged-at-Rest Starting Point
In the meter version of the circuit, the capacitor's top plate connects through the 10 K resistor toward
the supply, and the meter reads the point between them. At rest (after discharging with button B and
letting things settle in the reversed variant), the capacitor blocks all steady current — it behaves like
a resistor of *nearly infinite* value. The book's resistor-pair picture explains what the meter shows: in
a series pair, the bigger the second resistance, the more of the supply voltage appears across it. With the
capacitor playing an almost-infinite second resistor, essentially *all* the voltage sits across the
capacitor and none across the real resistor. This calm, fully blocked state is what the sudden pulse in
Step 2 disrupts.

### Step 2: Button A Delivers a Sudden Pulse
Pressing button A abruptly changes the voltage on one plate. Real conduction current — actual moving
charge — rushes through the wire and piles onto that plate. This charge stops at the plate; the insulating
gap is a wall. What the inrush *does* do is rapidly strengthen the electric field stretching across the
gap between the plates, and that changing field is the input to Step 3.

### Step 3: The Changing Field Bridges the Gap
Here is Maxwell's move. The growing electric field in the gap acts, in every measurable way, like a current
flowing through the gap: it produces a magnetic field around the capacitor just as a wire would, and it has
exactly the same size as the current arriving on the plate. This is the **displacement current** — a field
effect standing in for moving charge. Its immediate, tangible consequence sits on the far plate: the
strengthening field induces a matching voltage there, pushing an equal conduction current out of the bottom
plate and into the rest of the circuit. During the pulse, the capacitor's near-infinite effective resistance
momentarily *disappears*, and the circuit behaves as if the gap weren't there at all.

### Step 4: The Meter Sees the Pulse Arrive
On the output side, the meter's reading leaps — a rise so fast that on an oscilloscope it appears
instantaneous (a digital multimeter, which updates only a few times a second, softens it into a visible
jump). The pulse has crossed the component that "blocks current." In the reversed version of the circuit,
where the resting voltage was 9 V, pressing button A produces a *negative* pulse and the meter dives toward
0 V instead — same mechanism, opposite direction, proving the effect passes fluctuations either way. What
happens next depends on the capacitor beginning to fill, which is Step 5.

### Step 5: Charging Chokes Off the Displacement Current
As the capacitor charges, its own voltage rises to oppose the supply, the arriving conduction current dies
away — and since the displacement current always equals the arriving current, it dies away in step. The
electric field settles at a new, constant strength; a constant field is not a changing field, so the
"current" through the gap fades to zero. The meter shows this as the slow decay after the spike: the
capacitor recharging through the 10 K resistor on the familiar RC schedule (T = R × C = 10,000 × 0.001 =
10 seconds), gradually restoring the fully blocked state of Step 1.

### Step 6: Repeat the Pulses Fast Enough and the Gap Never Closes
One pulse gets one spike through the gap. But feed the capacitor an endless train of alternating pulses —
which is exactly what **alternating current (AC)** is — and the electric field in the gap never stops
changing, so the displacement current never stops flowing. The capacitor conducts continuously for AC while
still blocking DC completely. This is the deep reason behind the capacitive-coupling behavior you saw with
the LED, and it is the bridge to Maxwell's larger discovery in the next section: a field that keeps changing
can keep a current — and, it turns out, a *wave* — going indefinitely.


## 3. Block Diagram

```text
              conduction current                        conduction current
              (real moving charge)                      (real moving charge)
 Battery ──> wire ──> top plate  ┊  gap  ┊  bottom plate ──> wire ──> meter/LED
                          │      ┊       ┊       ▲
                          └──> growing electric field ──┘
                               "displacement current"
                        (no charge crosses — the changing
                         field carries the current across
                         and even makes a magnetic field)

 field changing  ──> current flows        field steady ──> current = 0  (blocks DC)
```


## 4. Key Parameters

| Parameter | Value | Notes |
| :---------- | :------ | :------ |
| Displacement current size | Equals the conduction current arriving at the plate | The circuit's current is continuous around the loop |
| Condition for it to flow | The electric field must be *changing* | Steady field → zero displacement current → DC blocked |
| Pulse rise time (oscilloscope) | Effectively instant | A digital meter, updating slowly, shows a softened jump |
| Decay after the spike | RC schedule, T = 10 K × 1,000 µF = 10 s | The capacitor recharging through the resistor |
| Direction dependence | None — works for either polarity | Why capacitors pass AC in both half-cycles |


## 5. Common Misconceptions
- **Misconception:** "Displacement current is electrons sneaking through the capacitor's insulator."
  **Reality:** No charge crosses the gap (if it did, the capacitor would be broken — that's called
  dielectric breakdown). Displacement current is a *changing electric field* that behaves like a current;
  the moving charges stop at the plates.

- **Misconception:** "If no charge moves, it's just a bookkeeping trick — not a real current."
  **Reality:** It has a current's most physical signature: it generates a **magnetic field**. Maxwell's
  equations treat it on equal footing with conduction current, and every radio wave that reaches your phone
  is the changing-field mechanism sustaining itself through empty space — hard to dismiss as bookkeeping.

- **Misconception:** "The meter's spike proves the capacitor conducted DC for a moment."
  **Reality:** The capacitor passed a *fluctuation* — a change. The distinction matters: steady DC never
  passes, no matter how long you wait, while any sudden change passes immediately. "Blocks DC, passes
  changes" are two faces of one rule: current crosses only while the field is changing.

- **Misconception:** "This is an obscure detail only physicists care about."
  **Reality:** Every capacitor in every AC or audio circuit "conducts" by exactly this mechanism, and
  wireless communication exists because of it. It is arguably the most consequential correction ever made
  to an equation.


## 6. Why this matters everywhere: from a breadboard puzzle to radio and light
The question you asked at the breadboard — *how did the pulse cross the gap?* — is the very question that
bothered **James Clerk Maxwell** (1831–1879) in the 1860s. The mathematics of electricity in his day said
current couldn't cross a capacitor's gap, yet circuits plainly behaved as if it did. Maxwell's fix was the
displacement-current term: a changing electric field counts as a current and creates a magnetic field.

That one term detonated far beyond capacitors. With it, his equations closed into a loop: a changing
electric field creates a magnetic field, and a changing magnetic field creates an electric field (Faraday's
induction — the subject of your Classes 5 and 6). Chase the loop and you get a disturbance where each field
continuously regenerates the other — a self-propagating **electromagnetic wave** that needs no wires and no
medium at all. Maxwell calculated its speed from laboratory constants and got the measured speed of light:
light *is* such a wave. Radio, Wi-Fi, radar, microwave ovens, X-rays — the whole electromagnetic family —
travel by the mechanism he invented to explain what your capacitor just did. Heinrich Hertz confirmed the
waves experimentally in 1887, and within a decade radio was born.

So the spike on your multimeter is a genuinely deep observation: you watched a current exist where no
charge was flowing. The same physics, cycled billions of times per second inside an antenna, is how this
sentence may have reached the device you're reading it on. (For the full story of Maxwell's four equations,
see the companion piece [Maxwell's Equations][05].)


## Bottom line
A capacitor's gap stops every electron, yet a sudden pulse crosses it — because the inrush of charge builds
a rapidly **changing electric field** in the gap, and a changing electric field acts exactly like a current:
equal in size to the current arriving at the plate, complete with its own magnetic field. Maxwell named it
**displacement current**, and it flows only while the field is changing — which is why your meter spiked and
then decayed as the capacitor filled, why steady DC stays blocked forever, and why endlessly-changing AC
passes through as if the gap weren't there. Add this one idea to the laws of electricity and they predict
self-sustaining electromagnetic waves traveling at the speed of light — radio, Wi-Fi, and light itself.
For more, see [Displacement current][01], [James Clerk Maxwell][02], [Electromagnetic radiation][03], and
[Capacitor][04].



[01]:https://en.wikipedia.org/wiki/Displacement_current
[02]:https://en.wikipedia.org/wiki/James_Clerk_Maxwell
[03]:https://en.wikipedia.org/wiki/Electromagnetic_radiation
[04]:https://en.wikipedia.org/wiki/Capacitor
[05]:maxwells-equations.md
