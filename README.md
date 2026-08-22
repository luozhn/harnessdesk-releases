# HarnessDesk Beta

HarnessDesk is a Windows desktop workspace for using multiple native Coding Agents from one interface.

This repository is the **public Beta download and feedback repository** for HarnessDesk. The main development/source repository is separate and remains private.

## What HarnessDesk does

HarnessDesk provides one desktop workspace for projects and native Agent sessions while keeping each Agent in control of its own execution loop, tools, authentication and authoritative session history.

Current Beta integrations include:

- Codex
- Claude Code
- Project / native Session management
- Conversation history display and continuation
- Markdown-rendered Agent responses
- Changes / Diff view
- Project Context support (`AGENTS.md` / `CLAUDE.md` where applicable)
- History search where the native Agent exposes a bounded history interface
- Native slash-command / skill surfaces where supported

## Download

Use the **Releases** section on this repository to download the latest Windows installer.

> The first public Beta package is being prepared. If there is no Release listed yet, check back after the initial package is uploaded.

## Before installing

HarnessDesk is currently a **Beta build**.

- Use Git or another version-control system for important projects.
- The Windows installer is currently unsigned. Windows SmartScreen may display an "Unknown publisher" / reputation warning.
- HarnessDesk does not replace Codex or Claude Code. To use an Agent, install and sign in to that Agent on your own computer first.
- HarnessDesk does not store Codex / Claude authentication tokens as its own credentials.

## Basic usage

1. Install HarnessDesk.
2. Make sure the native Agent you want to use (Codex and/or Claude Code) is installed and authenticated.
3. Open HarnessDesk.
4. Add/open a project folder.
5. Select or create a native Agent session.
6. Use the Conversation view to continue work and the Changes panel to inspect file modifications.

See [BETA_TESTING.md](./BETA_TESTING.md) for the recommended test checklist.

## Known limitations

See [KNOWN_ISSUES.md](./KNOWN_ISSUES.md).

Important current limitations include:

- Stable Codex full-text history indexing is not available because the stable native interface does not currently provide the bounded/pageable contract HarnessDesk requires for indexing. Opening an individual Codex session can still display its native history snapshot.
- Full Codex TUI slash-command parity is not available through the current stable App Server surface.
- The installer is not code-signed yet, so SmartScreen/reputation warnings are expected on some systems.
- Cross-version upgrade behavior is still Beta-level and needs broader real-machine testing.

## Report a bug

Please use this repository's **Issues** tab.

For a useful report, include:

- HarnessDesk version
- Windows version
- Agent used (Codex / Claude Code)
- What you expected
- What actually happened
- Reproduction steps
- Screenshot if relevant
- HarnessDesk Diagnostics information when available

Do **not** post passwords, API keys, authentication tokens, private repository contents or other secrets in a public Issue.

## Beta status

HarnessDesk is under active development. Public Beta feedback may result in UI, protocol and packaging changes between releases.
