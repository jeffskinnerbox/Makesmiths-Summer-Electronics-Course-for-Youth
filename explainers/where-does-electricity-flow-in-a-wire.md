# Where Does Electricity Flow in a Wire?
I'm told that direct current (DC) flows uniformly through the entire cross-section of the wire.
The current travels equally through the core and the outer edges.
On the other hand, alternating current (AC) pushes toward the outside of the wire (the "skin effect").

What is the answer to these questions:

1. For AC current, how deep into the wire is the "skin effect"?
1. Does the skin effect vary with AC frequency, or voltage level, or size of the wire?
1. What are the practical/engineering impacts of the skin effect?

Good news first: your starting picture is **correct**. DC really does spread itself evenly across the whole
cross-section, and AC really does crowd toward the surface. The only thing missing is the *number* — "how
deep is the skin?" — and once you have that one number, all three questions fall out of it.

So before the questions, let's check the two facts you started with.


## Fact check
**Claim 1 — "DC flows uniformly through the entire cross-section."**
*Correct.* With steady DC, the current settles into the path of least resistance, and for a uniform wire that
means spreading out evenly — every square millimeter of copper, core and edge alike, carries the same share.
A fat wire beats a thin one purely because it offers more parallel cross-section. Nothing here depends on
where in the wire you look.

