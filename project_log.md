# List of what I worked on each day

3/21/2026: Created notebook, github repository, mdfiles, chose dataset

3/30/2026: Modified raw data (German Credit from UCI Statlog, 1000 rows) through SQLite. 
target varaibles: bad_credit = 1 -> bad credit and bad_credit = 0 -> good credit
Excluded sensitive fields of personal status & sex, and foreign worker
Overall Goal: Predict interpretable triage to auto-approve, manual review, or a auto-decline

3/31/2026: Within the 0–12 month duration bucket, default risk differs strongly across checking-status groups—A11: 35.87% (n=92), A12: 29.67% (n=91), A13: 16.67% (n=30), A14: 7.53% (n=146)—suggesting checking status provides predictive signal beyond loan term length.
The relationship between duration and bad-credit risk depends on checking-status group. Longer durations correspond to disproportionately higher bad rates for A11/A12 compared to A14, indicating that loan term length and checking-account status interact rather than contributing purely independent effects.

4/13/2026: Set the triage policy thresholds today.
A logistic regression model outputs a predicted probability of bad credit 𝑝. To support an interpretable screening workflow, we define a triage policy with two thresholds: applicants with 𝑝 ≤ 0.15 are auto-approved, applicants with 0.15 < 𝑝 < 0.85 are routed to manual review, and applicants with 𝑝 ≥ 0.85 are auto-declined. On the held-out test set, the auto-approve bucket contained 64 applicants with an observed bad-credit rate of 4.69%, while the auto-decline bucket contained 27 applicants with an observed bad-credit rate of 77.78%. The remaining 209 applicants fell into manual review with an observed bad-credit rate of 31.58%, consistent with this region representing borderline/uncertain cases.
