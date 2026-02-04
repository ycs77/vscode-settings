---
agent: agent
description: Generate Git commit messages
---

Execute commit-message skill with this context: "${input:context:The context of the code changes}"

CRITICAL: Follow the skill's process exactly as documented, using terminal commands for all git operations. DO NOT use any built-in tools like get_changed_files to read file changes.
