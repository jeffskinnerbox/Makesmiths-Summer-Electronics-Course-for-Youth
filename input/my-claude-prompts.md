
# My Claude Code Prompts

## Creation of a Course Syllabus
Start with the following:

```bash
# clear claude code's contest
/clear

# initialize the CLAUDE.md file
/init

# set model to opus
/model opus

# use planning mode
/plan

# work hard
/effort high
```

### 1st Claude Code Prompt
Only read the @input/BOM.md, @input/my-notes.md, @input/my-vision.md files,
and chapters 1 to 11, 25, 26, 28 of @input/Make-Electronics-2nd-Edition.pdf.
From this, you are to create a course syllabus document using the /syllabus_generator skill.
Place your document in the file @electronics-primer-syllabus.md.

My preferred sequence of class session:
* Class 1 — Electricity is a Flow - **Experiments 1–2** in *Make: Electronics (2nd Ed.)*
* Class 2 — Resistance and Ohm's Law - **Experiments 3–5** in *Make: Electronics (2nd Ed.)*
* Class 3 — Switches, Relays, and Automatic Control - **Experiments 6–8** in *Make: Electronics (2nd Ed.)*
* Class 4 — Capacitors, Transistors, Light & Sound - **Experiments 9–11** in *Make: Electronics (2nd Ed.)*
* Class 5 — Magnetism and Coils - **Experiments 25+28** in *Make: Electronics (2nd Ed.)*
* Class 6 — Generating Your Own Power - **Experiment 26 + Wrap-Up** in *Make: Electronics (2nd Ed.)*
  (Whole class could participate in a single build)

Within the document you create, include this prompt,
and all question you ask me, along with my responses.
Place this in the document as an appendix and reference it at the beginning of the document
and anywhere else in the text when its a useful reference.

In a subsequent steps, I expect this document will used to help prepare
the course design and materials developed for the course.
Think Very Hard about what must be specified in this document
so a robust lesson plan and lecture notes can be created.

I expect there will be some issues,
so use the /grill-me skill for all things that require further clarification.

---

### 2nd Claude Code Prompt
Use the /bill_of_materials_generator to improve the @input/my-bom.md file and put the improved file in BOM.md.
Use the /grill-me to clarify any questions you may have.
Make sure to follow the reference links to get information about sources & cost.

---

### 3rd Claude Code Prompt
Using the /lesson_plan_generator skill, create lesson plans for all six classes.
Make sure lesson plan follows the outline in the @electronics-primer-syllabus.md document
and make use of the /theory_of_operation, /history_and_application, and explainer skills.
Make sure the lesson plans flow easily from 1 to 6 with minimal gaps or repetition in key work & concepts.
Put the lesson plan for class X in @/lesson_plans/class-0X-lesson-plan.md file for X, 1 thru 6 class numbers.
Create a lesson plan for class 1 then stop and let me review it.

---

