# Inductance and Resistance: Why a Coil Across a 9-Volt Battery Isn't the Short It Looks Like
In Class 5 you wound wire around a screwdriver (Experiment 25) and clipped a 9-volt battery straight across
it — and in Experiment 28 you did nearly the same thing with an entire 100-foot spool of hookup wire. On
paper this looks exactly like the battery-abuse disaster of Experiment 2: a fat copper path from the
battery's plus terminal to its minus terminal, with nothing obvious in between to limit the current. The
wire should glow, the battery should cook. Yet the LED blinks politely, the coil merely gets warm, and
nothing bursts into flame.

What is the answer to these questions:

1. Why doesn't a coil across a 9-volt battery repeat the dead-short meltdown of Experiment 2?
1. What happens in the first instant after you connect the battery — the **transient**?
1. What sets the current once everything settles down — the **steady state** — and where does the heat go?

The short answer: two different effects protect you on two different timescales. In the first fraction of a
second, the coil's **inductance** fights the *change* in current — current starts at zero and can only ramp
up gradually, because building a magnetic field takes energy and time. After that, the coil's
**resistance** takes over: 100 feet of thin copper wire is not zero ohms, and neither is the inside of a
9-volt battery, so the current levels off at a few amps rather than climbing toward infinity. The coil
still works the battery hard — that's why you only press the button briefly — but "hard" is a long way from
"short circuit." Let's take it apart.


## 1. Overview
A coil of wire connected to a battery is an **inductor**: a component that stores energy in a magnetic
field, and therefore resists any *change* in the current flowing through it. When you first apply voltage,
the rising current builds a magnetic field around the turns, and that growing field induces a voltage back
into the coil that opposes the battery (this self-opposition is called **self-inductance**, and the
opposing push is the **back-EMF**). The result is that current cannot jump instantly to its final value —
it climbs along a smooth exponential curve governed by the **time constant τ = L / R**, the inductive twin
of the RC time constant you measured in Class 4.

Once the field is fully built, the transient is over and the coil behaves like what it physically is: a
long piece of copper wire with a definite resistance. The steady-state current is set by plain Ohm's law —
the 9 volts divided by the total resistance around the loop, which is the wire's own resistance plus the
battery's **internal resistance** (a real battery is not a perfect voltage source; chemistry inside it
limits how much current it can deliver). For a 100-foot spool of 26-gauge wire that works out to roughly an
amp or two — enough to warm the wire and drain the battery in minutes, which is why the experiment says
*press the button briefly*, but nowhere near the runaway you'd get from a true zero-ohm short.


## 2. Detailed Operation

### Step 1: The Battery Connects and Voltage Appears Across the Coil
Pressing the button (or touching the clip) puts the battery's full 9 volts across the two ends of the coil.
At this exact instant, something surprising is true: **the current through the coil is still zero.** An
inductor's defining rule is that its current cannot change instantaneously — just as the capacitor in
Class 4 could not change its *voltage* instantaneously. So at the moment of connection the coil looks, for
one fleeting instant, like an *open* circuit, not a short. All 9 volts sit across the coil, and current is
just beginning to rise. This rising current is the input to Step 2 — and in Experiment 28, this is the
moment the *first* LED flashes: while the coil is still "blocking," current detours through the LED branch
instead.

### Step 2: The Rising Current Builds a Field, and the Field Pushes Back
As current begins to flow, it creates a magnetic field around every turn of wire — and because the turns
are stacked close together, each turn's field threads through its neighbors, multiplying the effect (this
is why a coil is so much stronger than a straight wire, and why the iron screwdriver core in Experiment 25
strengthens it further). But a *growing* field is a *changing* field, and by **Faraday's law of
induction** a changing field induces a voltage in any wire it threads — including the very coil that
created it. By **Lenz's law**, that induced voltage always opposes the change that caused it: it pushes
against the battery, holding the current back. The battery must spend this period doing work against the
back-EMF, and that work doesn't vanish — it is being banked, joule by joule, as energy stored in the
magnetic field. The still-climbing current feeds Step 3.

### Step 3: Current Ramps Along the Exponential — the τ = L / R Transient
The tug-of-war between the battery (pushing current up) and the back-EMF (holding it back) produces the
same curve you saw in the Class 4 RC experiment, with the roles swapped: current rises fast at first, then
ever more slowly, closing in on its final value. The pace is set by the time constant **τ = L / R**, where
L is the coil's inductance (in henries) and R is the total resistance in the loop. After one time constant
the current has reached about **63%** of its final value; after five it is essentially there. For these
experiments τ is short — on the order of a fraction of a millisecond up to a few milliseconds `[VERIFY]` —
which is why the first LED's flash in Experiment 28 is only a blink: the coil's "blocking" phase is real
but brief. When the current stops changing, the back-EMF dies away to zero, handing over to Step 4.

