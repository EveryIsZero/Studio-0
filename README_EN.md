# Studio 0 — Modbus Debugging Tool

<p align="center">
  <strong>Professional-grade Modbus protocol debugging &amp; simulation tool</strong><br/>
  <img src="https://img.shields.io/badge/Python-3.12+-3776AB?logo=python&amp;logoColor=white" alt="Python"/>
  <img src="https://img.shields.io/badge/PyQt5-5.15+-41CD52?logo=qt&amp;logoColor=white" alt="PyQt5"/>
  <img src="https://img.shields.io/badge/Modbus-RTU%20%7C%20TCP%20%7C%20ASCII-blue" alt="Modbus"/>
  <img src="https://img.shields.io/badge/No--Code-Visual%20HMI-green" alt="No-Code"/>
  <img src="https://img.shields.io/badge/Low--Code-Python%20Scripts-orange" alt="Low-Code"/>
</p>

<div align="center">
  <strong>🌐 Language / 语言：</strong>
  <a href="README.md">🇨🇳 中文</a> | <a href="README_EN.md"><b>🇺🇸 English</b></a>
</div>

---

## 🔖 Tags / Topics

<div align="center">

| Tag | Chinese | Description |
|-----|---------|-------------|
| **`python`** | 🐍 Python | Built on Python 3.12 / PyQt5 |
| **`modbus`** | 📡 Modbus | RTU / TCP / ASCII support |
| **`no-code`** | 🎨 免代码 | Graphical UI, zero code for Modbus debug & data binding |
| **`low-code`** | ✏️ 弱代码 | Built-in Python script engine for automation |
| **`custom`** | ⚙️ 自定义 | Fully configurable widget properties |
| **`hmi` / `scada`** | 📊 HMI 组态 | Industrial HMI / data visualization |
| **`industrial` / `iot`** | 🏭 工业自动化 | For industrial automation &amp; IoT |

</div>

---

## 📖 Table of Contents

