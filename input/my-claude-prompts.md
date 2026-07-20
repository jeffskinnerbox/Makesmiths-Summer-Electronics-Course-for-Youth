
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

### 4th Claude Code Prompt
Using the /syllabus_generator skill, update the @electronics-primer-syllabus.md document so that it represents all 6 classes and not just the first class.

---

### 5th Claude Code Prompt
I'm told the speed of a randomly moving electron in a wire is about 10.0E6 m/sec.
I'm also told that the drift velocity of electron is less than 0.1 mm/sec when voltage is applied to that wire.
Electricity is all about pushing a long line of electrons, standing shoulder to shoulder, so electricity is instantaneous when a voltage is applied.

Using the /explainer skill, check the facts I stated and give me a proper answer to the questions:
1. If I had a pair of wires from earth to the sun, how long would it take to turn on a light bulb at the sun?
2. When would I see electron drift on the return path of the wire?
3. What is the speed of electricity?

Put you answer in @explainers/how-fast-is-electricity.md

---

### 6th Claude Code Prompt
I'm told that direct current (DC) flows uniformly through the entire cross-section of the wire.
The current travels equally through the core and the outer edges.
On the other hand, alternating current (AC) pushes toward the outside of the wire (the "skin effect").

Using the /explainer skill, check the facts I stated and give me a proper answer to the questions:
1. For AC current, how deep into the skill is the "skin effect"?
2. Does the skin effect vary with AC frequency, or voltage level, or size of the wire?
3. What are the practical/engineering impacts of the skin effect?

Put you answer in @explainers/where-does-electricity-flow-in-a-wire.md

---

### 7th Claude Code Prompt
Nikola Tesla, Thomas Edison, both played key roles in the "War of the Currents".
Using the /explainer skill, tell me what did they all do,
and why did George Westinghouse & Nikola Tesla together win this war?

Put you answer in @explainers/war-of-the-currents.md

---

### 8th Claude Code Prompt
When a great deal of current is flowing in a wire, it can heat-up and get very hot.

Using the /explainer skill, check the facts I stated and give me a proper answer to the questions:
1. What mechanism in the wire that is causing the heating?
2. What is the relationship between the size of the wire, the amount of current, and the amount of heat produced?
3. Is this relationship the same for DC and AC currents?
4. Why do electrical power plant's high power lines, going long distance, use very high voltages, and are high above the ground?

Put you answer in @explainers/why-do-wires-heat-up.md

---

### 9th Claude Code Prompt
For each of the subdirectories in this project, create README.md files for the subdirectories
@communications, @handouts, @lesson_plans, @explainers, and @input.
Within these README.md file, describe the purpose of of the subdirectory and purpose of each of the file in it.

---

### 10th Claude Code Prompt
Create a @README.md file that summarizes the course in 500 words or less.
Then for each of the subdirectories in the project root directory,
give a description of the purpose (stated first) and contents of the subdirectory in 100 words or less.

---

