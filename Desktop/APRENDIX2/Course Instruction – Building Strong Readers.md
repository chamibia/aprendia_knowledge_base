# Course Instruction – Building Strong Readers

**Course ID:** `READING_COURSE_01`

---

## 1. Course Manifest

| Field | Value |
|-------|-------|
| **Title** | Building Strong Readers |
| **Description** | A sequential, flexible course supporting teachers in crisis-affected and low-resource settings to build confident, joyful readers. Module 1 introduces how reading develops (required) → Module 2 provides practical engagement routines (required) → Deep Dives offer targeted modules on decoding, comprehension, joyful learning, inclusion, and materials. The course balances decoding and meaning, skills and relationships, structure and creativity. Every step is low-prep, inclusive, multi-lingual-aware, and actionable. |
| **Target Experience** | Beginner to intermediate |
| **Target Tech Literacy** | Low to medium |
| **Teaching Context** | Crisis-affected, low-resource |
| **Typical Class Size** | 40–100 students |
| **Known Constraints** | Limited books, multilingual classrooms, limited teacher training, low prep time |

### Learning Objectives

- Teach reading as meaning-making: Move beyond memorization toward understanding.

- Build decoding foundations: Strengthen sound-letter connections and blending strategies.

- Increase participation: Use interactive, predictable routines that reduce stress.

- Support multilingual learners: Bridge familiar languages and language of instruction.

- Foster joy and confidence: Help every child see themselves as a reader.

### Pedagogical Frame

Reading is both cognitive and relational. Strong readers grow through structured decoding practice, oral language development, meaningful comprehension, and emotionally safe classrooms. This course emphasizes:

- Predictable routines

- Modeling thinking

- Active participation

- Low-cost materials

- Identity-affirming instruction

### Design Scope

- **Includes:** phonemic awareness, phonics, fluency, vocabulary, comprehension, multilingual scaffolds, joyful pedagogical practices, low-cost materials strategies
- **Excludes:** advanced literary analysis, formal reading assessments, national curriculum sequencing

### Microlearning Contract

| Constraint | Value |
|------------|-------|
| Per-interaction time cap | 90–120 seconds |
| Module 1 total | ≤12 minutes |
| Module 2 total | ≤12 minutes |
| Deep Dives total | ≤10–12 min each |
| Input types | Buttons, short text (≤25 words), quick polls, slate/notebook prompts |
| Message limit | 2 bot turns per anchor (teach → tiny action/reflection/quiz) |
| End-of-module quiz (Core & Deep Dives) | 3 items: recall → understanding → application; pass = 2 of 3; 1 retake per item; see **§3** (End-of-module quizzes) and system prompt §9 |

### Tone Guidance

Affirming, clear, practical. Avoid reading jargon. Normalize mixed reading levels. Emphasize progress over speed. Celebrate effort. Echo teachers' language back when possible.

### AI Guidance Notes

- **Concepts vs Strategies:** Module content includes both **concepts** (e.g. "Reading is more than decoding") and **strategies** (e.g. "Daily Picture Talk"). **Concepts are for AI reference only—do NOT show them to the user.** Use concepts to guide tone, emphasis, and framing. **Strategies are what users see**—deliver them through examples, stories, and actions. Never present concepts as separate content or labels.

- Never suggest speed-based competition

- Avoid memorization-only approaches

- Avoid shaming struggling readers

- Encourage ongoing, quiet observation of student skills by the user

- Always offer no-material variant

- After 2 short reflections, prompt: “Want to hear a teacher’s example?”

## 2. Course Onboarding (Reading Course Only)

> **CRITICAL:** These 3 questions apply **ONLY** when the user has selected Building Strong Readers **and** general onboarding (from `onboarding-agent.md`) is complete. Do **NOT** ask these during general onboarding. Do **NOT** ask these if the user selected a different course.

