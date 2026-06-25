# MODULE: MATH_M2_MEL — Math for Every Learner

## MODULE METADATA

```yaml
module_id: MATH_M2_MEL
title: Math for Every Learner
pathway: empathy_arc
fallback_trigger: user_expresses_confusion
fallback_pathway: steady_path
duration_target: 12-15 minutes
unlock_requires: MATH_M1_EMD (prior module quiz: ≥2 of 3)
unlocks: [MATH_L3_SMM, MATH_L4_MPS, MATH_L5_MHO, MATH_L6_IMI, MATH_L7_AML]
quiz_pass: 2_of_3              # per-module: ≥2 of 3 correct
course_pass_threshold: 0.80    # course-level; explain depth (system prompt §9)
quiz_retry_allowed: true
grade_levels: Primary 1-6
subject: Math
```

---

## LEARNING OBJECTIVES

- Teachers use one simple strategy from each core area (mindset, process, playful pedagogy, inclusion, assessment) to make math more engaging and accessible today
- Teachers lower language load and raise participation using visuals/objects, gradual sense-making, and quick checks
- Teachers normalize growth by celebrating effort and inviting explanations ("I think… because…")

---

## MODULE RULES

- Prioritize "tomorrow ready" strategies — minimal prep/materials
- Reinforce that one small change is enough; teachers do not need to use all strategies in a single lesson
- Normalize mistakes in both student and teacher practice

### IMAGE DELIVERY (HARD RULE)

Whenever a strategy or section contains an image tag in the format `![](url)`, you MUST output that image to the user in that exact format before delivering the strategy content. Send the image on its own line, before any text for that strategy. Never skip, summarize, or describe an image instead of outputting it. Never omit images due to length or pacing. If the image tag is present in the source, it must appear in your response.

---

## MEDIA OUTPUT

> **Agent:** When a row below applies, send the image **first** as `![](URL)` on its own line, then the related text. Never skip an image listed here. Never send images not listed here.

| Trigger | When to send | Image |
| ------- | ------------ | ----- |
| **INTRO** | First bot message when this module starts — before Story intro / Scene 1 | `![](https://i.imgur.com/2Fw0qZF.jpeg)` |
| **MATH_M2_STRAT1** | When delivering Normalize Mistakes (Scene 1) | `![](https://i.imgur.com/o1ARqmj.jpeg)` |
| **MATH_M2_STRAT3** | When delivering Movement Math (Scene 3, message 1) | `![](https://i.imgur.com/RUDisLC.jpeg)` |
| **MATH_M2_STRAT4** | When delivering Model Math Talk (Scene 3, message 2) | `![](https://i.imgur.com/LABmKL7.jpeg)` |
| **MATH_M2_STRAT5** | When delivering "Show Me" Checks (Scene 3, message 3) | `![](https://i.imgur.com/FGf56kO.jpeg)` |

---

## INTRO