### Step 4: Steady State — the Coil Becomes Plain Resistance
With the current constant, the magnetic field is constant too — and a constant field induces nothing.
The inductance has, electrically speaking, left the room. What remains is the copper itself: 100 feet of
26-gauge hookup wire has roughly 4 ohms of resistance distributed along its length (22-gauge, about
1.6 ohms), and a fresh 9-volt alkaline battery adds another ohm or two of internal resistance of its own.
Ohm's law now rules: roughly 9 V ÷ (4 Ω + 1.5 Ω) ≈ **1.5–2 amps** for the 26-gauge spool. This is why the
schematic "doesn't seem to make sense" until you remember the coil is not an ideal wire — in steady state
the low-resistance coil path carries nearly all the current, the voltage across it is too small to light
the LED, and the LED goes dark. The steady current also produces steady heating, which is Step 5's story.

### Step 5: Where the Heat Goes — and Why It's a Slow Warm, Not a Flash
The steady-state current dissipates power as heat in every ohm it passes through: **P = I² × R**. Two
things keep this civilized. First, the coil's resistance is spread along the *entire* 100 feet of wire, so
the heat is generated everywhere at once and shed from a large surface area — the spool warms gradually
instead of one spot flashing hot, the same reason (from the *Why Do Wires Heat Up?* explainer) that a fuse
concentrates resistance in one thin spot on purpose. Second, a sizable share of the heating happens
*inside the battery*, across its internal resistance — which is why the battery itself gets warm and runs
down quickly. The Experiment 25 screwdriver coil, wound from only 6 feet of wire (≈ 0.1 Ω), really is
close to a short: there, the battery's internal resistance is nearly the *only* thing limiting the
current, the battery does most of the heating, and that is exactly why the book says to connect it only
briefly. Releasing the button ends the steady state and triggers Step 6.

### Step 6: Disconnection — the Field Collapses and Gives Its Energy Back
When you release the button, the current tries to stop instantly — but the inductor forbids sudden change
in *either* direction. The magnetic field, which has been quietly storing energy since Step 2, now
collapses, and the collapsing field induces a voltage of the *opposite* polarity — often briefly much
larger than the 9 volts that built it — driving the stored energy back out as a short, sharp pulse (the
**inductive kick**, or flyback). In Experiment 28 this pulse is exactly what lights the *second*,
reverse-wired LED at the moment of release. The transient and the steady state are thus bookends: the
field borrows energy from the battery on the way up, holds it for as long as current flows, and repays it
in one burst on the way down.


## 3. Block Diagram

```text
CONNECT                    TRANSIENT (τ = L/R)                 STEADY STATE              DISCONNECT
Battery 9V ──> Coil looks ──> Current ramps up ────────> Current = V / R_total ──> Field collapses
               "open";        (back-EMF opposes,          (coil = plain wire        (inductive kick:
               current = 0    field stores energy;         resistance; I²R           stored energy out
               LED 1 flashes  ~63% per time constant)      heat in wire + battery;   as reverse pulse;
                                                           LED 1 goes dark)          LED 2 flashes)
```

Compare the two protective mechanisms side by side:

```text
   First milliseconds:   INDUCTANCE limits the rate of change  (di/dt held back by back-EMF)
   Ever after:           RESISTANCE limits the amount          (I = V / R, heat spread along the wire)
```


## 4. Key Parameters

| Parameter | Typical Value | Notes |
| :---------- | :--------------- | :------ |
| 22-gauge copper wire resistance | ≈ 16 Ω per 1,000 ft | 6 ft (Exp 25 coil) ≈ 0.1 Ω; 100 ft ≈ 1.6 Ω |
| 26-gauge copper wire resistance | ≈ 41 Ω per 1,000 ft | 100 ft (Exp 28 spool) ≈ 4 Ω |
| 9V alkaline internal resistance | ≈ 1–2 Ω (fresh) | Rises as the battery drains; limits worst-case current |
| Steady-state current, Exp 28 spool | ≈ 1.5–2 A | 9 V ÷ (wire R + battery internal R) |
| Time constant τ = L / R | ~0.1–5 ms | Sets how long the "blocking" transient lasts |
| Current after 1 τ / 5 τ | 63% / ≈ 99% of final | Same exponential rule as the Class 4 RC network |

`[VERIFY]` — the inductance of a hand-wound coil (and hence τ) depends heavily on turn count, spool
geometry, and whether an iron core is present; treat τ and the current figures as orders of magnitude for
the kit's parts, not measured specs.


## 5. Common Misconceptions
- **Misconception:** "The inductance is what saves the wire from melting."
  **Reality:** Inductance only *delays* — it shapes the first milliseconds. The steady-state current is set
  entirely by resistance (wire plus battery). If the total resistance really were zero, the current would
  keep ramping until something failed; inductance would merely schedule the disaster, not prevent it.

