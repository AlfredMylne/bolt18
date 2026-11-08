# CLAUDE.md

## Project purpose

This workspace supports the recovery and documentation of the original Bolt 18 fly-by-wire control system. The immediate goal is to reconstruct the original architecture before proposing any redesign or replacement.

## Working rules

- Preserve all original recovered project files without modification.
- Keep analysis separate from recovered source material.
- Distinguish confirmed facts, engineering inference, unverified assumptions, and missing information.
- Do not write replacement steering software during the initial recovery phase.
- Record source evidence for every important technical conclusion.
- Prohibit live hardware commissioning or controller flashing before the staged testing plan is approved.

## Directory roles

- `original/` — unmodified copies of recovered files
- `analysis/` — software, hardware, steering, propulsion, CAN, and I/O assessments
- `diagrams/` — architecture and wiring diagrams
- `tools/` — utilities for CoDeSys or CAN analysis
- `tests/` — simulation and hardware bench-test planning
- `development/` — experimental or non-production work only

## Required documentation outputs

- System architecture
- Hardware inventory
- Software architecture
- I/O mapping
- CAN-bus message catalogue
- Steering control description
- Electrical wiring diagrams
- Safety and failure-mode assessment
- Testing procedures
- Outstanding technical questions

## Recovery priority

1. Confirm the original CoDeSys project, PLC target, hardware, and firmware requirements.
2. Identify controller inputs, outputs, and safety behaviour.
3. Analyse CAN traffic and message definitions.
4. Reconstruct electrical interfaces and documentation.
5. Produce a safe staged testing plan.

## Required inputs

Ask the user to provide the original project archive or the specific files below if direct Dropbox access is not available:

- `Bolt18_0_01.pro`
- `Bolt18_0_01.SYM`
- `Bolt18_0_01.SDB`
- `Bolt18_0_0100005533r.ci`
- `Bolt18_0_0100005533s.ci`
- `BoltCANdatas.dbc`
- `BoltCANdatas.ini`
- `TorqSpeedCtrl_PDU2_1_0.dbc`
- `Livorsij1939Map.rtf`
