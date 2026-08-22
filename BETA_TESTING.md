# HarnessDesk Beta Testing Guide

Thanks for testing HarnessDesk.

The most useful feedback is not only whether the application launches, but whether a real native Agent session behaves correctly through a normal coding workflow.

## Suggested smoke test

### 1. Launch and setup

- Install HarnessDesk.
- Launch it from the Start Menu or desktop shortcut.
- Confirm the app opens normally without requiring a terminal window.
- Confirm your installed Codex / Claude Code integration is detected as expected.

### 2. Project workflow

- Add or open a Git-backed test project.
- Confirm the project appears in the sidebar.
- Close and reopen HarnessDesk and confirm the project/session selection restores sensibly.

### 3. Native Agent session

Test at least one Agent you already use natively.

- Open an existing native session, or create a new one.
- Send a short prompt.
- Confirm the response streams/completes normally.
- Confirm headings, lists, code blocks and line breaks render correctly.
- Continue the same session after restarting HarnessDesk.

### 4. Changes / Diff

Ask the Agent to make a harmless change in the test project.

- Confirm the Changes panel updates.
- Open the changed file.
- Confirm the Diff is readable and corresponds to the real Git working tree.

### 5. Project Context

If you use native project instructions:

- Codex: check `AGENTS.md` behavior.
- Claude Code: check `CLAUDE.md` / `.claude/CLAUDE.md` behavior.

HarnessDesk should use the provider-native project context rather than silently copying those files into its own database.

## What to report

Please report issues through this repository's Issues tab and include:

1. HarnessDesk version
2. Windows version
3. Agent and Agent version if known
4. Exact reproduction steps
5. Expected result
6. Actual result
7. Screenshot/video if useful
8. Diagnostics information if available

## Privacy reminder

This is a public repository. Before posting logs or screenshots, remove:

- API keys / authentication tokens
- passwords
- personal information
- private source code you do not want to publish
- private repository names/paths if sensitive

For reproducible bugs, a minimal test project is preferred over sharing a private production repository.
