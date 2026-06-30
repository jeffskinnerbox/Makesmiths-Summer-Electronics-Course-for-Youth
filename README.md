
# Summer Electronics Course for Youth

**Makersmiths course code:** ELL-W101 <br>
**Term:** Summer 2026 (Tuesdays, June 23 – July 28) <br>
**Where:** [Makersmiths][01] makerspace, Leesburg, VA


## About The Course

The **Summer Electronics Course for Youth** is a 6-week, hands-on primer in analog electronics for students
ages 12–15. It meets once a week for a fixed 2-hour evening class (6:00–8:00 PM), with about six students
working in teams of one or two while attending parents help at the bench. The goal is intuition, not theory:
students leave with a feel for how the electric and electronic world around them actually works, and a sense
of how much more there is to learn.

The course follows *[Make: Electronics, 2nd Edition][02]* by Charles Platt, working through the book's
experiments using the official ProTechTrader component pack. It is built around doing — every class is a lab.
Learning is reinforced by a build journal and verbal "explain-it" demonstrations rather than grades: students
show a working circuit and explain, in their own words, why it behaves as it does.

The six classes run in three phases:

- **Phase 1 — Foundations** (Classes 1–2): electricity as a flow; resistance and Ohm's law.
- **Phase 2 — Controlling Electricity** (Classes 3–4): switches and relays; capacitors, transistors, light and sound.
- **Phase 3 — Magnetism, Generation & the KidWind Capstone** (Classes 5–6): magnetism and coils; generating your own power.

Each phase ends with a hands-on milestone — explain the LED, build a light-and-sound project, and finally
light an LED from a moving magnet, the same principle a KidWind wind turbine uses.


## About This Repository

This is a **course-authoring workspace**, not a software project. Its product is the set of teaching
documents above, generated and refined as GitHub-flavored Markdown using the Claude Code skills in
`.claude/skills/`. Everything flows from a single source of vision (`input/my-vision.md`): the skills turn it
into a syllabus, a bill of materials, and per-class lesson plans that must all stay mutually consistent. Cost
and sourcing information lives only in the BOM. See `CLAUDE.md` for the full authoring pipeline and conventions.


## Project layout

### `.claude/`
**Purpose:** the Claude Code tooling that generates and refines the course documents.<br>
**Contents:** `skills/` — the document generators (`/syllabus_generator`, `/bill_of_materials_generator`,
`/lesson_plan_generator`, plus lecture-note skills), prose-refinement skills (`/edit-article`,
`/writing-shape`, `/file-combining`, `/readme-wizard`), and `shared/definitions.md`, which fixes the
course terminology every skill uses.

### `input/`
**Purpose:** the source material and instructor intent that feed the authoring pipeline.<br>
**Contents:**
`my-vision.md` (the specification — primary input to every skill), `my-notes.md` (background on the text and
component packs), `my-bom.md` (the unpriced BOM source), `my-claude-prompts.md` (the prompt playbook driving
each document), and `Make-Electronics-2nd-Edition.pdf` (the course's primary text).

### `lesson_plans/`
**Purpose:** the generated course deliverables — the heart of the repository.<br>
**Contents:** `syllabus.md` (course-level overview, schedule, and assessment), `BOM.md` (the bill of materials and single source of truth
for cost and sourcing), and the six per-class files `class-01-lesson-plan.md` … `class-06-lesson-plan.md`,
each combining one 2-hour session's lesson plan (experiments and flow) with its lecture notes. These
documents must agree on class numbering, titles, experiments, and components.

### `handouts/`
**Purpose:** student-facing materials printed and handed out at the bench.<br>
**Contents:** `cheatsheet.md`, a per-class quick reference (starting with Class 1) condensing key ideas into at-a-glance form, such as the
water-vs-electricity analogy mapping pressure and flow to voltage and current.

### `explainers/`
**Purpose:** short supplementary "but *why*?" reading that deepens intuition beyond the experiments.<br>
**Contents:** five standalone pieces — `war-of-the-currents.md`, `why-do-wires-heat-up.md`,
`where-does-electricity-flow-in-a-wire.md`, `how-fast-is-electricity.md`, and `build-a-lemon-battery.md` —
each posing a single question (or build) and answering it in plain English.

### `communications/`
**Purpose:** outreach to parents and students, separate from the in-class teaching materials.
<br>**Contents:** `letter-to-parents.md` (the instructor's pre-course introduction) and `registration.md` (event and
registration details, including student/parent contact information — kept out of version control via
`.gitignore` for privacy).


[01]:https://makersmiths.org/
[02]:https://www.amazon.com/Make-Electronics-Learning-Through-Discovery/dp/1680450263
