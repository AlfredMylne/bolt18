# Hardware Inventory

## Status
This inventory has been updated with evidence recovered from the archive and should be treated as a preliminary engineering baseline.

## Confirmed findings
- Original project folder: `D:\Dropbox\TIVA\AC_Bolt\MDI_boat\IOXp_CodeR1`
- Project file: `Bolt18_0_01.pro`
- Embedded project metadata includes the signature `CoDeSys+` and the version string `2.3.9.28`
- The project naming and document set indicate an STW ESX-IOXp controller family
- Supporting documentation is present in `MDI_boat\SensorWks` for ESX-IOXp and CoDeSys
- The project archive contains development variants for `Livorsi`, `UQM`, and combined `LivorsiUQM` controller logic
- The CAN archive includes a custom `BoltCANdatas.dbc` and a UQM torque/speed controller DBC named `TorqSpeedCtrl_PDU2_1_0.dbc`

## Preliminary hardware inventory
- Controller: STW ESX-IOXp (confirmed by folder names and documentation set)
- Development environment: CoDeSys 2.3 project format (`2.3.9.28` confirmed in the binary project header)
- Operator interfaces: Livorsi references and `Livorsi` test projects
- Propulsion drive integration: UQM motor-drive test projects and UQM CAN database
- CAN network: recovered J1939-compatible and proprietary message definitions
- Electrical source: SolidWorks assembly and connection-list files under `MYD0703_BOLT18 Mk2\Bolt18 - Mark2\SW\Electrical`

## Evidence limitations
- The SolidWorks electrical export is not a complete pin-to-pin wiring list; it contains wire metadata and a single segment element, not the full pin assignment table.
- The available XML appears to be partial and does not yet provide complete connector numbering or net assignment details.
- Further confirmation of the final hardware revision and exact I/O module population requires direct review of the original project database and the full electrical design set.

## Items still to confirm
- Final PLC model and revision
- Actual I/O module count and expansion cards
- Power distributor and battery connection topology
- Steering actuator driver and fault circuit details
- Complete connector pin numbers and load allocation
