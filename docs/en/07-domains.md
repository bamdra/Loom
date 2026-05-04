# 🌐 Product vs Dev — two ways to think

## What domains are

Loom has two work domains — **Product** and **Dev**. You'll find the toggle at the top of the Agents panel.

**Product** is for work that starts with a need and ends with something a person can see and touch — requirements, specs, wireframes, prototypes, design handoff.

**Dev** is for work that starts with a spec or a bug and ends with verified, running code — stack detection, implementation planning, code writing, test verification.

## When to use which

| Your situation | Domain |
|---------------|--------|
| "I need to figure out what to build" | **Product** |
| "I know what to build — now build it" | **Dev** |
| "The design is done, time to code" | **Dev** |
| "I want a prototype to show someone" | **Product** |
| "There's a bug in the login page" | **Dev** |
| "We need to rethink the user flow" | **Product** |

## How agents change behavior

When you switch domains, each agent role shifts its focus:

| Role | Product mode | Dev mode |
|------|-------------|---------|
| **Analysis** | Clarify user goals, acceptance criteria, constraints | Triage request, identify affected modules, scope risk |
| **Design** | Spec, page flows, component structure, data model sketch | Implementation plan, file-level breakdown, interface contracts |
| **Implement** | Prototypes, HTML/CSS/JS, React components | Write or modify production code, follow conventions |
| **Review** | Completeness, visual fidelity, interaction correctness | Correctness, style, edge cases, security rubric |

## Switching domains

Click the **Product** or **Dev** button at the top of the Agents panel. The switch takes effect immediately and is remembered across sessions.

<!-- screenshot: product-dev-toggle -->

## A typical project flow

Most projects use both domains:

1. **Start in Product** — figure out what to build
   - "I want a tool that does X"
   - Analysis clarifies goals, Design proposes structure
   - You get a spec and maybe a prototype

2. **Switch to Dev** — actually build it
   - The spec becomes the implementation target
   - Implement writes code, Review checks it
   - You get working software

3. **Back to Product** (if needed) — iterate on the experience
   - "The flow feels off, let's rethink step 3"
   - Back to Product thinking, then Dev again

The switch is instant. Your agents adapt. Your project files stay the same.