At the start of Building Strong Readers (Module 1), ask only these 3 short questions. **Ask them one at a time, in order — never combine two or more into a single message.** Wait for the teacher's response to each question before asking the next. Store responses as structured tags for personalization and linguistic adaptation. Responses will be used to:

- Adapt examples to the language of instruction

- Suggest appropriate Deep Dive modules

- Adjust routines based on available materials

- Provide multilingual scaffolds when needed

required onboarding questions:

1. What language do most of your students use when speaking in the classroom? (store as: primary_spoken_language)

2. What language are students learning to read during reading lessons (language of instruction)? (store as: language_of_instruction)

3. What types of reading teaching materials are available in your classroom? (button-based options: none / a few textbooks / textbooks for every student / a few storybooks / a library of storybooks) (store as: reading_materials_available)

Onboarding design principle:

onboarding must:

- ask one question at a time — **never send Q1, Q2, and Q3 together in the same message**, even though all 3 are part of the same short onboarding flow

- be short (≤90 seconds)

- use button-based responses where indicated

- avoid technical language

- not burden teachers with linguistic terminology

- quietly power personalization through inference

---

## 3. Level Structure & Unlock Rules

> **IMPORTANT:** Pathways (`module_arc`) are pre-assigned per module below. The AI reads these assignments from module metadata — it does not infer pathways from user signals.

**Structure overview:**
- **Core modules (required):** Module 1, Module 2 — must be completed in order
- **Deep Dives (optional):** Modules 3–7 — unlock after Module 2; can be completed in any order

### End-of-module quizzes (system prompt §9)

Align all mini-quiz behavior with **`system_prompt.md` §9**, **`quiz_rationale.md`**, and **`example_quiz_questions.md`**.

| Rule | Detail |
|------|--------|
| **Structure** | **3 items** per module: **Q1 recall** (MC/TF) → **Q2 understanding** (open-ended; hidden keywords) → **Q3 application** (scenario) |
| **Pass module / unlock** | **≥2 of 3** correct; up to **1 retake per item** (new question, same type, alternate item bank — **NEVER re-ask the original question**) |
| **Course pass / explain** | **≥80%** of all quiz items in the **course** (see system prompt; `course_pass_threshold` in module YAML) |
| **Module YAML** | `quiz_pass: 2_of_3` and `course_pass_threshold: 0.80`. Legacy `quiz_threshold: 0.80` = course-level only, not the per-module bar. |
| **Key Concepts in modules** | For agent delivery only; **not** for quiz stem copy (§9). |

### Module 1 – How We Learn to Read (Core)  
- module_id: READING_M1_HWLR  
- module_arc: steady_arc  
- purpose: foundation understanding of how reading develops; must complete to unlock Module 2  
- time: ≤ 12 minutes total  
- bot_behavior:

1. Load steady_arc pathway at module start  
2. Introduce module: “Reading is more than saying words. It connects sounds, print, and meaning.”  
3. Deliver each strategy in fixed order:

   - picture talk

   - sound awareness warm-ups

   - blending & segmenting

   - link words to meaning

   - mini shared writing

4. For each strategy:

   - teach (≤60s): explanation + 1 localized example (adapted to language_of_instruction)

   - Do (≤60s): tiny classroom action OR 1-item check

5. Deliver mini quiz (3 items, auto-scored, recall → understanding → application) → pass = ≥2 of 3; if not passed → one retry with alternate item bank; course-level % rules in system prompt §9

   - True/False: Reading is only saying words correctly.

   - Multiple choice: Oral language helps reading because it builds (A: speed / B: vocabulary & understanding / C: handwriting)

   - Open-ended: Why are blending and segmenting important for readers?

**Module 2 - Making Reading Engaging & Inclusive**  
- module_id: READING_M2_MREI  
- module_arc: steady_arc  
- purpose: build teacher awareness that engagement and emotional safety increase reading participation and comprehension; unlocks Deep Dives  
- time: ≤ 12 minutes total  
- bot_behavior:

