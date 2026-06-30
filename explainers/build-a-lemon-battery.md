# Building and Testing a Lemon Battery


How do you turn a piece of fruit into a battery that lights an LED? This piece backs the *Make: Electronics*
[Experiment 5, *Let's Make a Battery*][01] (Class 2 of the course), checks the specific build you have in
mind — two lemons cut in half for a four-cell battery, zinc nails and 12-gauge copper wire for electrodes,
lighting one red LED — and ends with a materials table and step-by-step build-and-test instructions.


## First, a fact-check of your plan


You had most of it right, with two things worth fixing before you start:

1. **Which metal is which electrode.** You wrote "zinc nails and 12 AWG copper wire for cathode & anode,"
   but the roles are the other way around. The **zinc nail is the anode** (the negative terminal, where the
   metal dissolves and *gives up* electrons) and the **copper wire is the cathode** (the positive terminal,
   where electrons are *collected*). The [ACS "Build a Lemon Battery"][02] guide says it plainly: "The penny
   is the **cathode**… The nail is the **anode**." Your metals are correct — just label zinc as **−** and
   copper as **+**.

2. **Your LED is not actually a low-current LED.** The [red LED you linked][04] is a standard 5 mm
   "super bright" diffused red — its own spec is **2 V–2.2 V forward voltage at 20 mA**. That 20 mA rating is
   the catch: a lemon cell can only push a tiny current (well under 1 mA), so a 20 mA part will glow only
   faintly, and its frosted lens spreads that faint light even thinner. It *may* work in a dark room with
   four or more cells, but a genuine **low-current LED** (one rated to be visible at ~1–2 mA) is the right
   part and is what Experiment 5 specifies. More on this below.

Everything else — four cells, lemons halved, nails and copper wire — is a reasonable build. Just know that
**four cells is the practical minimum**; [ResearchParent's "Simple Lemon Battery"][03] used four and still
recommends keeping "5 or 6 on hand," and ACS uses seven. Have a couple of spare lemons ready.


## How a lemon battery works


A battery converts **chemical energy into electrical energy**, and a lemon cell does it with two rules of
chemistry. First, some metals give up electrons more easily than others. Zinc is "eager" — drop it into acid
and its atoms dissolve into the juice as positively charged zinc ions (Zn²⁺), each leaving **two electrons
behind in the metal**. Copper is "reluctant" — it mostly just sits there. Second, the lemon's juice is a mild
acid (citric acid) full of charged particles, which makes it an **electrolyte**: a liquid that carries charge
between the two metals.

Put a zinc nail and a copper wire into the same lemon, close together but not touching, and you have a
complete cell:

- At the **zinc nail (anode, −)**, zinc dissolves and piles up spare electrons.
- Connect a wire from the nail to the copper, and those electrons flow through that external wire — **that
  flow is your electric current**, and it's what lights the LED on the way.
- At the **copper wire (cathode, +)**, the arriving electrons are handed off to hydrogen ions (H⁺) from the
  acid, which pair up and bubble off as hydrogen gas. (ACS notes you may see "small bubbles at the cathode" —
  that's the hydrogen.)

The juice itself completes the loop inside the lemon, carrying charge from the copper side back to the zinc
side. Electrons go the long way (through your wire and LED); ions shuffle the short way (through the juice).
Stop either path and the current stops.


## Why it must be copper *and* zinc


The voltage of a cell comes from the **difference between the two metals' eagerness to give up electrons**, a
property chemists measure as "electrode potential." Zinc and copper sit far apart on that scale — zinc about
−0.76 V, copper about +0.34 V — a gap of roughly **1.1 V in theory**, which real lemon cells deliver as about
**0.7–0.9 V** once you account for the messy losses inside a piece of fruit.

The key word is *difference*. If you used **two copper electrodes**, or two zinc ones, there would be no
difference in eagerness and therefore **no voltage and no current** — just two identical metals in juice. You
need two *different* metals, and the further apart they are on the scale, the more voltage you get per cell.
Zinc-and-copper is the classic pairing because the metals are cheap, safe, far apart on the scale, and zinc
is the one that does the dissolving. This is the exact same trick Alessandro Volta used in 1800 to build the
first real battery — his "voltaic pile" stacked copper and zinc discs separated by brine-soaked cloth. Your
lemons are Volta's pile with citric acid standing in for the brine.


## The red LED: forward voltage, and why one cell can't do it


An LED is a one-way valve for current, and it has a **threshold called the forward voltage (Vf)** — the
minimum push needed before it conducts and lights at all. Below Vf, almost no current flows and the LED stays
dark; above it, current flows and it glows. Your linked LED lists **Vf = 2.0–2.2 V**.

Now compare that to one lemon cell at **~0.8 V**. A single cell isn't even close — it can't clear the 2 V
threshold, so the LED stays dark no matter how long you wait. The fix is to wire cells **in series**
(end to end, nail-to-copper, nail-to-copper…), which **adds their voltages**:

| Cells in series | Approx. open-circuit voltage | Past the red LED's ~2.1 V threshold? |
|:---------------:|:----------------------------:|:------------------------------------:|
| 1 | ~0.8 V | No |
| 2 | ~1.6 V | No |
| 3 | ~2.4 V | Just barely |
| **4 (your plan)** | **~3.2 V** | Yes, with some margin |

This is exactly why **red** is the color to use. Red LEDs have the **lowest forward voltage** of any color;
green, blue, and white LEDs need roughly 3–3.4 V and would demand even more lemon cells to light. Picking red
is what makes a four-cell fruit battery feasible at all.

Why build in margin past 2.1 V instead of stopping at three cells? Because **open-circuit voltage is the
best case**. The moment current flows, the lemon's high internal resistance "eats" some of that voltage, and
the LED sees less than the meter showed with nothing connected. Four cells give you headroom for that loss;
three can be right on the edge.


## Why a low-current LED matters so much


Here's the part your linked LED gets wrong. Voltage gets the LED *over the threshold*, but **current is what
makes light**, and a lemon battery is terrible at supplying current. Each cell has a high **internal
resistance** — the juice, the small electrode area, and the hydrogen bubbles all fight the flow — so even a
four-cell stack typically delivers only **tenths of a milliamp to maybe one milliamp**.

A standard LED like the one you linked is built and rated for **20 mA**. Asked to run on a fraction of a
milliamp, it produces only a faint glow — and its diffused/frosted lens scatters that glow until it's hard to
see. A **low-current LED** (sometimes sold as "high-efficiency") is engineered to be clearly visible at
**about 1–2 mA**, which is right in the range a lemon battery can actually supply. That's why *Make:
Electronics* Experiment 5 — and the course Bill of Materials — call for a low-current LED, not a general one.

**Recommendation:** use a clear (not diffused) **low-current red LED** if you can get one; it's the single
biggest improvement to this build. If you stick with the LED you have, compensate by using **more cells**
(five or six), keeping electrode contact firm, and viewing it in a **dark room** — and don't be surprised if
it's a dim glow rather than a bright point of light.


## Materials


For your plan: a four-cell battery from two halved lemons, lighting one red LED.

| Item | Qty | Notes |
|:-----|:---:|:------|
| Fresh lemons | 2 (+1–2 spare) | Cut each in half → four cells. Roll firmly on the counter first to break the juice sacs. Soft, juicy lemons work best |
| Zinc nails (galvanized) | 4 | The **anode (−)**. Galvanized roofing or common nails; the zinc coating is what reacts |
| 12 AWG solid copper wire | 4 pieces, ~2–3″ each | The **cathode (+)**. Strip off any insulation so bare copper meets the juice; scuff dull wire bright with sandpaper |
| Red LED | 1 | **Low-current red LED strongly preferred** (visible at ~1–2 mA). Your standard 20 mA [super-bright red][04] will glow only dimly — see above |
| Alligator-clip test leads | 5 | Four to chain the cells in series, one to close the loop through the LED |
| Digital multimeter | 1 | To measure single-cell (~0.8 V) and full-stack (~3.2 V) voltage on the DC-volts range |
| Knife + cutting board | 1 | Adult handles the knife; lemon juice is acidic |
| Safety glasses | 1 per person | Lemon juice stings eyes; wear them while cutting and assembling |
| Paper towels | a few | Juice is messy |


## Step-by-step: build the battery


1. **Prep the lemons.** Roll each whole lemon firmly under your palm on the counter for a few seconds to
   rupture the internal juice sacs — this frees up electrolyte and noticeably improves output. Then cut each
   lemon in half, giving you **four cells**. Lay the halves cut-face-up so the juicy face is exposed.
2. **Prepare the electrodes.** Cut four ~2–3″ pieces of 12 AWG copper wire and strip them fully bare; if the
   copper looks dull, scuff it shiny with sandpaper (oxide film hurts performance). Have your four zinc nails
   ready.
3. **Build each cell.** Into each lemon half, push **one zinc nail** and **one bare copper wire** about an
   inch apart, deep into the juicy flesh but **not touching each other** (if they touch, the cell shorts and
   does nothing). You now have four single cells of ~0.8 V each.
4. **Wire the cells in series.** Using alligator-clip leads, connect **the copper (+) of one cell to the zinc
   nail (−) of the next** — copper-to-nail, copper-to-nail — down the line of all four. Series wiring is what
   adds the voltages. Never connect copper-to-copper or nail-to-nail.
5. **Leave the two ends free.** After chaining all four, one end of the row is a free **copper (+)** terminal
   and the other is a free **zinc nail (−)** terminal. The LED goes between these two.


## Step-by-step: test it


1. **Check one cell first.** Set the multimeter to **DC volts** (2 V range). Touch the red probe to a cell's
   copper and the black probe to its zinc nail. Expect **~0.7–0.9 V**. Near 0 V means the electrodes are
   touching or the copper is oxidized — re-seat them or brighten the wire.
2. **Check the whole stack.** Probe across the two free ends of the four-cell chain (copper at one end, nail
   at the other). Expect roughly **~2.8–3.4 V** open-circuit. If it's much lower, one cell in the chain is
   weak or a clip is loose — work along the row re-checking each junction.
3. **Connect the LED — mind the polarity.** The LED only passes current one way. Connect its **long leg
   (the LED's + anode) to the free copper (+)** terminal, and its **short leg (− cathode) to the free zinc
   nail (−)** terminal. (ACS states it the same way: longer lead to the penny/cathode side, shorter lead to
   the nail/anode side.)
4. **Look — in dim light.** With a low-current LED you should see a clear glow; with the standard super-bright
   LED expect a faint one, best seen with the lights down. If it doesn't light, **flip the LED first** — a
   backwards LED is the most common cause — then check the steps below.
5. **If it still won't light:** add a fifth and sixth cell to push more voltage and current; make sure every
   electrode is pushed in firmly and copper-to-nail order is unbroken; re-brighten dull copper; and confirm
   the lemons are fresh and well-rolled. As a last resort, swapping in a true low-current red LED almost
   always settles it.


## The takeaway


A lemon battery works because **two different metals in an acid** set up a voltage, zinc dissolving to push
electrons through your wire while copper collects them. One cell (~0.8 V) can't clear a red LED's ~2.1 V
**forward voltage**, so you stack four in **series** to add up past it — and you choose **red** because it has
the lowest threshold of any color. The quiet catch is **current**: a lemon delivers only a fraction of a
milliamp, so a **low-current LED** is what actually lets you see the result. Get those three ideas — different
metals, series voltage, and tiny current — and you understand not just this fruit battery but every battery,
and the chemistry behind Volta's original pile.


[01]:https://www.amazon.com/Make-Electronics-Learning-Through-Discovery/dp/1680450263/
[02]:https://www.acs.org/content/dam/acsorg/education/outreach/kidszone/kids-zone-build-a-lemon-battery.pdf
[03]:https://researchparent.com/simple-lemon-battery/
[04]:https://www.amazon.com/dp/B09B9BYS8V
