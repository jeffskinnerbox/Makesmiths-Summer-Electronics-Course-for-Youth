
# My Vision
Based on [*Make: Electronics (2nd Ed.)*][02] by Charles Platt,
this is my vision of how the [Makersmiths'][06] course
called [Summer Electronics Course for Youth][07]
will operate in the Summer of 2026.
The purpose of the course is to give the students some intuition
about how electricity works and how it can be made useful.
Students will work in teams and can share kits.
If a student would like to work on experiments at home,
they can purchase their own kit from Amazon for $100 to $160.
(This home version of Kit [Pack 1][09] mirrors Experiments 1–11 in Chapters 1 & 2 of the [book][02]
and can include a digital multi-meter and batteries. Note: the shared class kits are the Standard pack —
Makersmiths supplies the multimeters and batteries separately; see `lesson_plans/BOM.md`.)

## Electronics Primer Course at Makersmiths
I'm preparing to teach a makerspace course for 12 to 15 year old students.
This course is a primer for electricity & electronics concepts.
I view this Electronics Primer course as first part of what could be a three part course outlined in `my-notes.md`.
At this time, only this course is being planned & developed.
The syllabus for this Electronics Primer course is documented in `lesson_plans/syllabus.md`.

The purpose of the course is to give the students some intuition
about how electricity works and how it can be made useful.
Some the targeted students are part of the [KidWind][04] program,
and what they learn here should be helpful in their KidWind assignment.

The course will be based on some proven materials,
the book "[Make: Electronics, 2nd Edition][01]", by Charles Platt.
The book can be purchased for $25 or its free for a [PDF version][02].
There are official kits, supporting the experimentation documented in the book.
[ProTechTrader][03] is the only vendor tested & approved by by the author.

Below is my vision of the courses goals, audience, structure, tools needed,
instructor instructions, and the class session activities over time.

## High Level Course Description
### Class Structure
This is a hands-on course where students meet together for 2 hours class session, over a 6 week period.
The students will work as individuals or in pairs and will both be referred to as teams here.

### Class Audience
The number of students in a class are expected to be approximately 6.
Some adults (most likely parent of the students) will be attending and they will provide guidance & assistance as needed.
There will be a single instructor who will lead the discussion and activities of the students.

### Required Tools
Each student will have the [book][01] documenting the experiments to be performed.
Each team will have a [Make: Electronics 2nd Edition - Component Pack][05],
a digital multimeter, batteries.

### Class Activities
* Prior to Class
  * Prior to attending the class session, the student will be encouraged to read the [book][01] about the experiment they will be performing.
* Start of Class Session
  * The instructor will start the class by reviewing what was documented about the experiments to be performed.
  * The instructor will transform complex technical concepts into clear, accessible explanations using narrative storytelling frameworks.
  * Where it can be helpful, the instructor will provide some history and example applications of the technical concepts.
* Performing the Experiments
  * The teams will perform the experiments outline in the syllabus.
  * Instructor will monitor the teams progress and provide assistance as needed.
  * The instructor should allow mistakes to be made,
    encourage the teams to think through what they did wrong, and develop there own course of action.
  * When the team successfully completes the experiment, as the team to explain to others what was physically going on.
* End of Class
  * The instructor will describe for the class what they should have learned.
  * The instructor will provide a theory of operation is a description of how some real world
    device or system work using the electrical/magnetic concept that were experimentally learned.
* Preparation for Next Class Session
  * Instructor will provide a very brief description of what will be done in the next class
  * The instructor will encourage the students to read the [book][01] about the experiment they will be performing in the next class.

### Class Instructions
The instructor will have a step-by-step lesson plan to guide the during the class session.
This for each step, the lesson plan will document what the instructor should be telling the class,
what they class should be physically doing, and what the class should be learning & accomplishing.
These instructions should document things electrical/magnetic concept that were experimentally learned,
good explanations of what what is physically going on,
theory of operation is a description of how some real world device or system,
and history and example applications of the technical concepts.

### Student Goals
At the conclusion of the this 6 class session course,
the students should be able to discuss what experiments were performed
and what electrical/magnetic physical processes where used to get the result they observed.
The should also be able to describe some real world device/systems that use these electrical/magnetic physical processes.

### Closing
Discuss direct references to [KidWind][04] and how what was learned could relate.
The instructor can close the course by talking about potential follow on course and what additional concepts could be learned.

## Additional Source Materials
These are are additional source material the instructor may find useful,
or in some cases, the students might find useful.
The instructor could create new experiments for the students,
or the student could be instructed to view videos about some topic in the course.

* [Every Basic Electronic Component Explained in 21 Minutes](https://www.youtube.com/watch?v=HGNKhLActDo)
* [Every Type of Electric Generator Explained](https://www.youtube.com/watch?v=-7CyYxqIacg)
* [Every Type of Battery Explained](https://www.youtube.com/watch?v=2G6Rn99sVmM)
* Another source of ideas could be the [Engineer's Mini-Notebook][08] series by Forrest M. Mims

## How to Use `my-vision.md`
Using the this `my-vision.md` file as key source material for the development of additional documentation for the course.
This can automated by using the skills listed below:


| Skill | Prompt & Input File | Output File |
|:------:|:------:|:------:|
| `/syllabus_generator` | `my-vision.md` | `lesson_plans/syllabus.md` |
| `/bill_of_materials_generator` | `my-bom.md` | `lesson_plans/BOM.md` |
| `/lesson_plan_generator` | `my-vision.md`, `lesson_plans/syllabus.md`, "Make: Electronics, 2nd Edition"  | `lesson_plans/class-00-lesson-plan.md` |
| `/explainer` | "Make: Electronics, 2nd Edition" | `lesson_plans/class-00-lesson-plan.md` |
| `/history_and_application` | "Make: Electronics, 2nd Edition"  | `lesson_plans/class-00-lesson-plan.md` |
| `/theory_of_operation` | "Make: Electronics, 2nd Edition"  | `lesson_plans/class-00-lesson-plan.md` |


Also use the skill `/grill-me` to ask me any clarifying questions concerning anything AI created.



[01]:https://www.amazon.com/Make-Electronics-Learning-Through-Discovery/dp/1680450263/
[02]:https://someplace-else.neocities.org/books/Make%20Electronics%202nd%20Edition.pdf
[03]:https://www.protechtrader.com/Make-electronics-component-pack-1-2nd-edition
[04]:https://kidwind.org/
[05]:https://www.protechtrader.com/Make-electronics-component-pack-1-2nd-edition
[06]:https://makersmiths.org/
[07]:https://makersmiths.org/event-6729146
[08]:https://github.com/alaricmoore/MiniEngineeringNotebooks
[09]:https://www.amazon.com/ProTechTrader-Make-Electronics-Component-Educational/dp/B01EKO6FYQ?th=1