1. Load steady_arc pathway at module start  
2. Introduce module: “A few students volunteer to read, while many stay silent. Engagement and emotional safety change that.”  
3. Deliver each strategy in fixed order:

   - picture walks

   - shared reading & finger tracking

   - echo → choral → independent

   - thinking aloud

   - peer discussion

4. For each strategy:

   - teach (≤60s): explanation + 1 localized example (adapted to language_of_instruction)

   - Do (≤60s): tiny classroom action OR 1-item check

5. Deliver mini quiz (3 items, auto-scored, recall → understanding → application) → pass = ≥2 of 3; if not passed → one retry with alternate item bank; course-level % rules in system prompt §9

   - Multiple choice: Why is choral reading helpful? (A: builds speed only / B: confidence & fluency / C: saves time)

   - True/False: Thinking aloud helps students see how comprehension works.

   - Open-ended: How can peer discussion increase participation in your classroom?

---

### Deep Dives (M3–M7)

> **IMPORTANT:** Modules 3–7 are **Deep Dives**. They unlock simultaneously after Module 2 completion. The user may complete them in any order. Present the Deep Dive options after Module 2 so the user can choose which to do first. This is a distinct list from the Main Menu — never call it a "menu."

| Module ID | Name | Pathway | Time | Completion |
|-----------|------|---------|------|------------|
| `READING_M3_BBWR` | Building Blocks of Word Reading | `steady_arc` | ≤12 min | Mini-quiz: ≥2 of 3 (1 retry) |
| `READING_M4_MMVFC` | Making Meaning with Vocabulary, Fluency, and Comprehension | `empathy_arc` | ≤12 min | Mini-quiz: ≥2 of 3 (1 retry) |
| `READING_M5_CJHRE` | Creating Joyful & Healing Reading Experiences | `empathy_arc` | ≤12 min | Mini-quiz: ≥2 of 3 (1 retry) |
| `READING_M6_SAL` | Supporting All Learners | `steady_arc` | ≤12 min | Mini-quiz: ≥2 of 3 (1 retry) |
| `READING_M7_TMRI` | Texts & Materials for Reading Instruction | `empathy_arc` | ≤12 min | Mini-quiz: ≥2 of 3 (1 retry) |

**Unlock:** All Deep Dives unlock after Module 2 completion (no fixed order between M3–M7)

**Completion per Deep Dive:** Mini-quiz: ≥2 of 3 to pass; one retry with alternate item bank. Course completes when all required modules and selected Deep Dives are done. Course-level % rules: system prompt §9.

---

### Module 3 – Deep Dive: Building Blocks of Word Reading  
- module_id: READING_M3_BBWR  
- module_arc: steady_arc  
- purpose: strengthen decoding foundations and word-reading skills  
- time: ≤ 12 minutes total  
- bot_behavior:

1. Load steady_arc pathway at module start  
2. Introduce module: “Strong readers can break words into parts and put them back together.”  
3. Deliver each strategy in fixed order:

   - help children hear sounds in language (phonological awareness)

   - connect sounds to letters (phonics)

   - model blending & segmenting (phonics)

   - teach how print works (print concepts, oral language)

   - word building with manipulatives

6. For each strategy:

   - adapt example automatically based on inferred language structure (phoneme-based, syllable-based)

   - teach (≤60s): explanation + 1 localized example (adapted to language_of_instruction)

   - Do (≤60s): tiny classroom action OR 1-item check

7. Deliver mini quiz (3 items, auto-scored, recall → understanding → application) → pass = ≥2 of 3; if not passed → one retry with alternate item bank; course-level % rules in system prompt §9

   - True/False: Sound games require printed books.

   - Multiple choice: Decoding helps students (A: memorize words / B: read new words independently / C: read faster only)

   - Open-ended: Why is understanding sound and language important for reading?

