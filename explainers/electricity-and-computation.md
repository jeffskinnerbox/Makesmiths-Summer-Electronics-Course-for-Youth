# Electricity and Computation: Claude Shannon's Thesis
In Class 3 you wired up relays and switches and watched them snap between two states — **on** and **off**.

What is the answer to these questions:

1. What is the circuit actually *for* — the current and voltage, or the on/off state?
1. What did people know about computing with switches before 1937?
1. What did a 21-year-old graduate student named Claude Shannon prove in his master's thesis, and why does
   it matter?

Here's the idea to hold onto before we start: in the relay and switch experiments, the voltage, the current,
the resistance — all of that is just **plumbing**. It's the mechanism. The actual *point* of the circuit is
the **state** it creates: switch open or switch closed, relay energized or not, light on or off. That
distinction — state is the goal, electricity is just the mechanism that gets you there — turns out to be one
of the most important ideas in the history of technology. In 1937, a young engineer named **Claude Shannon**
figured out exactly how far that idea could go, and the answer built the modern computer.


## The circuit's real job: making a state, not making current flow
Think back to the manual switch and relay experiments. You could measure the voltage across the relay coil,
the current through it, the resistance of the wire — real electrical properties, all correct, all
measurable. But none of that was why you built the circuit. You built it so that flipping one switch would
cause another part of the circuit to be **either on or off** — a light, a motor, a second relay. The
electricity was doing work, sure, but the work it was doing was to **create and hold a state**: one of
exactly two conditions, with nothing in between.

This shows up again and again in electronics, often in disguise. A thermostat's contacts don't care about
their own voltage drop — they care whether the furnace circuit is *open* or *closed*. A doorbell button
isn't valued for its resistance — it's valued for switching a chime circuit *on*. Once you notice it, you'll
see this pattern everywhere: **the goal is the state; the volts and amps are just how you build and move
that state around.** Keep that in mind, because it is exactly the observation that let one graduate student
change the world.


## Before 1937: switching was a craft, not a science
By the 1930s, the Bell Telephone System already used huge banks of electromechanical **relays** to route
phone calls automatically — no human operators needed for the switching itself. These relay circuits were
enormous and intricate, built by trial and error, engineer intuition, and years of hard-won experience. There
was no formula that told you the *fewest* relays needed to perform a given switching job, no systematic way
to check whether a design was correct, and no shared language for describing what a circuit of switches
actually *did*. It was skilled craftsmanship — closer to an art than an engineering discipline. Meanwhile, in
an entirely separate corner of intellectual life, mathematicians had spent nearly a century working out
**symbolic logic**: a system invented by the British mathematician **George Boole** in the 1840s for
manipulating statements that are strictly **true or false**, using operators like AND, OR, and NOT. Boole's
algebra was elegant, rigorous — and, at the time, considered a piece of abstract philosophy with no obvious
connection to machinery at all. Two separate worlds: telephone engineers building switching circuits by feel,
and logicians working with true/false statements on paper. Nobody had connected them.


## The insight: a switch is a Boolean variable
Claude Shannon was 21 years old, finishing a master's degree in electrical engineering at MIT, when he wrote
that connection down. Two experiences primed him for it. As an undergraduate at the University of Michigan,
he had taken a philosophy course covering Boole's symbolic logic — unusual reading for an engineering
student. Then, during a summer job at Bell Telephone Laboratories, he worked directly with the relay circuits
that ran the phone network's automatic switching — the same electromechanical tangle described above.

Shannon noticed something nobody had put into words before: a relay or switch has exactly **two** possible
states — open or closed, on or off — and Boole's logic has exactly **two** possible truth values — false or
true. Two states, two values. They're the same mathematical object wearing different clothes. If you let
"switch closed" stand for "true" and "switch open" stand for "false," then wiring switches **in series**
behaves exactly like the logical operator **AND** (both must be closed for current to pass), and wiring
switches **in parallel** behaves exactly like **OR** (either one closed lets current through). A
normally-closed relay contact that opens when energized behaves like **NOT** (it flips true to false). Every
circuit built purely from on/off switches, no matter how complicated, could be written down as a Boolean
expression — and, just as importantly, any Boolean expression could be built as a circuit.

His 1937 master's thesis, **"A Symbolic Analysis of Relay and Switching Circuits,"** laid this out in full.
It showed how to translate a switching circuit into Boolean algebra, simplify that algebra using rules
mathematicians already knew, and translate the simplified algebra back into a circuit — usually one with
noticeably fewer relays than the original. Switching circuit design stopped being a craft passed down by
intuition and became a branch of mathematics: you could now *prove* a design was correct, and *calculate* the
minimum number of switches needed, instead of guessing and testing.


## Why this thesis still runs the world
Every digital device you've ever touched — phone, laptop, game console, calculator — is built from circuits
that have exactly two stable states, just like your Class 3 relay, except the switches are now **transistors**
switching in billionths of a second instead of relays clacking open and shut. Engineers still call those two
states **0** and **1**, wire transistors together to build **AND**, **OR**, and **NOT** gates exactly as
Shannon described, and combine millions of those gates into adders, memories, and processors. The chip in
your phone is, at its logical core, the same idea in Shannon's thesis — just scaled up from a handful of
relays to billions of transistors, and sped up from clicks per second to billions of switches per second.

That's why historians of technology often call Shannon's thesis **the most important master's thesis of the
twentieth century**: it supplied the missing bridge between electrical engineering (which knew how to build
circuits) and mathematical logic (which knew how to reason about true and false) — the exact bridge every
digital computer depends on. The next time you flip a switch or watch a relay click, remember: you're not
just moving electricity. You're creating a state — true or false, on or off — and that simple act, done
billions of times a second inside a modern processor, is computation itself.


## Bottom line
In Class 3, the relay circuit's real purpose wasn't its voltage or current — it was the **on/off state** it
created, with the electricity serving only as the mechanism to make and hold that state. Before 1937,
switching circuits were built the same way for decades — by skilled trial and error, disconnected from the
formal logic mathematicians had already worked out with Boole's true/false algebra. **Claude Shannon**, a
21-year-old MIT master's student who'd studied Boole's logic in college and then worked hands-on with Bell
Labs' relay switching circuits, saw that a two-state switch and a two-value Boolean variable are the same
thing — and proved in his 1937 thesis that any switching circuit could be designed, simplified, and verified
using Boolean algebra. That single insight turned circuit design from art into science, and it is the direct
intellectual ancestor of every logic gate in every computer chip made since. For more, see
[Claude Shannon][01], [A Symbolic Analysis of Relay and Switching Circuits][02], [George Boole][03], and
[Boolean algebra][04].



[01]:https://en.wikipedia.org/wiki/Claude_Shannon
[02]:https://dspace.mit.edu/handle/1721.1/11173
[03]:https://en.wikipedia.org/wiki/George_Boole
[04]:https://en.wikipedia.org/wiki/Boolean_algebra
