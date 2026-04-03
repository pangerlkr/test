---
name: iterative-bugfix-on-single-script
description: Workflow command scaffold for iterative-bugfix-on-single-script in test.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /iterative-bugfix-on-single-script

Use this workflow when working on **iterative-bugfix-on-single-script** in `test`.

## Goal

Rapid, repeated fixes and improvements to a specific script file, often to address a bug or security issue.

## Common Files

- `scripts/dev_server.js`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Identify issue in script (e.g., security vulnerability).
- Make a fix and commit changes to the script file.
- Test the fix; if incomplete, make further adjustments.
- Repeat commit(s) to the same script file until the issue is resolved.

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.