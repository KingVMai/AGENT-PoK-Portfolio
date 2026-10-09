# Architecture overview

Agent PoK is designed as a local bridge between an AI conversation and a selected development workspace.

## Components

1. **Chrome extension (Manifest V3):** browser-side interaction, task transport, user controls and execution status.
2. **Native Messaging bridge:** controlled communication between the extension and an installed local host.
3. **Python execution host:** structured workspace file operations, trusted-development commands and status reporting.
4. **Workspace documentation:** maintained project-level source of truth for continuity across sessions.
5. **Tests and diagnostics:** regression tests and manual acceptance checks.

## Web dashboard (LAN observer)

A Python HTTP dashboard supplies browser-accessible monitoring. The canonical server listens on localhost, while a separate GET/HEAD-only observer exposes dashboard data on a trusted private LAN interface. systemd user units start services automatically and restart them on failures. Private LAN address changes may require reconfiguration. This is not a public web service and has no confirmed end-user login mechanism.

## Engineering considerations

- Explicit workspace selection and machine-readable task/result messages.
- Idempotency and acknowledgement guards where delivery ambiguity could otherwise cause duplicate execution.
- Recovery-first approach: retain verified working versions, investigate failures and avoid automatic destructive cleanup.
- Visible task results and human control points.

## Important limits

Browser UI integrations depend on third-party DOM structures and can require maintenance when the interface changes. Trusted local command execution is not an operating-system sandbox. This private-use project has not undergone an independent security certification.

Detailed implementation and source code are intentionally not distributed in this portfolio.
