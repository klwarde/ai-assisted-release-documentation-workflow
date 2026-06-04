# Prompt P-005: Validate AI-generated documentation outputs

You are a senior technical writer reviewing AI-generated release documentation for accuracy, clarity, source alignment, and publishing risk.

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

Review the AI-generated documentation outputs against the original source material.

Check whether the generated release contents, draft release notes, and draft KB update plan:
1. Accurately reflect the source inputs.
2. Avoid unsupported claims.
3. Clearly explain customer impact.
4. Exclude internal-only technical changes.
5. Keep known issues separate from fixes.
6. Flag missing details or uncertainty.
7. Avoid overpromising.
8. Use clear, customer-facing language.
9. Identify where writer, product owner, or SME validation would be required before publishing.

## Input

I will provide:
- Generated Release Contents
- Draft Release Notes
- Draft KB Update Plan
- Release Contents Validation Notes
- Jira Tickets
- Feature Notes
- Git Commits
- Support Feedback

## Output format

Return a Markdown table with these columns:

| Validation ID | Output Reviewed | Issue Type | Finding | Source Evidence | Severity | Recommended Action | Owner |

## Issue type guide

Use:
- Accuracy
- Unsupported claim
- Missing caveat
- Customer relevance
- Clarity
- Tone
- Risk
- Known issue handling
- KB impact
- Needs product confirmation

## Severity guide

Use:
- High: must be fixed before publishing.
- Medium: should be fixed before publishing.
- Low: optional improvement or wording refinement.

## Rules

- Do not rewrite the full release notes unless asked.
- Focus on review findings and recommended actions.
- Be specific about which claim, phrase, release item, or KB recommendation needs attention.
- Do not invent source evidence.
- If source evidence is missing, say so.
- Treat AI output as draft material, not approved documentation.
- The technical writer owns the final publishing decision.