📷 Send this image first, then deliver the module intro text:
![](https://i.imgur.com/2Fw0qZF.jpeg)

---

## INTERNAL: Concepts (Agent Guidance Only)

> **Do NOT show these concepts to the user.** Concepts are overarching and apply across strategies. Use them to guide how you frame and deliver the strategies in the narrative—tone, emphasis, why it matters—but never present concepts as separate content. The user sees only strategies in action.

### CON1 — Celebrating Mistakes Builds Resilience

Many learners associate errors with embarrassment or punishment, which can be intensified by stress or trauma. When teachers reframe mistakes as information, students feel safer to try again and persist through challenges. Publicly valuing mistakes and revisions normalizes productive struggle and keeps learners focused rather than opting out when a task becomes difficult.

### CON2 — Low-Language Routines Invite All Learners

When tasks allow showing, drawing, telling, or acting, language barriers and confidence hurdles shrink. Using local materials, gestures, and quick models means many learners can start immediately, build understanding, and then add words. This raises participation in large and multilingual classes and makes math feel relevant to everyday life.

### CON3 — Show First, Then Name

Starting with visible models (objects, sketches, gestures) lets children see what the math looks like before they must explain it. Moving from concrete to numeric ties vocabulary to meaning, prevents empty recitation, and makes strategies easy to comprehend. Modeling is a bridge from doing to understanding.

### CON4 — Tiny Checks Guide Next Steps

Assessment during learning produces more useful information than long tests after a period of time. Quick checks keep anxiety low, reveal misunderstandings early, and help teachers decide whether to revisit, extend, or differentiate. When learners see checks as ways to get support—not punishment—effort and comfort increase.

---

## EMPATHY_ARC SCENE MAPPING

> **Agent:** Generate narrative scenes at runtime. **Show only strategies to the user.** Concepts guide your framing but are never delivered explicitly. Use this mapping to know which strategy belongs in each scene. **Pacing:** Scene 3 has 3 strategies—deliver one strategy per message; do not compress into one scene. Use `<break>` between them.

| Scene | Strategy | Concept (guides delivery; do not show) | Narrative brief |
|-------|----------|----------------------------------------|-----------------|
| Scene 1 | STRAT1 (Normalize Mistakes) | CON1 | A teacher models a mistake on purpose and shows the class how she fixes it. Students see that mistakes are information, not failure. Show the strategy in action—no concept definitions. |
| Scene 2 | STRAT2 (Use Real-World Problems) | CON2 | A teacher uses a local, real-world problem (sharing food, market, measurement) instead of textbook examples. Students engage because they recognize the situation. Show the strategy in action. |
| Scene 3 | STRAT3 + STRAT4 + STRAT5 (Movement Math, Model Math Talk, "Show Me" Checks) | CON3 + CON4 | Weave together: movement to make math concrete, sentence frames for explaining thinking, and "Show Me" finger checks for instant feedback. Show strategies in action—no concept definitions. |

---

## EMPATHY_ARC REFLECTION PROMPTS

> **Agent:** Use these prompts at the specified points. Wait for user response before continuing.

| Step | Prompt |
|------|--------|
| Reflection #1 (after Scene 1) | Have you experienced something like this—students afraid to be wrong, or a moment when modeling a mistake changed the mood in your class? |
| Reflection #2 (after Scene 3) | What part of this story stood out to you? |

---

## STRATEGIES (User-facing)

> **Agent:** These are what the user sees—through the narrative. Deliver strategies in action; never deliver concepts as separate content.

### MATH_M2_STRAT1 — Normalize Mistakes
📷 Send this image first, then deliver strategy content:
![](https://i.imgur.com/o1ARqmj.jpeg)

**Description:** Model and celebrate mistakes to help children build resilience and reduce math anxiety.

**Expanded explanation:** Make your own mistake on purpose and show the class how you fix it. Circle the error, name what happened ("I rushed and counted twice here"), and correct it calmly. Invite students to share "favorite mistakes" and reframe them positively. A 30-second "teacher mistake moment" can shift the class from fear to curiosity.

**Examples / Variations:**
- Solve a problem wrong on purpose, circle the error, fix it aloud
- "Favorite mistake of the day" share
- Redirect "I failed" to "I need help. Let's check another way"

**Reflection prompt:** What's one problem you could solve wrong on purpose tomorrow?

**Quiz item:** Why should teachers celebrate mistakes? (Keywords: learning, reduce anxiety, resilience, information)

---

### MATH_M2_STRAT2 — Use Real-World Problems
**Description:** Connect math tasks to everyday activities like sharing food or measuring water.

**Expanded explanation:** Tie problems to daily tasks that use no special materials: sharing food fairly, market counting with beans or bottle caps, water measurement (how many cups fill a bucket), skip-counting while cleaning or lining up. Use local names, places, and objects so children see math as a tool for fairness, planning, and fun.

**Examples / Variations:**
- "Your mother has 12 groundnuts and 4 children. How can she share fairly?"
- Count beans at lunch; share snacks equally
- Use bottle caps to model; ask pairs to explain using "Each child gets ___ because ___"

**Reflection prompt:** What daily activity could you turn into tomorrow's math problem?

**Quiz item:** Give one example of a real-world math task. (Keywords: share, sharing, food, water, measure, divide, mangoes, groundnuts)

---

### MATH_M2_STRAT3 — Movement Math
📷 Send this image first, then deliver strategy content:
![](https://i.imgur.com/RUDisLC.jpeg)

**Description:** Use physical actions to make math concrete, then capture it in sketch and numbers.

**Expanded explanation:** Have students show quantities with fingers, then draw, then write. "Show me 5 with your fingers. Now show me 3 more. How many altogether?" Movement makes the math visible before the numbers. Includes students who hesitate to speak and regulates energy in crowded rooms.

**Examples / Variations:**
- Fingers for addition: show 5, show 3 more, count total
- Draw fingers on slates, then write the equation
- Hopscotch for skip-counting; clap patterns

**Reflection prompt:** Where could movement replace talk in your next math lesson?

**Quiz item:** Why is movement helpful for teaching math? (Keywords: concrete, physical, includes learners, low language)

---

### MATH_M2_STRAT4 — Model Math Talk
📷 Send this image first, then deliver strategy content:
![](https://i.imgur.com/LABmKL7.jpeg)

**Description:** Teach the talk you want to hear with sentence frames and mini think-alouds.

**Expanded explanation:** Solve a problem aloud while talking through your thinking. Write a sentence frame on the board: "I solved it by ___. It makes sense because ___." Ask pairs to practice with the same frame. Gives students the vocabulary and structure to explain their reasoning, especially in multilingual classrooms.

**Examples / Variations:**
- "I solved it by making equal groups. It makes sense because 12 divided into 3 groups gives 4 in each."
- Frame: "I solved it by ___. It makes sense because ___."
- Pairs practice with the frame; share with another pair

**Reflection prompt:** What sentence starter could you try tomorrow?

**Quiz item:** Why do sentence frames help students explain their thinking? (Keywords: vocabulary, structure, confidence, express ideas)

---

### MATH_M2_STRAT5 — "Show Me" Checks
📷 Send this image first, then deliver strategy content:
![](https://i.imgur.com/FGf56kO.jpeg)

**Description:** Students respond with fingers, slates, or cards for instant all-class feedback.

**Expanded explanation:** Ask all students to show the answer at once—fingers, slates, or cards. "The pattern is 2, 4, 6... Show me the next number with your fingers." Scan the room to see what everyone is thinking. When you spot different answers, pause: "I see some different answers. Let's figure this out together." Instant, low-anxiety checks that guide your next step.

**Examples / Variations:**
- Fingers for number patterns
- Slates for quick answers
- Scan the room before moving on; address confusion in the moment

**Reflection prompt:** Where could a "Show Me" check fit into your next lesson?

**Quiz item:** What is the main benefit of a "Show Me" check? (Keywords: see all students, instant, whole class, adjust teaching)

---

## QUIZ

> **Agent:** Deliver all 3 items (recall → understanding → application). User must get **≥2 of 3** correct to unlock Deep Dives. Provide correct answer + 1-sentence explanation after each item. If not passed, offer one retry per item with alternate items from QUIZ_BANK_ALT (system prompt §9).

### QUIZ_ITEM_1

| Field | Value |
|-------|-------|
| **Type** | Multiple choice |
| **Question** | Why should teachers celebrate mistakes? |
| **Options** | A) To embarrass students into trying harder / B) To show that mistakes are part of learning and reduce anxiety / C) To identify which students are struggling / D) To save time during lessons |
| **Correct** | B |
| **Feedback** | Celebrating mistakes helps students see errors as learning opportunities, which builds resilience and reduces math anxiety. |

### QUIZ_ITEM_2

| Field | Value |
|-------|-------|
| **Type** | Short answer (accept keywords) |
| **Question** | Give one example of a real-world math task you could use in your classroom. |
| **Accept keywords** | share, sharing, food, water, measure, seating, time, budget, divide, pencils, materials, groundnuts, mangoes |
| **Example answers** | "Sharing 12 pencils among 4 groups," "Measuring water for drinking," "Figuring out seating for the class" |
| **Feedback** | Real-world problems help students see why math matters and keep them engaged. |

### QUIZ_ITEM_3

| Field | Value |
|-------|-------|
| **Type** | Multiple choice |
| **Question** | What is the main benefit of a "Show Me" check? |
| **Options** | A) It gives students a grade / B) It lets the teacher see what all students are thinking at once / C) It replaces the need for teaching / D) It only works with small classes |
| **Correct** | B |
| **Feedback** | "Show Me" checks give instant, whole-class data so teachers can adjust their teaching in real time. |

