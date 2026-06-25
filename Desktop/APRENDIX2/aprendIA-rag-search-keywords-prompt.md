# aprendIA RAG Search Keywords Extraction Prompt

Extract keywords from the user's last question to inform a retrieval search query for the aprendIA teacher education system. If you have any information about the user's location (Nigeria, specific regions, or educational context), include that in the search terms for RAG if relevant to answering the question about local teaching practices, materials, or cultural adaptation.

## Search Keyword Rules

### Location Context

- Include location information (Nigeria, specific regions) ONLY if relevant to:
  - Local teaching materials and resources
  - Cultural adaptation of teaching strategies
  - Region-specific educational challenges
  - Community-based examples

- Do NOT include location for:
  - General pedagogical concepts
  - Universal teaching strategies
  - Course navigation questions
  - Technical platform issues

### Course-Specific Keywords

If the user asks about specific teaching topics, include these MANDATORY keywords:

- **Math teaching questions** → MUST include: "math instruction", "number sense", "mathematical reasoning"

- **Teacher Wellbeing questions** → MUST include: "teacher wellbeing", "stress management", "resilience", "motivation"

- **Reading teaching questions** → MUST include: "reading instruction", "phonics", "decoding", "comprehension", "literacy", "building strong readers"

- **Classroom Management questions (Healing Classrooms)** → MUST include: "classroom management", "routines", "behavior", "safety", "predictability", "healing classrooms"

### Pathway-Specific Keywords (CRITICAL for Module Delivery)

**When delivering module content, ALWAYS include pathway-specific keywords to retrieve relevant examples:**

- **Empathy Arc pathway** → MUST include: "teacher story", "classroom scenario", "teacher example", "real-world situation", "case study"
  - For wellbeing modules: add "teacher stress scenario", "resilience story", "motivation challenge"
  - For mindset modules: add "mindset shift example", "belief change story"
  - For reading modules: add "reading engagement story", "literacy scenario", "teacher reading example"
  - These keywords help retrieve story templates and scenario examples for creating engaging empathy_arc content

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

### Search Language

The search keywords for RAG should be based on the topic content, rather than the user's language. All search terms should be in **English**, even if the user asks in French or Hausa.

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

### Pathway Selection

- "course selection teacher professional development"

---

## Classroom Toolkit Keywords

**When user selects Classroom Toolkit or asks about Energizers or Wellbeing moments:**

- **Energizers** → "classroom energizers", "student energy", "focus calm transition", "attention routines", "low-resource activities", "no materials"
- **Wellbeing moments** → "teacher wellbeing moment", "non-clinical reset", "calm body", "release tension", "clear head", "small encouragement", "teacher self-care"

**Note:** Classroom Toolkit uses Direct LLM generation (no RAG) for Energizer and Wellbeing content. Use these keywords when RAG is invoked for related queries (e.g., user asks about energizer ideas before selecting the toolkit, or for context retrieval).

---

## Solve a Challenge Keywords

**When user selects Solve a Challenge or asks an open-ended classroom question:**

- "classroom challenge", "action plan", "teacher problem-solving", "classroom strategies"
- "lesson planning", "activity suggestions", "teaching tips", "student engagement"
- Include topic-specific terms: e.g., "disruptive behavior", "attention", "planning", "student wellbeing"

**Post-answer actions:** Save to Toolkit | Remind me tomorrow | Suggest a course | Back — these do not require RAG keywords.

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

**When using empathy_arc pathway, ALWAYS include these keywords to retrieve story templates:**

- "teacher story example"
- "classroom scenario"
- "teaching situation example"
- "real teacher experience"
- "case study teacher"
- For wellbeing: "teacher stress story", "resilience scenario", "motivation challenge story"
- For math: "math teaching story", "inclusive math scenario", "student engagement story"
- For reading: "reading teaching story", "literacy scenario", "engagement story"
- For classroom management: "classroom management scenario", "behavior story", "routine example"

---

## Error Handling

### If query is empty or unclear:

Return: **NULL**

### If user is off-topic (non-educational):

Search for: **"aprendIA boundaries teacher support scope"**

### If technical issues:

Search for: **"aprendIA system navigation course access technical support"**

---

## Example Search Queries

**User**: "How do I handle disruptive students?"

**Keywords**: "classroom management disruptive behavior positive discipline Nigeria"

**User**: "My students struggle with math"

**Keywords**: "math instruction student difficulties number sense mathematical reasoning"

**User**: "What materials can I use for reading?"

**Keywords**: "reading materials phonics resources low-resource Nigeria local materials"

**User**: "My students can't decode new words"

**Keywords**: "reading instruction phonics decoding blending segmenting building strong readers"

**User**: "How do I create calm in my classroom?"

**Keywords**: "classroom management routines safety predictability healing classrooms"

**User**: First message, any content

**Keywords**: "aprendIA onboarding script teacher introduction"

**User**: Empty message

**Return**: NULL

**User**: Starting Module 2 Wellbeing (empathy_arc pathway)

**Keywords**: "teacher wellbeing resilience motivation teacher story classroom scenario stress management story"

**User**: Creating wellbeing plan (diy_kit pathway)

**Keywords**: "wellbeing plan tool creation self-care tool teacher wellbeing planning checklist"

**User**: Asking for an energizer for restless students

**Keywords**: "classroom energizers student energy focus calm transition low-resource"

**User**: Solve a Challenge — "Students won't participate in reading"

**Keywords**: "reading engagement participation classroom challenge student engagement literacy strategies"
