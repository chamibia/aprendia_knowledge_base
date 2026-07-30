# MODULE: AIL_M3_ALEC — Active Learning for Every Child

## MODULE METADATA

```yaml
module_id: AIL_M3_ALEC
title: Active Learning for Every Child
pathway: empathy_arc
fallback_trigger: user_expresses_confusion
fallback_pathway: steady_path
duration_target: 12-15 minutes
unlock_requires: AIL_M2_ALA (prior module quiz: ≥2 of 3)
unlocks: AIL_M4_HLLCM, AIL_M5_DRPCE, AIL_M6_PAL   # all three deep dives unlock simultaneously
quiz_pass: 2_of_3              # per-module: ≥2 of 3 correct
course_pass_threshold: 0.80    # course-level; explain depth (system prompt §9)
quiz_retry_allowed: true
grade_levels: Primary 1-6
subject: Active and Inclusive Learning
```

---

## LEARNING OBJECTIVES

- Teachers identify barriers that may prevent children from participating in classroom learning.
- Teachers understand how inclusive, active learning increases participation and belonging.
- Teachers explore how to implement active learning strategies into daily lessons.

---

## TEACHER MOTIVATIONS & PAIN POINTS

- "I try to teach everyone the same way, but some students struggle to understand."
- "I do not have time or resources to plan different lessons for different students."
- "The lessons I have aren't appropriate for all my students but I don't know how to adapt them."
- "My students think learning is only important for doing well in school."

---

## MODULE RULES

- Focus on small adjustments and tips for lesson planning, not redesigning full lessons.
- Emphasize planning ahead for inclusion instead of reacting after.
- Emphasize that inclusive strategies support all learners, not just those who are struggling.

---

## INTERNAL: Concepts (Agent Guidance Only)

> **Do NOT show these concepts to the user.** Use them to guide how you frame and deliver the strategies in the narrative — tone, emphasis, why it matters — but never present concepts as separate content. The user sees only strategies in action.

### AIL_M3_CON1 — Learner Variability is Normal

Children come to school with different backgrounds, experiences, abilities, and learning preferences. Inclusive teaching means planning for this variability from the start, not adapting after the fact. When all children can access and engage with a lesson, everyone learns better.

### AIL_M3_CON2 — Inclusion Does Not Lower Expectations

Inclusive teaching does not mean making learning easier or lowering expectations. Inclusive teaching makes learning accessible so every child has the opportunity to participate. Barriers can prevent students from engaging in the learning process, but removing them does not dilute the content — it just makes it more accessible.

### AIL_M3_CON3 — Planning for Inclusion Makes Teaching More Effective

When teachers plan for different learners ahead of time, they are more prepared during teaching. Time in the classroom is limited, so teachers must be intentional about the active learning that takes place. Planning ahead can not only increase student participation, but also increase teacher confidence during a lesson.

### AIL_M3_CON4 — Inclusive Strategies Benefit Every Child

Strategies that support one group of learners often help all learners. For example, using visuals or movement can support children learning a new language while also strengthening understanding for others. In diverse classrooms, inclusive strategies create more ways for children to participate and succeed, building a stronger sense of belonging and shared learning for everyone.

---

## EMPATHY_ARC SCENE MAPPING

> **Agent:** Generate narrative scenes at runtime. **Show only strategies to the user.** Concepts guide your framing but are never delivered explicitly. Use this mapping to know which strategy belongs in each scene. **Pacing:** Scene 3 has 2 strategies — deliver one strategy per message; do not compress into one scene. Use `<break>` between them. Do not send Scene 2 and Scene 3 back-to-back; allow the user to absorb each scene.

**Per-scene delivery structure (apply to every strategy in every scene):**
1. Open with the strategy name and a relevant emoji (e.g. "🔗 Connect Learning to Children's Lives"). This is the first line of the message.
2. Deliver the narrative scene — the story showing the strategy in action (3–4 sentences, plain text).
3. Add one short sentence on how this strategy helps in the classroom (practical benefit or what the teacher gains — not a definition).
4. Ask the reflection question for that scene. Wait for the teacher's response before moving to the next scene.

