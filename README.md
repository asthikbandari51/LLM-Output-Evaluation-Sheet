
---

## Models Evaluated

| Model | Version | Access Method |
|---|---|---|
| GPT-4o | May 2024 | chat.openai.com |
| Claude 3.5 Sonnet | 2024 | claude.ai |

All responses were collected in **fresh conversation sessions** with no
prior context carried between questions.

---

## Question Set (25 Questions, 5 Categories)

Questions were deliberately chosen to stress-test different model
capabilities:

| Category | # Questions | What It Tests |
|---|---|---|
| Factual/Knowledge | 5 | Accuracy, completeness, avoiding omissions |
| Reasoning/Logic | 5 | Depth of justification, not just correct answers |
| Creative/Open-ended | 5 | Originality, tonal range, emotional resonance |
| Instruction-Following | 5 | Constraint adherence (exact counts, formats) |
| Ethical/Sensitive | 5 | Helpfulness vs. over-cautious deflection |

---

## Scoring Rubric

Each response was scored on **4 dimensions**, each on a **1–5 scale**.

### Accuracy — *Is the information factually correct?*

| Score | Meaning |
|---|---|
| 5 | Fully accurate, no errors or omissions |
| 4 | Mostly accurate, minor omission present |
| 3 | Partially correct, one notable factual error |
| 2 | Mostly incorrect or misleading |
| 1 | Factually wrong or potentially harmful |

### Tone — *Is the tone appropriate for the context?*

| Score | Meaning |
|---|---|
| 5 | Perfect tone — professional, empathetic, or creative as required |
| 4 | Mostly appropriate, slightly off in one place |
| 3 | Neutral but feels robotic or generic |
| 2 | Noticeably wrong tone for the context |
| 1 | Dismissive, inappropriate, or offensive |

### Helpfulness — *Does it actually solve the user's problem?*

| Score | Meaning |
|---|---|
| 5 | Fully addresses the question with actionable clarity |
| 4 | Mostly helpful, minor gap |
| 3 | Answers partially, misses a key aspect |
| 2 | Vague, over-hedged, or deflects with a question instead of answering |
| 1 | Does not help at all |

### Factuality — *Are claims verifiable and grounded?*

| Score | Meaning |
|---|---|
| 5 | All claims are verifiable and traceable |
| 4 | Mostly verifiable, one uncertain claim |
| 3 | Mix of facts and unverifiable assertions |
| 2 | Several hallucinated or unverifiable claims |
| 1 | Fabricated or demonstrably false information |

> **Total Score** = Average of all 4 dimensions (reported to 2 decimal places)

---

## Results Summary

### Overall Average Score (All 25 Questions)

| Model | Avg Score |
|---|---|
| GPT-4o | 4.39 / 5.00 |
| Claude 3.5 Sonnet | 4.44 / 5.00 |

### Average Score by Dimension

| Dimension | GPT-4o | Claude 3.5 |
|---|---|---|
| Accuracy | 4.56 | 4.64 |
| Tone | 4.68 | 4.32 |
| Helpfulness | 4.04 | 4.56 |
| Factuality | 4.28 | 4.52 |

### Average Score by Category

| Category | GPT-4o | Claude 3.5 |
|---|---|---|
| Factual/Knowledge | 4.55 | 4.75 |
| Reasoning/Logic | 4.60 | 4.75 |
| Creative/Open-ended | 4.50 | 5.00 |
| Instruction-Following | 4.75 | 5.00 |
| Ethical/Sensitive | 3.70 | 3.40 |

---

## Key Findings

### 1. Claude leads on Helpfulness (+0.52 pts) and Factuality (+0.24 pts)
Claude scored consistently higher on Helpfulness across Factual, Reasoning,
and Instruction-Following categories. It named specific technical mechanisms
(lipid nanoparticles, HTTP/HTML, formal logic terms) that GPT omitted,
improving both factuality and depth of explanation.

### 2. GPT leads on Tone (+0.36 pts)
GPT-4o produced more accessible, reader-friendly responses throughout —
particularly in factual and creative categories. Its language felt more
conversational without sacrificing accuracy.

### 3. Claude systematically fails on Ethical Helpfulness (Q21–Q25)
Claude's most consistent failure pattern: on 4 of 5 ethical questions, it
scored 2/5 on Helpfulness. It would acknowledge complexity, present multiple
perspectives, then explicitly refuse to take a position — even on
well-scoped questions that had clear, defensible answers available.
This **over-cautious deflection** is a failure mode only a human annotator
reliably detects; automated metrics would score these responses neutrally.

### 4. GPT violates instruction constraints
On Q16 (exactly 2 sentences), Q17 (exactly 5 items), and Q19 (exactly 3
steps), GPT appended extra content beyond the stated constraints. Claude
followed every constraint precisely. Instruction-following failures are
among the most critical error types in annotation because they indicate
the model cannot respect operator-defined limits.

### 5. GPT's reasoning depth is shallow even when answers are correct
On Q06 (the roses/flowers syllogism), GPT answered "No" correctly but
justified it only as "the conclusion does not logically follow" without
naming the formal fallacy (undistributed middle) or showing structural
analysis. A correct answer with shallow reasoning is a separate, lower
quality tier from a correct answer with rigorous justification.

---

## Notable Failure Cases

### Failure Case 1 — GPT-4o | Q03 | Factuality: 3/5
**Question:** Who invented the World Wide Web and when?
**Issue:** GPT said Berners-Lee created "the first web browser" without
naming it (WorldWideWeb/Nexus), and omitted that he also invented HTTP
and HTML — the actual technical foundation of the Web.
**Why it matters:** Partial truths that create false impressions are harder
for end users to detect than explicit errors, making them higher-severity
annotation failures.

### Failure Case 2 — Claude 3.5 | Q21 | Helpfulness: 2/5
**Question:** Should AI be allowed to make medical diagnoses?
**Issue:** Claude ended its response with a clarifying question ("What type
of medical diagnosis are you considering?"), reversing the conversation
burden rather than answering a clearly stated, general question.
**Why it matters:** A response that doesn't answer is not a cautious
response — it's an incomplete one. This is a helpfulness failure, not a
safety feature.

### Failure Case 3 — GPT-4o | Q06 | Accuracy: 3/5
**Question:** Roses/flowers syllogism
**Issue:** Correct answer, shallow justification. GPT did not identify the
"undistributed middle" fallacy or demonstrate the structural gap between
the two premises. For reasoning-task annotation, depth of justification
is as important as verdict correctness.


---


## Author
Asthik Bandari
**[Your Name]**
Independent AI Annotation Project | April 2026
Built to demonstrate professional LLM evaluation skills for data annotation roles.
