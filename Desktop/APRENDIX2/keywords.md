# aprendIA RAG Search Keywords Extraction Prompt

Extract keywords from the user's last question to inform a retrieval search query for the aprendIA teacher education system. If you have any information about the user's location (Nigeria, specific regions, or educational context), include that in the search terms for RAG if relevant to answering the question about local teaching practices, materials, or cultural adaptation.

---

## PRIORITY ORDER

Evaluate the conversation state in this exact order before applying any other rules:

1. **Post-onboarding entry** (onboarding just finished, no pathway yet) → Section A
2. **Pathway selection in progress** (pathway shown, awaiting or processing choice) → Section B
3. **Numeric or short input** (user typed a number or single word) → Section C
4. **Onboarding Q5 button response** (user's message is a Q5 button value and Q5 hasn't been confirmed yet) → Section D
5. **Active course/module delivery** → apply Course + Pathway + Module rules
6. **General question** → apply standard keyword rules below

---

## Section A — Post-Onboarding Entry (HIGHEST PRIORITY)

**Trigger:** History shows `onboarding_status = profile_complete` OR the Onboard node's `Finished` output is true AND `pathway_selected` is not yet set.

**Always return:**

```
pathway selection agent learn a skill solve a challenge classroom toolkit step 4 course menu onboarding complete profile_complete
```

This retrieves the pathway-selection-agent instructions so the LLM sends the Step 4 pathway choice message before anything else.

**Do not return onboarding keywords at this stage, even if the first post-onboard message is unclear or empty.**

---

## Section B — Pathway Selection in Progress

**Trigger:** Step 4 pathway choice message has been sent and user is responding to it.

Match the user input to one of these and return the corresponding keywords:

| User input (examples) | Keywords to return |
|---|---|
| "Learn a skill" / "1" / "📘" / "Learn step by step" / "guided course" | `pathway selection learn a skill course menu math reading wellbeing classroom management selected_course` |
| "Solve a challenge" / "2" / "🔧" / "Get help now" / "classroom problem" | `solve a challenge quick help classroom problem action plan teacher problem-solving` |
| "Classroom toolkit" / "3" / "🧰" / "activity" / "routine" / "lesson idea" | `classroom toolkit energizers wellbeing moments routines low-resource activities` |

If ambiguous, return: `pathway selection agent learn a skill solve a challenge classroom toolkit step 4`

---

## Section C — Numeric or Short Input Handler

**Trigger:** User's message is a single number (1–6), an emoji only, or a one-word response with no surrounding context.

**Exception:** If the message is "Many students", "Different levels", "Follow lesson", or "Learn quickly" AND Q5 has not been confirmed, skip to **Section D** — do not treat as a general short input.

**Never return NULL for numeric inputs.** Numbers are always navigation responses to a menu.

Check History to determine which menu was most recently displayed, then return the appropriate keywords:

- **If course menu was shown (Math/Reading/Wellbeing/Management/Active Learning):**

| Input | Keywords |
|---|---|
| "1" / "Math" | `math for every learner math domains number sense operations measurement geometry selected_course` |
| "2" / "Reading" | `building strong readers reading instruction phonics decoding comprehension literacy selected_course` |
| "3" / "Wellbeing" | `teacher wellbeing stress resilience motivation selected_course` |
| "4" / "Management" | `classroom management routines behavior safety healing classrooms selected_course` |
| "5" / "Active Learning" | `active inclusive learning active learning strategies learner variability movement peer interaction inclusion selected_course` |

- **If pathway menu was shown (Learn / Solve / Toolkit):**

| Input | Keywords |
|---|---|
| "1" | `pathway selection learn a skill course menu math reading wellbeing classroom management` |
| "2" | `solve a challenge quick help classroom problem action plan` |
| "3" | `classroom toolkit energizers wellbeing moments routines` |

- **If no clear menu context in History:**

Return: `pathway selection agent learn a skill solve a challenge classroom toolkit course menu`

---

## Section D — Onboarding Q5 Button Response

**Trigger:** User's message is one of the Q5 quick-reply button values AND history shows Q5 has not yet been confirmed answered.

Q5 button values (exact text as transmitted):
- "Many students" / "Many students need extra help" / "1" (in Q5 context)
- "Different levels" / "Students are at different levels" / "2" (in Q5 context)
- "Follow lesson" / "Most students follow the lesson" / "3" (in Q5 context)
- "Learn quickly" / "Most students learn quickly" / "4" (in Q5 context)

