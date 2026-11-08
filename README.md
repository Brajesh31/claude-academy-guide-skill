# claude-academy-guide-skill

A Claude Code skill for helping users find relevant learning paths, courses, tutorials, and practical exercises for Claude products and workflows.

## Overview

This skill is designed for questions where the user wants to learn how to use Claude or apply AI to a particular task. It encourages matching the learning recommendation to the user's actual goal instead of suggesting generic training material.

It is useful for onboarding, self-paced learning, team enablement, and planning structured training.

## When to Use It

Use this skill when users ask:

- How to get started with Claude or a Claude product.
- How to use a particular feature or workflow.
- What Claude can do for a specific task.
- How to learn skills, projects, artifacts, connectors, or MCP workflows.
- How to train a team, class, or organization.
- Which tutorial or learning path best matches a goal.
- How to prepare onboarding or training material.

It is intended for learning-oriented questions. When a user is already in the middle of a task and simply wants the task completed, prioritize completing the task.

## What It Does

- Identifies the user's learning objective.
- Matches the objective to relevant course or tutorial topics.
- Distinguishes beginner, intermediate, and advanced learning needs.
- Recommends learning material only when the match is meaningful.
- Connects conceptual learning with practical use cases.
- Avoids inventing course names, features, or learning resources.

## Installation

```bash
git clone https://github.com/Brajesh31/claude-academy-guide-skill.git ~/.claude/skills/academy-guide
```

## Usage

Invoke the skill when a learning recommendation is needed:

```text
/academy-guide
```

Describe the product or feature, the learner's current experience, and the outcome they want to achieve.

## Recommendation Workflow

1. Clarify what the learner wants to accomplish.
2. Identify the relevant Claude product, feature, or workflow.
3. Determine the learner's current level and context.
4. Find a course or tutorial that directly addresses the goal.
5. Explain why the material is relevant.
6. Suggest a practical exercise that reinforces the learning.
7. If no strong match exists, say so instead of forcing a recommendation.

## Learning Path Structure

A useful learning path can include:

| Stage | Focus | Expected Outcome |
|---|---|---|
| Foundation | Core concepts and terminology | Understand the feature |
| Guided practice | Follow a focused tutorial | Complete a basic workflow |
| Applied practice | Use the feature on a real task | Build practical confidence |
| Advanced use | Explore integrations and constraints | Handle more complex workflows |
| Team adoption | Share conventions and examples | Use the workflow consistently |

## Team and Classroom Enablement

For group training, define the audience, learning objectives, session duration, and expected hands-on output. Use short demonstrations followed by guided exercises. Include a clear way to evaluate whether participants can apply the workflow independently.

## Quality Checklist

- The recommendation directly matches the user's question.
- The course or tutorial actually exists.
- The learner's level is considered.
- The recommendation includes a reason, not just a title.
- Practical exercises reinforce the stated objective.
- Unavailable or uncertain learning resources are not presented as confirmed.

## Repository Contents

- `SKILL.md`: Main skill instructions and learning-resource matching workflow.
- `README.md`: Usage, recommendation process, and learning-path guidance.

## Maintenance

Keep the matching criteria accurate as products and learning catalogs change. Verify course availability before presenting a recommendation as current.
