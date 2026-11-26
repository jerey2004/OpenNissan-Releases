<div align="center">

![BakedECU mascot logo](BakedECU_Logo.png)

# BakedECU

**Garage-built vehicle diagnostics, with a little personality.**

*Formerly OpenNissan • Independent Windows diagnostic software • Beta*

[**Download the latest release**](https://github.com/jerey2004/OpenNissan-Releases/releases)

</div>

---

## What is BakedECU?

**BakedECU** is an independently developed Windows vehicle diagnostic application. It currently focuses on read-only diagnostic communication with select Nissan modules over a compatible **Nissan VI2 J2534 interface**, with separate generic emissions OBD-II features for supported OBDLink SX adapters.

The project is enthusiast-built and still in beta: it is **not a full replacement for Nissan CONSULT** and isn't guaranteed to work on other Nissan or Infiniti vehicles.

## Current capabilities — v0.9.16

- **VIN-first diagnostics** with supported vehicle restrictions.
- **5-, 8-, or 12-module** automatic read-only scan profiles (8, 11, or 15 fixed diagnostic requests respectively).
- **16 independently vehicle-tested DTC-reading module targets** on the 2024 Nissan Versa SR N18, including manually selected ADAS pilots.
- Read-only ECM OBD-II trouble code reading, live data and supported-PID monitoring.
- Reports, local known-code annotations, and JSON/CSV exports.
- VI2/J2534 x86 communication helper and separate generic OBDLink SX support.
- Built-in update checks, package checksum/manifest verification, backup and rollback.
- **BakedECU mascot and branding**, replacing the OpenNissan app name.

**Important:** Individual successful module tests do not imply that a full 16-module automatic scan is implemented. The full verified automatic profile currently contains 12 modules; the front radar, lane camera, and rear side radar pilots remain separate manual operations.

## Windows download & installation

Go to [**GitHub Releases**](https://github.com/jerey2004/OpenNissan-Releases/releases) and download the appropriate v0.9.16 asset:

| Download | Use it for |
| --- | --- |
| `BakedECU_0.9.16_Portable_win-x64.zip` | **New installations** — extract and launch `BakedECU.exe` |
| `OpenNissan_0.9.16_Portable_win-x64.zip` | **Existing OpenNissan 0.9.15 users** — compatibility bridge discovered by the old built-in updater |

The old **OpenNissan-Releases** GitHub repository name is retained temporarily so already installed clients can still locate their update. Its public branding is now BakedECU.

**System requirements:** Windows 10/11 x64, Microsoft Edge WebView2 Runtime, and compatible diagnostic interface drivers. The portable ZIP is built self-contained for the .NET runtime; interface drivers are not included.

### Upgrading from OpenNissan

If you have OpenNissan 0.9.15, use **Check for Updates** after both v0.9.16 ZIP files have been published. The compatibility update installs BakedECU and leaves an `OpenNissan.exe` launcher that starts the new application, so old shortcuts continue to work. Switch your shortcut to `BakedECU.exe` when ready.

## Supported systems on the reference test vehicle

**Verified individual diagnostic responses:** ECM, TCM, ABS, BCM, IPDM, METER, EPS, SRS, HVAC, TPMS, Intelligent Key, Sonar, Front Laser/Radar, Lane Camera, Rear Side Radar Left, Rear Side Radar Right.

**Not yet independently verified in BakedECU:** 3-channel Gateway, IVC, Wireless Charger, AV Control Unit, and Occupant Detection. Additional model/year support and ADAS calibration functions are not claimed.

## Safety, licensing and project status

This is **beta software**, intended for vehicles you own or are authorized to diagnose. Do not use experimental operations during SRS servicing, vehicle programming, or ADAS calibration. Unsupported operations may fail or return incomplete information; zero matching DTC records is not a universal guarantee that a vehicle is fault-free.

**BakedECU is independently developed, not affiliated with, sponsored by, or endorsed by Nissan Motor Co., Ltd. or Infiniti.** Manufacturer names are used only to describe compatibility. No OEM CONSULT software, proprietary drivers, or service databases are included in the compiled downloads.

BakedECU is a proposed project brand; formal trademark clearance has not been completed. Bug reports and feedback are welcome through the project's GitHub repository.
