# Week 5 - Internship Progress
## FlyRank AI Machine Learning Internship

**Assignment:** Capstone Modeling Lane (Build Phase)

**Objective:**
To build the first real model for the project lane, compare it against 
the Week 4 rule-based baseline on the same data and same metric, and 
perform honest error analysis before trusting the results.

**Work Completed:**

1. **Method choice:** Used Logistic Regression (readable baseline-beater) 
   and Random Forest (stronger, still explainable via feature importance). 
   Since the lane's real question is "which pages should be reviewed 
   FIRST" — a ranking/scoring problem — both models output a probability 
   used as a ranking score, evaluated with Precision@50 rather than 
   accuracy.

2. **Split design:** Used a client-holdout split (grouped by `client_id`, 
   not a random row split) via `GroupShuffleSplit`, confirming zero 
   client overlap between train and test. This matches the same split 
   design used for the Week 4 baseline, keeping the comparison fair.

3. **Model vs Baseline comparison** (Precision@50, same test split):

   | Method | Precision@50 | ROC-AUC |
   |---|---|---|
   | Base rate (random) | 0.559 | — |
   | Baseline rule (Week 4) | 0.640 | — |
   | Logistic Regression | 0.660 | 0.580 |
   | Random Forest | 0.540 | 0.603 |

   Logistic Regression slightly outperformed both the baseline rule and 
   Random Forest on Precision@50, showing that added model complexity 
   did not automatically translate to a better ranking at the top of 
   the list.

4. **Error analysis:** Top 3 features by importance in the Random Forest 
   were `impressions_90d`, `avg_position`, and `content_age_days` — 
   consistent with the Week 4 signal checks, not a sign of leakage. 
   Of the top 50 ranked pages, 23 were incorrectly flagged — mostly 
   pages with high impressions and long time-since-update but a flat/up 
   trend, which the model couldn't distinguish from early-stage decline.

**Deliverable:** `work/notebooks/w05_model.ipynb`

**Files in this folder:**
- `w05_model.ipynb`
Committed to my repository and submitted on the portal.
You can review the completed notebook directly here:
https://github.com/abdullahawan0043-glitch/Flyrank-machine-learning-internship/blob/main/work/notebooks/w05_model.ipynb
Regards,
Muhammad Abdullah Awan
