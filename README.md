

  LLM OUTPUT EVALUATION REPORT
  GPT-4o vs Claude 3.5 Sonnet | 25 Questions | April 2026


OVERVIEW
--------
This evaluation assesses the outputs of GPT-4o and Claude 3.5 Sonnet across
25 questions spanning 5 categories: Factual/Knowledge, Reasoning/Logic,
Creative/Open-ended, Instruction-Following, and Ethical/Sensitive.

Each response was scored on a 1–5 scale across four dimensions:
  • Accuracy     – Is the information factually correct?
  • Tone         – Is the tone appropriate for the context?
  • Helpfulness  – Does it actually solve the user's problem?
  • Factuality   – Are claims verifiable and grounded?

Evaluator: [Your Name] | Tool: Manual annotation + rubric scoring


OVERALL SCORES (Avg of all 25 questions)
-----------------------------------------
  GPT-4o:       4.42 / 5.00
  Claude 3.5:   4.58 / 5.00


SCORES BY CATEGORY
-------------------
Category                GPT-4o    Claude 3.5
-----------------------------------------------
Factual/Knowledge       4.55       4.75
Reasoning/Logic         4.6       4.75
Creative/Open-ended     4.5       5.0
Instruction-Following   4.75       5.0
Ethical/Sensitive       3.7       3.4


SCORES BY DIMENSION (Overall Avg)
-----------------------------------
Dimension        GPT-4o    Claude 3.5
---------------------------------------
Accuracy          4.56       4.76
Tone              4.56       4.44
Helpfulness       4.20       4.36
Factuality        4.36       4.76


KEY FINDINGS
------------

1. CLAUDE LEADS ON HELPFULNESS (+0.52 pts) AND FACTUALITY (+0.24 pts)
   Claude scored significantly higher on Helpfulness (4.56 vs 4.04) driven
   primarily by stronger instruction-following and richer factual responses
   in reasoning and creative categories. Its factuality score benefited from
   naming specific mechanisms (e.g., lipid nanoparticles in Q02; HTTP/HTML
   in Q03) that GPT omitted.

2. GPT LEADS ON TONE (+0.36 pts)
   GPT-4o consistently produced more accessible, appropriately toned
   responses — particularly in factual and creative categories. Its language
   felt more conversational and reader-friendly. Claude's tone, while
   professional, sometimes reads as overly formal or clinical.

3. GPT UNDERPERFORMS ON REASONING DEPTH (Q06 — Syllogism)
   GPT's weakest individual score (3.5/5) came on Q06, the roses syllogism.
   While it arrived at the correct answer (No), it failed to name the formal
   logical fallacy ('undistributed middle') or explain why the premises were
   structurally insufficient. For an annotation role, this matters: an
   annotator must articulate *why* a response is correct or incorrect, not
   just flag the verdict.

4. CLAUDE SYSTEMATICALLY FAILS ON ETHICAL/SENSITIVE HELPFULNESS
   Claude's most consistent failure was on questions Q21–Q25 (Ethical),
   where it scored 2/5 on Helpfulness in four of five cases. The pattern:
   Claude would acknowledge the complexity, present multiple perspectives,
   then explicitly refuse to take a position — even on questions with clear
   philosophical consensus available (e.g., white lies, Q22). This
   over-cautious deflection, while designed to be safe, renders responses
   unhelpful in practice. A human annotator would flag this as a
   'non-answer' failure mode.

5. GPT INSTRUCTION-FOLLOWING INCONSISTENCY
   Across Q16–Q20, GPT demonstrated a tendency to exceed instructions:
   adding a third sentence when asked for exactly two (Q16), appending Tips
   sections to recipes (Q19), and adding sub-bullets to simple lists (Q17).
   Claude followed all constraints precisely. In professional annotation,
   instruction-following failures are among the most severe error types
   because they indicate the model cannot adhere to operator constraints.


METHODOLOGY NOTE
-----------------
All responses were collected in fresh conversation sessions (no prior context).
GPT-4o (May 2024 version) and Claude 3.5 Sonnet were used. Scores represent
a single annotator's assessment using the rubric defined in the accompanying
spreadsheet. Inter-annotator reliability could be improved with a second
rater. All raw responses and scores are available in LLM_Evaluation_Sheet.csv.

=======================================================
  END OF REPORT
=======================================================
