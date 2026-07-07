# The Role of Feedback: From a Buzzing Relay to Self-Driving Cars
In Class 3's relay oscillator (Experiment 8), you wired a relay so that its own output — the closing of its
contacts — reached back around and controlled its own input, the coil. Press the button once, and the relay
buzzes and clicks on its own, over and over, with no further help from you.

What is the answer to these questions:

1. How does routing a relay's output back to its own input make it oscillate?
1. What is feedback, and what's the difference between the two kinds?
1. Why does this same idea show up in thermostats, cruise control, robots, and self-driving cars?

The short answer: what you built is a **feedback loop** — the single most important idea in how machines
regulate themselves. The relay oscillator is a toy-sized, audible version of a principle that also keeps a
thermostat holding 70°F, keeps a drone hovering in place, and keeps a self-driving car centered in its lane.
Let's take it apart.


## 1. Overview
A **feedback loop** exists whenever a system's output is fed back around and used to influence its own
input. There are exactly two flavors. In **negative feedback**, the fed-back signal opposes or cancels the
thing that caused it — the system pushes back toward a target and settles down (this is how a thermostat
holds a steady temperature). In **positive feedback**, the fed-back signal reinforces the thing that caused
it — the effect grows or repeats itself rather than settling, which is why a microphone held too close to a
speaker shrieks, and why a relay oscillator buzzes.

The Class 3 relay oscillator wires a relay's **normally-closed (NC) contact** in series with its own coil.
Current flows into the coil through that NC contact, which energizes the coil's electromagnet; the magnet
pulls the armature, which *physically opens the very contact that was feeding it*. With current cut, the
magnet releases, the spring snaps the armature back, the NC contact closes again — and the whole cycle
repeats, entirely on its own, for as long as power is supplied. That self-interrupting loop, running at the
speed of the relay's mechanical response, is what produces the clicking or buzzing sound. It's the same
circuit that powered old electric doorbells and trembler bells for over a century.


## 2. Detailed Operation

### Step 1: Button Press Applies Power
Pressing the button connects the supply voltage to the circuit. Current has a path into the relay's coil
**only through the relay's own normally-closed (NC) contact** — the contact that is closed by default when
the coil is unpowered. This is the setup condition: at rest, the path is open for current to flow, ready to
begin the cycle. This closed path is the input to Step 2.

### Step 2: Coil Energizes and Builds a Magnetic Field
Current flows through the coil, and the coil becomes an electromagnet. Inside the relay, this magnetic force
begins pulling on a spring-loaded metal armature — the moving part that physically carries the NC contact.
This takes a small but nonzero amount of time (the relay's **operate time**, typically a few milliseconds for
a small electromechanical relay), because the armature has mass and the magnetic field needs time to build.
That built-up pull is the input to Step 3.

### Step 3: The Armature Moves and Opens Its Own Feedback Path
Once the magnetic pull is strong enough to overcome the return spring, the armature snaps toward the coil.
Because the very contact carrying current to the coil is mounted on this armature, the armature's own motion
**physically breaks the connection that was powering the coil**. This is the feedback step: the output
(armature position) reaches back and cuts off the input (coil current) that caused it. This is a form of
**negative feedback on current** — the moving contact acts to remove the very cause of its own motion — but
because the whole assembly has mechanical momentum and a spring, it doesn't simply settle at a midpoint; it
overshoots and disconnects completely, feeding the next step.

### Step 4: Coil De-Energizes and the Spring Resets the Armature
With the current path broken, the electromagnet's field collapses (again, not instantly — this is the
relay's **release time**). The return spring, no longer fighting the magnetic pull, pulls the armature back
to its rest position. As it returns, the armature **re-closes the NC contact**, restoring the very path that
powers the coil. This reset is the input that hands control back to Step 1, and the cycle begins again
immediately — with no further input from the button, which only needed to supply continuous power.

### Step 5: The Cycle Repeats, Producing Continuous Oscillation
Steps 1 through 4 now repeat on their own, driven entirely by the relay's own mechanical timing (operate
time plus release time) rather than by anything external. Each full cycle produces one audible click, and
enough clicks per second blur into the buzz you hear. This self-sustaining repetition — output continuously
re-triggering input — is exactly what the word **oscillator** means: a circuit that produces a repeating
signal with no repeating input.

### Step 6: A Capacitor Slows and Smooths the Cycle
Wired straight, the bare relay clicks as fast as its own mechanics allow — often fast enough to burn or
pit the contacts from constant arcing. Placing a capacitor (as in the experiment: 1,000 µF, 2,200 µF, or
4,700 µF) across the coil changes the timing without changing the feedback structure. When the NC contact
opens, the capacitor — charged during Step 2 — discharges into the coil instead of letting it de-energize
immediately, keeping the coil powered for a short extra stretch. A **larger capacitor stores more charge and
releases it more slowly**, so it holds the coil energized longer, which lengthens the "on" portion of each
cycle and slows the oscillation rate. This is why the experiment has you try three capacitor sizes side by
side: bigger capacitance, slower and gentler clicking; the underlying feedback loop is unchanged, only its
timing is tuned.


## 3. Block Diagram

```text
   Button ──> Supply Voltage ──> NC Contact (closed) ──> Coil ──> Magnetic Field
                                       ^                                │
                                       │                                v
                              Spring resets armature <── Armature pulled, opens NC contact
                                       │                                │
                                       └────────── feedback path ───────┘
```

Compare this to the general shape every feedback system shares:

```text
Target/Setpoint ──> [Compare] ──> Error ──> [Controller] ──> Output ──> Plant/Process
                        ^                                                    │
                        └──────────────── Sensor / feedback path ────────────┘
```

