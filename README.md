# UK weekly board

A weekly strategy review of a job search by a ten-seat advisory panel that reasons independently, names the real bottleneck, and fires its own dated triggers.

**Type:** Claude scheduled task · **Area:** Job search automation

## What it does

- Gathers the week's evidence first and labels each finding (verified current, verified historical, user-stated, inference, unknown).
- Ten seats with separate jobs: Strategist, Skeptic (attacks the evidence), Opposing Counsel (attacks the conclusion), Operator, Economist, Risk Officer (owns the pre-mortem), Creative, Advocate, Auditor (checks the instruments), Decision Maker.
- Names the bottleneck from the funnel (discovery, targeting, positioning, interview, closing or execution) and compares segments against a naive baseline.
- Gives three ranked actions with named artefacts, and fires dated triggers as written instead of moving them again.

## Guardrails

- Concur openly: if the seats agree, say so and stop. No manufactured dissent.
- Do not restate: a finding named three times escalates to why it isn't happening.
- Sends and submits nothing.

## When it triggers

> Weekly strategy review of a job search by a ten-seat advisory panel over the week's evidence. Says whether the search is converting, names the bottleneck, gives three actions, and sets dated triggers that get fired as written.

## What's in this repo

- `SKILL.md`: the skill itself, the file Claude or Codex reads.
- Not included: Project files are personal and not published.
- Written to be generic: where the skill relies on the user's own files, it names them by role, not by content.

## Install

This is a Claude scheduled-task prompt. Create a scheduled task in the Claude desktop app and paste the body of `SKILL.md` as its prompt, or save it as `~/.claude/scheduled-tasks/uk-weekly-board/SKILL.md`. It expects the project files it names to exist.
