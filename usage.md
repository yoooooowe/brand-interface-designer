# Usage

## Recommended composition

Use the files in this order:

1. `agents/brand-led-ui-designer.md` as the base agent/system prompt
2. `references/taste-reference.md` as a supporting reference
3. One of the briefs in `examples/` as a starting point
4. Your own project context, constraints, and visual references

## Suggested instruction to add

```md
Refer to `references/taste-reference.md` when defining visual direction, evaluating hierarchy, or avoiding generic UI patterns.

Do not optimize for completeness first. Optimize for visual judgment first.

Use typography, spacing, and composition to create hierarchy before relying on color, cards, borders, or decorative effects.
```

## Minimal task brief

```md
Project:
[what the screen is]

Goal:
[what the user needs to do]

This should feel:
- calm
- premium
- sharp
- minimal

Closer to:
- Robinhood restraint
- Linear precision

Avoid:
- generic SaaS
- loud gradients
- too many cards

What must stand out:
- [primary emphasis]

What should stay quiet:
- [secondary content]
```