---

## QUIZ_BANK_ALT

> **Agent:** Use these items if retry is needed.

### ALT_ITEM_1

| Field | Value |
|-------|-------|
| **Question** | Why is movement helpful for teaching math? |
| **Options** | A) It tires students out so they sit still later / B) It makes math concrete and includes students who hesitate to speak / C) It's only for young children / D) It replaces the need for explanation |
| **Correct** | B |

### ALT_ITEM_2

| Field | Value |
|-------|-------|
| **Question** | Why do sentence frames help students explain their thinking? |
| **Options** | A) They give students the vocabulary and structure to express ideas / B) They make answers shorter / C) They only help students who speak English / D) They replace the need for understanding |
| **Correct** | A |

### ALT_ITEM_3

| Field | Value |
|-------|-------|
| **Question** | What is one way to normalize mistakes in your classroom? |
| **Accept keywords** | model, teacher mistake, celebrate, favorite mistake, fix, correct, circle error |

---

## OPTIONAL_ENRICHMENT

> **Agent:** Offer only after quiz is passed. Not required for completion.

### DIY_ACTIVITY_1: Growth Mindset Wall

| Field | Value |
|-------|-------|
| **Time** | ~15 minutes |
| **Materials** | Paper, chalk |
| **Steps** | 1. Students share a mistake they made / 2. Class helps reframe it positively / 3. Add to the wall display |
| **Variation (younger)** | Drawings of mistakes |
| **Variation (older)** | Short written notes |

### DIY_ACTIVITY_2: Human Number Line

| Field | Value |
|-------|-------|
| **Time** | 10-15 minutes |
| **Materials** | Optional: chalk or tape |
| **Steps** | 1. Mark start/end points of a life-sized number line / 2. Call a number; student stands at that spot and explains / 3. Student shows +2 (or other operation) with steps / 4. Repeat with other students |
| **Variation (younger)** | Help students move along the line together |
| **Variation (older)** | Students draw on slates first, then volunteer demonstrates |
