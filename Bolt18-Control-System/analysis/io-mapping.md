# I/O Mapping

## Status
The I/O map is still incomplete and must remain clearly marked as preliminary. The current evidence supports a partial map only.

## Confirmed evidence
- Original project folder names and files are consistent with an ESX-IOXp CoDeSys PLC application.
- `Bolt18_0_01.pro` carries the CoDeSys `2.3.9.28` project metadata, confirming a legacy PLC development environment.
- The DBC and test project names indicate separate evaluation paths for `Livorsi`, `UQM`, and combined `LivorsiUQM` interfacing.
- The SolidWorks electrical export contains wire records, including `AC Distribution box-1` and `Battery box connector-3`, but not a complete pin assignment table.

## Preliminary I/O classification

### Likely inputs
- Steering command input(s): likely from a steering wheel or lever command source
- Throttle or torque demand input(s): implied by the presence of `UQM` and Livorsi control projects
- Vehicle speed / engine speed feedback: present in CAN DBC definitions and J1939 mapping
- Battery and system state signals: engine, coolant, oil, and fuel level signals are present in the DBC
- Safety and fault inputs: implied by the UQM system status message and fault flags

### Likely outputs
- Motor or inverter command signals: UQM command messages such as `UniversalCommand` and `AccelerationLimitsCommand`
- Drive enable / disable logic: present in UQM command messages (`Enable`, `DisableAccLim`)
- Fault indication and status outputs: system status and watchdog messages show fault and alarm monitoring
- CAN communications: both proprietary and J1939-related message sets are present

## Confirmed vs unverified
- Confirmed: the project is a CoDeSys ESX-IOXp system with UQM and Livorsi integration paths.
- Confirmed: the CAN files include engine speed, torque, and vehicle speed signals.
- Unverified: steering-specific input and output pin assignments are not yet recovered in a readable format.
- Unverified: exact digital and analogue I/O allocation, actuator driver channels, and fault outputs remain missing.

## Missing information required for a reliable map
- Project variable list from the original `.SDB` / `.SYM` database
- Final I/O list from the PLC configuration or controller appendix
- Connector pin assignment table from the electrical design set
- Wiring labels associated with steering actuator, throttle, battery, fault bus, and emergency-stop loops