The relay oscillator is a stripped-down special case: there is no separate sensor and no adjustable
setpoint — the mechanical contact *is* both the comparator and the feedback path, hard-wired to always flip
the moment its own condition is satisfied.


## 4. Key Parameters

| Parameter | Typical Value | Notes |
| :---------- | :--------------- | :------ |
| Relay operate time | ~5-15 ms | Time for coil energizing to pull the armature |
| Relay release time | ~2-10 ms | Time for spring to reset the armature after de-energizing |
| Coil-only oscillation rate | tens of Hz (audible click/buzz) | Set purely by relay mechanics |
| With 1,000 µF capacitor | slower, several Hz | Larger RC-like time constant with coil |
| With 4,700 µF capacitor | slowest of the three tested | More stored charge extends "on" time further |

`[VERIFY]` — exact operate/release times and resulting oscillation frequencies depend on the specific relay
model used in the kit; treat the values above as typical orders of magnitude for small electromechanical
relays, not a spec for your exact part.


## 5. Common Misconceptions
- **Misconception:** "The relay oscillator needs a repeating signal fed into it to keep clicking."
  **Reality:** The button supplies steady, unchanging power. The repeating behavior comes entirely from the
  relay feeding its own output back into its input — no oscillating input exists anywhere in the circuit.

- **Misconception:** "Feedback always calms a system down."
  **Reality:** Only **negative** feedback (output opposing its own cause) tends toward stability. **Positive**
  feedback (output reinforcing its own cause) drives runaway growth or, as here, self-sustained repetition.
  Whether feedback stabilizes or destabilizes depends on its sign and its timing, not on the mere presence of
  a feedback path.

- **Misconception:** "The capacitor is what causes the oscillation."
  **Reality:** The oscillation exists with no capacitor at all — it's a direct result of the self-breaking
  contact. The capacitor only changes the *timing* (slower, gentler cycles); remove it and the relay still
  oscillates, just faster and harder on the contacts.


## 6. Why this matters everywhere: feedback as a general-purpose idea
Strip away the relay and the capacitor, and what's left is a shape that shows up in almost every controlled
system humans build: **measure what's actually happening, compare it to what you want, and use the
difference to correct the output.** That difference is called the **error signal**, and a system built this
way is a **closed-loop control system** — "closed" because the loop from output back to input is complete,
the way the relay's NC contact completes a loop back to its own coil.

A **thermostat** is the everyday example: it measures room temperature (the sensor), compares it to the
temperature you set (the target), and turns the furnace on when the room is too cold and off when it's warm
enough — negative feedback holding the room near a steady setpoint, the same "measure, compare, correct"
shape as the relay, just with a slower, tunable loop instead of a hardwired mechanical one.

**Control theory** is the branch of engineering that studies exactly this shape mathematically — how fast a
loop should react, how much it should correct, and how to avoid it overcorrecting into oscillation (imagine a
thermostat so aggressive it overshoots hot, then cold, then hot again — an unwanted echo of the relay
oscillator's runaway behavior). The most common tool of the trade is the **PID controller**
(Proportional-Integral-Derivative), which blends three ways of reacting to error — how big the error is
right now, how long it's persisted, and how fast it's changing — into one smooth correction. Nearly every
robot, drone, cruise control system, and industrial process running today has a PID loop, or something like
it, at its core.

**Robotics** leans on this constantly. A robot arm's motor doesn't just "move to a position" open-loop and
hope — an encoder feeds back the arm's actual position, a controller compares it to the target position, and
the motor is driven by the resulting error, correcting continuously until the error shrinks to zero. A
line-following robot reads its sensor, compares what it sees to "centered on the line," and steers by the
error, hundreds of times per second — negative feedback keeping the robot centered exactly the way negative
feedback keeps a thermostat's room at temperature.

**Self-driving cars** stack many of these loops on top of each other. Cameras, radar, and lidar continuously
measure the car's position relative to the lane lines and nearby vehicles (sensing); a control system
compares that to where the car *should* be (comparison); and it corrects the steering, throttle, and brakes
accordingly (correction) — thousands of times per second, forming a closed loop from sensor to actuator and
back to sensor again. Zoom in far enough, and even that towering stack of machine learning and sensor fusion
rests on the same primitive you heard clicking on your breadboard: an output looping back to adjust its own
input.


## Bottom line
The relay oscillator "just" routes its own output back to its own input, and that single wiring choice is
enough to turn a steady button-press into continuous, self-sustained buzzing — because the moving contact
breaks the very connection that powers it, resets, and repeats, a case of feedback whose timing produces
oscillation rather than stability. That same core idea — sense the output, compare it to a target, correct
the input — is **feedback**, and depending on its sign it either stabilizes a system (**negative feedback**,
as in a thermostat) or drives it into runaway repetition (**positive feedback**, as in the relay or a
screeching microphone). Scaled up and formalized, this is exactly what **control theory** studies, what a
**PID controller** implements, what makes a **robot arm** hold a position, and what lets a **self-driving
car** stay centered in its lane — all of them are, underneath the sensors and software, the same
measure-compare-correct loop you built with a relay and a breadboard. For more, see [Feedback][01],
[Negative feedback][02], [Electromechanical relay][03], [PID controller][04], and
[Trembler bell / electric bell mechanism][05].



[01]:https://en.wikipedia.org/wiki/Feedback
[02]:https://en.wikipedia.org/wiki/Negative_feedback
[03]:https://en.wikipedia.org/wiki/Relay
[04]:https://en.wikipedia.org/wiki/PID_controller
[05]:https://en.wikipedia.org/wiki/Electric_bell