- [Product Overview](#product-overview)
- [⭐ Interface Overview](#-interface-overview)
- [System Requirements](#system-requirements)
- [Download & Install](#download--install)
- [Quick Start (5-Minute Guide)](#quick-start-5-minute-guide)
- [Feature Details](#feature-details)
  - [Protocol Support](#protocol-support)
  - [Data Acquisition & Monitoring](#data-acquisition--monitoring)
  - [Command / Write](#command--write)
  - [Slave Simulation](#slave-simulation)
  - [Multi-Device Management](#multi-device-management)
  - [Communication Log](#communication-log)
  - [Alarm System](#alarm-system)
  - [Script Automation (Low-Code)](#script-automation-low-code)
- [Interface Guide](#interface-guide)
- [Data Point Configuration](#data-point-configuration)
- [Connection Parameters](#connection-parameters)
- [FAQ](#faq)
- [Version History](#version-history)
- [Software License](#software-license)
- [Feedback & Support](#feedback--support)
- [Support the Author](#support-the-author)

---

## Product Overview

**Studio 0** is a professional-grade Modbus debugging &amp; simulation tool built on **Python / PyQt5**, designed for engineers, system integrators, and developers in industrial automation.

### Tech Stack

| Component | Technology | Version |
|-----------|-----------|---------|
| **Language** | Python | 3.12+ |
| **UI Framework** | PyQt5 | 5.15+ |
| **Protocol Stack** | Custom (pymodbus-based) | — |
| **Distribution** | PyInstaller | Single exe, no Python needed for users |

### Core Philosophy: No‑Code + Low‑Code

Studio 0 is built on the principle that **anyone can build professional industrial monitoring interfaces without writing code**:

- **🎨 No‑Code**: **Graphical UI operation** — select COM port, click to connect, switch tabs for data areas, drag sliders, click send. Zero lines of code.
- **✏️ Low‑Code**: Built-in **Python script engine** for advanced automation: scheduled tasks, condition triggers, data computation. Standard Python syntax, easy to learn.

### Use Cases

| Scenario | Description |
|----------|-------------|
| **Device integration** | Connect PLCs, VFDs, instruments — read/write in real time |
| **Protocol analysis** | Capture & decode frames, locate faults |
| **Slave simulation** | Simulate slave devices for host testing |
| **Function validation** | Test host software without physical hardware |
| **Learning & teaching** | Understand Modbus protocol internals |
| **HMI prototyping** | Rapid industrial UI mockups (no-code) |

### Core Advantages

- ✅ **Full three-protocol coverage** — RTU / TCP / ASCII in one tool
- ✅ **Master & Slave dual mode** — poll data as master or respond as slave
- ✅ **Out of the box** — no Python or dependencies to install
- ✅ **Free to use** — personal and commercial
- ✅ **No-code HMI** — drag-and-drop editor with 30+ visual widgets
- ✅ **Low-code scripting** — built-in Python engine, unlimited extensibility
- ✅ **Complete logging** — every frame recorded and exportable

---

## ⭐ Interface Overview

> 💡 **Studio 0 ("0号工坊") main interface** — all features in one window. Modbus communication debugging and data binding without writing code.

### Main Interface Screenshot

The actual Studio 0 main window (**I/O Binding — Bit Operations** tab):

<p align="center">
  <img src="screenshots/main_interface.png" width="900" alt="Studio 0 Main Interface - 0号工坊"/>
  <br/><em>▲ Full interface: menu bar · device connection panel (left) · I/O binding workspace (center) · status bar (bottom)</em>
</p>

| Area | Function | How to Use |
|------|----------|------------|
| **Menu Bar** | File / View / Config / Help | Global functions |
| **Toolbar** | Device list · Connect · Disconnect · Advanced Monitor | One-click actions |
| **Left Panel** | Device management: name, connect/disconnect buttons, COM port | Graphical serial config |
| **Center Workspace** | I/O Binding: Bit Ops / Coils / Holding Registers (Z3Z4) | Tab switching |
| **Data Widgets** | Text labels, sliders, config button, send button, progress | Drag to use |
| **Bit Operation Table** | B0–B15 ↔ Bit.16–Bit.31 register mapping | Visual bit-level R/W |
| **Status Bar** | Ready state / current port | Real-time feedback |

### No-Code Workflow

Using Studio 0 requires **zero coding**:

1. **Configure Connection** — Select COM port in the left panel, click 「Connect」(blue button)
2. **Bind Data** — Switch between **Bit Operations / Coils / Holding Registers** tabs
3. **Adjust Parameters** — Drag sliders, type label names, click 「Config」for details
4. **Send Commands** — Click 「Send」to write data to device, progress bar shows status
5. **Monitor Status** — Bit operation table shows real-time status of each bit (B0–B15 → register bits)

### Advanced Monitor Mode

The toolbar provides an **Advanced Monitor** entry for detailed data views (batch register viewing, message log, etc.).

---

### 🧩 Complete Widget Catalog

Studio 0's HMI editor provides **6 categories, 30+ widgets**, covering all common industrial HMI needs:

#### ① Data Display

| Widget | Description | Best For |
|--------|-------------|----------|
| **📊 Data Label** | Live numeric value (int/float/hex/string) | Temp, pressure, RPM |
| **📝 Static Text** | Fixed label text (titles, units, notes) | Decorative text |
| **📋 Multi-row Table** | Tabular display of multiple registers | Batch register view |
| **📅 Date/Time** | System or device timestamp display | Time display |
| **🔢 Arithmetic Sum** | Sum/avg/min/max across data points | Energy stats, totals |

#### ② Status Indicator

| Widget | Description | Best For |
|--------|-------------|----------|
| **🔴 Status Lamp** | Color change + optional blink by value/enum | Run/Stop/Alarm |
| **🏷️ Status Tag** | Text + background color联动 | Device status text |
| **📡 Device Status** | Online/offline/error summary | Connection overview |
| **🔋 Battery** | Battery icon + percentage | Mobile device power |

#### ③ Command / Write

| Widget | Description | Best For |
|--------|-------------|----------|
| **🔘 Command Button** | Click to send preset write command | Start/stop, reset |
| **🔄 Auto-reset Button** | Momentary pulse trigger | Jog, step control |
| **📋 Command Table** | Batch write multiple registers | Parameter batch set |
| **⚡ Batch Control** | One-click write to multiple points | Global start/stop |
| **📥 Dropdown List** | Select preset value → send | Mode switch, gear select |

#### ④ Interaction

| Widget | Description | Best For |
|--------|-------------|----------|
| **🎚️ Slider** | Drag to continuously adjust value | PID setpoint, brightness |
| **🔘 Switch** | ON/OFF toggle button | Enable/disable |
| **🎮 Graphic Switch** | Custom-icon touch switch | Custom UI style |

#### ⑤ Instrument

| Widget | Description | Best For |
|--------|-------------|----------|
| **🎯 Gauge** | Classic analog pointer meter (scale/range/color) | RPM, pressure, flow |
| **🚗 Speedometer** | Semi-circular speed gauge | Motor speed, linear speed |
| **🔄 Numeric Dial** | Circular large-number display | Key parameter highlight |
| **📐 Progress Ring** | Circular percentage ring | Completion rate, utilization |
| **▬ Progress Bar** | Horizontal/vertical bar | Level, load |
| **🌡️ Thermometer** | Thermometer-style with scale | Temperature display |
| **🧭 Compass** | Direction indicator (N/S/E/W + angle) | Wind direction, antenna azimuth |

#### ⑥ Chart

| Widget | Description | Best For |
|--------|-------------|----------|
| **🍩 Donut/Pie Chart** | Proportional distribution | Energy breakdown, fault types |
| **📈 Real-time Trend** | Scrolling time-series line chart | Trend monitoring, waveform |
| **📉 Historical Curve** | Time-axis history replay | Historical analysis |
| **📊 Bar Chart** | Multi-channel comparison | Multi-device compare |
| **⚬ Scatter Plot** | XY scatter distribution | Correlation analysis |

#### ⑦ Decoration

| Widget | Description |
|--------|-------------|
| **📑 Page Tab** | Multi-page tabbed navigation |
| **➖ Divider** | Section separator line |
| **〰️ Flow Line** | Animated flow effect (pipe medium direction) |
| **🖼️ Background Image** | Background image (device layout / process flow) |

---

### Universal Widget Properties

Every widget supports these **common base parameters** via graphical forms:

| Parameter | Description | Example |
|-----------|-------------|---------|
| **X / Y** | Position on canvas | X=100, Y=200 |
| **Width / Height** | Size in pixels | W=160, H=60 |
| **Angle** | Rotation (degrees) | 0, 45, 90 |
| **Refresh Interval (ms)** | Data update frequency | 500 (fast) ~ 5000 (slow) |
| **Data Binding** | Which Modbus data point to link | Select from configured points |

Each widget also has **exclusive extended properties** (gauge min/max/scale divisions, lamp color mapping table, chart sampling interval, etc.), all presented as form fields in the property panel.

---

## System Requirements

### Minimum

| Item | Requirement |
|------|-------------|
| **OS** | Windows 7 SP1 / Windows Server 2012 R2 or later |
| **CPU** | x86_64 architecture, 1 GHz or higher |
| **RAM** | 2 GB |
| **Disk** | 200 MB free space (program + runtime + config) |
| **Display** | 1024×768 resolution or higher |

### Recommended

| Item | Requirement |
|------|-------------|
| **OS** | Windows 10 / Windows 11 (64-bit) |
| **CPU** | 2 cores or more |
| **RAM** | 4 GB or more |
| **Display** | 1920×1080 or higher |

### Notes

- ⚠️ This software runs on **Windows only**; macOS and Linux are not supported
- ⚠️ It is recommended to use a path **without Chinese characters or special symbols**
- ⚠️ The first launch may take a few seconds to initialize (loading UI components)
- ⚠️ If blocked by antivirus, add the program folder to the whitelist (false positive for PyInstaller packages)

---

## Download & Install

### Step 1: Download

1. Go to the [Releases](https://github.com/EveryIsZero/Studio-0/releases) page
2. Find the latest `Studio 0 Release 4.3.4.69.zip`
3. Click to download (about 40 MB)

### Step 2: Extract

1. Extract the zip to any directory
   - Recommended: `D:\Studio 0\` or `C:\Tools\Studio 0\`
   - ❌ Not recommended: Desktop or deep Chinese paths (e.g. `C:\Users\张三\Downloads\`)
2. After extraction you should see:

```
Studio 0/
├── Studio 0.exe           <- Main program (double-click to launch)
├── _internal/             <- Runtime dependencies (do not delete or move)
│   └── (Python runtime files)
├── cfg/                   <- User configuration (auto-generated on first run)
├── 微信捐赠码.png         <- Donation QR (WeChat), same level as exe
├── 支付宝捐赠码.jpg       <- Donation QR (Alipay), same level as exe
└── manual.html            <- Bilingual manual (switchable language, works offline)
```

> ⚠️ **Important**: `Studio 0.exe` must sit in the **same directory** as `_internal/`. If separated or deleted, the program will not start.

### Step 3: Launch

Double-click `Studio 0.exe` to start.

On first launch the following initialization is performed automatically:
- Create the `cfg/` configuration directory
- Generate default configuration files
- Initialize the database

---

## Quick Start (5-Minute Guide)

Follow these steps to complete a full Modbus data acquisition in 5 minutes:

### Prerequisites

You need a Modbus-capable device (or use Slave Simulation mode for self-test). The example below uses a **Modbus RTU serial connection**.

### Step 1: Create a connection (30s)

1. After launching Studio 0, click **「New Connection」** on the toolbar
2. In the dialog, choose the protocol type: **「RTU」** (serial mode)
3. Configure serial parameters:
   - **Port**: the COM port of your device (e.g. `COM3`)
   - **Baud rate**: must match the device (common: `9600` / `19200` / `38400` / `115200`)
   - **Data bits**: usually `8`
   - **Stop bits**: usually `1`
   - **Parity**: usually `None`
4. Click **「OK」** to save

### Step 2: Add data points (1 min)

1. In the data configuration area, click **「Add Data Point」**
2. Fill in:

   | Field | Description | Example |
   |-------|-------------|---------|
   | **Slave address** | Target device Modbus address | `1` |
   | **Function code** | Operation type | `03` (read holding registers) |
   | **Start address** | Register start address (decimal) | `0` |
   | **Quantity** | Number of registers/coils | `10` |
   | **Data type** | Parse method | `INT16` (16-bit signed) |

3. Click **「Confirm」**
4. Repeat to add more points

### Step 3: Start acquisition (10s)

1. Click **「Connect」** on the toolbar
2. Select the data points to acquire
3. Click **「Start Acquisition」**
4. Real-time values appear, refreshing at the configured interval

### Step 4: Write data (30s)

1. Find the item to modify in the data list
2. **Double-click the value column** (or right-click → "Write")
3. Enter the new value
4. Click **「Confirm Write」**
5. Check the result (success / failure + error code)

### Step 5: View logs (anytime)

1. Switch to the **「Communication Log」** panel
2. See all sent/received Modbus frames (raw hex + decoded fields)
3. Logs support **copy** and **export** to a text file

> 💡 **Tip**: If you have no physical device, use built-in **Slave Simulation** for self-test — enable "Slave Mode" from the menu, configure a local mapping table, then connect from another window as master.

---

## Feature Details

### Protocol Support

Studio 0 fully supports the three mainstream Modbus transports:

#### Modbus RTU (Serial)

| Parameter | Description |
|-----------|-------------|
| **Medium** | RS-232 / RS-485 / RS-422 |
| **Interface** | Serial (COM port) |
| **Typical use** | Field devices, PLCs, VFDs, instruments |
| **Frame** | Address + Function code + Data + CRC |
| **Traits** | Compact binary, high efficiency, most common in industry |

**Common serial parameter presets:**

| Scenario | Baud | Data | Stop | Parity |
|----------|------|------|------|--------|
| Default | 9600 | 8 | 1 | None |
| High speed | 115200 | 8 | 1 | None |
| Legacy | 4800 | 7 | 2 | Even |

#### Modbus TCP (Ethernet)

| Parameter | Description |
|-----------|-------------|
| **Medium** | Ethernet (TCP/IP) |
| **Connection** | IP address + port |
| **Default port** | `502` (Modbus standard) |
| **Typical use** | Networked PLCs, remote I/O, gateways |
| **Frame** | MBAP header + PDU (function code + data) |
| **Traits** | Reliable TCP transport, supports routing |

```
IP:     192.168.1.100
Port:   502 (standard Modbus port)
Timeout: 3000 ms
```

#### Modbus ASCII (Serial)

| Parameter | Description |
|-----------|-------------|
| **Medium** | RS-232 / RS-485 |
| **Interface** | Serial (COM port) |
| **Encoding** | ASCII (each byte as two ASCII chars) |
| **Delimiters** | Starts with `:`, ends with `CR LF` |
| **Checksum** | LRC (Longitudinal Redundancy Check) |
| **Traits** | Human-readable, good for debugging, lower efficiency than RTU |

> 💡 **Which protocol?** If the device manual says nothing, most industrial devices use **Modbus RTU**. Ethernet devices usually use **Modbus TCP**. ASCII is rare, mainly for manual frame inspection.

---

### Data Acquisition & Monitoring

#### Supported data types

| Type | Description | Range | Typical use |
|------|-------------|-------|-------------|
| **INT16** | 16-bit signed | -32768 ~ 32767 | Temp, pressure sensors |
| **UINT16** | 16-bit unsigned | 0 ~ 65535 | Status word, counters |
| **INT32** | 32-bit signed | ±2.1 billion | Large-range measurements |
| **UINT32** | 32-bit unsigned | 0 ~ 4.2 billion | Accumulators, timestamps |
| **FLOAT32** | IEEE 754 single | ±3.4E38 | Precise readings, setpoints |
| **FLOAT64** | IEEE 754 double | ±1.7E308 | High-precision computing |
| **HEX** | Hexadecimal | 0x0000 ~ 0xFFFF | Raw register value |
| **STRING** | ASCII string | variable | Model, description |
| **BYTE ARRAY** | Byte array | variable | Binary blocks |
| **BIT** | Single bit | 0 / 1 | Switch, flag |

#### Supported function codes

| Code | Name | Dir | Description |
|------|------|-----|-------------|
| **01** | Read Coils | R | Read discrete outputs |
| **02** | Read Discrete Inputs | R | Read discrete inputs |
| **03** | Read Holding Registers | R | Read analog/params (most common) |
| **04** | Read Input Registers | R | Read read-only analog |
| **05** | Write Single Coil | W | Control one discrete output |
| **06** | Write Single Register | W | Set one parameter |
| **0F (15)** | Write Multiple Coils | W | Batch discrete control |
| **10 (16)** | Write Multiple Registers | W | Batch parameter setting |

#### Coefficient & conversion

Raw values stored in devices often need scaling to obtain physical values. Studio 0 supports a **coefficient**:

```
Actual value = raw value × coefficient + offset
```

**Example: temperature sensor**

| Param | Value | Note |
|-------|-------|------|
| Raw | `2500` | register value read |
| Coefficient | `0.01` | 0.01°C per unit |
| Offset | `0` | none |
| **Actual** | **25.00 °C** | displayed value |

#### Byte order

Different vendors may use different byte orders (big/little endian), causing multi-byte parse errors. Studio 0 supports:

| Order | Description | Use |
|-------|-------------|-----|
| **ABCD** (big endian) | high byte first | Modbus std, most PLCs |
| **DCBA** (little endian) | low byte first | some Intel-arch devices |
| **BADC** | word swap | special vendors |
| **CDAB** | double-word swap | special vendors |

> 💡 **Troubleshooting**: if a float looks unreasonable (huge/tiny/NaN), the byte order is likely wrong. Try switching it.

---

### Command / Write

Besides passive reading, Studio 0 can actively send write commands to control devices and change parameters.

#### Write methods

| Method | Operation | Use |
|--------|-----------|-----|
| **Single write** | double-click value → enter → confirm | change one param |
| **Batch write** | select multiple points → batch send | set several params |
| **Command button** | place button in HMI → click to send | frequent shortcuts |
| **Slider** | drag slider → continuous send | adjust setpoint (e.g. PID) |

#### Write safety

- ✅ Confirmation dialog before writing (prevents mis-operation)
- ✅ Shows last successfully read value as reference
- ✅ Optional **write password**
- ✅ All writes logged and traceable

---

### Slave Simulation

Slave Simulation lets you test Modbus logic **without physical hardware**.

#### How it works

Studio 0 runs as a Modbus **Slave**, listening for master requests and responding per a preset **data mapping table**.

#### Steps

1. Select **「Slave Mode」** from the menu or toolbar
2. Configure slave parameters:
   - **Slave address**: this unit's address (e.g. `1`)
   - **Listen port / serial**: per protocol
3. Define the **data mapping table**:
   - Set initial values and types per address range
   - e.g. addresses 0~9 as INT32, all init to 0
4. Start slave listening
5. Connect from another device (or another window) as master to read/write

#### Use cases

- 🔧 Simulated testing during host software development
- 📚 Learning Modbus interaction
- 🧪 Debug environment to reproduce field issues
- ✅ Virtual slave node in automated tests

---

### Multi-Device Management

Studio 0 supports **connecting and managing multiple Modbus devices** simultaneously, each with independent config.

#### Features

- Independent connection params per device (IP/port/serial)
- Independent data point list per device
- Independent acquisition interval per device
- Devices do not affect each other; one disconnecting won't stop others
- Device grouping and tagging

#### Recommendation

| Count | Suggestion |
|-------|------------|
| 1~5 | Tabs in the main window |
| 6~20 | Use grouping |
| 20+ | Split into multiple project files |

---

### Communication Log

Studio 0 automatically records the full Modbus frame for every transaction.

#### Content

| Field | Description |
|-------|-------------|
| **Timestamp** | Send/receive time, ms precision |
| **Direction** | TX (send) / RX (receive) |
| **Raw frame** | Full frame in hex |
| **Decoded** | Address, function code, data as text |
| **Elapsed** | Request-to-response time (ms) |

#### Operations

- **Live view**: scroll in the log panel
- **Filter/search**: by time range, direction, function code
- **Export**: to `.txt` / `.csv` (open in Excel)
- **Clear**: one-click clear buffer (exported files unaffected)

> 💡 **Tip**: when communication fails, check the raw frames first. Comparing request and response hex quickly tells whether the device is silent, timed out, or returned an exception code.

---

### Alarm System

Studio 0 has a multi-level threshold alarm to notify you on abnormal data.

#### Alarm types

| Type | Trigger | Example |
|------|---------|---------|
| **High limit** | value above upper limit | Temp > 80°C |
| **Low limit** | value below lower limit | Pressure < 0.1 MPa |
| **Deviation** | too far from target | outside ±5% |
| **Rate of change** | changes too fast | > 10 within 1s |

#### Notification

| Method | Description |
|--------|-------------|
| **Sound** | Alarm sound (customizable) |
| **Popup** | Center-screen detail window |
| **Log** | All events recorded |
| **Color mark** | Out-of-range values highlighted |

#### Configuration

1. Right-click a data point → **「Set Alarm」**
2. Choose alarm type and threshold
3. Choose notification method
4. Enable/disable the rule

---

### Graphical HMI

Studio 0 provides rich graphical controls for at-a-glance data.

#### Controls

| Control | Use | Data |
|---------|-----|------|
| **Data label** | Show live value | single point |
| **Gauge** | Analog pointer meter | single analog |
| **Progress bar / dial** | Percentage | bounded value |
| **Trend chart** | History tracking | time series |
| **Bar chart** | Multi-channel compare | multiple points |
| **Status lamp** | On/off indicator | 0/1 or enum |
| **Command button** | One-click send | writable point |

#### Operation

1. Enter **「HMI Editor」** mode
2. Drag controls from the palette onto the canvas
3. Double-click a control to bind data and set properties
4. Adjust layout, color, font
5. Save and switch to run mode

---

### Script Automation

Studio 0 has a built-in script engine for automation.

#### Capabilities

- Scheduled data acquisition and writing
- Condition triggers (act when a value meets a condition)
- Data computation and processing
- Looped batch operations
- External integration (HTTP, file I/O)

#### Usage

1. Open the **「Script Editor」**
2. Write automation scripts (Python-like syntax)
3. Set trigger (timer / manual / event)
4. Run the script
5. View output in the panel

> 📌 **Note**: scripting is advanced; learn the basics first.

---

## Interface Guide

The main window has the following regions:

```
┌─────────────────────────────────────────────────────┐
│  Menu   File | Edit | View | Tools | Help          │
├─────────────────────────────────────────────────────┤
│  Toolbar  [New] [Conn] [Disc] [Poll] [Stop] [...]   │
├──────────┬──────────────────────┬───────────────────┤
│          │                      │                   │
│  Device  │   Data list area     │  Detail / Chart   │
│  tree    │   (addr/name/        │  panel            │
│  list    │    value/quality/    │                   │
│          │    status)           │                   │
│          ├──────────────────────┤                   │
│          │   Comm log panel     │                   │
│          │   (TX/RX frames)     │                   │
├──────────┴──────────────────────┴───────────────────┤
│  Status   Connected: COM3 @9600 | Devices: 3 | 1s   │
└─────────────────────────────────────────────────────┘
```

### Regions

| Region | Function | Tip |
|--------|----------|-----|
| **Menu** | Global entry | File manages projects, View switches views |
| **Toolbar** | Common shortcuts | Right-click to customize buttons |
| **Device tree** | Left panel, all configured devices | Right-click add/delete/rename |
| **Data list** | Center, live values | Double-click to write, right-click to config |
| **Detail panel** | Right, selected data details | Switch to chart/log view |
| **Log panel** | Bottom, comm frames | Resizable / closable |
| **Status bar** | Bottom, status & stats | Online count, refresh rate |

---

## Data Point Configuration

### Full parameter list

| Param | Required | Description | Example |
|-------|----------|-------------|---------|
| **Name** | Yes | Display name | "Motor RPM" |
| **Slave address** | Yes | Target Modbus ID | `1` ~ `247` |
| **Function code** | Yes | Modbus function code | `03` |
| **Start address** | Yes | Register start (decimal) | `0` |
| **Quantity** | Yes | Registers/coils count | `10` |
| **Data type** | Yes | How to parse raw | `INT16`, `FLOAT32` |
| **Coefficient** | No | Scale multiplier (default 1.0) | `0.01` |
| **Offset** | No | Scale offset (default 0) | `0` |
| **Byte order** | No | Multi-byte order | `ABCD` (big endian) |
| **Refresh** | No | Acquisition interval (ms) | `1000` (1s) |
| **Read only** | No | Disable writing | checked = read-only |

### Address calculation

Studio 0 uses **zero-based decimal addresses**:

| Notation | Addr 0 | Addr 1 | Addr 400001 |
|----------|--------|--------|-------------|
| **Zero-based (this app)** | `0` | `1` | `400000` |
| **One-based (some manuals)** | `0` or `1` | `1` or `2` | `400001` |

> 💡 **Tip**: if the manual says `400101`, enter `400100` here (subtract 1). Depends on vendor; try both if unsure.

---

## Connection Parameters

### RTU serial

| Param | Description | Common |
|------|-------------|--------|
| **Port (COM)** | Serial port number | COM1 ~ COM256 |
| **Baud Rate** | Speed | 9600, 19200, 38400, 115200 |
| **Data Bits** | Bits per frame | 7, 8 (usually 8) |
| **Stop Bits** | Stop bits | 1, 1.5, 2 (usually 1) |
| **Parity** | Error check | None, Odd, Even, Mark, Space |

### TCP network

| Param | Description | Common |
|------|-------------|--------|
| **IP address** | Target network address | 192.168.x.x |
| **Port** | Modbus TCP port | 502 (standard) |
| **Connect timeout** | Max wait to connect | 3000 ~ 10000 ms |
| **Response timeout** | Max wait for response | 1000 ~ 5000 ms |
| **Retries** | Auto-retry count | 0 ~ 3 |

### General

| Param | Description | Suggestion |
|------|-------------|------------|
| **Slave address range** | Valid | 1 ~ 247 (0 = broadcast) |
| **Frame gap** | Min gap between frames | ≥ 10 ms |

---

## FAQ

### Q1: App won't start / crashes?

| Cause | Fix |
|------|-----|
| Missing `_internal/` | Keep exe and _internal together |
| Antivirus block | Add folder to whitelist |
| Missing runtime | Install [Visual C++ Redistributable](https://aka.ms/vs/17/release/vc_redist.x64.exe) |
| Chinese path | Move to a pure-English path |

### Q2: Connection failed?

1. **Check physical link** — cable plugged? USB-RS485 driver installed?
2. **Match parameters** — baud/data/parity/stop must exactly match
3. **Confirm port** — check COM number in Device Manager
4. **Check slave address** — matches target device
5. **Cross-validate** — test same device with a known-good tool

### Q3: Data all zero or garbled?

- Wrong slave address (reading empty/nonexistent device)
- Wrong function code (e.g. used 04 but data is in 03)
- Wrong byte order (NaN/huge on float/long)
- Address offset (manual vs app convention)

### Q4: Write failed?

- Does the device support this write function code?
- Is the register read-only?
- Need to unlock write protection on device first?
- Is the value within valid range?

### Q5: Unstable / frequent timeout?

| Issue | Fix |
|-------|-----|
| Baud too high → errors | Lower baud (115200 → 9600) |
| Too many devices on bus | Reduce load or add repeater |
| Poll too fast | Increase interval (100ms → 1000ms) |
| Long/cross-talk cable | Use shielded twisted pair, away from power |

### Q6: How to back up / restore config?

All config is stored in `cfg/`. **Back up the whole `cfg/` folder** to save everything (connections, data points, HMI layout). To restore, put the backed-up `cfg/` back in place.

---

## Version History

Current version: **4.3.4.69** (v4.3.4.69)

| Version | Date | Note |
|---------|------|------|
| **4.3.4.69** | 2025-06 | First public release |

> Detailed changelog: see the Releases page or `readme.txt` inside the package.

---

## Software License

This software is **Freeware**, free for personal and commercial use.

### ✅ You may:
- Download and use for free
- Distribute the original package (unmodified)
- Use in personal or commercial projects

### ❌ You may not:
- Reverse engineer or decompile
- Crack or bypass any limitation
- Use it or its components for illegal purposes
- Claim it as your own or remove copyright notices
- **Obtain the source code** (not provided in this repo)

### Copyright

Copyright © EveryIsZero. All rights reserved.
Provided "as is" without warranty of any kind.

---

## Feedback & Support

### Bug reports & questions

- 📋 **GitHub Issues**: [Submit Issue](https://github.com/EveryIsZero/Studio-0/issues) — preferred, easy to track
- 💬 Please include:
  - Software version
  - OS version
  - Device model & comm parameters
  - Screenshot of the problem
  - Comm log (if any error)

### Feature suggestions

Welcome in Issues, tag as `enhancement`.

---

## Support the Author

If Studio 0 helps your work, buy the author a coffee ☕ — your support keeps it maintained!

<p align="center">
  <table>
    <tr>
      <td align="center">
        <strong>WeChat Pay</strong><br/><br/>
        <img src="donate/wechat_qr.png" width="220"/><br/>
        <em>Scan with WeChat</em>
      </td>
      <td width="40"></td>
      <td align="center">
        <strong>Alipay</strong><br/><br/>
        <img src="donate/alipay_qr.jpg" width="220"/><br/>
        <em>Scan with Alipay</em>
      </td>
    </tr>
  </table>
</p>

> Thanks to every supporter! Every donation means a lot to an independent developer ❤️

---

<p align="center">
  <sub>Made with ❤️ by <a href="https://github.com/EveryIsZero">EveryIsZero</a></sub>
</p>
