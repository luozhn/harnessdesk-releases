# Known Issues and Beta Limitations

This document tracks public-facing limitations that are relevant to Beta testers.

## Windows installer signing

The current Beta installer is not code-signed. Windows SmartScreen or reputation-based protection may warn that the publisher is unknown.

This warning is expected for the current Beta packaging and does not by itself indicate that the file was modified. Release notes should include a SHA-256 checksum so testers can verify the downloaded installer.

## Codex history indexing

HarnessDesk can open an individual stable Codex session and display a native conversation snapshot through the official native interface.

Stable Codex full-text history indexing is intentionally unavailable because the stable native interface does not currently provide the bounded/pageable history contract HarnessDesk requires for safe background indexing.

HarnessDesk does not work around this by reading or modifying Codex private databases.

## Codex slash commands

HarnessDesk exposes verified native commands available through the current stable Codex App Server surface. Complete TUI command parity is not guaranteed.

## Cross-version upgrades

Same-version install/reinstall has been exercised during development. Broader cross-version upgrade behavior still needs testing across more machines and future Beta versions.

## Beta compatibility

HarnessDesk integrates with native Agent products that may evolve independently. A future Codex or Claude Code update may temporarily affect discovery, session APIs, commands or UI mappings until HarnessDesk is updated.

If something worked before an Agent update and stops working afterward, include the Agent version in the bug report.
