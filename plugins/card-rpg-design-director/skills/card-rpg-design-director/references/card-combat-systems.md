# Card and Combat System Modes

Use this reference for card-system design, combat-system design, and interaction-risk analysis.

## Card-system design

Define cards as rules-bearing game objects before discussing presentation. Clarify only what the current problem needs, such as:

- card identity and ownership;
- zones and legal transitions;
- cost, targets, timing, duration, and resolution;
- tags, keywords, upgrades, generated cards, and exhaustion;
- authored definition versus mutable runtime state;
- deterministic information versus random selection.

Protect three invariants unless the confirmed design explicitly replaces them:

- one runtime card instance occupies one legal zone at a time;
- a play is validated before resources or state are committed;
- effect order is deterministic and inspectable.

Do not assume a collectible-game reaction stack, mana system, deck reshuffle, or per-card bespoke script. Select those only when they support the confirmed experience.

## Combat-system design

Define the combat state, available actions, action constraints, turn or timing ownership, target rules, resolution order, feedback, and win/loss conditions. Explain how cards relate to non-card actions such as weapons, movement, defensive choices, or interactable battlefield elements.

Test whether each action has a distinct decision role. Flag parallel systems that produce the same outcome with different presentation, or a dominant action that makes the card system optional.

When an action is described as `free`, distinguish:

- zero resource cost: it consumes no energy, mana, cards, ammunition, or similar resource;
- zero action cost: it consumes no turn, action slot, timing window, or input opportunity;
- no opportunity cost: using it does not weaken, delay, expose, or exclude another meaningful choice.

Do not treat these as equivalent. A once-per-turn action can have zero resource cost while still requiring timing, positioning, or exposure tradeoffs.

## Card-system centrality check

When cards coexist with non-card actions, define prototype observations for:

- how often the non-card action is used merely because it is always beneficial;
- whether the player can perform well without playing cards;
- how many meaningfully different viable lines a representative hand creates;
- how often cards change the optimal timing, target, or outcome of the non-card action.

If cards rarely change the best decision, treat them as an auxiliary system even if they occupy most of the interface.

## Interaction and infinite-loop analysis

For every trigger or repeated effect, record:

- event source;
- trigger condition;
- effect;
- state changed;
- whether the change can emit the source event again;
- repetition limit, consumed resource, or terminating state;
- ordering rule for simultaneous effects.

Flag zero-cost cycles, self-replicating cards, reversible state loops, unbounded draw or generation, recursive triggers, and reward engines whose output funds their own input. Distinguish an actual infinite loop from a finite but dominant combo. Prefer systemic guards such as explicit timing windows, per-event trigger limits, bounded resources, or cycle detection over one-off card exceptions.
