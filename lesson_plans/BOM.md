# Bill of Materials

This BOM covers the **Summer Electronics Course for Youth** (6 weekly classes, Summer 2026), based on
*Make: Electronics, 2nd Edition*. It is the **single source of truth for all cost and sourcing** — the
syllabus and lesson plans name components but never price them.

**Cost model:** This is a **makerspace purchasing budget** — what [Makersmiths][07] buys **once** to run the
course for **3 teams of 2 students (6 students total)** *(see [Appendix A](#appendix-a--source-prompt-and-clarification-qa), D1)*. Teams *share* the kits and the makerspace keeps and
reuses them; students do **not** keep a kit (a student who wants to experiment at home can buy their own — see
*Per-Team Optional*). Costs are shown as a course total, per team, and per student so planners can rescale.

* **Hardware -** 3 shared ProTechTrader *Make: Electronics* Standard Component Pack 1 kits (one per team), plus
  shared capstone parts (neodymium magnets, 26-ga magnet wire, and one spool of thicker 22-ga hookup wire) for
  Experiments 25, 26, and 28.
* **Software -** None. This is an analog electronics primer — no computers, programming, or Arduino.
* **Code Blocks -** None.
* **Tools -** Makersmiths provides the per-team multimeters and 9V/AA batteries (the Standard kit does not
  include them), plus shared safety glasses, hand tools, and short 3/4″ ID PVC tubes used as per-team
  coil forms for the Exp 26 hand generator (no spinning rig or drilling this year). Each student
  brings their own book, journal, and calculator.

Assumptions are stated inline and flagged `[VERIFY PRICE]` where a price may drift. Prices captured June 2026.

> **About this document.** This BOM was generated from `input/my-bom.md` with the `/bill_of_materials_generator` skill, following the reference links for sourcing and cost. **The originating prompt and the key design decisions are preserved in [Appendix A](#appendix-a--source-prompt-and-clarification-qa).** Where a costing decision is non-obvious, you will see a pointer such as *(see [Appendix A](#appendix-a--source-prompt-and-clarification-qa), D2)*. Several decisions are shared with the syllabus and trace to its own clarification interview ([`syllabus.md`](syllabus.md) Appendix A).

---

## Hardware

### Per-Team Required

Each of the 3 teams gets one kit. The **Standard** pack is chosen because Makersmiths already has the digital
multimeters and 9V/AA batteries the course requires, so the pricier Deluxe tier (which bundles those) is unnecessary *(see [Appendix A](#appendix-a--source-prompt-and-clarification-qa), D2)*.

| Item | Quantity | Item Cost | Source | Notes |
|:-----:|:-----:|:-----:|:-----:|:--------:|
| Make: Electronics Standard Component Pack 1 (2nd Ed.) | 3 | $94.55 | [ProTechTrader][03] | One per team; covers Exp 1–11; includes breadboard, resistors, LEDs, pots, switches, relays, capacitors, 2N2222 transistors, fuses, 8Ω speaker, test leads, hookup wire, hand tools. **Multimeter + 9V/AA batteries NOT included** — supplied by Makersmiths (see Tools) |

Per-Team Required Cost = $94.55 per team
Required Kit Subtotal = 3 × $94.55 = **$283.65** (3 teams)

### Per-Team Optional

| Item | Quantity | Item Cost | Source | Notes |
|:-----:|:-----:|:-----:|:-----:|:--------:|
| Spare Standard Component Pack 1 | 1 | $94.55 | [ProTechTrader][03] | Backup for dead components or an extra/odd student |
| Student's own Pack 1 (for home use) | 1 | $94.55–$106.55 | [ProTechTrader][03] / [Amazon][04] | Paid by the student/parent, not the course; lets a student experiment at home |

Per-Team Optional Cost = $0 to the course budget unless a spare kit is added (+$94.55)

### Shared Supplies

Bought once for the whole class. These cover the capstone (Exp 25/26/28) and the Exp 5 lemon battery. The
small cheap electronics spares (1N4001 diode, extra 1,000µF capacitor, 47Ω resistor, extra low-current LEDs)
are pulled from the Makersmiths electronics stock — see *Tools / Provided by Makersmiths* *(see [Appendix A](#appendix-a--source-prompt-and-clarification-qa), D5)*.

| Item | Quantity | Item Cost | Source | Notes |
|:-----:|:-----:|:-----:|:-----:|:--------:|
| Neodymium cylinder magnet, 3/4″ × 1″, axially magnetized (N42) | 3 | $14.53 ea | [K&J Magnetics][05] | **One per team** — the per-team hand-generator magnet for Exp 26 (Class 6); strong enough to flicker a low-current LED through a ~200 ft hand-wound 22-ga coil. No spinning rig is built this year *(see Appendix A, D3)* |
| 26 AWG enameled magnet wire, ~1 lb (~1,300 ft) spool | 1 | $27.00 | [Amazon][06] | Coil wire for **two of the three teams** (Exp 25/26/28); thin insulation packs **more turns** in the same space than hookup wire → stronger field / more output *(see Appendix A, D4)*. `[VERIFY PRICE]` (1/2-lb 650-ft spools run ~$30) |
| 22 AWG solid hookup wire, ~500 ft spool | 1 | $20.00 | Amazon | Coil wire for **one team** (Exp 26 ~200 ft + Exp 28 ~100 ft) — deliberately the **thicker** wire so that team's coils have **fewer turns**, letting the class see how wire type affects the result *(see Appendix A, D4)*. `[VERIFY PRICE]` |
| Galvanized (zinc-plated) steel brackets/plates (small pack) | 1 | $5.00 | Hardware store | Zinc electrode for the Exp 5 lemon battery. `[VERIFY PRICE]` |
| Lemons (or squeeze-bottle lemon juice) | 1 | $3.00 | Grocery | Exp 5 electrolyte; class-day consumable |
| Copper-plated coins (US pennies) | ~6 | $0.00 | Provided | Copper electrode for Exp 5; brought from pocket change |

Shared Supplies Subtotal = (3 × 14.53) + 27.00 + 20.00 + 5.00 + 3.00 + 0.00 = **$98.59** (whole class)

### Shipping

| Item | Quantity | Item Cost | Source | Notes |
|:-----:|:-----:|:-----:|:-----:|:--------:|
| ProTechTrader shipping | NA | $0.00 | [ProTechTrader][03] | Free on orders $50+ (kit order is ~$284) |
| K&J Magnetics shipping | NA | $7.50 | [K&J Magnetics][05] | Flat small-order ship. `[VERIFY PRICE]` |
| Amazon shipping (magnet wire + hookup wire) | NA | $0.00 | [Amazon][06] | Free with Prime |

Shipping Subtotal = 0.00 + 7.50 + 0.00 = **$7.50** (whole class) `[VERIFY PRICE]`

### Cost Summary

For 3 teams / 6 students:

```text
Course Total = kits + shared supplies + shipping
             = 283.65 + 98.59 + 7.50
             = ~$389.74  (whole class)

Per team    = 389.74 / 3  = ~$129.91 per team
Per student = 389.74 / 6  = ~$64.96 per student
```

With one optional spare kit:

```text
Course Total (with spare kit) = 389.74 + 94.55 = ~$484.29  (~$80.72 per student)
```

> A student who wants their own kit for home use buys it separately (~$94.55–$106.55) and it is **not** part
> of the course budget above.

---

## Software

| Item | Source | Notes |
|:-----:|:-----:|:--------:|
| None | NA | Analog electronics primer — no software, programming, internet, or Arduino |

## Code Blocks

| Item | Quantity | Source | Notes |
|:-----:|:-----:|:-----:|:--------:|
| None | NA | NA | No code is provided or written in this course |

## Tools

### Provided by Makersmiths (no course cost)

| Item | Quantity | Source | Notes |
|:-----:|:-----:|:-----:|:--------:|
| Digital multimeter (with leads) | 3 | Makerspace | One per team — the Standard kit excludes it; measures V / I / R / continuity |
| 9-volt and AA batteries | as needed | Makerspace | Powers the experiments — the Standard kit excludes batteries |
| Safety glasses | 6+ | Makerspace | Worn for Exp 2 (short circuit/blow a fuse) and capstone work |
| Large screwdriver | 1 | Makerspace | Core of the Exp 25 electromagnet |
| Short 3/4″ ID PVC tube | 3 | Makerspace | One per team — the coil form for the Exp 26 hand generator; the strong magnet shuttles through the bore. Cut to length with a saw (no drilling, no spinning rig this year) |
| 1N4001 diode | 1 | Makerspace | Spare from electronics stock (capstone/Exp 28 reference) |
| Extra 1,000µF capacitor, 47Ω resistor, low-current LEDs | a few | Makerspace | Capstone spares from electronics stock (also present in Pack 1) |
| Shared hand tools (pliers, cutters, strippers) | as needed | Makerspace | Backups to the per-kit hand tools |

### Provided by Each Student

| Item | Quantity | Source | Notes |
|:-----:|:-----:|:-----:|:--------:|
| *Make: Electronics*, 2nd Edition | 1 | Student — [Amazon][01] or free [PDF][02] | Required course text (~$25 print, or free PDF) |
| Build journal (notebook) + pencil | 1 | Student | Primary record/assessment artifact |
| Simple calculator | 1 | Student | Handy for Ohm's Law work |

---


## Appendix A — Source Prompt and Clarification Q&A


This appendix preserves (1) the originating prompt that generated this BOM and (2) the key design decisions baked into the cost model. It is referenced from the top of the document and inline so every non-obvious costing choice can be traced to its source.


### A.1 Originating Prompt (verbatim)


> Use the /bill_of_materials_generator to improve the @input/my-bom.md file and put the improved file in BOM.md.
> Use the /grill-me to clarify any questions you may have.
> Make sure to follow the reference links to get information about sources & cost.


### A.2 Clarification & Key Design Decisions


Unlike the syllabus, the interactive `/grill-me` exchange from the original BOM-generation session was not transcribed at the time. The decisions below record the choices embodied in this BOM and where each traces. Several are shared with — and were settled in — the syllabus's clarification interview ([`syllabus.md`](syllabus.md), Appendix A), which is cross-referenced where it applies.


**D1 — Class size & team structure for costing.** The vision states "about 6 students" working in teams of 1–2. For a concrete purchasing budget the BOM assumes **3 teams of 2 students (6 total)**, one shared kit per team, kept and reused by Makersmiths; students do not keep a kit. Costs are given as a course total and per-team/per-student so a planner can rescale for a different headcount.

**D2 — Standard vs. Deluxe Component Pack 1.** The **Standard** pack is purchased rather than the pricier Deluxe tier because Makersmiths already owns the digital multimeters and 9V/AA batteries the Deluxe tier bundles. Those are supplied separately (see *Tools / Provided by Makersmiths*), so paying for the Deluxe bundle would be redundant.

**D3 — Capstone generator format (drives magnet & PVC line items, omits rig/drilling).** Summer 2026 uses **per-team hand generators**, not a whole-class spinning rig — so the BOM buys one neodymium magnet and one short PVC coil-form per team and includes **no** dowel/plywood/hole-saw/drill costs. Traces to [`syllabus.md`](syllabus.md), Appendix A, Q3.

**D4 — Coil-wire split (two wire types on purpose).** The BOM buys thin **26-ga magnet wire** for two teams and thicker **22-ga hookup wire** for one team, wound on identical forms. This is deliberate so the class can compare turns-per-form and output by wire type (the "more turns → more output" lesson in Classes 5–6). Supports the pre-wound-coil plan in [`syllabus.md`](syllabus.md), Appendix A, Q2.

**D5 — Small electronics spares pulled from stock, not purchased.** The 1N4001 diode, an extra 1,000µF capacitor, a 47Ω resistor, and extra low-current LEDs are drawn from Makersmiths' existing electronics stock (and are already present in Pack 1), so they add **$0** to the course budget rather than appearing as purchases.

**D6 — Pricing currency, sourcing & verification.** Prices were captured **June 2026** by following the source reference links, and any figure that may drift is flagged `[VERIFY PRICE]`. Sourcing favors the author-approved vendor (ProTechTrader, free shipping over $50) for the kits, K&J Magnetics for the capstone magnets, Amazon for wire, and local/grocery/hardware sourcing for the Exp 5 lemon-battery consumables.


---

[01]:https://www.amazon.com/Make-Electronics-Learning-Through-Discovery/dp/1680450263/
[02]:https://someplace-else.neocities.org/books/Make%20Electronics%202nd%20Edition.pdf
[03]:https://www.protechtrader.com/Make-electronics-component-pack-1-2nd-edition
[04]:https://www.amazon.com/ProTechTrader-Make-Electronics-Component-Educational/dp/B01EKO6FYQ?th=1
[05]:https://www.kjmagnetics.com/dcx0-neodymium-cylinder-magnet
[06]:https://www.amazon.com/BNTECHGO-AWG-Magnet-Wire-Transformers/dp/B07H7GQPMC
[07]:https://makersmiths.org/
