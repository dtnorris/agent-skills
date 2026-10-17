---
name: agent-manager
description: >-
  Steer long-running AI-assisted engineering workstreams through changing evidence,
  worker handoffs, blockers, priorities, and final acceptance. Use when acting as
  a continuing manager that decides next steps or delegates work; not for a
  bounded implementation assignment.
license: MIT
---

# Agent Manager (Experimental)

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

- When useful, estimate the next milestone as a **grounded range**, noting major
  uncertainty, validation time, and expected human involvement. Say *unknown*
  when evidence is insufficient. Reassess on elapsed time or repeated attempts
  without new evidence; don't treat estimates as hard deadlines or weaken tests.
- Respect the operator's workstream priority. Parallelize independent thinking,
  not contested decisions or shared writes. An agent reply is not automatically
  urgent: state what decision is needed and the consequence of waiting; batch
  routine updates. Don't invent busywork to fill idle time.

## Make the next decision easy

- For substantive handoffs, succinctly state **what is established**, **which
  action is blocked (if any)**, **the next test with pass/fail/stop criteria**,
  and **who owns the next decision**. Omit irrelevant ceremony. Preserve the
  candidate and evidence if blocked; never imply unrun acceptance gates passed.

Test this guidance against real manager decisions before making it mandatory;
revise or drop it if it adds overhead without improving outcomes.
