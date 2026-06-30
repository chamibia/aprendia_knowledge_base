# MODULE: AIL_M1_TTEAL — The Three Elements of Active Learning

## MODULE METADATA

```yaml
module_id: AIL_M1_TTEAL
title: The Three Elements of Active Learning
pathway: steady_arc
duration_target: ≤5 minutes
unlock_requires: null
unlocks: AIL_M2_ALA   # unlocks immediately on reflection response — no quiz
quiz_pass: none        # Module 1 has no quiz; see Course Instruction §Module 1
course_pass_threshold: 0.80
quiz_retry_allowed: false
grade_levels: Primary 1-6
subject: Active and Inclusive Learning
```

---

## LEARNING OBJECTIVES

- Teachers can intentionally plan playful learning experiences with clear learning objectives.
- Teachers can promote active engagement with peers and learning materials.
- Teachers can create a positive classroom environment.

---

## TEACHER MOTIVATIONS & PAIN POINTS

- "I do not have enough materials or resources for activities."
- "I feel pressure to lecture because it seems faster and easier to manage."
- "I have too much content to cover, but I want my students to enjoy learning."
- "I want my students to feel safe and confident enough to join classroom activities."

---

## MODULE RULES

- This module is foundational, ensuring that users can define the three elements of active learning.
- Concepts should be presented linearly and informationally. They are not strategies, but foundational knowledge teachers need to have before doing the subsequent modules.
- Frame active learning as adaptable across subjects and age groups.
- Focus on small shifts that teachers can make immediately.
- Emphasize that active learning can take place in short, simple moments.

---

## DELIVERY INSTRUCTIONS

**Pathway:** `steady_arc`

**⚠️ No mini-quiz for this module.** Module 2 unlocks immediately when the teacher responds to the closing reflection. Do not deliver a quiz.

**Flow:** INTRO → CON1 → CON2 → CON3 → CLOSING REFLECTION → unlock AIL_M2_ALA

**Bot behavior (step by step):**

1. Send intro message: "Before we look at how to make your lessons more active, let's make sure we understand what active learning is. Every active learning lesson has three key elements: **a clear learning objective**, **active engagement with peers and learning materials**, and **a positive and safe learning environment**. We'll go through each one now. This will only take about 5 minutes."
2. Wait for any acknowledgment, then deliver AIL_M1_CON1. Begin with: "**Element 1: A Clear Learning Objective.**" Then deliver the concept content.
3. Wait for any response, then deliver AIL_M1_CON2. Begin with: "**Element 2: Engagement with Peers and Learning Materials.**" Then deliver the concept content.
4. Wait for any response, then deliver AIL_M1_CON3. Begin with: "**Element 3: A Positive and Safe Learning Environment.**" Then deliver the concept content.
5. Ask the closing reflection (see CLOSING REFLECTION section below). Wait for response.
6. Accept any response warmly. Acknowledge in 1–2 sentences. Store response as `weakest_element` signal for Module 2 personalization. Transition: "Let's move on to what this looks like in practice." Unlock Module 2 (AIL_M2_ALA) immediately.

**Chunking rules:**
- One concept per message — never combine
- **After each concept, stop and wait for any user response before sending the next concept. Do not send CON2 in the same turn as CON1, and do not send CON3 in the same turn as CON2.**
- Deliver in order: CON1 → CON2 → CON3
- Do not insert reflection prompts between concepts — one closing reflection only

---

## KEY CONCEPTS

### AIL_M1_CON1 — Concept 1: A Clear Learning Objective

**Description:** Plan and deliver playful learning experiences with clear learning objectives.

**Expanded Explanation:** A clear learning objective gives direction to both teachers and students. It helps ensure that playful activities are connected to meaningful learning instead of becoming participation without purpose. Not all play in the classroom is the same. Free play allows children to explore without a specific goal (e.g. "Today, we will go outside and play football during break"). Active learning uses play purposefully; every game, movement, or activity is designed to guide students toward a specific learning objective (e.g. "Today, we will roam the classroom searching for the hidden letter cards. When you find a letter card, raise your hand and then we will all practice saying the letter sound."). When planning active learning lessons, teachers should create learning objectives to guide and ground purposeful play experiences. Without a clear learning objective, an activity may be enjoyable but not support students' academic growth. With it, even a simple game or movement activity can become a powerful learning experience. Learning objectives do not need to be long or complicated; they are simple "I can…" statements describing what students should be able to do by the end of a lesson or activity (e.g. "I can write the names of the plane shapes" or "I can match the word to the picture card."). Clear objectives can also help teachers think creatively about playful activities that can support student learning, ensuring that a lesson is engaging, age-appropriate, and academically meaningful.

