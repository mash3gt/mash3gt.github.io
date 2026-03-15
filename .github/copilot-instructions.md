# Copilot Repository Instructions

## Release Safety

- Do not run `git push` from the agent.
- Stop after commit and wait for user confirmation.
- The user performs push and final publish steps.

## Planning Gate

- Before implementation, create an implementation plan and wait for user approval.
- Start implementation only after explicit approval.

## Long-Run Checkpoint

- If work continues for more than 5 minutes, pause and share the current status.

## Review Gate

- After implementation, show a concise diff summary.
- Wait for explicit user approval before commit or any release-related command.

## Verification

- Run verification after implementation is complete.
- For web apps, also perform deployment and UI checks.
- Update TODO.md if any planned items were completed.
