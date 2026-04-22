# Atomic Habits — Claude Skills

![image](./image/logo.png)

A personal knowledge system that converts the frameworks from James Clear's
*Atomic Habits* into actionable skills for Claude. Instead of reading the book
again when you need it, you describe your situation and Claude applies the
right framework automatically.

---

## How it works

Each `.md` file in `/skills` is not a summary — it's a behavioral instruction
for Claude. When you describe a real situation, Claude reads the relevant skill
and responds within that framework without you having to ask for it explicitly.

You never say *"apply the 1% rule"*. You just say *"I want to start running
but always quit after two weeks"* and Claude figures out what applies.

---

## Folder structure

```
Atomic Habits/
│
├── README.md                   # This file
│
├── skills/                     # One skill per concept
│   ├── one_percent_rule.md
│   ├── systems_over_goals.md
│   └── ...                     # More skills as chapters are processed
│
├── raw-notes/                  # Original notes per chapter (your own words)
│   ├── cap01_one_percent.md
│   ├── cap02_systems_over_goals.md
│   └── ...
│
└── context/
    └── my_profile.md           # Your current habits, goals, personal context
```

---

## Skills available

| File | Concept | Activate when... |
|---|---|---|
| `one_percent_rule.md` | Marginal gains compounded | Feeling overwhelmed, no visible progress, want to start small |
| `systems_over_goals.md` | Process over outcome | Goal-fixated, lost motivation, keep restarting the same thing |

*More skills added as chapters are processed.*

---

## Claude Code setup

1. Point your project context to this folder
2. Add this to **Instructions**:

```
You have access to my Atomic Habits skills folder. When I describe a situation,
read the relevant skill files and apply the framework. Be direct and actionable.
Don't mention the files explicitly — just apply the concepts.
```

3. Drop any new `.md` into `/skills` and it's available immediately.

---

## Example prompts to try

These are plain descriptions — no need to mention the book or any concept:

- *"I want to start exercising but every time I try I quit after 2 weeks"*
- *"I set a goal to read 20 books this year but already lost motivation"*
- *"I want to change my mornings but don't know where to start"*
- *"I've been trying to get my finances in order for years and nothing sticks"*
- *"I keep restarting the same habits over and over"*

---

## How to add a new skill

1. Paste your raw chapter notes into a conversation with Claude
2. Ask: *"Convert this into a skill using the same format as the existing ones"*
3. Save the output to `/skills/concept_name.md`
4. Add a row to the skills table above

---

## context/my_profile.md

This file is the most important one you're not using yet. It tells Claude
who you specifically are — your current habits, recurring struggles, goals,
and daily routine. Without it, Claude applies the frameworks generically.
With it, Claude applies them to your actual life.

Suggested sections:

```markdown
# My Profile

## Current habits (what's actually working)
## Recurring struggles (what never sticks)
## Goals for this year
## Daily routine (rough sketch)
## Areas I want to improve
```