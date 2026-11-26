<div align="center">

# OpenNissan

### Independent Nissan Diagnostic Software for Windows

**VIN-first diagnostics • Nissan VI2/J2534 development • Read-only module testing**

[**Download releases**](https://github.com/jerey2004/OpenNissan-Releases/releases) · [**View release history**](https://github.com/jerey2004/OpenNissan-Releases/releases)

> **Beta software:** OpenNissan is an independent project and is not affiliated with, sponsored by, or endorsed by Nissan or Infiniti.

</div>

## About OpenNissan

OpenNissan is an independently developed Windows diagnostic application built to make Nissan vehicle diagnostics more accessible. The project is being developed and tested against real vehicle responses, with a focus on dependable communication, clear diagnostic reports, and controlled, read-only operations.

**This repository hosts compiled Windows releases and release notes.** It is not the project's source-code repository.

## Current progress — v0.9.15 Beta

On the **2024 Nissan Versa SR (N18)** reference vehicle, **16 control modules have individually returned valid read-only diagnostic responses** through a Nissan VI2 interface.

| Available automatic scan | Modules | Diagnostic requests |
| --- | ---: | ---: |
| Standard | 5 | 8 |
| Expanded | 8 | 11 |
| Full verified Versa profile | 12 | 15 |

**Modules in the 12-module scan:** ECM, TCM, ABS, BCM, IPDM, instrument cluster (METER), electric power steering (EPS), airbag (SRS), HVAC, tire-pressure monitoring (TPMS), Intelligent Key, and Sonar.

**Individually tested ADAS modules:** Front Laser/Radar, Lane Camera, Rear Side Radar Left, and Rear Side Radar Right. These four remain separate experimental tests in v0.9.15 and are **not yet part of automatic scanning**.

> A successful DTC request verifies a specific communication operation, not full feature support, calibration capability, or a guarantee that the vehicle has no faults. Combined scan/report behavior requires separate validation.

## Features

- VIN-first vehicle identification and vehicle-specific diagnostic safeguards
- Standard, expanded, and 12-module scan options on the supported reference profile
- Read-only DTC checks for supported modules, with per-module status reporting
- Individual, explicitly confirmed experimental diagnostic tests
- Diagnostic reports and JSON exports
- Nissan VI2 J2534 05.00 communication support, tested with the reference vehicle
- OBDLink SX support for applicable functions; enhanced module compatibility varies by interface
- Built-in GitHub release updater with backup and rollback support
- Portable Windows release packages

### Not supported yet

OpenNissan **does not currently provide** ECU flashing/reprogramming, key programming, module coding, DTC clearing, active tests, or ADAS calibration. It is **not** a complete replacement for Nissan CONSULT at this stage.

## Download & installation

1. Open the [**Releases page**](https://github.com/jerey2004/OpenNissan-Releases/releases).
2. Select the newest suitable beta release and download the Windows portable package (for example, `OpenNissan_0.9.15_Portable_win-x64.zip`).
3. Extract the ZIP to a writable folder, such as `Documents\OpenNissan`.
4. Launch the OpenNissan application from the extracted folder.
5. Install or configure the correct driver for your diagnostic interface. Microsoft Edge WebView2 Runtime may also be required.
6. Connect to an authorized vehicle, identify its VIN, and start with the standard read-only scan.

**Updates:** If you already have a compatible OpenNissan version installed, use its built-in updater to check this repository for newer releases. Close other applications that may be using the diagnostic interface before scanning.

## Compatibility

| Item | Current status |
| --- | --- |
| Windows 10 / 11 (64-bit) | Target platform |
| Nissan VI2 J2534 05.00 | Vehicle-tested diagnostic interface |
| OBDLink SX | Supported for applicable functions; feature coverage may differ |
| 2024 Nissan Versa SR (N18) | Primary validated vehicle profile |
| Other Nissan / Infiniti models | Not yet validated for expanded module diagnostics |

Do **not** assume the Versa-specific CAN addresses or diagnostic requests are suitable for other models or model years.

## Development roadmap

- Verify the complete 12-module combined scan and add the four tested ADAS modules to an optional 16-module profile
- Investigate IVC, wireless charger, and 3-channel CAN gateway diagnostics
- Map AV control unit and occupant detection read-only diagnostics
- Improve manufacturer-specific DTC descriptions and module identification
- Add independently tested vehicle profiles beyond the reference Versa

## Safety & feedback

Use OpenNissan only on vehicles you own or are authorized to service. Perform tests with the vehicle stationary and follow the applicable service procedures, especially around airbag and ADAS systems. Experimental features should not be used during programming, calibration, or safety-system service.

When reporting a problem, include the **OpenNissan version**, **Windows version**, **interface/driver**, **vehicle model/year**, the operation attempted, and the relevant **redacted** diagnostic report. Remove VINs, personal identifiers, credentials, and confidential service data before posting logs publicly.

## Project status

**Active beta development.** Functionality is introduced incrementally and promoted only after controlled testing. The latest release notes are the authoritative source for changes and known limitations in each version.

---

<div align="center">

**OpenNissan — building independent Nissan diagnostics, one verified module at a time.**

</div>
