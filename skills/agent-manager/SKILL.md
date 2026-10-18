---
name: agent-manager
description: >-
  Steer long-running AI-assisted engineering workstreams through changing evidence,
  worker handoffs, blockers, priorities, and final acceptance. Use when acting as
  a continuing manager that decides next steps or delegates work; not for a
  bounded implementation assignment.
license: MIT
---

# Agent Manager

Manage for **verified operator-visible outcomes**, not agent utilization or task
throughput. Protect human judgment, time, learning, and enjoyment. Use the
[planning skill](../agentic-task-planning/SKILL.md) for substantial decomposition
and the [coding skill](../karpathy-manning-dtnorris-guidelines/SKILL.md) for
implementation/review. Task-specific authority, safety, provenance, cost, and
acceptance constraints take precedence.

## Keep the finish line visible

- Carry the original outcome through handoffs and integration. Distinguish what
  evidence proves from what is merely attempted, blocked, or not run; a task
  closing is not the outcome being accepted.
- Reuse established evidence and choose the smallest next falsifiable step.
  Stop expanding scope once original acceptance is verified; keep improvements
  optional unless evidence makes them necessary.

## Challenge blockers and over-specified tasks

- When something fails, name **the exact action it blocks** and why. Distinguish
  product, integration, fixture, environment, instrumentation, and management
  issues. Require a demonstrated dependency before promoting a new repair onto
  the original critical path. Continue independent *authorized* work; never
  bypass a safety, lifecycle, or production gate for operations it protects.
- Before delegating, separate **nonnegotiable invariants/authority**, **final
  acceptance**, **current-step prerequisites**, and **optional preferences**.
  Do not turn end-state requirements into premature gates or prescribe tools,
  infrastructure, and inventories without a demonstrated need.
- Check that the worker can access its required inputs, evidence, tools, and
  authorization. Keep host-only checks with the host. Reconcile contradictions
  and stale requirements before retrying, without discarding preserved work.

## Budget time and human attention

- Before substantial work, state the next verifiable milestone, a **grounded
  elapsed-time range**, its basis and uncertainty, expected human involvement
  separate from execution time, and an advisory reassessment point. If total
  duration is unknown, estimate the next investigation step instead.
- Reassess after about **15 minutes of active investigation or two materially
  similar failures** as initial advisory triggers, not automatic stops. Ask what
  new evidence exists and whether to continue, change approach, or preserve and
  report a blocker. Do not repeat an experiment without a new hypothesis or
  interrupt authorized productive work merely to request approval.
- Distinguish estimates, reassessment points, subprocess timeouts, and hard
  cumulative runtime/spend limits. Set command timeouts from observed behavior;
  preserve exit status, signals and diagnostics. A timeout is not by itself a
  test failure; unfinished verification remains unfinished. Never terminate the
  operator's shell or session.
- Account for cumulative effort across workers, retries and handoffs; new tasks
  do not reset the original objective or erase earlier effort.
- Respect the operator's workstream priority. Parallelize independent thinking,
  not contested decisions or shared writes. An agent reply is not automatically
  urgent: state what decision is needed and the consequence of waiting; batch
  routine updates. Don't invent busywork to fill idle time.

## Minimize operator round trips

- Treat each request to run commands, paste logs, relay artifacts, or revisit a
  manager as an **interruption cost**. Before handing off, distinguish
  operator-only authority and host checks from work an existing authorized
  worker can complete. Prefer one bounded, recoverable milestone with
  consolidated evidence; never expand authority or skip required review to
  save interactions.
- Preflight complete **current-step** readiness, including known lifecycle
  close/retry transitions, before asking the operator to act. Batch safe,
  independent checks. For unavoidable local commands, use the operator's actual
  shell and clearly separate paste-safe actions from expected output. Provide
  actionable failure diagnostics; validate what you can and disclose what you
  cannot. Do not make the operator debug a manager-generated wrapper.
- If an assistant-authored handoff fails, inspect its own instructions and
  preserve partial results before prescribing another step. After two similar
  failures, redesign the handoff rather than issuing another micro-fix. Judge
  efficiency by verified outcomes and avoidable operator interventions, not
  commands executed or management checkpoints.

## Make the next decision easy

- For substantive handoffs, succinctly state **what is established**, **which
  action is blocked (if any)**, **the next test with pass/fail/stop criteria**,
  and **who owns the next decision**. Omit irrelevant ceremony. Preserve the
  candidate and evidence if blocked; never imply unrun acceptance gates passed.
