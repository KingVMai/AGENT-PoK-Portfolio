# Agent PoK

**A local AI-to-workspace execution companion** — a KingVMai portfolio project.

**Status:** Working private prototype · Chrome-first · Source code not publicly distributed

Agent PoK connects an AI conversation with a selected local development workspace. It is designed to reduce repetitive copying of terminal commands, file changes and diagnostic output, while keeping work inspectable and recoverable.

## The problem

AI-assisted development becomes slow when every file inspection, script execution and test result must be manually copied between the browser and a computer. Long conversations can also make project continuity difficult.

## What I built and validated

- A Chrome Manifest V3 extension communicating with a local Python Native Messaging host.
- Structured task requests and machine-readable results for selected workspace operations.
- Local file inspection and editing workflows, command execution for trusted development and validation through tests.
- Workspace activity, diagnostics, status and continuity controls.
- Project-state continuity using maintained documentation and an Initialize / Resume workflow.
- A regression suite with **637 tests passing** in the recorded October 2026 development snapshot.

## Architecture (high level)

```text
Human + ChatGPT
      |
Chrome extension (JavaScript / Manifest V3)
      |
Native Messaging connection
      |
Local Python host
      |
Selected development workspace
      |
Structured execution result -> conversation
```

[Architecture details](docs/ARCHITECTURE.md) · [Validation and limits](docs/VALIDATION.md) · [Demo walkthrough](docs/DEMO.md)

## My contribution

**Project owner and workflow designer:** defined the product concept, requirements, architecture decisions, desired user experience, acceptance criteria and safety trade-offs. Coordinated AI-assisted implementation, investigated failures, tested real workflows and drove iterative regression fixes.

This is an **AI-assisted software engineering and quality assurance project**, not a claim that every line of source code was manually written.

## Screenshots and demo

Curated, privacy-checked screenshots and a short video demonstration are being prepared. This portfolio repository will be updated with visual evidence before the link is used in a CV.

## Current scope

Agent PoK is a personal local tool, not a public extension or hosted service. The source repository remains private. This showcase describes the project without releasing its internal engine, personal logs or credentials.

**KingVMai** · Project portfolio · 2026
