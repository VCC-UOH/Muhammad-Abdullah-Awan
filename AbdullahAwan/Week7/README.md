# Week 7 — Content Action Playbook

## Assignment Overview
This week's assignment required turning my validated Week 5/6 model output 
into a practical, human-reviewed content action playbook — the same structure 
that becomes the recommendations section of a deployed research paper.

## What I Did
1. **Ranked actions + reason codes**: Generated a ranked queue from the Week 5 
   model, mapping each page to a reason code (e.g. `stale_but_visible_high_risk`, 
   `page1_ctr_gap`, `model_flagged_decline_risk`) and a corresponding action 
   (`refresh_priority`, `review_snippet_title`, `review_for_refresh`, 
   `monitor_only`, `no_action`).
2. **Intended use and limits**: Documented that this playbook is decision-support 
   only, using claim-ladder-safe language, and explicitly named the dataset's 
   limits (observational data, active-content survivor filter, no experiment 
   behind any "cause" claim).
3. **Human review + no-go list**: Wrote explicit human-review rules (every 
   action requires editor sign-off) and a 5-item "do NOT automate" list — 
   covering auto-publishing, de-indexing decisions, treating "no_action" as 
   permanently safe, cross-client score comparison, and presenting scores 
   without their Precision@50/base-rate context.
4. **Monitoring & retrain triggers**: Defined a light monitoring plan (tracking 
   Precision@50 drift and reason-code distribution shifts) and concrete 
   retrain triggers (new monthly data, monitoring alerts, data contract changes).
5. **Exports for the paper**: Exported the ranked queue CSV (regenerated per 
   run, kept out of git by the CI leak-guard), committed a reusable figure 
   (action distribution chart) to `work/figures/`, and committed the metrics 
   JSON receipts to `work/outputs/` — these exact files feed next week's 
   deployed research paper.

## What I Learned
- A model score is not a finished product — it only becomes useful once it is 
  translated into ranked, reviewable actions with clear reasoning attached.
- Explicitly writing a "no-go" list is as important as writing the recommended 
  actions — naming what should NOT be automated protects against overreach.
- Committing lightweight receipts (figures, metrics JSON) instead of large 
  regenerable data files keeps a repository clean while still preserving 
  reproducibility.

## Challenges Faced
- Balancing being genuinely useful (concrete ranked actions) against 
  overclaiming (avoiding language that suggests the model guarantees results).
- Deciding what belongs in the no-go list required thinking through realistic 
  misuse scenarios, not just the intended use case.

## Deliverable
Repository, notebook, and full code/output for this assignment:
https://github.com/abdullahawan0043-glitch/Flyrank-machine-learning-internship/blob/main/work/notebooks/w07_action_playbook.ipynb

Full FlyRank ML Internship repository:
https://github.com/abdullahawan0043-glitch/Flyrank-machine-learning-internship