**Module 4 – Deep Dive: Making Meaning with Vocabulary, Fluency, and Comprehension**  
- module_id: READING_M4_MMVFC  
- module_arc: empathy_arc  
- purpose: deepen teacher understanding of vocabulary, and comprehension as meaning-making  
- time: ≤ 12 minutes total  
- bot_behavior:

1. Load empathy_arc pathway at module start  
2. Introduce module with vignette: “Students read the passage correctly, but when asked what it means, they look confused”  
3. Poll: “Is this something that happens in your classroom?” (A: This happens often / B: Sometimes / C: Rarely)  
4. Provide brief reflection based on response  
5. Deliver each strategy in fixed order:

   - teach new words in context (vocabulary)

   - use retelling to check understanding (comprehension)

   - build fluency through weekly text studies (fluency)

   - ask good questions (comprehension)

   - use familiar languages and background knowledge

6. For each strategy:

   - scenario prompt (classroom moment story)

   - teacher reflection or quick poll

   - strategy insight

   - mini-check or micro-action

   - if multilingual classroom is inferred → include brief home-language bridge suggestion

7. Deliver mini quiz (3 items, auto-scored, recall → understanding → application) → pass = ≥2 of 3; if not passed → one retry with alternate item bank; course-level % rules in system prompt §9

   - Multiple choice: Fluency supports (A: speed only / B: comprehension / C: handwriting)

   - True/False: Asking deeper questions helps students think beyond the text.

   - Open-ended: Give one example of a question that helps students think more deeply about a story.

**Module 5 – Deep Dive: Creating Joyful & Healing Reading Experiences**  
- module_id: READING_M5_CJHRE  
- module_arc: empathy_arc  
- purpose: foster joyful, identity-affirming, and healing lessons  
- time: ≤ 12 minutes total  
- bot_behavior:

1. Load empathy_arc pathway at module start  
2. Introduce module with vignette: “A student who rarely speaks smiles when a story includes a character from her community.”  
3. Poll: “Is this something you’ve seen in your classroom?” (A: I’ve seen this / B: I’m not sure / C: I haven’t tried this)  
4. Provide brief reflection based on response  
5. Deliver each strategy in fixed order:

   - make reading aloud expressive & interactive

   - create a class story together

   - invite creative expression

   - choose questions that reflect children’s world

   - reader’s theater

6. For each strategy:

   - scenario prompt (classroom moment story)

   - teacher reflection or quick poll

   - strategy insight

   - mini-check or micro-action

   - emphasize participation over perfection throughout

7. Deliver mini quiz (3 items, auto-scored, recall → understanding → application) → pass = ≥2 of 3; if not passed → one retry with alternate item bank; course-level % rules in system prompt §9

   - Multiple choice: Why include local names or settings in stories? (A: for speed only / B: for relevance & fun / C: to simplify text)

   - True/False: Participation is more important than perfect reading.

   - Open-ended: What is a topic children can create their own stories about in an upcoming lesson?

**Module 6 - Deep Dive: Supporting All Learners**  
- module_id: READING_M6_SAL  
- module_arc: steady_arc  
- purpose: support multilingual learners and those with varied reading levels  
- time: ≤ 12 minutes total  
- bot_behavior:

1. Load steady_arc pathway at module start  
2. Introduce module: “Every classroom includes learners at different levels. Strong teachers plan for all of them.”  
3. Deliver each strategy in fixed order:

   - teach skills in different ways

   - use quick checks

   - focus groups

   - support language use

   - use peer support

4. For each strategy:

   - if primary_spoken_language ≠ language_of_instruction → elevate bridging suggestions

   - teach (≤60s): explanation + 1 localized example

   - Do (≤60s): tiny classroom action OR 1-item check

5. Deliver mini quiz (3 items, auto-scored, recall → understanding → application) → pass = ≥2 of 3; if not passed → one retry with alternate item bank; course-level % rules in system prompt §9

   - True/False: Quick checks should be long and graded.

   - Multiple choice: Giving choice helps students feel (A: confused / B: capable / C: controlled)

   - Open-ended: How can making connections between languages support reading development?

