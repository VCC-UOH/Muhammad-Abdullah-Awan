# Week 6 — Validation Audit & Model Honesty Check

## Assignment Overview
This week's assignment required auditing my own Week 5 machine learning model 
the same way a research paper's methodology would be audited — applying the 
"attack your own model" rigor taught in this week's live session, which used 
FlyRank's own research paper as the example.

## What I Did
1. **Paper methodology review**: Selected two findings from FlyRank's "State of 
   AI-Driven SEO" research paper and wrote constructive methodology questions 
   for each — one about whether word-count/age were measured before or during 
   the observed growth window, and one about whether a feature-importance 
   ranking is meaningful when the top features are direct arithmetic 
   components of the label itself (Health Score).
2. **Honest split before/after**: Re-ran my Week 5 Random Forest model under 
   two conditions — a random row split (dishonest) and a grouped, client-holdout 
   split (honest) — and reported both numbers side by side to show the gap 
   caused by client-level memorization.
3. **Leakage audit**: Ran a full attack-your-own-model checklist, including a 
   deliberate leak test (adding a label-derived column and watching the score 
   jump toward a near-perfect 1.000), then removed it and kept the honest number.
4. **Claim rewrite**: Rewrote three of my own earlier claims (from Week 4 and 
   Week 5) into public-safe, decision-support language, following the 
   claim-ladder principle — matching words to the actual strength of evidence.

## What I Learned
- A model's score means nothing without a same-split, same-metric baseline 
  comparison sitting next to it.
- The gap between a random-split score and a grouped-split score is itself a 
  finding — it reveals how much of the original number was memorization rather 
  than real signal.
- Reviewing someone else's published work constructively (asking "how do we 
  make this stronger" rather than looking for mistakes) is the same skill as 
  reviewing your own work honestly.

## Challenges Faced
- Understanding exactly how FlyRank's Health Score formula made Average 
  Position and Impressions circular inputs to the model in their appendix, 
  and articulating that critique respectfully rather than as a "gotcha."
- Designing the deliberate leak test in a way that convincingly demonstrated 
  the test harness itself was working correctly (i.e., that it WOULD catch 
  leakage if leakage were present).

## Deliverable
Repository, notebook, and full code/output for this assignment:
https://github.com/abdullahawan0043-glitch/Flyrank-machine-learning-internship/blob/main/work/notebooks/w06_validation_audit.ipynb

Full FlyRank ML Internship repository:
https://github.com/abdullahawan0043-glitch/Flyrank-machine-learning-internship
