# MODULE: MATH_M5_MHO — Making Math Hands-On

## MODULE METADATA

```yaml
module_id: MATH_M5_MHO
title: Making Math Hands-On
pathway: empathy_arc
fallback_trigger: user_expresses_confusion
fallback_pathway: steady_path
duration_target: 10-15 minutes
unlock_requires: MATH_M2_MEL (prior module quiz: ≥2 of 3)
unlocks: null
quiz_pass: 2_of_3              # per-module: ≥2 of 3 correct
course_pass_threshold: 0.80    # course-level; explain depth (system prompt §9)
quiz_retry_allowed: true
grade_levels: Primary 1-6
subject: Math
```

---

## LEARNING OBJECTIVES

- Teachers understand the importance of hands-on manipulatives and visuals for conceptual math
- Teachers use local materials at no/low cost in ways that support student learning and inclusion
- Teachers practice designing simple activities to make math engaging
- Teachers implement short, predictable, active strategies that link actions to math concepts and work in large classes

---

## MODULE RULES

- Always assume materials are scarce, unless the user indicates otherwise. Focus on local, found, or shared materials
- Normalize movement and noise as part of learning
- Link hands-on learning to inclusion and wellbeing, where possible

### IMAGE DELIVERY (HARD RULE)

Whenever a strategy or section contains an image tag in the format `![](url)`, you MUST output that image to the user in that exact format before delivering the strategy content. Send the image on its own line, before any text for that strategy. Never skip, summarize, or describe an image instead of outputting it. Never omit images due to length or pacing. If the image tag is present in the source, it must appear in your response.

---

## MEDIA OUTPUT

> **Agent:** Send image first as `![](URL)` on its own line when a row applies. Never skip an image listed here. Never send images not listed here.

| Trigger | When to send | Image |
| ------- | ------------ | ----- |
| **INTRO** | First bot message when this deep dive starts | *(add URL when available — skip if not yet set)* |
| **MATH_M5_STRAT1** | When delivering Collect Local Materials | `![](https://i.imgur.com/XsTNN1P.jpeg)` |
| **MATH_M5_STRAT2** | When delivering Number Cards & Bands of 10 | `![](https://i.imgur.com/JWQQVle.jpeg)` |
| **MATH_M5_STRAT4** | When delivering Everyday Items | `![](https://i.imgur.com/SMATUZi.jpeg)` |
| **MATH_M5_STRAT5** | When delivering Place Value Charts & Bundling | `![](https://i.imgur.com/nA3MnMI.jpeg)` |
| **MATH_M5_STRAT6** | When delivering Materials Routines & Roles | `![](https://i.imgur.com/y75YXTf.jpeg)` |
| **MATH_M5_STRAT8** | When delivering Matching & Sorting | `![](https://i.imgur.com/nRqNq2h.jpeg)` |
| **QUIZ** | Before delivering the module recap and quiz | `![](https://i.imgur.com/U6WESHX.jpeg)` |

---

## INTERNAL: Concepts (Agent Guidance Only)

> **Do NOT show these concepts to the user.** Use them to guide your vignette — what the teacher in the story understands, struggles with, and discovers. Do not define these concepts explicitly; show them through what happens in the classroom.

### MATH_M5_CON1 — Hands-on = Minds-on

Active learning deepens understanding. Hands-on routines help children move from "I can say it" to "I understand it." When learners handle real objects, clap or step while counting, or sketch quick models, they anchor new ideas in memory and stay engaged. In large or stressed classrooms, short hands-on tasks also help with emotional and energy regulation.

### MATH_M5_CON2 — Manipulatives Make Abstract Concrete

Children understand concepts like place value and operations more quickly when they can see and feel the quantities. Start with objects, then draw the objects, then write the numbers. Manipulatives do not have to be costly or fancy—safe, countable, and available is enough.

### MATH_M5_CON3 — Local Materials Work

Sticks, stones, bottle caps are free and familiar. Using local materials lowers costs and raises participation. Build a stock over time by collecting items from the environment and storing them in a dedicated box or bin. Invite families or staff to contribute safe items.

### MATH_M5_CON4 — Play with Purpose

Games, role play, and physical modeling embody quantity, operations, and comparison so students can feel and see math structures. Each playful step points to a mathematical representation. These strategies make math concrete, engaging, and inclusive.

### MATH_M5_CON5 — Active, Playful Math Strengthens Learning and Wellbeing

Playful, movement-rich strategies let children do the math with bodies, voices, and simple objects before they speak or write. Short games and role plays help regulate energy and emotions. Choice within activities builds agency and belonging. Tone stays joyful and predictable.

---

## EMPATHY_ARC FLOW

> **Agent:** Follow the `empathy_arc` pathway as specified in `global_pathway_instructions.md`. Generate the vignette at runtime — do not deliver strategies as a list or define them abstractly. Each strategy must be shown through what the teacher in the story does, tries, or notices. The vignette runs throughout the entire module.

### VIGNETTE SETUP

Adapt names, grade, and class size to the user's context if known. Otherwise use these defaults.

**Teacher:** A primary teacher with a culturally appropriate name for the local context  
**Grade/Context:** Primary 3–4, large class (35–45 students), limited or no purchased materials  
**Challenge:** Students are learning place value or grouping but have nothing concrete to work with. Some are guessing, some are disengaged, and the teacher isn't sure how to make the concept visible without spending money.

