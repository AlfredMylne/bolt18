# BOLT 18 — ORIGINAL CONTROL SYSTEM RECOVERY REPORT

## 1. Inventory of recovered files

The recovered source archive is available at:

- `D:\Dropbox\TIVA\AC_Bolt\MDI_boat`

The following principal project materials were located and preserved in the local workspace under `original/`:

### CoDeSys project files
- `MDI_boat\IOXp_CodeR1\Bolt18_0_01.pro`
- `MDI_boat\IOXp_CodeR1\Bolt18_0_01.SDB`
- `MDI_boat\IOXp_CodeR1\Bolt18_0_01.SYM`
- `MDI_boat\IOXp_CodeR1\Bolt18_0_0100005533r.ci`
- `MDI_boat\IOXp_CodeR1\Bolt18_0_0100005533r.ri`
- `MDI_boat\IOXp_CodeR1\Bolt18_0_0100005533s.ci`
- `MDI_boat\IOXp_CodeR1\Bolt18_0_01.wibu.ini`

### Development and test projects
- `MDI_boat\IOXp_Test\CAN_ALL_esx_ioxp1.pro`
- `MDI_boat\IOXp_Test\can_Livorsi_esx_ioxp.pro`
- `MDI_boat\IOXp_Test\LivorsiUQM_esx_ioxp1.pro`
- `MDI_boat\IOXp_Test\UQM_esx_ioxp1.pro`
- `MDI_boat\IOXp_Test\UQM_esx_ioxp2.pro`

### CAN-bus and messaging files
- `MDI_boat\BoltCANdatas.dbc`
- `MDI_boat\BoltCANdatas.ini`
- `MDI_boat\TorqSpeedCtrl_PDU2_1_0.dbc`
- `MDI_boat\TorqSpeedCtrl_PDU2_1_0.ini`
- `MDI_boat\Livorsij1939Map.rtf`

### Controller documentation and references
- `MDI_boat\SensorWks\CoDeSys.doc`
- `MDI_boat\SensorWks\esx-iox_datenblatt_en.pdf`
- `MDI_boat\SensorWks\ESX-TC3 Getting Started(2.03r0).chm`
- `MDI_boat\SensorWks\repositoryarchive_3s_en.pdf`
- `MDI_boat\SensorWks\TC3_TC3G_User_Manual.chm`

### Electrical and interface material
- `MDI_boat\12_7_2012-MYD0703-Bolt 18 MK2.easm`
- `MDI_boat\Connectors\Deutsch\...`
- `MDI_boat\Livorsi\...` related operator interface and control documents
- `MDI_boat\CANInformation\...` supporting CAN/J1939 reference material

## 2. Identification of controller hardware

The recovered project names and associated documentation strongly indicate that the original controller is an STW ESX-IOXp unit running CoDeSys-based logic.

Supporting evidence:
- Folder naming and project file naming use `IOXp` and `esx_ioxp` naming conventions.
- `SensorWks` contains STW ESX-IOXp documentation and CoDeSys references.
- `CoDeSys.doc` and `ESX-TC3 Getting Started(2.03r0).chm` are present in the recovery archive.

Preliminary conclusion:
- Controller family: STW ESX-IOXp
- Development environment: CoDeSys 2.3 / TC3-era compatible toolchain
- Further confirmation is required from the project metadata and controller-specific configuration files.

## 3. Assessment of the original CoDeSys project

The following file types are present and consistent with a real CoDeSys PLC project:
- `.pro` project file
- `.SDB` symbol database
- `.SYM` symbol definitions
- `.ci` compile/target binary element files
- `.ri` runtime-related files
- `.wibu.ini` for target communication and boot configuration

This indicates a working control project rather than a partially recovered or synthetic mock-up.

Preliminary assessment:
- The original project is likely a PLC application for steering and propulsion control using the ESX-IOXp hardware.
- The presence of `UQM` and `Livorsi` development variants suggests the controller was adapted and tested against alternative propulsion and operator-interface modules.
- No software modification is being performed at this stage; the original project remains preserved for analysis.

## 4. Preliminary steering architecture

The steering-work investigation is currently limited to evidence from the recovered project package and documentation. No direct inspection of the internal PLC logic has yet been performed in the current workspace.

