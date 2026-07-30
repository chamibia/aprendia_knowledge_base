# MODULE: MATH_M4_MPS — Math Process Skills

## MODULE METADATA

```yaml
module_id: MATH_M4_MPS
title: Math Process Skills
pathway: empathy_arc
fallback_trigger: user_mastery >= 0.90
fallback_pathway: explain_exchange
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

- Teachers understand the five math process skills (problem solving, reasoning, communication, connections, representation) and can name them during instruction
- Teachers apply holistic approaches (head = strategy/sense-making, heart = persistence/regulation, hands = doing/trying) to build process skills
- Teachers guide learners to explain and check their thinking (not just give answers) using concrete models, drawings, and sentence frames

---

## MODULE RULES

- When introducing Strategy 4 (Ask Children to Justify Answers), emphasize that this is not meant to be punishment. It should be a positive interaction that gives students the opportunity to ask "does what I found make sense?" and show what they know
- Do not say or imply that explanations must be verbal—nonverbal options also build process skills

### IMAGE DELIVERY (HARD RULE)

Whenever a strategy or section contains an image tag in the format `![](url)`, you MUST output that image to the user in that exact format before delivering the strategy content. Send the image on its own line, before any text for that strategy. Never skip, summarize, or describe an image instead of outputting it. Never omit images due to length or pacing. If the image tag is present in the source, it must appear in your response.

---

## MEDIA OUTPUT

> **Agent:** Send image first as `![](URL)` on its own line when a row applies. Never skip an image listed here. Never send images not listed here.

| Trigger | When to send | Image |
| ------- | ------------ | ----- |
| **INTRO** | First bot message when this deep dive starts | `![](https://i.imgur.com/7lL4fgz.jpeg)` |
| **MATH_M4_STRAT1** | When delivering Show-Draw-Tell (Scene 1) | `![](https://i.imgur.com/5zsivB6.jpeg)` |
| **MATH_M4_STRAT4** | When delivering Ask Children to Justify Answers (Scene 3, message 2) | `![](https://i.imgur.com/Sij78H6.jpeg)` |
| **QUIZ** | Before delivering the module recap and quiz | `![](https://i.imgur.com/HlRWscB.jpeg)` |

---

## INTERNAL: Concepts (Agent Guidance Only)

> **Do NOT show these concepts to the user.** Concepts are overarching and apply across strategies. Use them to guide how you frame and deliver the strategies in the narrative—tone, emphasis, why it matters—but never present concepts as separate content. The user sees only strategies in action.

### MATH_M4_CON1 — Process Skills

Process skills = problem solving, reasoning, communication, connections, representation. Particularly in emergency settings, these skills help children make good decisions with limited information. Reasoning and communication reduce guessing and encourage evidence ("How do we know?"). Connections link math to everyday life (including health, safety, livelihoods, etc). Representation encourages learners to show ideas (with stones, dots, lines, body movements, etc) and make math practical. Math routines like estimate→try→check are useful for teaching process skills.

### MATH_M4_CON2 — Holistic Instruction

Holistic instruction = head (thinking), heart (persevering), hands (playful engagement). "Head" focuses on sense-making; "heart" builds resilience, calm, and willingness to try; "hands" uses movement and touch to anchor attention and deepen learning. Short, playful math tasks can help regulate emotions and invite participation from all children, especially in large classes. Teachers should celebrate persistence and visible strategies to make math instruction more holistic. This balance keeps lessons engaging and inclusive, even with limited time and materials.

### MATH_M4_CON3 — Math as a Journey

Math as a journey = focus on thinking/explaining, not just right answers. Discouraging prior experiences, interrupted schooling, and trauma can make children fear mistakes. Treat tasks as journeys with checkpoints (estimate→try→check). Encourage reflection ("I used… because…") and partner explanations (using a familiar language, even if not the language of instruction). Praise effort, strategy choice, and clear explanations over speed or correctness. Use quick "sense checks" ("Is 11+6 closer to 20 or 25? Why?") so learners can experience their own growth, not just focus on final scores.

---

## EMPATHY_ARC SCENE MAPPING

> **Agent:** Generate narrative scenes at runtime. **Show only strategies to the user.** Concepts guide your framing but are never delivered explicitly. Use this mapping to know which strategy belongs in each scene. **Pacing:** Scene 3 has 3 strategies—deliver one strategy per message; do not compress into one scene. Use `<break>` between them.

**Per-scene delivery structure (apply to every strategy in every scene):**
1. Open with the strategy name and a relevant emoji (e.g. "✋ Show-Draw-Tell"). This is the first line of the message.
2. Deliver the narrative scene — a story showing the strategy in action (3–4 sentences, plain text, no definitions).
3. Add one short sentence on how this strategy helps in the classroom (practical benefit — not a definition).
4. Ask the reflection question for that scene. Wait for the teacher's response before moving to the next scene.

Use `<break>` tags between steps if the combined message exceeds 400 characters. Never skip or compress any of the four steps. Scene 3 has 3 strategies — deliver one per message; do not compress into one turn.

| Scene | Strategy | Concept (guides delivery; do not show) | Narrative brief |
|-------|----------|----------------------------------------|-----------------|
| Scene 1 | STRAT1 (Show-Draw-Tell) | CON1 | A teacher uses the SDT routine: pose a problem, learners SHOW with objects, DRAW a quick model, then TELL a partner using a sentence frame ("I think… because…"). Show the strategy in action—no concept definitions. |
| Scene 2 | STRAT2 (Use Concrete Materials) | CON2 | A teacher provides bottle caps, sticks, or beans for hands-on exploration. Show grab-group-compare or similar routine. Learners work with materials to tackle a problem. Show the strategy in action. |
| Scene 3 | STRAT3 + STRAT4 + STRAT5 (Encourage Show Thinking, Ask to Justify, Provide Sentence Frames) | CON3 | Weave together: learners show thinking with gestures/drawings/objects, teacher asks "why?" warmly, sentence frames ("I think… because…") support explanation. Show strategies in action—no concept definitions. |

---

## EMPATHY_ARC REFLECTION PROMPTS

> **Agent:** Use these prompts at the specified points. Wait for user response before continuing.

| Step | Prompt |
|------|--------|
| Reflection #1 (after Scene 1) | Where can you use Show-Draw-Tell in a math lesson this week? |
| Reflection #2 (after Scene 3) | What part of this story stood out to you? |

---

## STRATEGIES (User-facing)

> **Agent:** These are what the user sees—through the narrative. Deliver strategies in action; never deliver concepts as separate content.

### MATH_M4_STRAT1 — Show-Draw-Tell (SDT)
📷 Send this image first, then deliver strategy content:
![](https://i.imgur.com/5zsivB6.jpeg)

**Description:** Model math thinking by showing, drawing, then telling.

**Expanded explanation:** Show-Draw-Tell (SDT) is a short routine that turns private thinking into visible evidence. Pose a one-sentence problem, then give 20-30 seconds for learners to SHOW the problem with objects (e.g., equal groups of manipulatives, pointing on a number line). Next, ask them to DRAW a quick model (e.g., bar graph, equation, number line). Finally, ask learners to TELL a partner one sentence using a posted sentence frame ("I think… because…" or "I solved it by… then I checked by…"). This keeps language demands low at first and adds words only after a model has been created. SDT fits any math domain and works even with no special materials.

**Examples / Variations:**
- Organize data into groups → draw a bar graph → "I solved it by…"
- Points on a number line → draw and label a picture equation → "It makes sense because…"
- Count steps from one end of the room to the other → write and compare step numbers → "I checked by…"

**Reflection prompt:** Where can you use SDT in a math lesson this week?

---

### MATH_M4_STRAT2 — Use Concrete Materials

**Description:** Provide physical objects like bottle caps, sticks, or seeds to explore math through touch and movement.

**Expanded explanation:** Particularly in high-stress settings, hands-on work steadies attention and builds understanding. Materials do not have to be fancy—bottle caps, beans, sticks, paper, cups of different sizes. Setting up small, repeatable routines can help students become comfortable using materials, like grab-group-compare (pull a random number of beans, make equal groups and count leftovers). If materials are scarce, students can work in small groups to share or you can create materials using scraps of paper.

**Examples / Variations:**
- Grouping with caps/buttons/beans
- Skip counting with groups of items
- Measuring with string/hand spans
- Comparing container capacities
- Place-value building with groups of items
- Bottle cap addition

**Reflection prompt:** What free material could you collect for your next lesson?

---

### MATH_M4_STRAT3 — Encourage Children to Show Thinking

**Description:** Invite learners to describe how they solved problems using words, gestures, objects, or drawings.

**Expanded explanation:** Open multiple pathways to explaining math thinking so language or confidence are not barriers. Offer a simple response menu (show, use objects, draw, tell) and use it daily. Students can use paper or slates to show their process, use manipulatives or draw pictures, act out short math stories. If needed, invite pairs to work together in a familiar language or create small groups for sharing limited materials.

**Examples / Variations:**
- Think (or sketch) → pair → share
- Act out a word problem
- "Air number line" with fingers, showing jumps forward/back
- Build on desk → create a matching drawing → describe using a sentence frame

**Reflection prompt:** How could you let your students explain math without words?

---

### MATH_M4_STRAT4 — Ask Children to Justify Answers
📷 Send this image first, then deliver strategy content:
![](https://i.imgur.com/Sij78H6.jpeg)

**Description:** Ask learners to explain why their answer makes sense or why they chose a particular method.

**Expanded explanation:** Make asking "why?" a short, friendly part of every math lesson to lessen guessing and increase sense-making. Asking for justification reveals misconceptions, strengthens reasoning, and gives learners a habit that serves them long-term. Post sentence frames ("I think… because…" / "I used… to figure out…") and rehearse them in short turn-and-talks. Keep the tone warm—this is sense-making, not punishment. When students struggle, point to the model and ask a probing question ("Where do you see 3 groups?").

**Examples / Variations:**
- Quick turn-and-talk to share reasoning
- Checklist prompts on the board ("Plan? Model? Check?")
- Oral defense of solution using a sentence frame
- Estimate check—students stand along a line indicating too small / about right / too big

**Reflection prompt:** How could you ask your learners "why" more often?

---

### MATH_M4_STRAT5 — Provide Sentence Frames

**Description:** Provide structured language supports like "I think… because…" to help children express ideas clearly.

**Expanded explanation:** Giving language scaffolds helps every learner contribute clearly, especially language learners or students whose math language is still developing. Post "math talk" sentence frames (e.g., "I started by…" / "I grouped…" / "I checked by…" / "I disagree because…") and model one-sentence responses. Use them in turn-and-talk routines and refresh frames across the week. Keep frames visible at child height and celebrate when learners use a frame unprompted.

**Examples / Variations:**
- Math reasoning frames: "I solved it by ___" / "The answer makes sense because ___" / "I checked by…"
- Exit slips using a chosen frame
- Peer feedback frames: "I noticed…" / "Next time try…"

**Reflection prompt:** What sentence starter could you introduce in the next lesson?

---

## 7. Quiz Questions

📷 Send this image first, then deliver the module recap and quiz:
![](https://i.imgur.com/HlRWscB.jpeg)

> **Deliver exactly one item per type, in this fixed order: Q1 recall → Q2 understanding → Q3 application. User must get ≥2 of 3 correct to pass. If an answer is incorrect, offer one retake using a different item of the same type from this bank — never re-ask the same question.**

#### Question 1: Recall

- **Sentence frames help students:**
  - Options: Stay silent / Work faster / Communicate ideas

- **Students should not use objects, drawings, or gestures to show their thinking.**
  - Options: True / False

- **Why should students justify their answers?**
  - Options: To give grades / To slow down lessons / To build reasoning skills

#### Question 2: Understanding

- **What does "show, draw, tell" help students do in math?**
  - Keywords: show thinking, explain, model

- **How do sentence frames support students in math class?**
  - Keywords: structure, communication, language support, clear

- **Why are physical objects helpful when learning math?**
  - Keywords: hands-on, concrete, include, feel

#### Question 3: Application

- **Scenario 1:**
  During a lesson, students give answers quickly, but do not check if their answers make sense. The teacher wants students to slow down and think more carefully.
  *What could the teacher do to help students justify their answers?*

- **Scenario 2:**
  A teacher is teaching equal groups on the board, but students seem confused and are not participating. The teacher wants to make the lesson more hands-on.
  *How could the teacher use concrete materials in this lesson?*

- **Scenario 3:**
  A teacher gives the problem "8 + 6 =" and students quickly say the answer, but cannot explain their thinking. The teacher wants students to make their thinking visible step-by-step.
  *How could the teacher use the "show-draw-tell" routine to support students?*

---

## OPTIONAL_ENRICHMENT

> **Agent:** Offer only after quiz is passed. Not required for completion.

### DIY_ACTIVITY_1: Math Talk Circle

| Field | Value |
|-------|-------|
| **Time** | ~15 minutes |
| **Materials** | No materials needed |
| **Steps** | 1. Pose a problem / 2. Each learner explains how they solved it / 3. Celebrate different approaches |
| **Variation (younger)** | Gestures |
| **Variation (older)** | Full sentences |
| **Observation** | Learners confidently share ideas |

### DIY_ACTIVITY_2: Math Check Relay

| Field | Value |
|-------|-------|
| **Time** | ~10 minutes |
| **Materials** | No materials needed |
| **Steps** | 1. Pose a problem / 2. Learners think silently for 15 seconds, then show an answer on fingers or slates / 3. Call "Because!"—pairs say one reason their answers make sense using "I think… because…" / 4. Call "Check!"—pairs choose a fast check (stones, sketch, etc) / 5. Spotlight a few checks and share the correct answer |
| **Variation (younger)** | Gestures or show with objects |
| **Variation (older)** | Write their explanation |
| **Observation** | More learners use frames spontaneously |
