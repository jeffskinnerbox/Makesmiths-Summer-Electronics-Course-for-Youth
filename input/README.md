
Source material for the **Summer Electronics Course for Youth** (Makersmiths course code **ELL-W101**).
This directory holds the instructor's intent and reference material that the `.claude/skills/` pipeline
reads to generate the course deliverables under `lesson_plans/` (syllabus, BOM, per-class lesson plans,
and per-class lecture notes). `my-vision.md` is the primary input to every skill; the other
files supply supporting detail and the workflow that drives the pipeline.


| File | Purpose |
|:-----|:--------|
| `my-vision.md` | This defines what is expected to be accomplished in the course and its overall goal or purpose. It should cover the courses name, duration, class structure, target audience, student goals, required tools, special class activates, special source materials. |
| `my-notes.md` | This defines a planned sequence of instruction, one of which is the classes covered by the syllabus. It contains the content, materials, resources needed by the classes covered by the syllabus. Think of as the curriculum and it gives the course a context in which it resides. |
| `my-bom.md` | This is a list things that need to be purchased, or some how acquired, by the instructor to teach the course. This would be tools, supplies or consumables used by the instructor or students in the course. It should say how is it sourced, who acquires it (instructor or student), and if its a shared resource of each student has a copy. A full BOM is generated from it, using the `/bill_of_materials_generator` skill, and placed in `lesson_plans/BOM.md`. |
| `my-claude-prompts.md` | The instructor's prompt playbook — the exact prompts (and recommended session settings: Opus, plan mode, high effort) that drive each document through the pipeline. Read it to understand the intended workflow and ordering. |
| [`Make-Electronics-2nd-Edition.pdf`][01] | The course's primary text (Charles Platt), ~850 pages / 32 MB. Read with the Read tool a page range at a time (max ~20 pages/request); experiment titles appear inline. The course covers Experiments 1–11, 25, 26, and 28. |



[01]:https://someplace-else.neocities.org/books/Make%20Electronics%202nd%20Edition.pdf

