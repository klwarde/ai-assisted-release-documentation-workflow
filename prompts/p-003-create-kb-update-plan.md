# Prompt P-003: Create KB update plan

You are a senior technical writer planning knowledge base updates for a fictional SaaS product release.

## Product context

DeskPilot is a fictional SaaS customer support platform for small and mid-sized businesses. It helps support teams manage customer tickets, automate routine workflows, track service-level targets, and maintain a customer-facing knowledge base.

## Release context

Release: DeskPilot 2.4

Release theme: Faster support workflows, clearer automation controls, and improved ticket visibility.

Target users:
- Support agents
- Support team leads
- Workspace admins
- Customers who submit tickets or use the help centre

## Task

Create a draft knowledge base update plan using the generated release contents table.

Use the release contents to:
1. Identify existing help articles that may need updates.
2. Suggest new articles only if clearly needed.
3. Explain what needs to change in each article.
4. Assign a priority.
5. Decide whether the update should be included, deferred, or handled with caution.
6. Flag details that require writer, product, or SME validation.

## Input

I will provide:
- Generated Release Contents table

## Output format

Return a Markdown table with these columns:

| KB Plan ID | Article Title | Article Type | Related Release Items | Priority | Update Required | Writer Decision | Validation Notes |

## Priority guide

Use:
- High: must be updated before or at release because the UI, workflow, permissions, or customer expectations have changed.
- Medium: should be updated soon, but the release note may be enough temporarily.
- Low: release note only may be sufficient unless the existing article already covers this area.

## Writer decision guide

Use:
- Include
- Defer
- Include with caution
- Needs confirmation

## Rules

- Do not suggest a KB update for every minor fix automatically.
- Prioritise articles affected by new features, UI changes, permissions, reporting changes, SLA behaviour, and known issues.
- Use the documentation impact notes in the generated release contents table.
- Keep article titles practical and customer-facing.
- Do not invent existing article names if the source does not provide them; suggest likely article titles instead.
- Flag missing details rather than inventing them.
- Do not promise future fixes or undocumented behaviour.
- Keep known issues separate from resolved fixes.