# Codex Implementation Handoff

Use this reference only after the relevant design is confirmed, or when the user explicitly asks for a task that preserves unresolved decisions as blockers.

## Readiness gate

Withhold the implementation task when an unresolved question would materially change the state model, action economy, timing or resolution order, integration boundary, or acceptance criteria. Return the blocking decisions and the smallest design test instead. Do not let Codex make those product decisions implicitly through code structure.

Produce one independently reviewable task with this contract:

## Task ID and title

Use a stable identifier and one outcome-focused title.

## Goal

Describe the observable result and why it matters to the current prototype.

## Confirmed design inputs

List only rules and decisions the implementation may rely on. Keep provisional ideas out of this section.

## Required context

List the project documents, scenes, scripts, resources, or prior tasks Codex should inspect before editing. Do not invent paths that have not been confirmed; use role-based descriptions when paths are unknown.

## Allowed change scope

Name the directories or files Codex may create or modify. If exact paths are unknown, instruct Codex to inspect first and report its proposed targets before editing.

## Prohibited changes

Identify unrelated systems, project settings, dependencies, plugins, generated content, or future features that must remain untouched.

## Implementation requirements

Specify behavior and invariants without dictating unnecessary code structure. Include data ownership, state transitions, or integration boundaries when they are part of the confirmed design.

## Acceptance criteria

Write observable pass/fail statements. Include relevant edge cases and the minimum Godot runtime check.

## Verification

State which parser checks, tests, launch steps, scene interactions, logs, or diffs should be inspected. Codex must report anything it could not verify.

## Deferred work

List explicitly excluded follow-up features so Codex does not implement them opportunistically.

## Blockers and open questions

If a decision materially changes architecture or behavior, make it a blocker. Do not let Codex choose silently. Minor implementation choices may remain with Codex when the acceptance criteria constrain the result adequately.
