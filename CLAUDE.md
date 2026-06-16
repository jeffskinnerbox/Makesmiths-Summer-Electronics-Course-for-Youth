# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repository is

This is **not a software project** — it is a course-authoring workspace. Its product is a set of
teaching documents for a [Makersmiths](https://makersmiths.org/) makerspace course,
the **Summer Electronics Course for Youth**, a 6-week, hands-on primer based on *Make: Electronics, 2nd Edition*
(Charles Platt). "Work" here means generating and refining Markdown course documents with the skills in
`.claude/skills/`, not writing or running application code.

## The authoring pipeline (most important thing to understand)

Documents are generated from a single source-of-vision and must stay mutually consistent. The chain is:

```
input/my-vision.md  (the Specification — instructor's intent)
        │
        ├─(/syllabus_generator)──────────────▶ electronics-primer-syllabus.md
        │
        ├─(/bill_of_materials_generator)─────▶ BOM  (source input/my-bom.md → improved BOM.md at repo root; the cost/sourcing source of truth)
        │
        └─(/lesson_plan_generator)───────────▶ lesson_plans/class-NN-lesson-plan.md
                                                     │
        lecture notes per class build up from these three skills, appended into one file:
        (/explainer, /history_and_application, /theory_of_operation) ▶ lecture_notes/class-NN-lecture-notes.md
```

The skill → input → output mapping is documented in `input/my-vision.md` ("How to Use" table). When asked
to "create the syllabus / lesson plan / BOM / lecture notes," invoke the matching skill rather than
free-writing. Use `/grill-me` (or `/grill-with-docs`, or the `AskUserQuestion` tool) to interview the
instructor and resolve open questions **before** finalizing a document.

The pipeline skills above produce documents from scratch. A second set of skills under `.claude/skills/`
**refines existing prose** rather than generating it — `/edit-article`, `/writing-shape`, and
`/file-combining` (plus `/readme-wizard` for the repo README). Reach for these when asked to tighten,
restructure, reshape, or consolidate a document that already exists, instead of regenerating it with a
pipeline skill.

**Appendix convention (applies to every generated document):** embed the originating prompt verbatim plus
the full clarification Q&A as an appendix, reference it from the top of the document, and cite it inline
wherever a non-obvious decision traces back to an answer (see `electronics-primer-syllabus.md` Appendix A
and `BOM.md` for the established pattern).

This workspace is a **reusable, course-agnostic template**: the same skills produce documents for any
Makersmiths course. `input/my-claude-prompts.md` is the instructor's prompt playbook and shows a second
course (a Line Following Robot) driven through the same pipeline — for software-heavy courses the chain
extends to a Specification → Development Plan, with those outputs written under `docs/`. For *this*
(analog electronics) course there is no software: the syllabus and the generated BOM (`BOM.md`) live at the
repo root (the original BOM source is `input/my-bom.md`), per-class lesson plans live under `lesson_plans/` as
`lesson_plans/class-NN-lesson-plan.md`, and per-class lecture notes go under `lecture_notes/`.

The repo-root `README.md` is the **instructor's own setup/bootstrap notes** (how to install the skills and
launch a session) — it is currently a stub, and it is *not* a generated course deliverable, so it is exempt
from the consistency rules below. Don't treat it as a document that must agree with the syllabus/BOM.

## Consistency rules (these override convenience)

- **Cost, pricing, quantities, and purchase/supplier links belong ONLY in the BOM.** The syllabus and
  lesson plans name components (and may link to a datasheet/info page) but must never include prices or
  purchase links. This is enforced by the skills and `.claude/skills/shared/definitions.md`.
- Syllabus, Lesson Plans, and BOM for the same course must agree on class numbering, titles, experiments,
  components, and assessment approach. If one exists, new documents must match it. Read the existing
  documents before generating a new one.
- A **Class is a fixed 2-hour session.** Terminology (Curriculum / Course / Class / Design Session;
  Syllabus / Lesson Plan / BOM; History & Application; Theory of Operation) is defined once in
  `.claude/skills/shared/definitions.md` — read it before generating course docs and use those terms exactly.

## Source material

`input/` holds the specification and reference material:
- `my-vision.md` — the instructor's vision/spec (primary input to every skill).
- `my-notes.md` — supporting notes; `my-bom.md` — the original BOM source (the improved BOM is generated to `BOM.md` at the repo root).
- `my-claude-prompts.md` — the instructor's prompt playbook (the exact prompts that drive each document;
  read it to understand intended workflow and ordering).
- `Make-Electronics-2nd-Edition.pdf` — **~850 pages, 32 MB. Cannot be read in one call.** Use the Read tool
  with a `pages` range (e.g., `pages: "37-56"`, max ~20 pages/request). The PDF reflows into many small
  pages, has no usable TOC up front, and experiment titles appear inline (e.g., "Experiment 3: Your First
  Circuit"); locate content by sampling page ranges. The course covers Experiments 1–11, 25, 26, 28.

## Markdown conventions and tooling

Generated documents are GitHub-flavored Markdown. Linting/formatting uses **markdownlint-cli2** with the
repo config `.markdownlint-cli2.jsonc` (not globally installed — run via `npx markdownlint-cli2 "**/*.md"`).
Note: that config is a **symlink into the instructor's dotfiles** (`~/.dotfiles/checker-files/`), so it
won't resolve on a fresh clone elsewhere — markdownlint falls back to defaults if the link is dangling.
Key non-default rules to honor when editing Markdown by hand:
- Unordered-list indent is **4 spaces** (`ul-indent`), not 2.
- Long lines are allowed (`line-length` = 300).
- Horizontal rules use the long form `---------------` (`hr-style`).
- Headings: 2 blank lines above, 0 below (`blanks-around-headings`).

All links in generated course documents use **reference-style** form (`[text][01]`) with definitions
collected at the bottom of the file, numbered `[01]`, `[02]`, … with no space before the colon and no
duplicate URLs.

Export to other formats with **pandoc** (installed): `pandoc -f gfm input.md -o output.docx`
(or `-o output.pdf` with a PDF engine).

## Common commands & recurring steps

There is no build or test suite. The relevant commands are:

```bash
npx markdownlint-cli2 "**/*.md"          # lint all Markdown against .markdownlint-cli2.jsonc
pandoc -f gfm electronics-primer-syllabus.md -o electronics-primer-syllabus.docx   # export a doc
```

Note: the linter is **not** clean on the generated docs — it reports pre-existing, tolerated style
warnings (e.g. `MD013` lines over 300, `MD036` emphasis-used-as-heading, `MD060` table-pipe spacing).
Don't assume your edit caused these or chase a zero-warning result; just confirm you didn't add *new* ones.

Per `input/my-claude-prompts.md`, the instructor runs each document-generation session with the model set
to Opus, in plan mode, at high effort.

**Consistency review (run after generating or editing any document):** re-read the source files and all
generated documents and reconcile them — component names, class numbering/titles, experiments, schedule,
and assessment must agree across `my-vision.md`, `my-notes.md`, the syllabus, the BOM, and any lesson plans.
The instructor invokes this as the recurring "review all `@input/*.md` and `@docs/*.md` files and make
sure they are consistent and correct" step.
