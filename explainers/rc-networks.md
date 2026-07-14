# The RC Network: How a Resistor and a Capacitor Tell Time
In Class 4's Experiment 9 (*Time and Capacitors*), you charged a 1,000 µF capacitor through a 1 K resistor
and watched your meter climb to 9 volts in about 3 seconds. Then you swapped in a 10 K resistor and the
same capacitor took roughly ten times longer. Electrons move through a wire at nearly the speed of light —
yet this little two-part circuit just measured out seconds, slowly enough for you to count them out loud.

What is the answer to these questions:

1. Why does a bigger resistor make the capacitor charge more slowly — and is it *exactly* 10× slower with a 10 K resistor?
1. Why does the voltage climb quickly at first and then slow to a crawl?
1. If you wait long enough, will the capacitor ever reach the full battery voltage?

The short answer: you built an **RC network** — R for resistor, C for capacitor — the simplest circuit in
electronics that has a *sense of time*. The resistor limits how fast charge can flow in; the capacitor
stores that charge and pushes back harder the fuller it gets. Multiply the two values together and you get
the circuit's **time constant**, T = R × C — the single number that tells you how fast this circuit "fills."
Every electronic device that blinks, beeps, delays, or keeps a beat has an RC network (or its descendant)
somewhere inside it. Let's take it apart.


## 1. Overview
An **RC network** is a resistor and a capacitor in series, and its job is to convert a voltage change into
a *timed* voltage change. Apply a voltage, and the capacitor does not jump to that voltage instantly —
it climbs toward it along a curve whose speed is set by the **time constant, T = R × C** (R in ohms, C in
farads, T in seconds). During each time constant, the capacitor gains **63% of the remaining gap** between
its current voltage and the supply voltage. Because it always takes 63% of *what's left*, the climb starts
fast and gets ever slower — and in theory the capacitor never quite reaches the supply voltage at all. In
practice, engineers call the job done after **five time constants**, when the capacitor is above 99% charged.

In your Experiment 9 circuit, R = 1 K (1,000 ohms) and C = 1,000 µF (0.001 farads), so T = 1,000 × 0.001 =
**1 second**: the capacitor reached 5.67 V after one second, 7.77 V after two, and was essentially full
after five — matching the "just over 3 seconds to read 9.0 V" you timed with the meter. Swap in the 10 K
resistor and T becomes 10 seconds, which is why the second charge felt so much slower.


## 2. Detailed Operation

### Step 1: Applying a Voltage Starts the Charge
Pressing button A connects the 9 V battery, through the resistor, to the capacitor's top plate. The
capacitor starts empty (you pressed button B first, which shorted its two leads together and drained any
stored charge), so its voltage is 0 V. At this instant the *entire* 9 V of the battery appears across the
resistor, because the capacitor isn't pushing back yet. That full 9 V across R is what drives the next step.

### Step 2: The Resistor Sets the Maximum Filling Rate
The resistor obeys Ohm's Law, so the initial current is I = V / R = 9 V ÷ 1,000 ohms = **9 milliamps** — the
fastest this circuit will ever charge. This is the resistor's whole role in the network: it is the
bottleneck that limits how quickly charge can be delivered to the capacitor. A 10 K resistor allows only
0.9 mA at the start — one-tenth the current, hence one-tenth the charging speed and a time constant ten
times longer. That inrush of charge begins piling up on the capacitor's plate, which is the input to Step 3.