Evidence gathered to date:
- `IOXp_CodeR1` contains the original project named `Bolt18_0_01`.
- `IOXp_Test` contains separate steering/control variants for `Livorsi`, `UQM`, and combined `LivorsiUQM` projects.
- The naming of the test projects suggests that operator inputs and propulsion-control logic were evaluated in modular variants.

This supports a preliminary hypothesis that:
- steering control and propulsion control were implemented as separate or semi-separated PLC functions,
- operator input signals may have been sourced from a steering wheel, joystick, or throttle-like interface,
- actuator output and fault handling remain to be confirmed by direct code inspection.

## 5. Preliminary propulsion control architecture

The project archive includes direct evidence of propulsion-focused variants:
- `UQM_esx_ioxp1.pro`
- `UQM_esx_ioxp2.pro`
- `LivorsiUQM_esx_ioxp1.pro`
- `CAN_ALL_esx_ioxp1.pro`

This indicates the original software evaluated or integrated controller behaviour for:
- UQM propulsion electronics
- Livorsi operator-side interfaces
- CAN communications across multiple device types

Further review is required to confirm the final deployed propulsion/control arrangement and whether the production project used a single controller architecture or a test matrix.

## 6. CAN-bus architecture

The following CAN files were successfully recovered:
- `BoltCANdatas.dbc`
- `TorqSpeedCtrl_PDU2_1_0.dbc`
- `BoltCANdatas.ini`
- `TorqSpeedCtrl_PDU2_1_0.ini`
- `Livorsij1939Map.rtf`

These files indicate:
- a proprietary custom CAN database (`BoltCANdatas.dbc`),
- a torque/speed controller DBC (`TorqSpeedCtrl_PDU2_1_0.dbc`),
- references to J1939-related message mapping (`Livorsij1939Map.rtf`).

Preliminary conclusion:
- The system appears to use a hybrid approach: proprietary messages plus J1939-compatible mapping.
- This matches the expected marine propulsion and steering environment.

## 7. Electrical documentation inventory

The archive contains evidence of electrical and connector-related material:
- `12_7_2012-MYD0703-Bolt 18 MK2.easm`
- `Connectors\Deutsch\...`
- `Livorsi\...` interface documentation
- `Battery\...` power system references
- `CANInformation\...` bus documentation

This is sufficient to proceed with a structured electrical documentation review, but the original design assembly path referenced in the project brief (`Mylne/MYD - Contracted Projects/...`) was not located in the local Dropbox snapshot inspected so far.

## 8. Missing information

The following items are still missing or require confirmation:
- Exact controller firmware revision and target configuration
- Final deployed I/O list and assignment table
- Steering actuator type and interface details
- Propulsion drive and control interfaces
- Complete pin list and connector numbering for sensors and actuators
- Full electrical design sets beyond the assembly file identified so far
- Whether the project used a single final production build or multiple interim development variants

## 9. Recommended software and hardware tools

### Software tools
- CoDeSys 2.3 or compatible legacy PLC environment
- DBC and CAN analysis tools (e.g., CANdb++/BusMaster or alternative open-source decoders)
- CSV/structured document tooling for signal mapping
- PDF and document review tooling for schematics and manuals

### Hardware tools
- Safe bench power supplies for PLC validation
- Simulated switching inputs and analog signal generation
- CAN bus monitor and logging hardware
- Isolated measurement instrumentation for voltage/current validation

## 10. Proposed recovery and testing plan

1. Preserve and review the original project files without modification.
2. Confirm target PLC model, firmware, and I/O assignment from the CoDeSys project metadata.
3. Review the DBC and CAN message definitions for steering and propulsion devices.
4. Map the available electrical documentation to the original controller architecture.
5. Produce validated system architecture and I/O mapping documents.
6. Develop a safe simulation of steering and propulsion inputs without live actuator control.
7. Only after review and approval, move to bench testing under controlled conditions.

## 11. Current status

The archive at `D:\Dropbox\TIVA\AC_Bolt` contains the principal original project assets needed for phase one of recovery. The files have been preserved in the workspace under `original/` and are intentionally excluded from Git tracking.

The next step is to inspect the recovered CoDeSys project content itself in order to extract:
- the PLC target configuration,
- project organization,
- I/O assignments,
- steering logic,
- propulsion logic,
- safety behaviour,
- and CAN routing.
