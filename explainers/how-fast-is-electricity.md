# How Fast Is Electricity?
I'm told the speed of a randomly moving electron in a wire is about 10.0E6 m/sec.
I'm also told that the drift velocity of electron is less than 0.1 mm/sec when voltage is applied to that wire.
Electricity is all about pushing a long line of electrons, standing shoulder to shoulder,
so electricity is instantaneous when a voltage is applied.

What is the answer to these questions:

1. If I had a pair of wires from earth to the sun, how long would it take to turn on a light bulb at the sun?
1. When would I see electron drift on the return path of the wire?
1. What is the speed of electricity?

Three speeds get tangled together whenever someone asks "how fast is electricity?" The whole puzzle —
and the answers to your three questions — comes loose the moment you keep them separate.

So before the questions, let's check the three facts you started with.

## Fact check
**Claim 1 — "A randomly moving electron in a wire travels about 10×10⁶ m/s."**
*Roughly right, a touch high.* The fast, jittery motion is real. In a metal like copper the relevant
figure is the **Fermi velocity**, about **1.6×10⁶ m/s** — so closer to 1–2 million m/s than ten million,
but you have the right idea and the right order of magnitude. The crucial part is the word *randomly*: each
electron ricochets off atoms in every direction, so all that blazing speed averages out to **zero net
travel**. It's a swarm of gnats in a jar, not a marching band.

**Claim 2 — "Drift velocity is less than 0.1 mm/s when voltage is applied."**
*Correct.* Apply a voltage and you tilt that random jitter ever so slightly in one direction. For an
ordinary current in household wire the net **drift velocity** works out to roughly **0.07 mm/s** — slower
than the minute hand of a clock. Your "< 0.1 mm/s" is spot on.

**Claim 3 — "Electricity is a long line of electrons standing shoulder to shoulder, so it's instantaneous
when voltage is applied."**
*Half-true, and the half that's wrong is the important half.* The "shoulder-to-shoulder" picture is a
genuinely useful intuition: the wire is *already full* of electrons, so you don't wait for one to crawl from
the switch to the bulb — push in one end and a different one pops out the far end almost at once, like water
in a pipe that's already full. **But it is not instantaneous.** Nothing in physics is. The "push" travels at
a large but *finite* fraction of the speed of light. And, strictly, the energy doesn't ride inside the line
of electrons at all — it travels in the **electromagnetic field around the wires**, which is what sets the
electrons moving. (Veritasium's [*The Big Misconception About Electricity*][01] is the famous deep dive.
Also see the follow-up videos, [*How Electricity Actually Works*][04] and [*I bought 1000 meters of wire to settle a physics debate*][05].)
For our purposes the headline is simply: **fast, but finite — capped by the speed of light.**

---------------

## The key idea: there are three speeds, not one
Almost every confusion about electricity comes from blurring these together:

1. **Thermal (random) speed — ~1.6×10⁶ m/s.** Blisteringly fast, but random, so it carries no current.
   Net progress: zero.
2. **Drift speed — ~0.1 mm/s.** The actual net crawl of electrons once voltage is applied. This is the
   "marching" part, and it is glacially slow.
3. **Signal (energy) speed — a large fraction of the speed of light.** The electromagnetic "go" command
   that races down the wire and sets *every* electron drifting nearly at once. This is what people *mean*
   when they say electricity is "fast."

Hold those three apart and your questions answer themselves.

## 1. How long to turn on a light bulb at the sun?
This is question 3 in disguise, so let's nail down the signal speed first, then come back.

The bulb lights when the **signal** — the electromagnetic field that switches the electrons on — reaches it.
That signal travels at essentially the speed of light, **c ≈ 3.0×10⁸ m/s**. The Earth–sun distance is one
**astronomical unit**, about **1.496×10¹¹ m** ([1 AU][02]).

```text
time = distance ÷ speed
     = 1.496×10¹¹ m ÷ 3.0×10⁸ m/s
     ≈ 499 seconds
     ≈ 8 minutes 19 seconds
```

So at the absolute speed-of-light limit, **about 8⅓ minutes** — the same trip sunlight makes, which is a fun
coincidence to point out. In a *real* cable the signal is slowed by the insulation around it (the [velocity
factor][03] of a typical line is roughly 0.6–0.7 of c), so a real pair of wires would take more like **12–14
minutes**. Either way: minutes, not instants — and absolutely *not* the millennia an electron itself would
need (see below).

## 2. When would I see electron drift on the return path?
Here's where keeping the three speeds separate pays off. Two very different answers, depending on what
"see drift" means:

**When does drift *begin* on the return wire?** Almost as fast as everything else. The electromagnetic field
sets up along *both* wires at once and couples across the small gap between them, so electrons in the return
path start drifting as soon as the signal reaches their stretch of wire — at the **signal speed (near c)**,
not after some long wait. Near the battery, return-path drift starts essentially immediately; out by the sun,
it starts at the ~8-minute mark when the wave gets there. The naive expectation — "I must wait for the signal
to run all the way to the sun *and back* (2 AU, ~16 minutes) before any return current flows" — is **wrong**.
You don't wait for the round trip.

**When would a *particular electron* drift all the way back?** Effectively never. At 0.1 mm/s, the time for
one electron to physically traverse a single AU is:

```text
time = 1.496×10¹¹ m ÷ 1×10⁻⁴ m/s
     = 1.496×10¹⁵ seconds
     ≈ 47 million years
```

So an electron that leaves Earth would take **tens of millions of years per AU** to creep to the sun. You
will see *current* (drift) on the return path within minutes; you will **never** see the *same electron*
complete the trip. That gap — minutes versus 47 million years — is the entire lesson in one comparison.

## 3. What is the speed of electricity?
It depends which "electricity" you mean — and that's the real answer:

- The **electrons themselves** drift at about **0.1 mm/s**. Painfully slow.
- The individual electrons' **random thermal motion** is about **1.6×10⁶ m/s**, but it nets to nothing.
- The **electrical signal/energy** — the thing that actually "turns on the bulb" — travels at a **large
  fraction of the speed of light**, typically **50–99% of c** (≈1.5–3×10⁸ m/s) depending on the wire and its
  insulation.

When someone says "electricity travels at the speed of light," they're talking about the **signal**, and
they're *nearly* right: it's a hair under light speed, and crucially it is **finite, not instantaneous**. The
electrons are the slowpokes; the field is the sprinter.

---------------

## Bottom line
Your model is mostly sound — you just had three different speeds wearing the same name. Electricity is a
pipe that's already full of electrons (true), each jittering at ~10⁶ m/s randomly (true) and drifting forward
at ~0.1 mm/s once switched on (true). What is **not** true is "instantaneous": the *signal* that starts the
drifting everywhere travels fast but finite, just under the speed of light. Wire Earth to the sun and your
bulb lights in about **8 minutes** — while any single electron that set out would still be drifting toward the
sun **47 million years** later.



[01]:https://www.youtube.com/watch?v=bHIhgxav9LY
[02]:https://en.wikipedia.org/wiki/Astronomical_unit
[03]:https://en.wikipedia.org/wiki/Velocity_factor
[04]:https://www.youtube.com/watch?v=oI_X2cMHNe0&t=192s
[05]:https://www.youtube.com/watch?v=2Vrhk5OjBP8