**Module 7 - Deep Dive: Texts & Materials for Reading Instruction**  
- module_id: READING_M7_TMRI  
- module_arc: empathy_arc  
- purpose: maximize reading instruction using limited materials  
- time: ≤ 12 minutes total  
- bot_behavior:

1. Load empathy_arc pathway at module start  
2. Introduce module with vignette: “A teacher has only one worn book to share with 40 students, but her class keeps finding new things to notice each time they open it.”  
3. Poll: “Is this something that happens in your classroom?” (A: This happens often / B: Sometimes / C: Rarely)  
4. Provide brief reflection based on response  
5. Deliver each strategy in fixed order:

   - one text, four ways

   - class decodable sentences

   - environmental print hunt

   - create letter/word cards

   - let children be authors

6. For each strategy:

   - scenario prompt (classroom moment story)

   - teacher reflection or quick poll

   - strategy insight

   - mini-check or micro-action

   - personalize examples based on materials_available; if primary_spoken_language ≠ language_of_instruction → elevate bridging suggestions

7. Deliver mini quiz (3 items, auto-scored, recall → understanding → application) → pass = ≥2 of 3; if not passed → one retry with alternate item bank; course-level % rules in system prompt §9

   - Multiple choice: Environmental print includes (A: store signs / B: food labels / C: newspapers / D: all of the above)

   - True/False: Re-reading a short text builds fluency and comprehension.

   - Open-ended: How could you use one short text across several days of reading instruction?

## **4. Personalization & Routing Rules**

> **Note:** These signals drive example selection, bridging emphasis, and Deep Dive suggestions — **NOT** pathway/arc selection (pathways are pre-assigned; see §3).

The bot should continuously track and update:  
- primary_language_spoken  
- language_of_instruction  
- materials_available  
- prior_completion

- quiz_gaps

- anchor_performance

- reflection_length

language bridging logic: 

If primary_language_spoken ≠ language_of_instruction:

- emphasize oral language bridging (Modules 1, 4, 6\)

- encourage think-pair-share in familiar language before whole-class responses

- provide sentence frames for sharing in the language of instruction

- normalize translanguaging (brief home-language processing → school-language output)

If primary_language_spoken \= language_of_instruction:

- emphasize vocabulary depth, fluency, and comprehension questioning

- reduce explicit bridging scaffolds unless requested

inferring language structure from language of instruction:

The bot should infer how reading is typically taught based on language_of_instruction.

If the language is primarily alphabetic (e.g. English, French, Spanish, Hausa):

- emphasize phoneme awareness and blending

- use sound-letter decoding examples

- model segmenting and blending explicitly

If the language is more syllable-based in early instruction (e.g. Swahili, Bantu languages, Arabic, Amharic):

- emphasize using phonemes to read syllables, then blending syllable units together to read words

- emphasize syllable clapping and chunking

Teachers are NOT asked to identify the language structure.

The system infers instructional approach from the language_of_instruction named.

inferring directionality:

The bot infers reading direction from language_of_instruction and automatically:

- adjusts finger-tracking examples

- adjusts print-concept modeling (start point, movement direction)

- avoids left-to-right assumptions as examples

Teachers are NOT asked about directionality directly.

materials-based routing:

If reading_materials_available \= “none” or “a few textbooks”:

- recommend modules 3 and 7 after completion of modules 1 → 2

- default examples to board-based shared texts

- emphasize environmental print, shared writing, and student-created texts

If “a few storybooks”:

- emphasize repeated read alouds and weekly text studies

If “library of storybooks”:

- emphasize comprehension questioning, fluency growth, and varied response formats

deep dive suggestion logic:

After Module 2 completion, suggest Deep Dives based on signals

- decoding quiz gaps → suggest Module 3

- comprehension quiz gaps → suggest Module 4

- engagement reflections → suggest Module 5

- multilingual indicators → suggest Module 6

- limited materials indicators → suggest Module 7

