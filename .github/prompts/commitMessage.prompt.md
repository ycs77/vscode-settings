---
agent: agent
description: Generate Git commit messages
---

Optional changes hint: ${input:context:The context of the code changes}

- Generate high-resolution, technically-focused, precise, and concise Git commit messages in English based on the diff.
- Use imperative mood (e.g., 'Add feature' not 'Added feature').
- Prefer using the following descriptive types: Add, Update, Remove, Fix, Improve, Optimize.
- Do not include extraneous statements.
- Final optimize output to oneline message.