**Claim 2 — "AC pushes toward the outside of the wire — the skin effect."**
*Correct, and for a good reason.* A changing current creates a changing magnetic field *inside* the wire, and
that changing field induces little swirling "eddy" currents (Lenz's law) that oppose the main current most
strongly at the **center** and least at the **surface**. The result: AC is shoved outward into a thin shell
near the skin. The faster the current alternates, the harder it gets pushed out. So your intuition is exactly
right — the only question is *how* thin that shell is.

---------------


## The key idea: one number called skin depth
The whole topic collapses into a single quantity, the **skin depth** (symbol **δ**, "delta"). It's the depth
below the surface at which the current density has dropped to about **37%** (technically 1/e) of its value at
the surface. Current doesn't stop dead at that line — it fades exponentially — but δ is the honest "most of
the action happens within here" number.

For a non-magnetic conductor like copper or aluminum, the formula is short:

```text
δ = sqrt( ρ / (π · f · μ) )

  ρ = resistivity of the metal  (copper ≈ 1.68×10⁻⁸ Ω·m)
  f = frequency of the AC       (in hertz)
  μ = magnetic permeability     (copper ≈ μ₀ = 4π×10⁻⁷)
```

The one feature to notice: **f is under a square root**. Multiply the frequency by 100 and the skin depth
shrinks by only 10. That single fact answers question 2 before we even get there.


## 1. How deep is the skin?
Deep enough to ignore at the wall outlet; vanishingly thin at radio frequencies. Plugging real numbers into
copper:

| Frequency        | Skin depth δ (copper) | What that's comparable to        |
|------------------|-----------------------|----------------------------------|
| 60 Hz (mains)    | ≈ 8.5 mm              | thicker than most wires you own   |
| 1 kHz            | ≈ 2.1 mm              | a thick speaker wire             |
| 100 kHz          | ≈ 0.21 mm             | a sheet of paper                 |
| 1 MHz (AM radio) | ≈ 66 µm               | a human hair                     |
| 1 GHz (Wi-Fi-ish)| ≈ 2.1 µm              | a bacterium                      |

A handy rule of thumb for copper: **δ ≈ 66 µm ÷ √(f in MHz)**, or equivalently **δ ≈ 66 mm ÷ √(f in Hz)**.

The punchline of the table: at **60 Hz the skin is ~8.5 mm deep**, which is *larger than the radius of almost
any wire in your house* — so for ordinary mains wiring the skin effect barely matters and DC's "uniform fill"
picture is still nearly true. But at **1 MHz the skin is thinner than a hair**, so a thick copper rod is
carrying current only in its outermost wisp and the entire core is dead weight.


## 2. Does it vary with frequency, voltage, or wire size?
Three separate questions, three clean answers:

- **Frequency — yes, strongly (this is the main lever).** Skin depth shrinks as **1/√f**. Higher frequency →
  thinner skin → current crammed nearer the surface. Going from 60 Hz to 1 MHz dropped δ from 8.5 mm to
  66 µm, a factor of ~130.
- **Voltage (or current level) — no, not at all.** Skin depth depends only on the *frequency* and the *metal*
  (its resistivity ρ and permeability μ). It does **not** depend on how many volts or amps you push. A 1-amp
  and a 1000-amp signal at the same frequency have the same skin depth; the big one just has proportionally
  more current packed into that same thin shell.
- **Wire size — δ itself doesn't change, but whether you *care* does.** The skin depth is a property of the
  metal and frequency, so it's the same number in a thin wire or a fat busbar. What changes is the
  *comparison*: skin effect only bites when the wire's radius is comparable to or larger than δ. If the whole
  wire is thinner than one skin depth (as at 60 Hz), current fills it almost uniformly and there's no penalty.
  Make the wire much fatter than δ and the extra copper in the core does essentially nothing.

A fourth hidden variable worth naming: **the metal.** Iron and steel have a high magnetic permeability μ,
which makes their skin depth far *smaller* than copper's at the same frequency — one reason steel is a poor
choice for high-frequency conductors.


## 3. What are the practical/engineering impacts?
This is where the thin shell starts costing real money:

1. **AC resistance is higher than DC resistance.** Squeezing current into a shell is the same as using a
   thinner wire — less effective cross-section means more resistance, more heat, more loss. The effect grows
   with frequency, so the same cable that's efficient at 60 Hz can be lossy at 1 MHz.
2. **Diminishing returns from thick wire at high frequency.** Past about one skin depth, adding copper to the
   core buys you almost nothing. There's no point in a fat solid conductor for RF — the middle is just
   expensive dead metal.
3. **Litz wire.** To beat this, high-frequency transformers and inductors use **Litz wire**: many thin,
   individually insulated strands woven together so that *every* strand sits near a surface. Lots of "skin,"
   little wasted core.
4. **Hollow conductors and tube busbars.** Since the center carries little current anyway, high-power RF and
   some power systems use **hollow tubes** or thin-walled conductors — same performance, less metal and weight.
5. **Surface plating matters more than the bulk.** Because RF current rides the outer few micrometers, plating
   a conductor with a thin layer of **silver** (lower resistivity than copper) noticeably cuts loss, while the
   cheaper metal underneath does the structural job. This is why RF connectors and waveguides are often silver-
   or gold-plated.
6. **Power transmission lines.** At 60 Hz, δ ≈ 8.5 mm, so very thick conductors would waste their cores.
   Utilities respond with **stranded** conductors and designs like **ACSR** (aluminum conductor, steel-
   reinforced) — a steel core for mechanical strength (it carries little current anyway) wrapped in aluminum
   strands on the outside where the current actually flows.
7. **PCB and chip design.** At gigahertz speeds the skin is microns deep, so trace **surface roughness** and
   plating finish start to dominate loss — a real headache in high-speed digital and microwave board design.

For the deeper dive, the [Wikipedia article on skin effect][01] has the full derivation and more material
tables, and [All About Circuits' AC resistance and skin effect][02] walks through it at a hobbyist level.


## Bottom line
Your mental model was right on both counts: DC fills the wire uniformly, and AC is pushed out toward the skin
by the wire's own changing magnetic field. The single number that governs everything is the **skin depth δ** —
the ~37%-current depth — and it scales as **1/√(frequency)**, depends on the **metal** (not the voltage or
current), and only *matters* once the wire is fatter than δ. At **60 Hz the skin is ~8.5 mm**, so household
wiring barely notices; at **1 MHz it's thinner than a hair**, so the entire core of a thick wire goes to
waste. Engineers fight back with Litz wire, hollow tubes, silver plating, and stranded ACSR lines — every one
of them a trick to put more copper where the current actually wants to be: near the surface.



[01]:https://en.wikipedia.org/wiki/Skin_effect
[02]:https://www.allaboutcircuits.com/technical-articles/learn-about-the-physics-behind-the-skin-effect-phenomenon/
