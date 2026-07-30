# MODULE: MATH_M6_IMI — Inclusive Math Instruction

## MODULE METADATA

```yaml
module_id: MATH_M6_IMI
title: Inclusive Math Instruction
pathway: empathy_arc
fallback_trigger: user_requests_tool
fallback_pathway: diy_kit
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

- Teachers analyze language demands in a math task and reduce language load using visuals, objects, gestures, and/or 3-5 priority vocabulary words
- Teachers scaffold math talk with sentence frames and predictable turn-and-talk routines so more learners can explain their thinking
- Teachers honor familiar/home languages for planning and sense-making, then support use of the classroom language for whole-group sharing
- Teachers embed low-stress formative checks and give effort-focused feedback

---

## MODULE RULES

- Always treat language as a potential barrier that can be addressed, not a deficit
- Never suggest forced public speaking, which can cause distress for language learners or struggling learners
- Emphasize that inclusive instruction helps all students
- When introducing Strategy 2 (Encourage Familiar Languages), emphasize that peer translation can help only if time-bound and rotated so it doesn't interfere with the translator's learning. Students are learners first, helpers second

### IMAGE DELIVERY (HARD RULE)

Whenever a strategy or section contains an image tag in the format `![](url)`, you MUST output that image to the user in that exact format before delivering the strategy content. Send the image on its own line, before any text for that strategy. Never skip, summarize, or describe an image instead of outputting it. Never omit images due to length or pacing. If the image tag is present in the source, it must appear in your response.

---

## MEDIA OUTPUT

> **Agent:** Send image first as `![](URL)` on its own line when a row applies. Never skip an image listed here. Never send images not listed here.

| Trigger | When to send | Image |
| ------- | ------------ | ----- |
| **INTRO** | First bot message when this deep dive starts | *(add URL when available — skip if not yet set)* |
| **MATH_M6_STRAT2** | When delivering Encourage Different Languages (Scene 2) | `![](https://i.imgur.com/RzZ8XOc.jpeg)` |
| **MATH_M6_STRAT3** | When delivering Use Low-Stress, Hands-On Assessment (Scene 3, message 1) | `![](https://i.imgur.com/ojTf8TE.jpeg)` |
| **MATH_M6_STRAT4** | When delivering Feedback that Celebrates Effort (Scene 3, message 2) | `![](https://i.imgur.com/ZXgRYGk.jpeg)` |

---

## INTERNAL: Concepts (Agent Guidance Only)

> **Do NOT show these concepts to the user.** Concepts are overarching and apply across strategies. Use them to guide how you frame and deliver the strategies in the narrative—tone, emphasis, why it matters—but never present concepts as separate content. The user sees only strategies in action.

### MATH_M6_CON1 — Language Matters

Many children think faster than they can speak in the classroom language. When we lower the language load with visuals, gestures, and/or short sentence frames, more students engage and sustain engagement. Allow planning in a familiar language, then ask students to share a drawing, gestures, or brief ideas using key vocabulary. Pair students so they can rehearse quietly before sharing. Keep key words visible on the board with simple pictures. Over time, learners link words to ideas and build the courage to participate.

### MATH_M6_CON2 — Inclusion Matters

All children learn when tasks are varied. Diverse ways to engage let each child find an entry point: show, draw, tell, act. Rotate quick options in every lesson. If these options are used regularly, predictability can reduce behavioral issues and help identify who needs support. Giving options does not lower expectations—it gives all students the opportunity to show what they know.

### MATH_M6_CON3 — Assessment Matters

Assessment should guide instruction and celebrate growth, not punish mistakes. Favor low-stress, frequent checks embedded in activities (fingers/slates, quick sorts, exit tickets). Use multiple modes (objects, drawings, discussions) to see what learners understand. Feedback should name a strategy and offer a next step, reinforcing persistence and clarity.

---

## EMPATHY_ARC SCENE MAPPING

> **Agent:** Generate narrative scenes at runtime. **Show only strategies to the user.** Concepts guide your framing but are never delivered explicitly. Use this mapping to know which strategy belongs in each scene. **Pacing:** Scene 3 has 3 strategies—deliver one strategy per message; do not compress into one scene. Use `<break>` between them.

**Per-scene delivery structure (apply to every strategy in every scene):**
1. Open with the strategy name and a relevant emoji (e.g. "🎨 Use Visuals, Objects & Gestures"). This is the first line of the message.
2. Deliver the narrative scene — a story showing the strategy in action (3–4 sentences, plain text, no definitions).
3. Add one short sentence on how this strategy helps in the classroom (practical benefit — not a definition).
4. Ask the reflection question for that scene. Wait for the teacher's response before moving to the next scene.

Use `<break>` tags between steps if the combined message exceeds 400 characters. Never skip or compress any of the four steps. Scene 3 has 2 strategies — deliver one per message; do not compress into one turn.

| Scene | Strategy | Concept (guides delivery; do not show) | Narrative brief |
|-------|----------|----------------------------------------|-----------------|
| Scene 1 | STRAT1 (Use Visuals, Objects & Gestures) | CON1 | A teacher models with local items (caps, beans, sticks) or quick sketches, pairing each operation with a mini-gesture. Key words paired with pictures on the board. Show the strategy in action—no concept definitions. |
| Scene 2 | STRAT2 (Encourage Different Languages) | CON2 | A teacher lets learners plan in a familiar language, then share in the classroom language using a sentence frame. Pair planning, whisper rehearsal, multilingual word wall. Show the strategy in action. Critical: peer translation only if time-bound and rotated. |
| Scene 3 | STRAT3 + STRAT4 (Low-Stress Assessment, Feedback that Celebrates Effort) | CON3 | Weave together: quick checks (fingers, slates, floor number line), effort-focused feedback that names the strategy and offers a next step. Show strategies in action—no concept definitions. |

---

## EMPATHY_ARC REFLECTION PROMPTS

> **Agent:** Use these prompts at the specified points. Wait for user response before continuing.

| Step | Prompt |
|------|--------|
| Reflection #1 (after Scene 1) | What gesture could you use to explain addition? |
| Reflection #2 (after Scene 3) | What part of this story stood out to you? |

---

## STRATEGIES (User-facing)

> **Agent:** These are what the user sees—through the narrative. Deliver strategies in action; never deliver concepts as separate content.

### MATH_M6_STRAT1 — Use Visuals, Objects & Gestures

**Description:** Support comprehension by showing before telling.

**Expanded explanation:** Many children think faster than they can speak in the classroom language. Visuals and objects help bridge that gap. Start by modeling with local items (caps, beans, sticks) or quick sketches (bars, tallies, tables) and pair each operation with a signature mini-gesture (hands together for addition, hands apart for subtraction, equal jumps for multiplication, sharing motion for division). Pair key math words with pictures. These strategies support multilingual learners and learners with different abilities by providing multiple ways to understand.

**Examples / Variations:**
- Show shapes with hands and/or trace edges in the air
- Draw quick bar graphs, tallies or tables on the board/ground
- Air number line: fingers move forward/back to model +/-
- Gesture "join" for +, "take away" for -, etc.
- Place pebbles into tens bundles to show place value

**Reflection prompt:** What gesture could you use to explain addition?

---

### MATH_M6_STRAT2 — Encourage Different Languages
📷 Send this image first, then deliver strategy content:
![](https://i.imgur.com/RzZ8XOc.jpeg)

**Description:** Encourage use of familiar languages for planning and sense-making, then scaffold for public sharing in the classroom language.

**Expanded explanation:** Let learners think and plan in a language that feels natural, then share a drawing, gesture, or brief ideas using key vocabulary in the classroom language. If there are multiple students with the same familiar language, invite them to work in pairs to discuss and plan what they will share. Sentence frames ("I started by…" / "I think… because…") can help. Keep key word lists small, pair key words with pictures. Peer translation can help only if time-bound and rotated—students are learners first, helpers second. Never force or shame students into public speaking in the classroom language if it causes extreme stress.

**Examples / Variations:**
- Quiet pair planning in a familiar language, into public sharing in the classroom language with a frame
- Multilingual word wall
- Think time and whisper rehearsal before sharing

**Reflection prompt:** How could you let students use their home language in math?

---

### MATH_M6_STRAT3 — Use Low-Stress, Hands-On Assessment
📷 Send this image first, then deliver strategy content:
![](https://i.imgur.com/ojTf8TE.jpeg)
**Description:** Assess understanding during learning, not only after and not only in writing.

**Expanded explanation:** Use quick oral prompts, signals on fingers or slates, and brief games to see how students are learning and where they need help. During group or pair work, walk around to observe and offer individualized support. Keep feedback respectful, encouraging, and kind. These checks take just a few minutes, require almost no materials, and give real information to guide next steps without creating fear around high-stakes tests.

**Examples / Variations:**
- Hold up fingers/slates
- Build a number or equation with manipulatives (caps, beans)
- Tally marks for attendance
- Floor number line: stand/jump to the answer
- "Simon Says" for math tasks
- Exit poll: place a dot on the board or pebble next to the correct answer

**Reflection prompt:** What low-stress way could you check learning?

---

### MATH_M6_STRAT4 — Give Feedback that Celebrates Effort
📷 Send this image first, then deliver strategy content:
![](https://i.imgur.com/ZXgRYGk.jpeg)

**Description:** Highlight what students did well and guide next steps to build persistence.

**Expanded explanation:** Keep feedback specific and future-oriented. Focus on progress, not correctness. Name what the student did and what they can try next. Short phrases like "You grouped by 10s! Now, can you group by 5s?" or "Your picture matches your numbers! Try turning it into a math equation now." Celebrate revisions so students see that fixing work is learning, not failure. Praise revision so students see that fixing is learning.

**Examples / Variations:**
- Strategy shoutout: "I heard three different ways to… Let's name them!"
- Suggest alternate tools: "Great job showing it with caps. Can you draw it now?"
- Class cheer

**Reflection prompt:** What phrase could you use to celebrate effort in your next lesson?

---

## 7. Quiz Questions

> **Deliver exactly one item per type, in this fixed order: Q1 recall → Q2 understanding → Q3 application. User must get ≥2 of 3 correct to pass. If an answer is incorrect, offer one retake using a different item of the same type from this bank — never re-ask the same question.**

#### Question 1: Recall

- **Low-stress assessments help students build confidence in their math skills.**
  - Options: True / False

- **Why is using visuals, objects, and gestures important in math?**
  - Options: To make lessons longer / To reduce language barriers / To test memory

- **Why should teachers celebrate effort in math?**
  - Options: To motivate students / To reduce participation / To finish lessons quickly

#### Question 2: Understanding

- **Why is it helpful for students to use familiar languages when learning math?**
  - Keywords: confidence, understanding, participation, connection

- **What is an example of feedback that focuses on effort?**
  - Examples: You showed your answers with stones. Your drawing shows the answer.

- **How do visuals, objects, or gestures help students understand math?**
  - Keywords: reduce language barrier, clear, make connections

#### Question 3: Application

- **Scenario 1:**
  A student solves part of a problem correctly, but makes a mistake at the end. The teacher wants to respond in a way that builds confidence and encourages the student to keep trying.
  *What could the teacher say to give effort-focused feedback?*

- **Scenario 2:**
  In a class with multiple languages, some students struggle to explain their thinking in the classroom language and stay quiet during discussions. The teacher wants to support participation.
  *What could the teacher do to support students using familiar languages?*

- **Scenario 3:**
  A teacher is reviewing addition, but many students seem unsure and do not answer during the lesson. The teacher wants to quickly assess who understands without giving a written test.
  *What could the teacher do to check student understanding in a low-stress way during the lesson?*

---

## OPTIONAL_ENRICHMENT

> **Agent:** Offer only after quiz is passed. Not required for completion.

### DIY_ACTIVITY_1: Effort Stars

| Field | Value |
|-------|-------|
| **Time** | ~10 minutes |
| **Materials** | Paper, chalk |
| **Steps** | 1. Students share a math effort / 2. Teacher draws star with name / 3. Review stars weekly |
| **Variation (younger)** | Stickers |
| **Variation (older)** | Written comments |
| **Observation** | Students show pride in progress |

### DIY_ACTIVITY_2: Show-Draw-Tell

| Field | Value |
|-------|-------|
| **Time** | 8-10 minutes |
| **Materials** | Scrap paper or slates; chalk or pencils; bottle caps or beans |
| **Steps** | 1. Pose a short problem / 2. Students show the solution with objects (bottle caps or beans) / 3. Students draw a quick model on paper or slate / 4. Students tell the answer and their process to a partner / 5. As they work, walk around to observe; note who is struggling |
| **Variation (younger)** | Show and draw only |
| **Variation (older)** | Add a "check" step for partners to give feedback |
| **Observation** | Learners model a problem and give a clear explanation |