- **Misconception:** "A coil of wire is basically a zero-ohm short."
  **Reality:** Thin wire has real, useful resistance — about 4 Ω per 100 ft at 26 gauge — and the battery
  contributes 1–2 Ω of internal resistance on top. Together they cap the current at a few amps. A "short
  circuit" is not a category; it's just Ohm's law with a very small R.

- **Misconception:** "An inductor blocks DC, like a capacitor."
  **Reality:** They are exact opposites (duals). A **capacitor** passes a sudden change and then blocks
  steady DC; an **inductor** blocks the sudden change and then passes steady DC freely. That's why in
  Experiment 28 the LED lights *during* the transient and goes dark in steady state — the reverse of the
  Class 4 capacitive-coupling flash.

- **Misconception:** "Nothing bad is happening, so the coil is a safe load."
  **Reality:** An amp or two through a 9-volt battery is heavy abuse — the battery warms, its voltage sags,
  and it drains in minutes. The experiments survive because the connection is *brief*, not because the load
  is gentle. The Experiment 25 screwdriver coil in particular is nearly a dead short saved only by the
  battery's own internal resistance.


## 6. Why this matters everywhere: every coil in the world does this
Strip away the screwdriver and the spool, and what's left is a rule that applies to every winding of wire
in every machine you own: **a coil resists change in its current, stores energy in its field while current
flows, and throws that energy back the instant you try to stop it.** Engineers spend as much effort
managing those three facts as they spend exploiting them.

Start with the machines you've already built in this course. Every **relay** coil from Class 3 is an
inductor, and every time its contacts open, the collapsing field produces the same inductive kick that lit
your second LED — except across delicate contacts or transistors, where a hundred-volt spike is unwelcome.
The standard cure is a **flyback diode**: a diode placed across the coil, pointed so it does nothing in
normal operation but gives the collapse pulse a safe loop to die in. The 1N4001 diode in your Experiment 26
parts list is exactly this kind of part, and you'll find a flyback diode across nearly every relay and
motor coil ever put in a product.

The transient you watched also explains **inrush current** in the other direction — why big motors dim the
lights for a moment when they start, and why power supplies are designed to survive their first
milliseconds. A motor's windings are inductors in series with very little resistance; at the instant of
switch-on (and before the spinning motor generates its own back-EMF) the current surges far above its
running value, limited at first only by exactly the two effects in this document: winding resistance and
the L/R ramp. Every switch, breaker, and fuse feeding a motor is sized around that transient.

And the **energy-banking** behavior — borrow from the supply, store in the field, repay on demand — is not
a nuisance to be tamed but the working principle of some of the most important circuits in electronics. A
car's **ignition coil** deliberately interrupts current through an inductor so the collapsing field piles
up tens of thousands of volts across a spark-plug gap. **Switch-mode power supplies** — the wall adapters
that charge every phone and laptop — switch current into an inductor thousands of times per second,
catching each collapse to convert one voltage to another with high efficiency. **Transformers** run the
same field-coupling trick continuously between two coils, and are the reason AC won the War of the
Currents you read about in Class 1. The blink of two LEDs on your breadboard is a slow-motion replay of
what happens inside all of them.


## Bottom line
A coil across a 9-volt battery *looks* like Experiment 2's dead short, but two effects, on two timescales,
keep it civilized. In the **transient** — the first milliseconds — the coil's **inductance** fights the
change: the rising current builds a magnetic field, the growing field induces a back-EMF that opposes the
battery, and current can only climb along the τ = L / R exponential (63% per time constant), which is why
Experiment 28's first LED flashes and goes out. In the **steady state**, the field is built, the back-EMF
is gone, and the coil is just long, thin copper: current settles at V ÷ R — a few amps set by the wire's
distributed resistance plus the battery's internal resistance — producing a slow, spread-out warmth rather
than a flash. Disconnect, and the stored field collapses, repaying its borrowed energy as the reverse pulse
that lights the second LED — the same inductive kick that flyback diodes tame in every relay, that ignition
coils exploit to make sparks, and that switch-mode supplies harness to charge your phone. For more, see
[Inductance][01], [RL circuit][02], [Lenz's law][03], [Electromagnet][04], [Internal resistance][05], and
[Flyback diode][06].



[01]:https://en.wikipedia.org/wiki/Inductance
[02]:https://en.wikipedia.org/wiki/RL_circuit
[03]:https://en.wikipedia.org/wiki/Lenz%27s_law
[04]:https://en.wikipedia.org/wiki/Electromagnet
[05]:https://en.wikipedia.org/wiki/Internal_resistance
[06]:https://en.wikipedia.org/wiki/Flyback_diode