### 11th Claude Code Prompt
I plan to do Experiment 5 (Let’s Make a Battery) of @input/Make-Electronics-2nd-Edition.pdf.
Give me step-by-step instructions for building an testing the lemon battery.
I'm also using these sources
[Build a Lemon Battery](https://www.acs.org/content/dam/acsorg/education/outreach/kidszone/kids-zone-build-a-lemon-battery.pdf),
and [Simple Lemon Battery](https://researchparent.com/simple-lemon-battery/).
I plan to use two lemon, each cut in half, making a 4 cell battery to light a singe red LED.
I plan to use zinc nails and 12 AWG copper wire for cathode & anode.
I plan to use [this Red LED](https://www.amazon.com/dp/B01AUI4WC8).

Describe how a lemon battery works, the importance of using copper & zinc, and the use of a low current LED.
Discuss the forward voltage of the red LED and how it must be overcome via multiple battery cells.

Using the /explainer skill, check the facts I stated and conclude with a table of materials needed, and step-by-step assembly instructions.
Put you answer in @explainers/build-a-lemon-battery.md

---

### 12th Claude Code Prompt
In class 3, the students are exposed to the concept of an object (relay) being in a discrete state (on or off).
The experiment doesn't emphasize this but this state is the whole purpose of the experiment's circuit.
The electrical properties (current, voltage, etc.) are not the purpose of the circuit but the created states are.

This observation, creating states is the purpose/goal and the electrical properties is just a mechanism to support the goal,
is often the case.
A relevant example of is the 1937 work of Claude Shannon when he wrote his master's degree thesis,
"A Symbolic Analysis of Relay and Switching Circuits".
In this thesis, Shannon showed how relay switching circuits could implement the essential operators of Boolean Algebra.
This change digital circuit design from an art to a science, and made the modern computer possible.

Using the /explainer skill give the story of Claude Shannon thesis and why its so important to today's world of computing.
Give a brief introductory description of the state of computation before Shannon's work.
Also in the introduction, the observation "creating states is the purpose/goal of the circuit and the electrical properties is just a mechanism to support the goal".

Put your explanation/story in @explainers/electricity-and-computation.md

---

### 13th Claude Code Prompt
In class 3, the students are told to create a relay oscillator.
The strange thing is that this oscillator is created by
simply taking the output of the relay and routes a portion of its output signal back to the relays input.
We see this in many electrical circuits.
How does it work, what are the important applications, what is the theory of operation?
What role does feedback play in the every day technologies we have around us?

Using the /explainer and /theory_of_operation skills to describe this important of feedback
and connect it with topics like control theory, robotics, self-driving cars.

Put your explanation/story in @explainers/the-role-of-feedback.md

---

### 14th Claude Code Prompt
In class 4, the students do experiments and are told about RC Networks, Capacitive Coupling, and Displacement Currents.
Review these topics in the @input/Make-Electronics-2nd-Edition.pdf, @lesson_plans/class-04-lesson-plan.md,
and @handouts/class-04-exp*.md documents. These are advance topics that the students will find challenging.

Using the /explainer and /theory_of_operation skills to describe this important of RC Networks, Capacitive Coupling, and Displacement Currents.
Create one explanation/story document for each topic and place them in @explainers directory.

---

### 15th Claude Code Prompt
In class 5 and 6, students are introduced to the relationship between electricity and magnetism.
Read lesson plans and Experiments 25, 26, and 28 of @input/Make-Electronics-2nd-Edition.pdf to find out what is in Class 5 & 6.
How has mankind exploited this relationship from the time of it discovery to the present day?

Starting from discovery of this relationship to the present time,
include a table capturing the dates, inventions, and the inventions value/impact on society.
The inventions must contain electricity and physical magnets or electromagnets within them.
The table should span the whole time, list the most impactful inventions, and have 100 or less inventions.

Using the /explainer and /theory_of_operation skills, create this story and table timeline.
Put your explanation/story in @explainers/electromagnetism-inventions.md.

---

### 16th Claude Code Prompt
Review materials for class 5 and 6.
When magnets move it creates moving electrons and when electrons move, it creates magnetism.
We call this combined behavior electromagnetism.
We can find natural sources of electrons flowing in the chemistry of batteries.
We can find natural sources of magnetism in magnetic materials.

1. When the chemistry runs it full course, the electrons stop flowing and the electric field stops.
   Does a natural magnet ever losses it magnetic field?
2. You can find a positive charged object or negative charged object in isolation.  You do not need to have the pair together.
   Magnets have a north and south pole but the always come together, you never find just a north or a south.
   Why is this?

Using the /explainer and /theory_of_operation skills, and answer my questions.
Put your explanation/story in @explainers/magnetic-monopoles.md.

---

### 17th Claude Code Prompt
Review materials for class 5 and 6.
When electricity flows through a wire, it creates a magnetic field around the wire.
Because the electricity “induces” this effect, it is known as inductance.
The field around a straight wire is very weak, but if we bend the wire into a circle, the magnetic force starts to accumulate
If we add more circles, to form a coil, the force accumulates even more.
And if we put a steel or iron object in the center of the coil, the effectiveness increases further.
You have made a electromagnet via a coiled wire.

Applying a 9-volt battery to a spool copper wire, as described above, seems like a very bad idea,
because you’re going to heat the wire very hot and your going to short out your battery.
But this doesn't seem to happen. Why? Explain the transient and steady-state behaviour.

Using the /explainer and /theory_of_operation skills, and answer my questions.
Put your explanation/story in @explainers/inductance-and-resistance.md.

---


