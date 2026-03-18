# Brand Interface Designer

A prompt kit for design agents that care about **taste**, not just tidy component specs.

Most UI design prompts are good at producing:
- design systems
- component inventories
- accessibility checklists
- developer handoff structure

They are much worse at producing interfaces that feel:
- calm
- premium
- branded
- sharp
- visually judged

This repo is an attempt to fix that.

## What this is

**Brand Interface Designer** is a small prompt library for building a UI design agent that:
- starts with visual attitude before components
- protects brand character from generic SaaS patterns
- uses hierarchy, typography, spacing, and restraint as the main tools of quality
- stays usable, scalable, and accessible

It is not a Figma plugin, code generator, or design system framework.
It is a **taste-aware prompt foundation** for design agents.

## Who it is for

This is for:
- product designers who want less template energy
- brand/UI designers who care about visual judgment
- teams building design agents or AI-assisted design workflows
- anyone tired of prompts that output "clean modern SaaS UI" over and over again

## What's inside

### `agents/brand-led-ui-designer.md`
The main agent spec.

It defines:
- the role
- aesthetic principles
- workflow
- hierarchy rules
- anti-generic checks
- how to turn brand into interface behavior

### `references/taste-reference.md`
The supporting taste system.

It explains:
- what to learn from references like Robinhood, Linear, Apple, and editorial commerce
- what to avoid in generic SaaS / crypto / UI-kit aesthetics
- practical heuristics for judging whether a UI feels premium or templated

### `examples/`
Ready-to-use task briefs for common screen types.

These are meant to make the agent easier to use in real projects.

## Core idea

The main shift is simple:

> Don't optimize for completeness first. Optimize for visual judgment first.

That means:
- define mood before components
- create hierarchy before decoration
- remove before adding
- let typography and composition do more work
- make brand show up beyond color

## Suggested file composition

Use the main agent prompt as the base system prompt.
Use `taste-reference.md` as a supporting reference when:
- defining visual direction
- evaluating refinement
- critiquing existing UI
- trying to avoid generic product patterns

A simple setup looks like this:

1. Load `agents/brand-led-ui-designer.md`
2. Load `references/taste-reference.md`
3. Provide a task brief with:
   - project context
   - desired feeling
   - references to move toward
   - styles to avoid
   - what must stand out
   - what should stay quiet

## Recommended prompt pattern

Use something like:

```md
Use the Brand-Led UI Designer perspective.

Project:
[what the screen or feature is]

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

## What makes this different

A lot of UI prompts collapse into one of two modes:

### 1. Design-system brain
Useful, but often too procedural.
The output is correct, complete, and forgettable.

### 2. Dribbble brain
Stylish at first glance, but weak under real product constraints.

This repo tries to sit in the middle:
- more taste than systems-only prompts
- more rigor than decoration-heavy prompts
- more brand sensitivity than generic UI kits

## Principles behind the repo

- Premium UI is usually quieter, not louder
- Strong hierarchy beats surface complexity
- Brand should survive in grayscale
- Too many cards usually means weak structure
- If removing 15–20% improves the design, it probably needed editing
- A strong interface should feel inevitable, not assembled

## Good use cases

- designing or critiquing dashboards
- improving generic fintech / crypto UI
- defining visual direction before building a component system
- reviewing a screen that feels "fine" but not distinctive
- training a design-focused agent to make better aesthetic tradeoffs

## Not ideal for

- purely visual trend exploration
- one-shot image generation prompts with no product logic
- teams that only want token specs and component states
- highly specific brand systems that already have a mature visual director

## Repo philosophy

This repo is intentionally opinionated.

It assumes that many interfaces are not weak because they lack polish.
They are weak because they lack judgment.

So the goal here is not to add more UI.
The goal is to make better decisions.

## If you use this

Adapt it.
Tighten it.
Replace the references with your own.
Push the taste further.

The best version of this repo is probably the one that becomes more specific to your own standards over time.
