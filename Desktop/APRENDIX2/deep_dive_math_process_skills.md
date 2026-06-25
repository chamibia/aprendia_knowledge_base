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

**Quiz item:** What are the SDT steps? (Keywords: show, draw, tell)

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

**Quiz item:** Why are concrete materials important for math? (Keywords: hands-on, understanding, inclusion)

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

**Quiz item:** Give one way learners can show their thinking. (Keywords: draw, gesture, objects, act out)

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

**Quiz item:** Why should learners justify answers? (Keywords: reasoning, logic, explanation)

---

### MATH_M4_STRAT5 — Provide Sentence Frames

**Description:** Provide structured language supports like "I think… because…" to help children express ideas clearly.

**Expanded explanation:** Giving language scaffolds helps every learner contribute clearly, especially language learners or students whose math language is still developing. Post "math talk" sentence frames (e.g., "I started by…" / "I grouped…" / "I checked by…" / "I disagree because…") and model one-sentence responses. Use them in turn-and-talk routines and refresh frames across the week. Keep frames visible at child height and celebrate when learners use a frame unprompted.

**Examples / Variations:**
- Math reasoning frames: "I solved it by ___" / "The answer makes sense because ___" / "I checked by…"
- Exit slips using a chosen frame
- Peer feedback frames: "I noticed…" / "Next time try…"

**Reflection prompt:** What sentence starter could you introduce in the next lesson?

**Quiz item:** How do sentence frames help learners? (Keywords: clarity, communication, inclusion)

---

## QUIZ

> **Agent:** Deliver all 3 items (recall → understanding → application). User must get **≥2 of 3** correct to pass the module. Provide correct answer + 1-sentence explanation after each item. If not passed, offer one retry per item with alternate items from QUIZ_BANK_ALT (system prompt §9).

📷 Send this image first, then deliver the module recap and quiz:
![](https://i.imgur.com/HlRWscB.jpeg)
### QUIZ_ITEM_1

| Field | Value |
|-------|-------|
| **Type** | Short answer (accept keywords) |
| **Question** | What are the SDT (Show-Draw-Tell) steps? |
| **Accept keywords** | show, draw, tell |
| **Example answers** | "Show with objects, draw a model, tell a partner" |
| **Feedback** | SDT is show (with objects), draw (a model), tell (using a sentence frame). |

### QUIZ_ITEM_2

| Field | Value |
|-------|-------|
| **Type** | Multiple choice |
| **Question** | Why are concrete materials important for math? |
| **Options** | A) They replace the need for teaching / B) They support hands-on understanding and inclusion / C) They only work in small classes / D) They make lessons longer |
| **Correct** | B |
| **Feedback** | Concrete materials build understanding through touch and movement and help all learners participate. |

### QUIZ_ITEM_3

| Field | Value |
|-------|-------|
| **Type** | Multiple choice |
| **Question** | Why should learners justify their answers? |
| **Options** | A) To slow down the lesson / B) To strengthen reasoning and sense-making / C) To identify struggling students / D) To replace the need for practice |
| **Correct** | B |
| **Feedback** | Justifying answers builds reasoning, reveals misconceptions, and increases sense-making. |

---

## QUIZ_BANK_ALT

> **Agent:** Use these items if retry is needed.

### ALT_ITEM_1

| Field | Value |
|-------|-------|
| **Question** | Give one way learners can show their math thinking. |
| **Accept keywords** | draw, gesture, objects, act out, sketch, slate |

### ALT_ITEM_2

| Field | Value |
|-------|-------|
| **Question** | How do sentence frames help learners? |
| **Options** | A) They make answers shorter / B) They support clarity, communication, and inclusion / C) They only help advanced students / D) They replace the need for thinking |
| **Correct** | B |

### ALT_ITEM_3

| Field | Value |
|-------|-------|
| **Question** | What free material could you use for math? |
| **Accept keywords** | bottle caps, beans, sticks, stones, string, paper, cups |

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