### Step 3: The Capacitor Pushes Back as It Fills
As charge accumulates, the capacitor's plates develop their own voltage — positive charge crowding one
plate, negative the other — and that voltage *opposes* the battery. The voltage left over to drive current
through the resistor is now only the **difference** (9 V minus the capacitor's voltage), so the current
shrinks as the capacitor fills. This is the book's balloon-and-faucet picture: the resistor is a partly
closed faucet, the capacitor a balloon, and the fuller the balloon gets, the harder it pushes back against
the incoming flow. Less difference → less current → slower filling, which produces the curve in Step 4.

### Step 4: The 63% Rule Produces the Charging Curve
Because the charging current is always proportional to the *remaining* voltage gap, the capacitor gains a
fixed fraction — **63%** — of whatever gap remains, during every time constant. Starting from 0 V with a
9 V supply and T = 1 second, the numbers run: 5.67 V after 1 s, 7.77 V after 2 s, 8.54 V after 3 s, 8.83 V
after 4 s, 8.94 V after 5 s. The book's image is a greedy cake-eater who always eats 63% of the cake still
on the plate: he starts with huge bites and ends with crumbs, but the cake is never entirely gone. That is
why your meter raced upward at first and then crawled — and why, in theory, the capacitor never *quite*
reaches 9 V. (The exact reason the fraction is 63% requires the mathematics of exponential curves — it is
the number 1 − 1/e — which is beyond this course; the behavior is what matters here.)

### Step 5: Five Time Constants and the Practical Finish Line
The gap keeps shrinking by 63% per time constant forever, so engineers draw an arbitrary but universal
finish line: **after five time constants, the capacitor is more than 99% charged and we call it done.**
For your 1 K / 1,000 µF circuit that is about 5 seconds; for the 10 K version, about 50 seconds to be truly
"full," even though your meter showed 9.0 V (a rounded reading) well before that. In the real circuit two
small effects nudge the numbers further: real capacitors slowly **leak** charge away even while charging,
and the meter itself steals a trickle of current to make its measurement — which is why your timed results
never exactly match the theory.

### Step 6: Discharge Runs the Same Movie Backward
Pressing button B connects the capacitor's two leads together, giving the stored charge a path to flow back
out. Discharge follows the same 63%-per-time-constant rule in reverse: the voltage falls fast at first, then
ever more slowly toward zero. (Through button B's near-zero resistance, T is tiny and the drain is nearly
instant; discharge a capacitor through a resistor instead, and it takes just as long to empty as it took to
fill.) The circuit is now reset to Step 1, ready to time another charge — which is exactly how a repeating
timer works, as Step 7 shows.

### Step 7: Charge, Trip, Reset, Repeat — the RC Network as a Clock
Nothing says a human has to press the buttons. Let the capacitor's rising voltage *trigger something* when
it crosses a threshold — a transistor turning on, for example — and let that something also discharge the
capacitor, and the cycle runs by itself: charge for T-ish seconds, trip, reset, repeat. This is precisely
what happens in Experiment 11's flasher, where each 3.3 µF timing capacitor charges through a 470 K resistor
until its transistor flips, over and over, about once a second. The RC network supplies the *tempo*; the
rest of the circuit just dances to it.


## 3. Block Diagram

```text
9V Battery ──> Button A ──> Resistor R ──> Capacitor C ──> back to battery
   (source)     (start)     (limits the      (fills, and
                             current)         pushes back)
                                                  │
                             Meter reads the growing voltage here:
                             fast at first, then slower — 63% of the
                             remaining gap per time constant T = R × C
```


## 4. Key Parameters

| Parameter | Value | Notes |
| :---------- | :------ | :------ |
| Time constant formula | T = R × C | R in ohms, C in farads, T in seconds |
| Exp 9 circuit, 1 K + 1,000 µF | T = 1 second | 1,000 × 0.001 = 1 |
| Exp 9 circuit, 10 K + 1,000 µF | T = 10 seconds | Ten times the resistance, ten times the time |
| Charge gained per time constant | 63% of the remaining gap | Never reaches 100% in theory |
| Voltage after 1, 2, 3, 4, 5 × T (9 V supply) | 5.67, 7.77, 8.54, 8.83, 8.94 V | The charging curve from the book's calculation |
| Practical "fully charged" | 5 time constants (> 99%) | Engineering convention |
| Initial charging current (1 K) | 9 mA | I = 9 V ÷ 1,000 ohms, the fastest moment of the charge |


## 5. Common Misconceptions
- **Misconception:** "The time constant is how long the capacitor takes to charge fully."
  **Reality:** T is how long it takes to gain **63%** of the remaining gap. Full charge (for practical
  purposes) takes about *five* time constants — and theoretically never arrives at all.

- **Misconception:** "The voltage rises at a steady rate, like filling a glass from a steady tap."
  **Reality:** The rise is fast at first and continuously slows, because the fuller capacitor pushes back
  harder, leaving less voltage to drive current through the resistor. You saw this on the meter: most of
  the 9 volts arrived in the first second.

- **Misconception:** "Current flows *through* the capacitor while it charges."
  **Reality:** Charge flows *onto* one plate and *off of* the other; no charge crosses the insulating gap
  between the plates. The circuit behaves as if current flows, but the capacitor is filling, not conducting.
  (What happens across that gap is its own story — see the displacement-current explainer.)

- **Misconception:** "My measured times didn't match the formula, so I did something wrong."
  **Reality:** Real batteries aren't exactly 9 V, real parts aren't exactly their labeled values, capacitors
  leak, and the meter itself draws a little current from the capacitor as it measures. Small mismatches are
  expected — comparing them to theory is *experimental verification*, the heart of learning by discovery.


## 6. Why this matters everywhere: electronics that keep time
Strip away the breadboard and what remains is a fundamental trick: **a resistor and a capacitor turn
voltage into time.** Digital electronics can switch in nanoseconds, but the human world runs in tenths of
seconds and seconds — blinking indicators, beeping alarms, delayed porch lights, intermittent windshield
wipers. Nearly every one of those delays traces back to some capacitor charging through some resistor
toward some threshold.

You will meet the payoff immediately in **Experiment 11**: the two-transistor flasher's tempo is set by two
RC networks — a 3.3 µF capacitor charging through a 470 K resistor on each side (T = 470,000 × 0.0000033 ≈
1.6 seconds, roughly the beat you saw). Swap in smaller capacitors and T shrinks a thousandfold, the
oscillation leaps to hundreds of cycles per second, and the blinking LED becomes an audible **tone** in the
loudspeaker — the pitch of the note is *literally* an RC time constant, played fast. The same idea powers
the famous **555 timer chip** (an RC network plus comparison circuitry, billions sold), sets the fade rate
of a camera flash recharging, debounces the buttons on a keyboard, and — run in reverse as a filter —
decides which frequencies pass through your headphones. One resistor, one capacitor, and a 63% rule: that
is the entire heartbeat of timed electronics.


## Bottom line
An RC network charges a capacitor through a resistor, and its personality is captured by one number: the
time constant **T = R × C**. The resistor throttles the current; the capacitor fills and pushes back; the
result is a curve that gains 63% of the remaining gap every T, starting fast and finishing (practically)
after five time constants — which is why your 1 K charge took seconds and your 10 K charge took ten times
longer, and why neither ever *quite* touched the battery voltage. Make that rising voltage trip a switch
and reset itself, and you have a clock — the beat behind Experiment 11's flasher, the pitch of its tone,
and the timing inside nearly every gadget that blinks or beeps. For more, see [RC circuit][01],
[RC time constant][02], [Capacitor][03], and the deeper treatment at [Electronics Tutorials][04].



[01]:https://en.wikipedia.org/wiki/RC_circuit
[02]:https://en.wikipedia.org/wiki/Time_constant
[03]:https://en.wikipedia.org/wiki/Capacitor
[04]:https://www.electronics-tutorials.ws/rc/rc_1.html