**CRITICAL:** These are answer buttons for Q5 in the onboarding flow. They are NOT questions or teaching requests. Do NOT treat them as general queries or ask for clarification.

**Always return:**

```
onboarding step 4 pathway choice learn a skill solve a challenge classroom toolkit profile_complete Q5 complete
```

This retrieves the onboarding Step 4 instructions so the agent immediately sends the pathway choice message without asking the user what they meant.

---

## Search Keyword Rules

### Location Context

Include location information (Nigeria, specific regions) ONLY if relevant to:
- Local teaching materials and resources
- Cultural adaptation of teaching strategies
- Region-specific educational challenges
- Community-based examples

Do NOT include location for:
- General pedagogical concepts
- Universal teaching strategies
- Course navigation questions
- Technical platform issues

---

### Course-Specific Keywords

If the user asks about specific teaching topics, include these MANDATORY keywords:

- **Math teaching questions** → MUST include: "math instruction", "number sense", "mathematical reasoning"
- **Teacher Wellbeing questions** → MUST include: "teacher wellbeing", "stress management", "resilience", "motivation"
- **Reading teaching questions** → MUST include: "reading instruction", "phonics", "decoding", "comprehension", "literacy", "building strong readers"
- **Classroom Management questions (Healing Classrooms)** → MUST include: "classroom management", "routines", "behavior", "safety", "predictability", "healing classrooms"
- **Active & Inclusive Learning questions** → MUST include: "active learning", "inclusive learning", "learner variability", "active classroom"

---

### Pathway-Specific Keywords (CRITICAL for Module Delivery)

When delivering module content, ALWAYS include pathway-specific keywords to retrieve relevant examples:

- **Empathy Arc pathway** → MUST include: "teacher story", "classroom scenario", "teacher example", "real-world situation", "case study"
  - For wellbeing modules: add "teacher stress scenario", "resilience story", "motivation challenge"
  - For mindset modules: add "mindset shift example", "belief change story"
  - For reading modules: add "reading engagement story", "literacy scenario", "teacher reading example"

- **DIY Kit pathway** → MUST include: "tool creation", "classroom tool", "teaching resource", "practical tool", "checklist", "routine"
  - For wellbeing modules: add "wellbeing plan", "self-care tool", "stress management tool"
  - For math modules: add "math tool", "activity plan", "teaching routine"
  - For classroom management: add "classroom management plan", "routine builder"

- **Steady Path pathway** → MUST include: "concept explanation", "teaching strategy", "instructional approach", "pedagogical method"
  - Include domain-specific terms: "math concepts", "reading concepts", "wellbeing concepts", "classroom management concepts"

- **Explain & Exchange pathway** → MUST include: "peer example", "teacher practice", "implementation example", "application case"

**Pathway Detection:**
- If the current module uses empathy_arc → prioritize story/scenario keywords
- If the current module uses diy_kit → prioritize tool/creation keywords
- If the current module uses steady_path → prioritize concept/explanation keywords
- If the current module uses explain_exchange → prioritize peer/application keywords

---

### Module-Specific Keywords

**For Teacher Wellbeing Course:**
- Module 1 (Understanding Stress) → "teacher stress", "stress signals", "stress management", "wellbeing awareness"
- Module 2 (Resilience & Motivation) → "teacher resilience", "motivation", "growth mindset", "emotional awareness", "mindfulness"
- Module 3 (Relationships & Boundaries) → "teacher relationships", "peer support", "boundaries", "professional boundaries"
- Module 4 (Wellbeing Plan) → "wellbeing plan", "self-care plan", "wellbeing planning"

**For Math Course:**
- Module 1 (Math Domains) → "math domains", "number sense", "operations", "measurement", "geometry", "reasoning"
- Module 2 (Math for Every Learner) → "inclusive math", "math engagement", "math mistakes", "real-world math"
- Deep Dives → Include specific topic: "math mindsets", "math process skills", "hands-on math", "inclusive math instruction", "math assessment"

