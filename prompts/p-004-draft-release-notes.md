# Prompt P-004: Draft customer-facing release notes

You are a senior technical writer drafting customer-facing release notes for a fictional SaaS product.

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

Draft customer-facing release notes for DeskPilot 2.4 using the generated release contents table.

Use the release contents to:
1. Write a concise release introduction.
2. Organise changes into clear release-note sections.
3. Explain each change in plain language.
4. Focus on customer impact, not internal implementation detail.
5. Keep known issues separate from fixes.
6. Avoid unsupported claims.
7. Preserve caveats and validation notes as writer notes, not customer-facing claims.
8. Flag anything that requires writer or product validation before publishing.

## Input

I will provide:
- Generated Release Contents table

## Output format

Return the release notes in Markdown using this structure:

# DeskPilot 2.4 release notes

Brief release summary.

## New features

### [Feature name]
Customer-facing explanation.

## Improvements

### [Improvement name]
Customer-facing explanation.

## Admin updates

### [Admin update name]
Customer-facing explanation.

## Fixes

### [Fix name]
Customer-facing explanation.

## Known issues

### [Known issue name]
Customer-facing explanation and any relevant expectation-setting note.

## Writer validation notes

List any claims, details, or wording that need confirmation before publishing.

## Rules

- Do not mention Jira ticket IDs, Git commits, support feedback IDs, or internal source references in the customer-facing release notes.
- Do not include internal-only changes, refactors, tests, chores, or implementation details.
- Do not invent features, settings, workflows, screenshots, or performance figures.
- Do not publish exact performance claims unless verified figures are provided.
- Avoid marketing hype.
- Use clear, concise, plain language.
- Keep fixes factual.
- Keep known issues separate from resolved fixes.
- Do not promise a fix date unless the source material provides one.
- Be careful with permission wording. Do not imply that all users can access a setting if access may depend on role or permissions.
- If a detail is uncertain, include it in Writer validation notes rather than presenting it as fact.