# Device Control Manager 🛠️

A powerful suite of Python-based utilities built with [Flet](https://flet.dev) to manage and monitor:

- USB Devices 🔌
- Bluetooth Devices 📡
- Wi-Fi Networks 📶

All through graphical control panels with real-time monitoring, classification, and structured logging.

---

## Table of Contents 📚

- [Features](#features)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Project Structure](#project-structure)
- [Usage](#usage)
- [Troubleshooting](#troubleshooting)
- [License](#license)

---

## Features ✨

### USB Device Management 🔌
- Enable/disable USB ports individually or in bulk.
- Monitor USB device connection and disconnection.
- Lock USB ports against unauthorized re-enablement.
- Structured JSON and `.log` based logging.

### Bluetooth Device Management 📡
- Enable/disable Bluetooth adapters.
- Block/unblock specific Bluetooth devices.
- Identify device type (Speaker, Headset, etc.).
- Admin privilege verification.

### Wi-Fi Network Management 📶
- Enable/disable Wi-Fi adapter.
- Block/unblock specific SSIDs (Wi-Fi networks).
- View available nearby Wi-Fi networks.

### Logging and Monitoring 📜
- Real-time structured activity logs.
- PrettyTable-formatted `.log` reports.
- Dynamic updates to connected/disconnected devices.

---

## Prerequisites ⚙️

- **Python 3.8+**
- **Flet**  
  ```bash
  pip install flet
  ```
- **psutil**  
  ```bash
  pip install psutil
  ```
- **prettytable**  
  ```bash
  pip install prettytable
  ```

✅ Must have **Windows OS**.  
✅ Scripts require **Administrator privileges** for full functionality.

---

## Installation 🚀

1. Clone this repository:
   ```bash
   git clone https://github.com/YourUsername/Device-Control-Manager.git
   cd Device-Control-Manager
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

---

## Project Structure 🗂️

```plaintext
Device-Control-Manager/
│
├── bluetooth.py
├── bluetooth_with_classifier_updated.py
├── wifi.py
├── port-enable-disable.py
├── individual-port-blocking.py
├── individual-port-fixed.py
├── Port_blocking_logging.py
├── README.md
├── requirements.txt
└── assets/ (optional)
```

### Key Scripts:

- **bluetooth.py** — Basic Bluetooth control.
- **bluetooth_with_classifier_updated.py** — Bluetooth classification + control.
- **wifi.py** — Wi-Fi network management.
- **port-enable-disable.py** — USB toggling utility.
- **individual-port-blocking.py** — Per-port USB control.
- **individual-port-fixed.py** — USB security and monitoring.
- **Port_blocking_logging.py** — USB activity structured logging.

---

## Usage 🧩

### Basic USB Control 🔌
```bash
python port-enable-disable.py
```

### USB Security and Monitoring 🔒
```bash
python individual-port-fixed.py
```

### USB Activity Logging 📋
```bash
python Port_blocking_logging.py
```

### Bluetooth Device Management 📡
```bash
python bluetooth.py
```

### Advanced Bluetooth (Device Type Detection) 🖥️
```bash
python bluetooth_with_classifier_updated.py
```

### Wi-Fi Control Panel 📶
```bash
python wifi.py
```

---

## Troubleshooting 🧹

- **Script fails or crashes**  
  → Ensure you're running on **Windows** with **Admin privileges**.

- **Missing Libraries**  
  → Install with `pip install flet psutil prettytable`.

- **No devices detected**  
  → Check if devices are properly connected and enabled.

- **Permission issues**  
  → Right-click and select **Run as Administrator** when launching Python scripts.

---

## Final Notes 🎯

- Restart your system after USB/Bluetooth changes for full effect.
- Extend Wi-Fi blocking scripts to schedule blocks automatically if needed.
- Future updates may include mobile control and more device types!

---

> ⭐ _Give the project a star if you find it useful! Contributions are welcome!_
