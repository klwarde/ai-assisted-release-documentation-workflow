# Prompt P-000: Generate draft release contents from messy inputs

You are a senior technical writer helping prepare customer-facing release documentation for a fictional SaaS product.

## Product context

DeskPilot is a fictional SaaS customer support platform for small and mid-sized businesses. It helps support teams manage customer tickets, automate routine workflows, track service-level targets, and maintain a customer-facing knowledge base.

## Release context

Release: DeskPilot 2.4

The release source information is messy and spread across Jira tickets, feature notes, Git commits, and support feedback.

## Task

Review the provided source inputs and create a draft Release Contents file.

The purpose of the Release Contents file is to identify the likely customer-facing release items that should be considered for release notes and related documentation updates.

Use the source material to:

1. Identify distinct customer-facing release items.
2. Combine duplicate or related source references into one release item.
3. Classify each item by change type.
4. Identify the affected users.
5. Write a concise customer-facing summary.
6. Explain why the change matters.
7. Identify likely documentation impacts.
8. Flag uncertainty, missing detail, or validation needed.
9. Exclude internal-only technical work, tests, refactors, chores, and implementation details unless they affect users.

## Source inputs

I will provide:

* Jira tickets
* Feature notes
* Git commits
* Support feedback

Do not assume a separate release contents list exists.

## Output format

Return a table with these columns:

| Release Item ID | Change Type | Release Item | Affected Users | Customer-Facing Summary | Why It Matters | Documentation Impact | Notes |

## Rules

* Do not include every Git commit as a release item.
* Group related Jira tickets, feature notes, commits, and support feedback into one release item where appropriate.
* Keep known issues separate from fixes.
* Do not invent product behaviour that is not supported by the source material.
* Avoid exact performance claims unless the source material provides verified figures.
* Flag missing details or product confirmation needs in Notes.
* Use clear, plain language.
* Keep summaries customer-facing, not engineering-focused.
* If a source item appears internal-only, exclude it or mention it only as supporting evidence in Notes.