### FLOW

1. **Vignette intro + poll** — Open with 2–3 sentences placing the teacher in this moment. End with a poll or question that invites the user to respond to the situation (not the strategy).
2. **Brief reflection** — Acknowledge the user's response in 1–2 sentences before continuing the story.
3. **For each strategy** (draw from STRATEGIES below):
   - Vignette continues — the teacher in the story tries, uses, or notices the strategy in action
   - Reflection prompt or quick poll tied to that classroom moment
   - Strategy insight (1–2 lines: what this does for learners)
   - Micro-action (one concrete thing the user can try)
4. **Story debrief** — Name what the teacher in the vignette did AND why it mattered (2–3 sentences; make the pedagogical principle explicit without jargon).
5. **Quiz** — Deliver all 3 items (recall → understanding → application).

### REFLECTION PROMPTS

| Step | Prompt |
|------|--------|
| After vignette intro | Have you been in a situation like this — where you wanted students to understand something but didn't have the right materials? What did you do? |
| Mid-module (after ~3 strategies) | What is the teacher in the story doing differently now? Have you tried anything similar? |

---

## STRATEGIES

> **Agent:** These strategies are the content of the vignette. Embed each one in the ongoing story — show the teacher using or discovering it in the classroom. Do not list or define strategies separately from the narrative.

### STRAT1 — Collect Local Materials
📷 Send this image first, then deliver strategy content:
![](https://i.imgur.com/XsTNN1P.jpeg)
Stones, bottle caps, sticks, beans for counting, grouping, measurement. Set roles for distribution/cleanup. Pre-counted sets. Share in pairs/groups if scarce.

### STRAT2 — Number Cards & Bands of 10
📷 Send this image first, then deliver strategy content:
![](https://i.imgur.com/JWQQVle.jpeg)

Bands of 10 show place value. Represent 13 = 10 + 3. Add by filling bands. Prompts: "Build 17. Now add 5. What changed?"

### STRAT3 — Number Lines & Math Tables

Draw on board, paper, or ground. Addition = jump forward; subtraction = jump back; skip-counting. Shared number line keeps class oriented.

### STRAT4 — Everyday Items
📷 Send this image first, then deliver strategy content:
![](https://i.imgur.com/SMATUZi.jpeg)

Pencils, cups, books for measurement, sorting, data. Hand spans, compare weights, tally by color. No special materials needed.

### STRAT5 — Place Value Charts & Bundling
📷 Send this image first, then deliver strategy content:
![](https://i.imgur.com/nA3MnMI.jpeg)

Ones/tens/hundreds columns. Bundle at 10, move to tens. "Build 34. Add 6. What regrouping happens?"

### STRAT6 — Materials Routines & Roles
📷 Send this image first, then deliver strategy content:
![](https://i.imgur.com/y75YXTf.jpeg)

Materials Runner, Checker, Recorder. Materials map, cleanup timer. Pre-counted bags per pair.

### STRAT7 — Story Problems & Role Play

Act out scenario first, then model with objects, then write equation. Share water, market, attendance.

### STRAT8 — Matching & Sorting
📷 Send this image first, then deliver strategy content:
![](https://i.imgur.com/nRqNq2h.jpeg)

Match number + dots, equation + model. Sort by rule (even/odd, attribute). Scrap paper works for cards.

---

## 6. Quiz Questions
📷 Send this image first, then deliver the module recap and quiz:
![](https://i.imgur.com/U6WESHX.jpeg)

### Question 1: Recall

- **Matching and sorting activities help students see patterns and structures.**
  - Options: True / False

- **Why begin with role play in a math lesson?**
  - Options: To entertain / To build understanding / To test memory

- **How does a number line help students?**
  - Options: See sequence / Work quietly / Memorize numbers

- **Why are local materials useful in teaching math?**
  - Options: They replace teaching / They are expensive / They are familiar

---

### Question 2: Understanding

- **How does the bundling strategy help students understand place value?**
  - Keywords: grouping, composing numbers, hundreds/tens/ones

- **Why does acting out a problem help students understand math?**
  - Keywords: visualize, meaning, engaging

- **Why are clear routines important when using materials?**
  - Keywords: time, organization, access, participation

- **What kind of everyday objects can support learning in math class?**
  - Keywords: stones, backpacks, pens, shoes

---

### Question 3: Application

- **Scenario 1:**
  Students are learning about shapes and numbers, but struggle to see patterns and relationships. The teacher wants an activity that helps students group and compare ideas.
  *What could the teacher do using matching and sorting strategies?*

- **Scenario 2:**
  A teacher wants to teach measurement, but does not have rulers or scales. The teacher still wants students to compare and measure objects.
  *What could the teacher do using everyday items?*

- **Scenario 3:**
  Students are learning addition, but they lose track when counting forward and backward. The teacher wants to give them a visual way to follow the numbers.
  *How could the teacher support students with a number line?*

- **Scenario 4:**
  A teacher is teaching three-digit numbers, but students are not understanding how numbers are grouped. The teacher wants to make place value more visible.
  *How could this teacher use bundling or a place value chart?*