Deep Dive options should display only incomplete Deep Dive modules

## **5. Module Construction Schema**

A module uses ONE arc for its entire strategy sequence. The arc is pre-assigned in the module metadata. The agent must load the arc at module start, follow its flow consistently for every strategy, and maintain the same interaction rhythm until the mini-quiz.

See `global_pathway_instructions.md` for full arc delivery specifications. Course-specific notes below.

| Arc | Flow Summary |
|-----|-------------|
| `steady_arc` | Introduction → for each strategy: explanation + 1 localized example → brief reflection or micro-action → [repeat] → mini-quiz |
| `empathy_arc` | Vignette intro + poll → brief reflection → for each strategy: vignette continues → reflection/poll → strategy insight → micro-action → story debrief → mini-quiz |

**Course-specific requirements:**

- Every module must have a clear title and metadata, including its pre-assigned `module_arc`
- Adapt examples to `language_of_instruction` and `reading_materials_available`
- Respect microlearning constraints: ≤12 minutes per module
- Include the 3-item mini-quiz (≥2 of 3 to pass; see system prompt §9)
- Do not mix arc structures within a module

## **6. Assessments & Unlocks**

- Module 1 unlock → Module 2: 3-item quiz (≥2 of 3); one retry with alternate item bank

- Module 2 unlock → Deep Dives: 3-item quiz (≥2 of 3); one retry

- Deep Dive completion: completion is modular; no fixed order. Mark a deep dive “complete” when 3-item mini-quiz is passed (≥2 of 3); if not passed → 1 retry with alternate item (see `quiz_rationale.md`); if still not passed → offer review recap

- **Summative Quiz:** Offer proactively when all seven modules are confirmed complete (`READING_M1_HWLR`, `READING_M2_MREI`, `READING_M3_BBWR`, `READING_M4_MMVFC`, `READING_M5_CJHRE`, `READING_M6_SAL`, `READING_M7_TMRI`). Follow `summative_quiz_building_strong_readers.md` exactly. **Do not offer until all seven modules are done.**

### Summative Quiz Rules

- **Source of truth:** `summative_quiz_building_strong_readers.md` — load and follow it in full.
- **8 questions**, fixed sequence: Q1–Q2 Recall → Q3–Q4 Understanding → Q5–Q6 Application → Q7 Observation (image) → Q8 Best Practice.
- **This is not a module quiz.** The module quiz rules from §9 of the system prompt (3 items, recall → understanding → application cycle) do NOT apply. The summative has its own delivery rules, scoring, and retake logic defined in its file.
- **Scoring:** 7–8 of 8 = pass; 5–6 of 8 = 1 shortened retry (4 questions, pass = 3–4 of 4); 0–4 of 8 = Review & Choice (warm review → teacher acknowledges → choice of retaking the course or a fresh 8-question quiz). Never state a score, fraction, or percentage to the teacher.
- **Q7 requires an image.** Send the image before asking the observation question. Do not skip Q7.
- **Q8 is Best Practice**, not Application. Do not label or treat Q8 as an Application question.

scoring principles:

- auto-score objective items

- open-ended responses are pattern-matched for conceptual keywords

- feedback must: affirm effort first; clarify misconception second; avoid evaluative tone

## **7. Safety/Feasibility Constraints**

instructional constraints:

- never require printed worksheets; electricity; internet in classroom; individual student textbooks (unless indicated in reading_materials_available)

- always offer no-material variant (oral, air writing, board-based); compact movement alternatives (no roaming required)

pedagogical safety:

- treat multilingualism as an asset

- never discourage use of familiar language for thinking

- encourage short scaffolded transitions into language of instruction

- avoid assuming English-based phonics rules apply universally

- encourage observation of student skills that is quiet and private

emotional safety:

- normalize mixed reading levels

- frame reading growth as developmental

- encourage celebration of small progress

- avoid deficit framing (“weak readers,” “behind,” etc)