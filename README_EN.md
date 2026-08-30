# Studio 0 — Professional Modbus Debugging Tool

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.12+-3776AB?logo=python&logoColor=white" alt="Python"/>
  <img src="https://img.shields.io/badge/PyQt5-5.15+-41CD52?logo=qt&logoColor=white" alt="PyQt5"/>
  <img src="https://img.shields.io/badge/Modbus-RTU%20%7C%20TCP%20%7C%20ASCII-blue" alt="Modbus"/>
  <img src="https://img.shields.io/badge/No--Code-Visual%20HMI-green" alt="No-Code"/>
</p>

> An industrial-automation Modbus debugging & HMI tool: build register monitors and visual panels **without code**, extend with **a little Python**.

---

## 1. Overview
Studio 0 combines Modbus master/slave debugging, register monitoring, packet analysis, data logging and visual panel building. It supports **RTU / ASCII / TCP / IP** and connects via **COM / TCP client·server / UDP client·server**.

## 2. Interface
- **Connection**: pick protocol & link mode, configure port/network, connect in one click.
- **Register Monitor**: batch-add registers, read/write live, waveform & alarms.
- **Packet Log**: hex/text view of traffic, filter, error highlight, export.
- **Design Canvas**: drag-drop widgets to build panels (value, progress ring, button…).
- **Script**: run Python scripts for custom logic.

![Main UI](screenshots/main_interface.png)

## 3. Install & Run
1. Download `Studio 0 Release_Vx.x.x.x.zip` from [Releases](https://github.com/EveryIsZero/Studio-0/releases).
2. Unzip anywhere, **no install** — double-click `Studio 0.exe`.
3. If a runtime DLL is missing, install [Visual C++ Redistributable](https://learn.microsoft.com/cpp/windows/latest-supported-vc-redist).

> Requirements: Windows 10 / 11. Bundled runtime, no Python needed.

## 4. Quick Start (3 steps)
1. **Connect**: pick protocol (e.g. Modbus TCP) + link mode (TCP client), enter IP/port, click Connect.
2. **Add registers**: in Register Monitor click Batch Add, set slave address, function code, start address, quantity.
3. **Read / Write / View**: click Read to refresh; double-click a cell to write; tick Waveform to plot.

## 5. Core Features
| Feature | Description |
|---------|-------------|
| Multi-protocol | RTU / ASCII / TCP / IP, master & slave |
| Link modes | COM / TCP client·server / UDP client·server |
| Register monitor | batch R/W, polling, waveform, alarms |
| Packet analysis | hex/text log, error highlight, export |
| Visual HMI | drag-drop widgets (value, ring, button…) |
| Data logging | CSV / database export, replay |
| Scripting | custom Python logic |

## 6. FAQ
| Issue | Fix |
|-------|-----|
| Cannot connect | check IP/port, COM busy, firewall; match protocol |
| No data | verify slave address, function code, address range |
| Font broken | don't put the app in a deep path with Chinese/spaces |
| Missing DLL | install Visual C++ Redistributable |

## 7. License & Feedback
- Free release for learning & technical exchange.
- Feedback & suggestions: open an [Issue](https://github.com/EveryIsZero/Studio-0/issues).
- If it helps, QR donation codes are included in the release package.

<p align="center">
  <sub>Made with by <a href="https://github.com/EveryIsZero">EveryIsZero</a></sub>
</p>
