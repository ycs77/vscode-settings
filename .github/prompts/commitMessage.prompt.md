---
agent: agent
description: Generate Git commit messages
---

# Git Commit Message Generator

## Guiding Principles

- Generate Git commit messages in English.
- Keep messages concise and focused on the core changes to help users and contributors understand what notable changes have been made in each commit.
- Use imperative mood (e.g., "Add feature" not "Added feature").
- Highlight the main purpose and impact of the changes without unnecessary details.
- DO NOT execute any Git commands or perform any Git operations.

## Change Types

Prefer using the following descriptive types:

- **Add** - for new features.
- **Update** - for updates in existing functionality.
- **Remove** - for removing features.
- **Fix** - for any bug fixes. Reference the reason from the context information if available.
- **Improve** - for enhancements to existing functionality (excluding performance).
- **Optimize** - for performance-related improvements.

If none of the above types are suitable, only then use other descriptive approaches such as **Refactor**, etc.

**Note on Adding Content:** When adding page/component content to a file that contains only a basic layout structure with empty content blocks, prefer using **Add** to describe the commit. Also use **Add** when the input context explicitly indicates that new functionality is being introduced. However, if the intent is unclear and the input context does not explicitly state it's a new feature, do not arbitrarily categorize it as adding functionality.

## Context Information

Context information: ${input:context:The context of the code changes}

When generating the commit message:
- If context information is provided, prioritize referencing it.
- If no context is provided, generate the commit message based on the actual Git code changes.
- If context conflicts with Git changes, carefully evaluate both sources and prioritize the one that more accurately reflects the actual intent and impact of the changes.
- For commits with multiple types of changes, choose the most significant or impactful change type for the subject line.
- For complex changes, create a concise summary in the subject line and provide details in the body if necessary.

## Output Format

- **Subject line**: Keep it concise and under 72 characters. Focus on clearly describing the core change. Aim for clarity over brevity.
- **Body**: Avoid including a body in most cases. The subject line should be sufficient to explain the change. Only include a body when:
  - The commit contains multiple distinct changes that need to be listed
  - Keep the body concise and avoid verbose technical details

  When including a body, separate it from the subject with a blank line and wrap lines at 72 characters.

Output only the commit message text without any additional explanation or formatting:

```plaintext
{subject_line}

{body_if_needed}
```
