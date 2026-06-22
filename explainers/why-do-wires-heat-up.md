# Why Do Wires Heat Up?
When a great deal of current is flowing in a wire, it can heat up and get very hot.

What is the answer to these questions:

1. What mechanism in the wire is causing the heating?
1. What is the relationship between the size of the wire, the amount of current, and the amount of heat produced?
1. Is this relationship the same for DC and AC currents?
1. Why do electrical power plants' high-power lines, going long distance, use very high voltages, and are high above the ground?

Your starting fact is **correct**: push a lot of current through a wire and it heats up — that's exactly why a
toaster glows, why a fuse blows, and why an overloaded extension cord can start a fire. The heating has a
name, **resistive heating** (also called **Joule heating** or **I²R loss**), and one tidy equation explains
all four of your questions at once. Let's build up to it.


## Fact check
**Claim — "A great deal of current flowing in a wire makes it heat up and get very hot."**
*Correct.* Every real wire has some electrical **resistance**, and forcing current through resistance
*always* produces heat. With a little current the warming is too small to notice; with a lot of current it
can melt insulation or glow red. The amount of heat isn't just "more current, more heat" in a straight line,
though — it climbs much faster than that, which is the key surprise in question 2.

---------------


## 1. The mechanism: electrons bumping into atoms
Inside a metal wire, current is a drift of electrons through a lattice of fixed metal atoms. As those
electrons are pushed along by the voltage, they **collide with the vibrating atoms** and lose a little of
their energy on each bump. That lost energy doesn't vanish — it becomes **extra vibration of the atoms**, and
vibration of atoms *is* heat. So the wire warms up.

That built-in opposition to electron flow is what we call **resistance** (symbol **R**, measured in ohms).
Resistance is friction for electrons, and like friction it turns orderly motion into heat. A material with
lots of collisions (high resistance, like nichrome) makes a great heating element; a material with few (low
resistance, like copper) makes a good wire that *wastes* little as heat.


## 2. Size, current, and heat: the I²R law
The heat produced per second (the power, in watts) is:

```text
P = I² · R

  P = heating power (watts)
  I = current (amperes)
  R = resistance of the wire (ohms)
```

Two relationships hide in that short formula, and both matter:

**Heat grows with the *square* of the current.** This is the big one. Double the current and you don't get
twice the heat — you get **four times** (2² = 4). Triple it and you get **nine times**. For example, 10 A
through a 0.1 Ω wire wastes 10² × 0.1 = **10 W**; bump it to 20 A and it jumps to 20² × 0.1 = **40 W**. This
square-law is why "a great deal of current" is so much worse than "a little" — and why it's the current, far
more than the voltage, that determines how hot a wire gets.

**Heat grows with resistance, and that's where wire size comes in.** A wire's resistance is:

```text
R = ρ · L / A

  ρ = resistivity of the metal (a constant for copper, aluminum, etc.)
  L = length of the wire
  A = cross-sectional area (how thick it is)
```

So a **thicker** wire (bigger area **A**) has **lower** resistance and runs **cooler** for the same current,
while a **thinner** or **longer** wire has higher resistance and runs hotter. That's the whole reason
electrical codes specify a minimum wire gauge for a given current: a thick enough wire keeps R — and therefore
I²R heat — safely low. A wire that's too thin for its current is a space heater waiting to happen.

Putting both together: **heat = (current)² × resistance**, where resistance rises with length and falls with
thickness. Want less heat? Use less current, a shorter run, or a fatter wire.


## 3. Is it the same for DC and AC?
**The mechanism and the I²R law are identical** — both DC and AC heat the wire by the same electron-collision
process, and for AC you simply use the **RMS** (root-mean-square) value of the current in P = I²R, which is the
"effective" current that does the same heating as an equivalent DC.

There's **one wrinkle for AC**: the **skin effect**. Alternating current crowds toward the outer surface of
the wire, leaving the core underused, so AC behaves as though it's flowing through a *thinner* wire — which
means a **higher effective resistance** and therefore **more heat** than DC of the same RMS value. At ordinary
power-line frequency (60 Hz) this is a small correction for normal wires, but at high frequencies it becomes
large. (See the companion note [Where Does Electricity Flow in a Wire?][01] for how deep the skin effect goes
and how it scales with frequency.) So: same fundamental law, with AC paying a small-to-large surcharge
depending on frequency.


## 4. Why high-voltage lines run at high voltage — and hang high up
These are two different "high"s answering two different problems, so let's take them in turn.

**Why very high *voltage*?** To dodge the I²R square-law over hundreds of miles. The power delivered is
**P = V × I** (volts × amps), so a given amount of power can be sent either as *high voltage and low current*
or *low voltage and high current*. Since heat loss depends on **I²**, you desperately want the current **low**
— and that means cranking the voltage **up**.

A concrete example: to send **1 megawatt** of power —

- at **1,000 volts** you'd need **1,000 amps**, and the I²R losses would be enormous;
- at **100,000 volts** you need only **10 amps** — and since loss scales as current squared, you've cut the
  heating loss by a factor of (1000/10)² = **10,000×**.

That is exactly why the grid steps voltage *up* to hundreds of thousands of volts for the long-distance trip
and *down* again near homes. And this is only possible because **transformers** can change AC voltage easily —
the very advantage that won the [War of the Currents][02] for AC over DC.

**Why so high *off the ground*?** Mostly safety and physics, not heat:

1. **Clearance from people and objects.** At 100,000+ volts those bare conductors are lethal, and you can't
   coat them in thick household-style insulation. Height keeps them out of reach of people, vehicles, trees,
   and buildings.
2. **Air itself is the insulator — but only if there's enough of it.** Very high voltage can **arc** (jump)
   across a gap to anything close enough. Keeping the lines high (and well separated) maintains enough air gap
   to stop the electricity from flashing over to ground.
3. **Room to sag and cool.** The conductors heat up under load and on hot days, expanding and **sagging**
   lower between towers; the extra height preserves a safe gap even at maximum sag. Being out in open air also
   lets them shed their (smaller, thanks to high voltage) heat.

So high voltage is about **efficiency** — beating the I²R loss — while high mounting is about **safety and
insulation**. They're separate fixes that happen to live on the same tower.


## Bottom line
Wires heat up because moving electrons **collide with the metal's atoms**, and that friction-like
**resistance** turns electrical energy into heat. The amount follows **P = I²R**: heat rises with the
**square** of the current and in proportion to the wire's resistance — which is why a **thicker** (or shorter)
wire runs cooler and a too-thin wire runs dangerously hot. DC and AC obey the **same law** (use RMS current
for AC), with AC paying a modest extra penalty from the skin effect that grows with frequency. And the grid
sends power at **very high voltage** precisely to keep the current — and thus the I²R heat — tiny over long
distances, while hanging those lines **high in the air** to keep their lethal, barely-insulated voltage safely
away from everything below.



[01]:where-does-electricity-flow-in-a-wire.md
[02]:war-of-the-currents.md