Use `<break>` tags between steps if the combined message exceeds 400 characters. Never skip or compress any of the four steps.

**⚠️ CRITICAL PACING RULE: Each scene = one strategy = one message. NEVER combine two strategies into one message. Scene 3 and Scene 4 are separate messages — deliver Scene 3, wait for the teacher's response, then deliver Scene 4.**

| Scene | Strategy | Concept (guides delivery; do not show) | Narrative brief |
|-------|----------|----------------------------------------|-----------------|
| Scene 1 | STRAT1 (Connect Learning to Children's Lives) | CON1 | A teacher is preparing a lesson and realizes her examples feel distant from students' daily lives. She makes a small change — replacing abstract examples with familiar objects like local foods or fabric. Students immediately recognize the context and engage. Show the strategy in action — no concept definitions. |
| Scene 2 | STRAT2 (Present Information in Multiple Ways) | CON2 | The same teacher (or another) explains a concept verbally but notices several students still look confused. She adds a gesture and shows an object. More students connect with the idea. Show the strategy in action — no concept definitions. |
| Scene 3 | STRAT3 (Offer Multiple Ways to Show Understanding) | CON3 | She gives students a choice in how to respond to a question — draw, act it out, or write a sentence. Quieter students who never raised their hand before begin to participate. Show the strategy in action — no concept definitions. |
| Scene 4 | STRAT4 (Eliminate Barriers Before They Happen) | CON4 | She reflects on her next lesson before class begins. She identifies a potential barrier — some students may not understand the instructions — and adjusts her plan: she will show the steps on the board and model them first. Show the strategy in action — no concept definitions. |

---

## EMPATHY_ARC REFLECTION PROMPTS

> **Agent:** Use these prompts at the specified points. Wait for user response before continuing.

| Step | Prompt |
|------|--------|
| Reflection #1 (after Scene 1) | Have you noticed students engage more when they see their own lives reflected in a lesson? What happened? |
| Reflection #2 (after Scene 3) | How could you offer students a choice in how they respond during your next lesson? |
| Reflection #3 (after Scene 4) | Which of these four strategies feels most realistic to try in your next lesson? |

---

## STRATEGIES (Reference for Narrative)

> **Agent:** Use these when constructing the narrative. Do not deliver as separate content — embody them in the story scenes.

### AIL_M3_STRAT1 — Connect Learning to Children's Lives

**Description:** Plan lessons that use students' real experiences, local examples, and familiar contexts to make learning meaningful.

**Expanded explanation:** When lessons connect to children's daily lives, they become easier to understand and more engaging. Students are more likely to participate in learning experiences when the content connects to their lives outside of school. In crisis-affected contexts, familiar references can help children feel more comfortable and grounded. Teachers should be intentional about making connections from learning to real life by asking connecting questions (e.g. "Where have you seen this before?").

**Examples / Variations:**
- Teachers allow students to lead a game that is normally played in the community.
- Bring in fabric to represent items in a math problem (e.g. "Fatou needs four different pieces of fabric for her sisters. She only has one. How many more does she need?").
- Students share their own examples related to topics (e.g. during a lesson about the capital city, students share experiences visiting family who live there).
- Teacher uses local foods, animals, and names in stories during reading lessons.

**Reflection prompt:** During your next lesson, what is a familiar reference you can use to connect learning to students' lives?

**Teacher Voice:** "My students pay more attention when they recognize themselves in lessons."

---

### AIL_M3_STRAT2 — Present Information in Multiple Ways

**Description:** Use different methods to explain ideas, like visuals, gestures, and objects.

**Expanded explanation:** Teachers can use gestures, objects, or demonstrations to help make ideas clearer for more learners. When content is only explained through speech or writing, some students may not understand or be able to make meaningful connections. Presenting information in multiple ways increases access to learning for all students. Children have different learning preferences: some students may learn better by looking at pictures while others may learn better by moving their bodies. This does not mean repeating the lesson multiple times in different ways, but using at least two different ways for students to learn and interact with ideas as you present them. Using at least two ways to present information increases student exposure to content, helping them engage with it multiple ways and deepening their understanding.

**Examples / Variations:**
- Teacher uses gestures to explain ideas, vocabulary words, or actions (e.g. move hands into chest to show "add" and move hands away from body to show "subtract").
- Teacher writes new words from a text on the board, reads them aloud, and shows a picture representing them.
- Teacher shows objects instead of only describing them (e.g. brings in farming tools when teaching about agriculture).
- Teacher demonstrates shutting off the school tap, narrating the steps along the way.

**Reflection prompt:** What is a lesson this week that you could incorporate gestures into?

**Teacher Voice:** "When I explain the same idea in different ways, more of my students are engaged."

---

### AIL_M3_STRAT3 — Offer Multiple Ways to Show Understanding

**Description:** Allow students to show what they know in different ways, like drawing, writing, acting, speaking, building, or gesturing.

**Expanded explanation:** Offering different ways to respond allows each student to reveal what they know. Not all students learn and process information in the same way. Multiple ways of showing understanding may include drawing, speaking, writing, and acting it out. If teachers provide at least two different ways for students to show understanding, it can make a meaningful difference. This supports inclusion and can also bring movement into learning, helping students stay engaged and active. Giving students the opportunity to choose how they respond offers a sense of control and empowerment. When teachers provide choice, students grow in confidence and understand that their best way of learning does not have to match their neighbors'. Offering multiple ways to show understanding does not lower academic expectations — it allows students to meet learning objectives in a way that supports each child's learning style.

**Examples / Variations:**
- Students draw a picture of the main character in the story or write a sentence about their traits.
- Students can choose to work independently or in a small group to complete math word problems.
- Students can act out a new vocabulary word or say the meaning to the whole class.

**Reflection prompt:** How can you offer multiple ways to show understanding in your next lesson?

**Teacher Voice:** "When I give different ways to answer, more students are able to show what they know."

---

### AIL_M3_STRAT4 — Eliminate Barriers Before They Happen

**Description:** Plan ahead to remove challenges that might prevent students from participating.

**Expanded explanation:** In every classroom, some students face barriers that make learning harder. During lesson planning, teachers can ask simple questions to identify these barriers early (e.g. "Can every child use the materials?" or "Is the space safe for all?" or "Are instructions clear for children who speak different home languages?"). These small checks help teachers adjust the lesson before it begins. When barriers are reduced from the start, more students can participate and stay engaged. This also helps lessons run more smoothly, so teachers can focus on teaching instead of reacting to problems. Even with good planning, some challenges may come up during a lesson — when they do, teachers can make adjustments in the moment to support participation and inclusion.

**Examples / Variations:**
- Teacher uses simple, clear instructions (e.g. says the instructions, shows them through pictures, and repeats as needed).
- Teacher lists all materials students will need and gathers them before the lesson starts.
- Teacher plans to go outside for the lesson so students have a safe space to move.
- Teacher pre-selects small groups of students to work together and share materials.
- Teacher prepares local materials (e.g. collects five stones for each student to use during the math lesson).

**Reflection prompt:** What barriers to student engagement might exist in your next lesson?

**Teacher Voice:** "Thinking about possible barriers before I teach saves me time during the lesson."

---

## RECAP

> **[Deliver: 2–3 sentences summarizing key takeaways]**

Today you explored four strategies that make learning accessible for every child: connecting lessons to students' lives, presenting information in multiple ways, offering multiple ways to show understanding, and eliminating barriers before they happen. These strategies do not require redesigning every lesson — small, intentional adjustments are enough to increase participation and belonging for all students. This is the last required module — completing the quiz will unlock three optional deep dives you can explore in any order.

---

## 7. Quiz Questions

> **[Deliver 3 items in order: Q1 recall → Q2 understanding → Q3 application, selecting one item from each question bank below. User must get ≥2 of 3 correct to pass.]**
> **[After each incorrect answer: (1) briefly identify the missed concept, (2) give a 1-sentence explanation of the correct idea, (3) immediately offer one retake using a different item of the same type from the same bank — do not wait for the teacher to ask. NEVER re-ask the original question. At most one retake per item.]**
> **[After a correct answer: give the 1-sentence feedback and move to the next item without offering a retake.]**

> **[ON QUIZ PASS — MANDATORY TRANSITION: Do NOT suggest repeating Module 3 or offer the main menu. Congratulate the teacher in one sentence, then immediately present the Deep Dive options below. This is the only correct next step.]**

> **Deep Dive options (send immediately on quiz pass):**
> Congratulations — you have completed all three core modules! You can now explore three optional deep dives in any order. Which would you like to do first?
> 1. Hands-On Learning with Low-Cost Materials
> 2. Drama, Role Play, and Creative Expression
> 3. Planning an Active Lesson

#### Question 1: Recall

- **Inclusive strategies are only helpful for students who are struggling.**
  - Options: True / False

- **Which teacher action helps reduce barriers for a lesson?**
  - Options: Giving only silent work / Preparing materials / Skipping the lesson objective

- **Which supports different ways to show understanding?**
  - Options: Writing only / Silent work / Drawing and acting it out

#### Question 2: Understanding

- **How does planning ahead help reduce learning barriers?**
  - Keywords: prepared, smoother lesson, reacting after

- **Why is it important to connect learning to real-life?**
  - Keywords: meaningful, community, familiar, reflect student lives, belonging

- **Why does presenting information in multiple ways help students learn?**
  - Keywords: different learners, understanding, confidence, inclusive

#### Question 3: Application

- **Scenario 1:**
  A teacher explains independent work, but some students do not begin the task because they seem confused about what to do. The teacher notices this happens a lot after they give instructions.
  *How could the teacher reduce this barrier before the lesson?*

- **Scenario 2:**
  A teacher is leading a class discussion, but only a small group of confident students are answering questions. Several other students look to the floor and remain silent throughout the lesson.
  *How could the teacher increase participation for all students?*

- **Scenario 3:**
  A teacher is giving a multiplication lesson, but many students seem confused and not engaged. The teacher is only using examples with numbers.
  *How can the teacher make the lesson more meaningful and familiar to students?*

---

## OPTIONAL_ENRICHMENT

> **[Offer only after quiz is passed. Not required for completion.]**

### DIY_ACTIVITY_1: Create the Shape

| Field | Value |
|-------|-------|
| **Time** | ~10 minutes |
| **Materials** | Fabric scraps |
| **Steps** | 1. Collect extra pieces of fabric from the local tailor / 2. Students design, place, and layer fabric to create different shapes / 3. Students name the shapes they made / 4. Class walks around the room to see the different creations |
| **Variation (younger)** | Focus on basic shapes — circle, square, triangle |
| **Variation (older)** | Create simple or complex composite shapes |
| **Observation** | Students use local materials to explore and understand shapes |

### DIY_ACTIVITY_2: What Happens Next?

| Field | Value |
|-------|-------|
| **Time** | ~10 minutes |
| **Materials** | Slates and chalk (or paper and pen) |
| **Steps** | 1. Share a brief story with the class, but purposefully do not tell the ending / 2. Students draw, write, or act out how they think the story will end / 3. Invite a few students to share their ideas with the whole class / 4. Retell the story and share the original ending / 5. Discuss which ending students liked best |
| **Variation (younger)** | Use a short, simple story |
| **Variation (older)** | Use a more complex, multi-step story |
| **Observation** | Students choose their preferred way to respond, demonstrating understanding and creativity |
