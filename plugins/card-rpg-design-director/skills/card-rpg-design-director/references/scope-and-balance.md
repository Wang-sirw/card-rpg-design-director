# Scope and Balance Modes

Use this reference for prototype scope, feature prioritization, and provisional numerical design.

## Prototype scope

Start with one design hypothesis. Define the minimum playable slice that can test it, the evidence to observe, and a stop condition. Separate:

- `Must simulate`: behavior required to answer the hypothesis;
- `May fake`: presentation or content that can be represented cheaply;
- `Defer`: systems that do not affect the current learning goal;
- `Do not build`: work whose value depends on an unvalidated premise.

For a solo project, treat new content pipelines, editors, generalized frameworks, extensive save compatibility, and broad data schemas as costs requiring an immediate prototype benefit.

## Feature prioritization

Prioritize by dependency and learning value before polish or completeness. For each feature, assess:

- player-facing value;
- uncertainty reduced;
- prerequisites and downstream consumers;
- implementation and content cost;
- rework risk if assumptions change;
- whether a cheaper test exists.

Recommend `Now`, `Next`, `Later`, or `Cut`, with a short reason. A feature is not `Now` merely because it is foundational in a hypothetical final architecture.

## Numerical assumptions and test ranges

State the model before values: turn length, expected actions, resource income, hand flow, encounter duration, damage or defense scale, and desired variance. Then provide a baseline and a small low/base/high test range.

For each range, state:

- intended behavioral effect;
- failure signal at the low end;
- failure signal at the high end;
- metric or observation to record;
- systems that would invalidate the comparison.

Prefer a few interpretable parameters over simultaneous tuning of many values. Never label untested numbers as balanced.
