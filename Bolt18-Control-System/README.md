# Bolt 18 Control System Recovery

This workspace documents the recovery, investigation, and controlled analysis of the original Bolt 18 fly-by-wire control system.

The objective is to understand the original design before any modification, replacement, or redevelopment work is considered.

## Scope

- Recover and preserve original project materials
- Identify controller hardware and software architecture
- Examine steering, propulsion, and CAN-bus functions
- Inspect electrical documentation and interface definitions
- Produce a documented engineering baseline
- Prepare safe recovery and testing procedures

## Repository conventions

- `original/` is reserved for recovered source material and must remain unchanged.
- `analysis/` contains structured engineering assessments and conclusions.
- `diagrams/` contains architecture and wiring diagrams.
- `tools/` contains scripts or utilities for analysis of CoDeSys and CAN data.
- `tests/` contains simulation and bench-test planning.

## Important note

Original proprietary project files are not committed to this repository until repository access and backup arrangements have been confirmed. The project structure is created here, but recovered source files should be added only after confirmation.

## Opening in VS Code

1. Open the repository root in VS Code.
2. Open the `Bolt18-Control-System` folder.
3. Use the Explorer to review the analysis and documentation files.
4. Place recovered source material under `original/` only after confirming the correct backup and access process.

## Initial investigation status

This project is currently in the recovery and documentation phase. No replacement steering logic or hardware redesign is being created at this stage.

## Recovered source inventory

The original project archive was located in `D:\Dropbox\TIVA\AC_Bolt\MDI_boat` and the relevant files were preserved under `original/` without modification.

See the detailed preliminary report here:
- [analysis/original-control-system-recovery-report.md](analysis/original-control-system-recovery-report.md)

## Dashboard prototype

A first dashboard mock-up for monitoring system health, steering, propulsion, safety and CAN activity is available here:
- [tools/dashboard/bolt18-dashboard.html](tools/dashboard/bolt18-dashboard.html)
- [tools/dashboard/README.md](tools/dashboard/README.md)