**Examples / Variations:**
- While weekly lesson planning for math, a teacher writes down the lesson objectives for each day of the week. Then they begin creating playful experiences that reflect what students are learning.
- Students practice identifying shapes by sorting everyday objects into groups. The lesson objective is "I can sort objects based on their shape."
- At the beginning of a lesson, a teacher uses the echo-choral-independent strategy to read the lesson objective with the whole class.
- At the end of the lesson, the teacher uses the lesson objective as a quick-check to assess if students understood the lesson (e.g. "Our learning objective was: 'I can solve two-digit addition problems.' Give me a thumbs up if you feel confident in solving these problems, give me a thumbs in the middle if you would like more practice, or give me a thumbs down if you would like to review this with me.").
- A teacher plans a movement activity where students walk around the room, pair with a peer, discuss a question about the shared text, and repeat. The lesson objective is "I can describe the main details of the shared text."

**Reflection Prompt:** What is a clear objective to help students understand the purpose of your next learning activity?

**Teacher Voice:** "When I started planning with a clear learning objective, I noticed students stayed focused and engaged."

---

### AIL_M1_CON2 — Concept 2: Engagement with Peers and Learning Materials

**Description:** Promote interactions with peers and/or materials that allow students to deeply think, discover, and interact during learning.

**Expanded Explanation:** Students learn more deeply when they are actively engaged with content instead of passively listening to information. Active engagement allows students to think, question, practice, discuss, explore, and apply ideas in meaningful ways. Playful learning experiences can help students stay motivated throughout a lesson, strengthening their understanding of a lesson objective. When teachers plan lessons, they should consider activities that connect to the learning objective and allow students to interact with content in creative ways. Engaging activities do not require a lot of time or a lot of resources; they can be short, simple opportunities for participation. Interacting with peers is a way for students to not only build a positive community, but also experience playful learning opportunities. Teachers can gather local resources (e.g. bottle caps, fabric, plastic bottles) as a cost-effective way to increase classroom learning materials. Using movement, question throws, or multiple ways of teaching and responding are also ways for students to become active participants in their learning. When students are engaged in learning, they are able to thrive today and in the future.

**Examples / Variations:**
- Students act out vocabulary words while classmates guess the meaning.
- Students work with a partner to write a simple book for the classroom library corner.
- Students work in small groups to create math word problems, then trade and solve.
- Students work together to make a map of the country out of scraps of fabric.
- Teacher uses plastic bottles for small groups to each plant a tomato seedling; groups water and measure the growth of their plant, then compare and contrast their plant with the other class groups.
- Teacher asks students to bring five stones each for a blending sounds activity.

**Reflection Prompt:** What is one way students could actively interact with materials or peers during your next lesson?

**Teacher Voice:** "When I gave students more opportunities to discuss ideas together, I noticed they were more excited to participate."

---

### AIL_M1_CON3 — Concept 3: Positive and Safe Learning Environment

**Description:** Create and maintain a positive and safe environment that allows students to feel included and confident to participate.

**Expanded Explanation:** Students are more likely to actively participate when they feel emotionally safe and included in the classroom community. Playful and active learning often asks students to share ideas, collaborate with peers, and take risks while learning. A positive classroom environment supports students to feel comfortable participating without fear, embarrassment, or judgment. Teachers play an essential role in creating a safe and supportive classroom environment. Teachers can model respectful interactions, valuing effort, and normalizing mistakes. Using other classroom management tools like greeting students, creating positive classroom rules, and using logical consequences support students to feel supported and safe. When teachers invest in a positive classroom, students will do the same. Classrooms that establish a sense of community have students who are more willing to ask questions, try new ideas, and stay engaged in playful learning.

**Examples / Variations:**
- A class chooses to especially focus on one positive classroom rule a week (e.g. Be a good listener, Raise your hand, Be respectful).
- Teacher praises effort, participation, and collaboration — not just correct answers.
- Teacher offers multiple ways to respond so that students can demonstrate their understanding in their preferred way.
- Teacher uses a closing circle every Friday before dismissal, allowing students to share their favorite part of the week.

**Reflection Prompt:** What is a classroom routine or teacher action that could help students feel safe to participate?

**Teacher Voice:** "When students felt included and respected, they began sharing their thinking more."

---

## CLOSING REFLECTION

> **Agent:** After delivering CON3, ask this question. Wait for the teacher's response before proceeding. Accept any answer warmly — do not score or evaluate.

**Prompt:** "Think about a lesson you taught recently. Which of the three elements do you feel most confident about — and which would you most like to strengthen?"

**On response:**
- Acknowledge warmly in 1–2 sentences (affirm what they named; do not correct or evaluate).
- Store the teacher's answer as `weakest_element` signal for Module 2 personalization (see Course Instruction §3 Personalization & Routing Rules).
- Transition: "Let's move on to what this looks like in practice."
- **Unlock Module 2 (AIL_M2_ALA) immediately.**

