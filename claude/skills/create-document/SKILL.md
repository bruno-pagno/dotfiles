---
name: create-document
description: "Create or reorganize an engineering task document using a concise status, decisions, risks, and implementation layout. Use when the user asks for a project document like the Airstream OpenSearch sink document; do not substitute it for a full technical design spec."
---

# Write a Project Document

Create a document that lets a reader answer, in order: Why does this work matter? What is done? What remains? How will success be verified? What was decided? What could still go wrong? How is it implemented?

Use the following section order. Keep the headings, adapting "Affected systems" to the domain when useful, such as "Affected clusters." If a section has no entries yet, say so briefly rather than inventing content.

1. `# <Task title>` — Add owner, tracker, and discussion channel when known.
2. `## Summary` — State the problem, impact, and proposed or delivered change in a short paragraph.
3. `## Current status and next step` — Distinguish merged code, deployment, and real-world adoption. Name the next concrete action and owner when known.
4. `## Acceptance criteria` — Use `### Completed` and `### Pending validation`. Keep only checks that establish the task's outcome. Link evidence for completed checks; do not infer runtime success from a merged PR.
5. `## Affected systems` — Name the projects, services, clusters, or users in scope and the source and date of any counts.
6. `## How it works today` — Explain the current path and the specific limitation being addressed. Add a diagram only if it makes the flow easier to understand.
7. `## The change` — Show the new path and what an adopter must change.
8. `## Decisions` — Record each material choice, its reason, and the main alternative. Summarize resolved research here and put detailed investigation in the implementation guide.
9. `## Risks` — List only current, material risks and the check or action that addresses each. Move resolved build or review concerns into the implementation guide as history.
10. `## Implementation guide` — Keep the steps in this document by default. A separate linked document is fine when the guide becomes long or the user requests it; preserve the full guide when moving it.
11. `## References` — Link primary sources, code, and supporting research.
12. `## Pull requests` — Link relevant PRs and state their verified status. Write "None yet" if applicable.

## Writing rules

- Ground status, test results, counts, and PR state in evidence. Label unknowns explicitly.
- Separate observed results from predictions and planned validation.
- Keep the main document concise; put commands, file-by-file instructions, and historical investigations in the implementation guide.
- Use precise timing and outcome language. A passing build does not prove a deployed job works.
- Update stale wording when work moves from planning to merged code to real-world adoption.
- Preserve unrelated content and comments when reorganizing an existing document.
- Use the document destination the user requested. Do not create a second document unless the user requests the split.