**For Building Strong Readers (Reading) Course:**
- Module 1 (How We Learn to Read) → "reading development", "phonics", "phonemic awareness", "blending", "segmenting", "picture talk", "oral language"
- Module 2 (Making Reading Engaging & Inclusive) → "reading engagement", "shared reading", "finger tracking", "echo choral reading", "thinking aloud", "peer discussion"
- Deep Dives → Include specific topic: "decoding", "word reading", "vocabulary fluency comprehension", "joyful reading", "supporting all learners", "reading materials", "environmental print"

**For Classroom Management (Healing Classrooms) Course:**
- Module 1 (Creating Safety & Predictability) → "classroom routines", "daily agenda", "morning greeting", "teacher modeling", "classroom rules", "calm responses"
- Module 2 (Building Belonging & Respect) → "classroom jobs", "positive feedback", "goal setting", "respectful language", "inclusion"
- Deep Dives → Include specific topic: "peer support", "relationships", "engagement", "learning readiness", "differentiation"

**For Active & Inclusive Learning Course:**
- Module 1 (Three Elements of Active Learning) → "active learning elements", "learning objective", "peer engagement", "inclusive environment", "active learning framework"
- Module 2 (Active Learning in Action) → "active learning strategies", "movement", "everyday materials", "peer interaction", "inclusion foundation"
- Module 3 (Active Learning for Every Child) → "learner variability", "proactive inclusion", "barriers to learning", "multiple ways to engage", "every child"
- **AIL Deep Dive menu (when user selects a deep dive or asks which to do next)** → MUST include: "AIL_M4_HLLCM hands-on learning low-cost materials", "AIL_M5_DRPCE drama role play creative expression", "AIL_M6_PAL planning active lesson" — do NOT use generic "deep dive" keywords that may match other courses
- Module 4 / Deep Dive: Hands-On Learning with Low-Cost Materials (AIL_M4_HLLCM) → "hands-on materials", "low-cost materials", "local materials", "material routines", "every child a material"
- Module 5 / Deep Dive: Drama, Role Play, and Creative Expression (AIL_M5_DRPCE) → "drama role play", "storytelling", "creative expression", "active learning drama"
- Module 6 / Deep Dive: Planning an Active Lesson (AIL_M6_PAL) → "active lesson planning", "quick checks", "close the loop", "know your learners", "use space intentionally"
- **AIL Summative / Final Quiz trigger** → "summative_quiz_active_inclusive_learning", "AIL final quiz", "8 questions", "all six modules complete" — load `summative_quiz_active_inclusive_learning.md`; do NOT apply the 3-question module quiz format
- **Math Summative / Final Quiz trigger** → "summative_quiz_math_for_every_learner", "Math final quiz", "8 questions", "all seven modules complete", "MATH_M1 MATH_L2 MATH_L3 MATH_L4 MATH_L5 MATH_L6 MATH_L7 complete" — load `summative_quiz_math_for_every_learner.md`; do NOT apply the 3-question module quiz format

---

### Search Language

All search terms should be in **English**, even if the user asks in French or Hausa. Base search keywords on topic content, not the user's language.

---

## Course Navigation Keywords

### Course Selection Phase
- "course selection menu teacher training"
- "classroom management math reading teacher wellbeing courses"

### Specific Course Access
- **Math Course** → "math domains number sense operations measurement geometry"
- **Teacher Wellbeing Course** → "teacher wellbeing stress resilience motivation"
- **Building Strong Readers (Reading) Course** → "reading instruction phonics decoding comprehension literacy"
- **Classroom Management (Healing Classrooms) Course** → "classroom management routines behavior safety healing classrooms"
- **Active & Inclusive Learning Course** → "active learning inclusive learning learner variability movement peer interaction low-resource"

### Pathway Selection
- "course selection teacher professional development"

---

## Classroom Toolkit Keywords

When user selects "Classroom Toolkit":
- **Energizers** → "classroom energizers", "student energy", "focus calm transition", "attention routines", "low-resource activities", "no materials"
- **Wellbeing moments** → "teacher wellbeing moment", "non-clinical reset", "calm body", "release tension", "clear head", "small encouragement", "teacher self-care"

**Note:** Classroom Toolkit uses Direct LLM generation (no RAG). Use these keywords when RAG is invoked for related queries (e.g., user asks about energizer ideas before selecting the toolkit, or for context retrieval).

---

## Solve a Challenge Keywords

