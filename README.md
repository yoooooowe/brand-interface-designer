# Brand Interface Designer

A taste-aware prompt kit for UI design agents.

It is built for one specific problem:

> most design prompts can produce structure, but very few can produce judgment.

They are usually good at generating:
- design systems
- component inventories
- accessibility checklists
- developer handoff formats

They are much worse at generating interfaces that feel:
- calm
- premium
- branded
- sharp
- intentional
- non-generic

**Brand Interface Designer** is a small prompt library meant to push agents away from default SaaS output and toward stronger hierarchy, stronger taste, and clearer brand character.

---

## Why this exists

A lot of UI design agents fall into one of two traps:

### 1. Design-system brain
The output is systematic, complete, and implementation-friendly — but visually forgettable.

### 2. Dribbble brain
The output looks stylish at first glance — but collapses under real product constraints, real content, and real usage.

This repo tries to sit in the middle:
- more taste than systems-only prompts
- more rigor than decoration-heavy prompts
- more brand sensitivity than generic UI kits
- more restraint than trend-driven prompt packs

---

## What this is

**Brand Interface Designer** is a prompt foundation for building a UI design agent that:
- starts with **visual attitude before components**
- protects brand character from generic product patterns
- uses **hierarchy, typography, spacing, and restraint** as the main tools of quality
- stays usable, scalable, and accessible
- critiques interfaces by looking for weak hierarchy, over-cardification, and template energy

It is **not**:
- a Figma plugin
- a code generator
- a design token compiler
- a complete design system framework

It is a **prompt kit for more judged interface design**.

---

## Who this is for

This repo is for:
- product designers who want less template energy
- brand/UI designers who care about visual judgment
- teams building AI-assisted design workflows
- people refining fintech / crypto / SaaS interfaces that feel too generic
- anyone tired of prompts that keep outputting “clean modern SaaS UI” in slightly different clothes

---

## What's inside

### `agents/brand-led-ui-designer.md`
The main agent spec.

It defines:
- the role and stance of the agent
- aesthetic principles
- workflow and hierarchy rules
- anti-generic checks
- how to turn brand into interface behavior
- how to think about restraint, tone, and component language

### `references/taste-reference.md`
The supporting taste system.

It explains:
- what to learn from references like Robinhood, Linear, Apple, and editorial commerce
- what to avoid in generic SaaS / crypto / UI-kit aesthetics
- practical heuristics for judging whether a UI feels premium, controlled, or templated
- how to translate taste into concrete interface decisions

### `examples/`
Ready-to-use briefs for common screen types:
- login
- dashboard
- asset detail
- landing page
- onboarding
- trading page

### `usage.md`
A lightweight guide for composing the prompt files together.

### `critique-mode.md`
A focused review mode for using the agent as a sharper UI critic.

It is built for:
- reviewing existing screens
- finding generic patterns
- identifying weak hierarchy
- deciding what to remove, merge, or quiet
- pushing an interface from “usable” to “judged”

---

## Core idea

The main shift is simple:

> Don't optimize for completeness first. Optimize for visual judgment first.

That means:
- define mood before components
- create hierarchy before decoration
- remove before adding
- let typography and composition do more work
- make brand show up beyond color
- avoid solving structure with more cards, borders, and UI containers

---

## What makes this different

A lot of prompt libraries tell a model to make something "beautiful," "modern," or "premium".
That usually produces familiar visual clichés.

This repo tries to make aesthetic quality more operational.

Instead of vague style goals, it emphasizes:
- hierarchy
- spacing rhythm
- typography load
- tonal restraint
- container reduction
- brand expression beyond color
- anti-template heuristics
- removal as a design move

In other words: it tries to turn taste into something an agent can actually use.

---

## Recommended setup

Use the files in this order:

1. `agents/brand-led-ui-designer.md` as the base system/agent prompt
2. `references/taste-reference.md` as supporting judgment and reference context
3. one of the briefs in `examples/` as a starting point
4. your own project context, constraints, and visual references

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

---

## Recommended prompt pattern

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

---

## Good use cases

- designing or critiquing dashboards
- improving generic fintech / crypto UI
- defining visual direction before building a component system
- reviewing a screen that feels “fine” but not distinctive
- training a design-focused agent to make better aesthetic tradeoffs
- pushing an existing interface toward stronger hierarchy and calmer surfaces
- critiquing an existing UI to identify what should be removed before anything gets added

---

## Not ideal for

- purely visual trend exploration
- one-shot image generation prompts with no product logic
- teams that only want token specs and component states
- situations where a mature brand system already dictates every visual decision

---

## Principles behind the repo

- Premium UI is usually quieter, not louder
- Strong hierarchy beats surface complexity
- Brand should survive in grayscale
- Too many cards usually means weak structure
- If removing 15–20% improves the design, it probably needed editing
- A strong interface should feel inevitable, not assembled
- Taste is often visible in what gets removed, not what gets added

---

## Repo philosophy

This repo is intentionally opinionated.

It assumes that many interfaces are not weak because they lack polish.
They are weak because they lack judgment.

So the goal here is not to add more UI.
The goal is to make better decisions.

---

## If you use this

Adapt it.
Tighten it.
Replace the references with your own.
Push the taste further.

The best version of this repo is probably the one that becomes more specific to your own standards over time.
