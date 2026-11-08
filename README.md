# Academy Guide Skill

A focused skill for recommending relevant learning materials when a user is asking how to use a Claude product or workflow. It prioritizes intent matching, accurate links, current catalog data, and restraint. A learning recommendation supplements a direct answer; it does not replace the answer.

## What This Skill Does

- Detects learning-oriented questions about Claude products and workflows.
- Distinguishes a request to learn from a request to complete an active task.
- Matches the user's goal to a course, tutorial, use case, product hub, or resource library.
- Recommends only resources that directly match the user's intent.
- Uses exact catalog URLs rather than constructing links from assumed titles.
- Avoids outdated course lists and invented learning resources.
- Keeps recommendations brief and optional.

## When to Use It

Use the skill when a user asks how to get started, how a feature works, what a product can do, how to learn a workflow, or how to prepare training and onboarding materials.

Do not use it merely because an active task happens to involve a Claude feature. When the user wants the task completed, prioritize completing the task instead of diverting them to a tutorial.

## Installation

~~~bash
git clone https://github.com/Brajesh31/claude-academy-guide-skill.git ~/.claude/skills/academy-guide
~~~

## Usage

Invoke:

~~~text
/academy-guide
~~~

Provide the learning objective, product or feature, learner level, and context. The skill instructions require a current catalog check before naming a specific learning item.

## Recommendation Workflow

1. Answer the user's immediate question first.
2. Determine whether the intent is genuinely educational.
3. Identify the relevant product surface or workflow.
4. Check the current catalog data when it is available and fresh.
5. Match the user's goal to the strongest available item.
6. Use the exact item URL returned by the catalog.
7. Recommend no more than one or two strong matches.
8. If no strong match exists, use the specified fallback only when the user clearly wants learning material.
9. Do not invent course, tutorial, use-case titles, or URLs.

## Catalog Freshness

The skill is intentionally designed not to embed a static course list. Learning catalogs change, so a saved list of item names and URLs can become stale.

Before recommending individual items, verify that the catalog can be fetched, that the response is valid JSON, and that its freshness metadata is current. If it is stale, malformed, unavailable, or missing required URL information, do not name specific course items. Use the fallback behavior described in SKILL.md.

## Recommendation Quality Checklist

- Is the user asking to learn rather than asking for an immediate task to be performed?
- Does the recommendation directly match the stated intent?
- Has the current catalog been checked for item names and exact URLs?
- Is the resource available to the intended audience?
- Is the item gated, and is that disclosed when relevant?
- Is the explanation brief and non-pushy?
- Would silence be better than a weak recommendation?

## Included Resource

- [Catalog verification checklist](resources/catalog-verification-checklist.md)

## Limitations

This skill does not contain a static course catalog. It cannot guarantee that a course will remain available, ungated, or unchanged. Catalog records must be checked at recommendation time.

## Repository Structure

~~~text
claude-academy-guide-skill/
├── SKILL.md
├── README.md
├── LICENSE
└── resources/
    └── catalog-verification-checklist.md
~~~

## License

Released under the MIT License. Copyright (c) 2026 Brajesh Kumar. See the root `LICENSE` file for the complete terms.