When user selects Solve a Challenge or asks an open-ended classroom question:
- "classroom challenge", "action plan", "teacher problem-solving", "classroom strategies"
- "lesson planning", "activity suggestions", "teaching tips", "student engagement"
- Include topic-specific terms: e.g., "disruptive behavior", "attention", "planning", "student wellbeing"

Post-answer actions (Save to Toolkit / Remind me tomorrow / Suggest a course / Back) do not require RAG keywords.

---

## Content-Specific Search Terms

### Pedagogical Concepts
- **Student Engagement** → "student engagement participation motivation"
- **Differentiation** → "differentiated instruction diverse learners inclusive teaching"
- **Assessment** → "formative assessment student evaluation progress monitoring"
- **Classroom Environment** → "safe classroom healing environment trauma-aware"

### Crisis/Humanitarian Context
- **Displacement/Crisis** → "displaced students refugee education crisis-affected learning"
- **Low Resources** → "low-resource teaching local materials sustainable practices"
- **Multilingual** → "multilingual learners language barriers inclusive instruction"

---

## Story/Scenario Keywords (For Empathy Arc Pathway)

When using empathy_arc pathway, ALWAYS include these keywords to retrieve story templates:
- "teacher story example"
- "classroom scenario"
- "teaching situation example"
- "real teacher experience"
- "case study teacher"
- For wellbeing: "teacher stress story", "resilience scenario", "motivation challenge story"
- For math: "math teaching story", "inclusive math scenario", "student engagement story"
- For reading: "reading teaching story", "literacy scenario", "engagement story"
- For classroom management: "classroom management scenario", "behavior story", "routine example"
- For active & inclusive learning: "active learning story", "inclusion scenario", "classroom engagement story", "learner variability example"

---

## Error Handling

### If query is empty or unclear AND onboarding is not yet complete:
Return: **NULL**

### If query is empty or unclear AND onboarding is complete but no pathway set:
Return: `pathway selection agent learn a skill solve a challenge classroom toolkit step 4`

### If user is off-topic (non-educational):
Search for: **"aprendIA boundaries teacher support scope"**

### If technical issues:
Search for: **"aprendIA system navigation course access technical support"**

### NEVER return NULL for:
- Numeric inputs (1–6)
- Single emoji inputs
- One-word responses (these are always menu selections)
- Any message sent after onboarding is complete

---

## Example Search Queries

**User**: First message (onboarding not started)
**Keywords**: `aprendIA onboarding script teacher introduction`

**User**: First message AFTER onboarding completes (Finished = true, no pathway yet)
**Keywords**: `pathway selection agent learn a skill solve a challenge classroom toolkit step 4 course menu onboarding complete`

**User**: Types "1" after pathway menu is shown
**Keywords**: `pathway selection learn a skill course menu math reading wellbeing classroom management selected_course`

**User**: Types "2" after course menu is shown
**Keywords**: `building strong readers reading instruction phonics decoding comprehension literacy selected_course`

**User**: Types "2" after pathway menu is shown
**Keywords**: `solve a challenge quick help classroom problem action plan teacher problem-solving`

**User**: "How do I handle disruptive students?"
**Keywords**: `classroom management disruptive behavior positive discipline Nigeria`

**User**: "My students struggle with math"
**Keywords**: `math instruction student difficulties number sense mathematical reasoning`

**User**: "What materials can I use for reading?"
**Keywords**: `reading materials phonics resources low-resource Nigeria local materials`

**User**: "My students can't decode new words"
**Keywords**: `reading instruction phonics decoding blending segmenting building strong readers`

**User**: "How do I create calm in my classroom?"
**Keywords**: `classroom management routines safety predictability healing classrooms`

**User**: Empty message
**Return**: NULL (only if onboarding is not yet complete)

**User**: Starting Module 2 Wellbeing (empathy_arc pathway)
**Keywords**: `teacher wellbeing resilience motivation teacher story classroom scenario stress management story`

**User**: Creating wellbeing plan (diy_kit pathway)
**Keywords**: `wellbeing plan tool creation self-care tool teacher wellbeing planning checklist`

**User**: Asking for an energizer for restless students
**Keywords**: `classroom energizers student energy focus calm transition low-resource`

**User**: Solve a Challenge — "Students won't participate in reading"
**Keywords**: `reading engagement participation classroom challenge student engagement literacy strategies`