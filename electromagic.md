
# Electromagic
This to build in the hope of creating awe & wonderment!

## Nothing Yet - Class 1

----

## Ohm's Law - Class 2
[An intuitive approach for understanding electricity](https://www.youtube.com/watch?v=X_crwFuPht4)
* For DC circuits, the water analogy is largely true

### Video Summary: "An intuitive approach for understanding electricity"
Thesis: the hydraulic/water analogy isn't just a hand-wave — it genuinely explains Ohm's law and voltage,
because both systems obey the same math for the same underlying reasons.

Opening demonstration:
* 1 m resistive wire across a 1 V supply: voltage declines smoothly and linearly from 1 V to 0 V (straight-line gradient).
* Splice a 100 Ω resistor mid-wire: voltage stays flat, drops sharply (a "step") across the resistor, then flat again — all the drop happens at the one component.
* This is just Ohm's law, but the equation gives no intuition. The marvel: electrons can't do math, yet they collectively arrange themselves to obey V = I·R every time.

The three quantities of Ohm's law (V = I·R):
* **Current (I)** — charge flow per time; literally counting electrons past a point. 1 A = 1 coulomb/s ≈ 6.2×10¹⁸ electrons/s, yet electrons drift astonishingly slowly (~1 mm every 4 s at 1 A). Drift velocity is linearly proportional to current.
* **Resistance (R)** — electrons collide with a vibrating atomic lattice (the "Plinko board" model); only on average do they drift forward. Oppositely-moving electrons cancel, so meters (and motors/LEDs) see only the net drift. Resistance makes heat, like friction.
* **Voltage (V)** — the hard one; the author admits it took years to grasp.

What voltage really is:
* Often called "electron pressure," but voltage is NOT a force — the force is the Coulombic force; voltage is electrostatic potential.
* Key analogy: voltage is to electrostatic potential energy as height is to gravitational potential energy. Push a ball up a hill → energy ∝ height; push an electron up a voltage → energy ∝ volts. Hence the electron-volt unit.
* A circuit is a track of variable height: the supply keeps a high reservoir of electrons one end, depletes the other, so electrons "roll downhill." Steeper slope (higher voltage) → more current. The "hill" is made of other electrons repelling each other.
* Where the energy lives: crowding like charges stores energy in the electric field in the space around them (energy ∝ field²). A battery uses chemistry to cram extra electrons toward one end, building the ~1 V "hill"; releasing them converts field energy to electron kinetic energy, ultimately dumped as heat until potential equilibrates flat.

The water-trough model (the payoff):
* A pump pushing fixed volume/second = constant-current source; water height = voltage; water = mobile electrons; trough = wire resistance.
* It reproduces the intro experiments exactly: smooth height gradient for a plain wire; flat-step-flat for an added resistor. A "live analog computer" plotting electron concentration vs. distance.

Consequences the model makes intuitive:
* Voltage is always relative — a voltmeter reads the difference between two points; pick a reference (a zero height).
* Voltage/resistive dividers — series resistors split the total drop in proportion to each resistance; water heights settle accordingly, no math needed.
* Power dissipation (P = I·V) — a plain wire spreads heat thinly; a resistor drops the whole voltage in one spot, so I·V dumps heat locally. Analogy: a long meandering creek vs. a waterfall dropping the same height in one place.
* Dynamic behavior — flip a switch and a wave surges, partially reflects off the resistor, and sloshes until it settles — exactly what electrons do, but near light-speed (~400 ns).

Rapid-fire clarifications (defending the model):
* Electrons really do move; even 60 Hz AC is so slow on electron timescales each half-cycle is treatable as DC.
* Conventional current (positive→negative) runs opposite to electron flow — a famous historical "blunder" that doesn't matter; just flip the labels.
* "Holes" aren't real — in some materials charge moves as electron vacancies; it's still electrons each moving a little.
* Real electrons are probabilistic waves, not billiard balls; they scatter off lattice vibrations, impurities, and crystal defects.
* The model even captures capacitance (charge per voltage), and shows why it's irrelevant for steady-state DC / Ohm's law.
* Scale: to make 2 cm of water ≈ 1 V with realistic electron counts, the trough would need to be ~7 billion miles deep. Closer line: "When we play with electricity in circuits, we are really only splashing with waves on top of a very deep ocean."

### Repeat Video's Demonstration
What you need:
* High Temp Resistance Wire (aka [Nichrome 80][03]) for Heating Elements, specifically [Ni80 20AWG 30Ft wire][01]
  This wire is 20 AWG wire has a diameter of 0.81mm and 2.10 ohms/m
  (**NOTE:** direct measurement of wire gave me 2.3 ohms/m)
* [100 Ohm Resistor, 5W 5% Tolerance Metal Oxide Film Resistor][02]
 (**NOTE:** direct measurement of resistor gave me 98.6 ohms)

We are using Nichrome wire.
Nichrome wire is a specialized heat-resistant alloy made primarily of nickel and chromium (usually an 80/20 ratio).
When electric current passes through it, the alloy heavily resists the flow of electrons,
generating intense, consistent heat without oxidizing or melting in the process.
Nichrome wire can withstand extreme temperatures up to 1,200°C (2,192°F) without oxidizing or breaking down.
Nichrome wire is the core heating element in toasters, hair dryers, and space heaters, industrial ovens, electronic vaporizers, etc.

----

## Battery Train
* [The Brilliant Science Behind the Homopolar Battery Train](https://www.youtube.com/watch?v=1TAMpaZRYqY)
* [This Battery Train Goes UP, Not Sideways!](https://www.youtube.com/watch?v=zpcZTd6ViUo)


| Item | Spec | Notes |
|--------|--------|-------|
| AA batteries | 1.5V alkaline | Energizer/Duracell work best |
| Neodymium disc magnets | 1/2" dia, N52 grade | 4–6 per battery, stacked |
| Copper wire coil | 20–22 AWG, bare copper | ~10–15 ft for a decent tunnel |


Suggest websites that don't just give you coding, but also teaches/explains of what the code is doing or why it was needed.
The website needs to be suitable for a 12 to 15 year old who already has some elementary coding skills.
The focus should be on algorithms and system design.

----

## Voltage Multiplier
* [The Simplest Voltage Booster? * Charge Pumps Tutorial](https://www.youtube.com/watch?v=dMSOaJuzrdY&t=30s)
* [Let's build a voltage multiplier!](https://www.youtube.com/watch?v=4alV5LzHLE4&t=40s)
* [Making 500,000 VOLT ARC with Marx Generator](https://www.youtube.com/watch?v=dje7uhyW23o)
* [Voltage multiplier 20* using capacitor and diode](https://youtube.com/shorts/mjGyeU6y-NE?si=QxikKWe3Cq0yq9Qj)
* [Voltage Multipliers - Half Wave Voltage Doubler Circuit](https://www.youtube.com/watch?v=yfykYXdAUNY&t=1s)
* [Voltage Multiplier Circuit using Capacitor and Diode](https://www.youtube.com/watch?v=HV5gZRhytY4)

* [How Electric Current Works Explained Simply](https://www.youtube.com/watch?v=ltvHdF2TO8w)
* [eletro_logic](https://www.youtube.com/@electro_logic)

----

## Ground Loop
A ground loop is an unwanted circular path in an electrical circuit that occurs when two or more devices are connected to a common ground
but have different ground reference potentials.
This voltage difference forces unintended electrical current to flow through the ground wiring,
manifesting as a loud hum or buzzing in audio and video

* [Ground Loop](https://www.youtube.com/watch?v=ep0jAeq1kzM)
* [Learning About Ground Loop Isolators Thanks To A Scam Product](https://hackaday.com/2026/06/15/learning-about-ground-loop-isolators-thanks-to-a-scam-product/)

----








## DIY Motor
* [3 Simple DIY Motor Experiments](https://www.youtube.com/watch?v=q9VpXz01msM)
* [How to build an electric motor. This video shows how to make your very ownelectric motor](https://www.youtube.com/watch?v=lwn15-Ze2b4)

## Joule Thief
* [Why This Circuit Works When It Shouldn’t](https://www.youtube.com/watch?v=Sh9aZ2uemk0)
* [short](https://youtube.com/shorts/wh-AgccO8zs?si=Is5o0O5famxvP9gj)

## Path of Least Resistance
* [Current does NOT take the Path of Least Resistance!](https://www.youtube.com/watch?v=rrIY1UlogBg)
* [How does electricity find the "Path of Least Resistance"?](https://www.youtube.com/watch?v=C3gnNpYK3lo)

## What is the Speed of Electricity?
* [How Electricity Actually Works](https://www.youtube.com/watch?v=oI_X2cMHNe0)

## Computation
* [Computers Are Just Rocks Doing Math](https://www.youtube.com/watch?v=sgVosaLhPV0)

## Solar Panels, Motors, etc. are Reversible Transducers
Solar panels convert light into electricity but you can also have solar panel convert electricity into light
Are all transducers reversible?

* [Taking Pictures with an LED](<https://www.youtube.com/watch?v=9J-b33tDjL0>)

## Radio Waves
* [How to Make EMP JAMMER Circuit at Home - Very Simple](https://www.youtube.com/watch?v=aEuy8xvEXXU)




[01]:https://www.amazon.com/gp/product/B0FBKZ6B35
[02]:https://www.amazon.com/uxcell-Tolerance-Resistance-Electronic-Experiments/dp/B07RT6X44H
[03]:https://pelicanwire.com/2024/07/the-role-of-nichrome-wire-in-modern-technology/

