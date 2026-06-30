
The generated course-deliverable documents for the **Summer Electronics Course for Youth** (Makersmiths
course code **ELL-W101**) — a 6-week, hands-on primer based on *Make: Electronics, 2nd Edition* by Charles
Platt. These are produced from `input/my-vision.md` by the `.claude/skills/` pipeline (`/syllabus_generator`,
`/bill_of_materials_generator`, `/lesson_plan_generator`) and each carries the appendix convention (the
originating prompt plus clarification Q&A). The syllabus, BOM, and all six lesson plans must agree on class
numbering, titles, experiments, components, and assessment.

A **Class** is a fixed 2-hour session (6:00–8:00 PM). The six classes run across three phases:
Phase 1 — Foundations (Classes 1–2), Phase 2 — Controlling Electricity (Classes 3–4), and
Phase 3 — Magnetism, Generation & the KidWind Capstone (Classes 5–6).


| File | Purpose |
|:-----|:--------|
| `syllabus.md` | Course-level overview — schedule, audience, format, primary text, components, phases, and the verbal "explain-it" assessment milestones. The map the lesson plans fill in. |
| `BOM.md` | Bill of Materials — the **single source of truth for all cost and sourcing**. Costs, quantities, and purchase/supplier links live here and *nowhere else* (the syllabus and lesson plans name components but never price or link them). Generated from `input/my-bom.md`. |
| `class-01-lecture-notes.md` | Class 1 — *Electricity Is a Flow*. Experiments 1 (*Taste the Electricity*) and 2 (*Let's Abuse a Battery!*). |
| `class-02-lecture-notes.md` | Class 2 — *Resistance and Ohm's Law*. Experiments 3 (*Your First Circuit*), 4 (*Varying the Voltage*), and 5 (*Let's Make a Battery*). |
| `class-03-lecture-notes.md` | Class 3 — *Switches, Relays, and Automatic Control*. Experiments 6 (*Very Simple Switching*), 7 (*Investigating a Relay*), and 8 (*A Relay Oscillator*). |
| `class-04-lecture-notes.md` | Class 4 — *Capacitors, Transistors, Light & Sound*. Experiments 9 (*Time and Capacitors*), 10 (*Transistor Switching*), and 11 (*A Modular Project*). |
| `class-05-lecture-notes.md` | Class 5 — *Magnetism and Coils*. Experiments 25 (*Magnetism*) and 28 (*Making a Coil React*). |
| `class-06-lecture-notes.md` | Class 6 — *Generating Your Own Power*. Experiment 26 (*Tabletop Power Generation*) plus the course wrap-up and KidWind capstone. |
