---
name: agentic-task-planning
description: >-
  Plans substantial AI-assisted engineering work: outcomes, task decomposition,
  dependencies, parallel ownership, integration, recovery, and acceptance.
  Use before multi-step/multi-agent projects or when revising a stalled plan.
  Skip for trivial changes or execution of an already-approved plan.
license: MIT
---

# Agentic Task Planning

Find the shortest safe path to an **integrated, verified, recoverable outcome**.
Optimize for useful completion and operator attention, not agent utilization or
number of tasks. Scale planning to the work; avoid process for its own sake.
Existing task, authority, safety, cost, and coding requirements take precedence.

## 1. Start with the whole outcome

- State the observable user/operator result, required safeguards, and who owns
  end-to-end acceptance. Check what already works before proposing new code.
- Identify the simplest viable approach, including one bounded change, a small
  diagnostic, or no change.
- For multi-component work, prove a small **continuous public-entry journey**
  early, using real handoffs and fakes only at declared external boundaries.
  When practical, show that removing a required handoff makes the test fail.
- Ask: **Could every component task pass while the promised journey still fails?**
  If yes, fix acceptance and integration plans before expanding the task list.

## 2. Decompose at verifiable seams

- Inspect current source, contracts, actual Git HEAD/worktree, and relevant
  evidence first. Mark assumptions and unresolved interfaces explicitly.
- Prefer independently testable, reviewable, recoverable changes. Avoid giant
  assignments and tiny tasks whose setup and handoff costs outweigh their value.
- Give each task a specific outcome, owner, change boundary, dependencies,
  positive/negative checks, and artifact handoff.
- Preserve original acceptance requirements through task splits or transfers.
  An uncertain experiment must not become a mandatory prerequisite without a
  demonstrated dependency.

## 3. Schedule integration, not just workers

- Map shared files, semantic contracts, mutable state, and repository authority
  before parallelizing. Default to one writer at a contested seam.
- Parallelize genuinely independent work with explicit ownership, candidate
  preservation, integration order, and a composed validation gate. Distinct
  worktrees/task IDs do not prove semantic independence; shared repos alone
  do not make parallel work impossible.
- Refresh exact source after another change lands. Never discard legitimate
  sibling work to satisfy a checkpoint or administrative assumption.
- Planning is not publication authority: commits, pushes, merges, and task
  completion still require the applicable operator authorization.

## 4. Verify the verifier

- Before expensive tests, qualify the actual execution root, fixture history,
  runtime, filesystem semantics, process boundaries, and relevant dependencies.
- Smoke-test wrappers and observers against representative text **and binary**
  output; preserve subprocess bytes, status, and exceptions.
- Use focused checks first, then cross-component tests, the continuous journey,
  and required full-suite gates. Keep negative safety checks.
- Attribute failures to the right layer: product, integration contract, fixture,
  environment, instrumentation, or management. Reproduce before fixing.
  Compare timing, coverage, and skips only on comparable baselines.

## 5. Preserve work and tell acceptance truth

- Save a complete, inspectable, baseline-bound candidate **before** costly
  validation or fragile session handoffs; include untracked files and hashes.
  Distinguish recoverable remote artifacts from host checkpoint registration.
- Separate implementation, focused proof, integrated candidate, current-source
  eligibility, end-to-end acceptance, and publication. None implies the next.
- Preserve failures, original candidate bytes, and provenance when main moves;
  require fresh reconciliation/validation before integration.
- Report PASS, FAIL, BLOCKED, and NOT RUN against the **original** acceptance
  criteria. Finding the next blocker does not prove it is the last.

## 6. Control the critical path

- Keep optional cleanup, tooling, and research off the finish line unless a
  required invariant proves otherwise. A genuine safety repair is not scope
  creep merely because it crosses repositories.
- Choose the cheapest next falsifiable gate; declare pass/fail and stop rules.
  Paid execution requires independently enforced finite cumulative spend or
  runtime limits that survive orchestration failure.
- Adapt plans to evidence without rewriting history or rescuing disposable old
  fixtures unnecessarily. Measure accepted behavior, recovery, human effort,
  and unexpected interventions—not task counts or generated code volume.

## Planning handoff

For substantial work, state concisely:

1. **Outcome:** whole-journey acceptance, owner, and negative control.
2. **Next gate:** smallest falsifiable experiment, pass/fail and stop decision.
3. **Work:** bounded tasks, dependencies, parallel seams, integration order.
4. **Evidence:** inspected baselines, recovery, unknowns, remaining gates,
   cost/safety and publication authority.

Omit irrelevant detail. Do not invent a new management framework or status
artifact simply to satisfy this skill.
