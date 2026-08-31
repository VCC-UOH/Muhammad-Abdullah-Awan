# Week 8 — Capstone: Deployed Research Paper

## Assignment Overview
This was the final and largest deliverable of the FlyRank AI Machine Learning 
Internship (ML-CAP-01) — assembling every weekly assignment into one deployed, 
public research paper built on real FlyRank search data, plus a final polish 
task tying the work back to FlyRank's real content problem.

## What I Did
1. **Assembled the capstone notebook** (`capstone.ipynb`), mirroring the 
   paper's structure: Question, Data, Methodology, Results (model vs. 
   baseline), Limitations, Ranked Recommendations, and Artifacts.
2. **Wrote and deployed a full public research paper** as a static webpage, 
   containing all required sections: Title + 5-sentence Abstract, 
   Introduction/Problem Statement, Data, Methodology, Results with charts, 
   Limitations & honest framing, Ranked Recommendations, Reproducibility, 
   and Acknowledgments & Data Credit (linked to flyrank.ai).
3. **Deployed via GitHub Pages** directly from my repository (`/docs` folder), 
   verified the live page loads correctly with all charts rendering on both 
   desktop and mobile, and recorded the exact deployed URL in 
   `submission/paper_url.txt` as required.
4. **Final polish task**: strengthened the paper's Introduction with explicit 
   case-study framing connecting my findings back to FlyRank's own research 
   on refresh timing as a measured lever; added a 5-minute demo outline 
   (question → method → one chart → one honest result → one recommendation) 
   for the optional Week 8 showcase; and drafted two shareable cuts of the 
   work — a methodology-focused social post and a 3-sentence employer-facing 
   summary — committed as the closing section of `capstone.ipynb`.
5. **Submitted the dedicated Capstone card** on the portal (separate from the 
   weekly assignments track), confirming the repo and deployed paper URL.

## Results Reported in the Paper
- Baseline rule (Week 4): Precision@50 = 0.240
- Random Forest, honest client-holdout split (Week 5/6): Precision@50 = 0.540, 
  ROC-AUC = 0.603 — a measured ~2.25x lift over the baseline on the identical 
  test split.
- Full leakage audit passed, including a deliberate leak test confirming the 
  validation harness correctly detects leakage when present.

## What I Learned
- Turning eight weeks of separate notebooks into one coherent, honestly-told 
  narrative is a distinct skill from doing the analysis itself.
- Deploying a static site via GitHub Pages (repo → docs/ folder → Settings → 
  Pages) is a genuinely free, ten-minute path from a notebook to a public, 
  shareable artifact.
- Writing a paper's Limitations section myself, before a reader finds the gaps, 
  is what earns trust rather than undermines it.

## Challenges Faced
- Managing relative image paths correctly for GitHub Pages took a few 
  iterations to debug when charts initially failed to render on the live page.
- Condensing eight weeks of technical work into a 5-sentence abstract and a 
  5-minute demo outline without losing the honest, validated result required 
  several rewrites.

## Deliverable
Live deployed research paper:
https://abdullahawan0043-glitch.github.io/Flyrank-machine-learning-internship/

Capstone notebook and full code/output:
https://github.com/abdullahawan0043-glitch/Flyrank-machine-learning-internship/blob/main/work/notebooks/capstone.ipynb

Full FlyRank ML Internship repository:
https://github.com/abdullahawan0043-glitch/Flyrank-machine-learning-internship
