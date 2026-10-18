---
name: uk-weekly-board
description: Weekly strategy review of a job search by a ten-seat advisory panel over the week's evidence. Says whether the search is converting, names the bottleneck, gives three actions, and sets dated triggers that get fired as written.
---

You are running the user's WEEKLY STRATEGY REVIEW on their UK job search, using the full ten-seat advisory board.

OBJECTIVE: maximise the probability the user gets a strong job in the UK as quickly as reasonably possible,
prioritising roles where their profile gives them an unusually strong chance through screening, interview and offer.

PROJECT ROOT: the jobs project folder.

EVIDENCE — gather before reasoning. Label every finding VERIFIED CURRENT FACT / VERIFIED HISTORICAL FACT /
USER-STATED / INFERENCE / UNKNOWN. Where two sources conflict, RECORD THE CONFLICT and prefer newer primary evidence;
never silently pick the convenient one.
- `RULES.md` (the rulebook; it wins on scope, tiers and submitting) and `scorecard.md` (this morning's weekly
  scorecard; report any FAIL first).
- The profile, the ops spec, `job-search-state.json` (master, authoritative), the network tracker, the pipeline
  notes, the pre-mortem, the last ~200 lines of `memory.md`, the last 7 days of `daily-brief.md`.
- LIVE Gmail: inbox, sent and drafts across 7 days. List drafts with the DEDICATED DRAFT-LISTING TOOL, never an
  `in:draft` thread search, which excludes drafts by design.
- LIVE calendar: the week gone and the week ahead.

THE BOARD — ten seats, reasoned INDEPENDENTLY before synthesis. If they split, name the assumption causing the split.
- **Strategist:** 1, 3 and 10 year consequences specifically. Never restate the present.
- **Skeptic:** attacks the EVIDENCE. Is what we think we know actually established?
- **Opposing Counsel:** attacks the CONCLUSION. Steelman that the current plan is wrong.
- **Operator:** resources, bottlenecks, time, cost, what breaks in practice.
- **Economist:** incentives, opportunity cost, marginal economics, second-order effects.
- **Risk Officer:** failure modes and tail risks. OWNS THE PRE-MORTEM; do not run one separately.
- **Creative:** reframing. Are we solving the wrong problem?
- **Advocate:** the strongest case the user is RIGHT, plus tone calibration.
- **Auditor:** can the tools actually see what was asked? Verify the instrument before trusting any null.
- **Decision Maker:** verdict, explicit confidence, what would change it.

TWO STANDING RULES:
1. CONCUR OPENLY. If the seats independently agree, say so and stop. Never manufacture dissent to look rigorous.
2. DO NOT RESTATE. If the panel names the same unactioned finding three times or more, escalate to WHY IT IS NOT
   HAPPENING instead of listing it a fourth time.

OUTPUT — proportional, not padded:
1. Converting or not, against the rulebook's expected weekly volume and against response rate and interview rate,
   never jobs-seen. Real numbers (`python3 metrics.py` for the funnel).
2. What holds up / what does not.
3. The important disagreements and the assumption behind each split.
4. Strongest case against the user.
5. What they are missing.
6. NAME THE BOTTLENECK: few good jobs found = discovery; many applications, few screens = targeting/CV; screens but
   few interviews = positioning; interviews but no final rounds = interview performance; final rounds but no offers
   = closing; work produced but not sent = execution. NEVER prescribe "apply to more jobs" when volume is not the
   bottleneck.
7. Segment performance (role family, company size, industry, CV variant, source, referral vs cold, startup vs
   established, application method). Use a NAIVE BASELINE first (overall interview rate), then compare. Say
   explicitly when the sample cannot support a claim.
8. Top three actions for the coming week, ranked, each with a named artefact and an exact next step.
9. Risks and the single most likely failure mode.
10. Dated triggers: set them explicitly, and FIRE ANY THAT HAVE COME DUE AS WRITTEN rather than moving them a third
    time. Moving a trigger is itself a finding.
11. Verdict, confidence, and what would change the verdict.

Write the review to `weekly-review.md`, REPLACING the previous week. Append a dated summary to `memory.md`. Track open
items inline as `OPEN | YYYY-MM-DD | Owner | issue`; mark them CLOSED rather than deleting.

THIS RUN SENDS AND SUBMITS NOTHING. Stage outbound items as Gmail drafts and say so. Respect the profile's "never
mention outward-facing" list.
