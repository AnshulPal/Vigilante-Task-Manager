# Intelligent Task Manager 🧠

A cross-platform task management and monitoring application built with [Flet](https://flet.dev). This project integrates multiple modules for:

- Process monitoring 📈
- Network monitoring 🌐
- Scheduled process distribution 🗓️
- Device management 🛠️
- Logs analytics 📊

All within a single, cohesive UI.

---

## Table of Contents 📚

- [Features](#features)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Project Structure](#project-structure)
- [Usage](#usage)
- [Configuration](#configuration)
- [Troubleshooting](#troubleshooting)
- [License](#license)

---

## Features ✨

### 1. Process Monitoring 🖥️
- Real-time CPU and memory usage, status, and security checks.
- Critical alerts for high usage or terminated processes.
- Dedicated logs panel for detailed process logs.

### 2. Network Monitoring 🌐
- Displays live network connections (IPv4 & IPv6) with usage stats.
- Background thread updates without blocking the UI.
- Separate logs panel for network events.

### 3. Scheduled Processes 📅
- Pie or bar charts (via Plotly) showing system vs. non-system tasks.
- Periodic updates with minimal overhead across platforms.

### 4. Process Chains 🌳
- Hierarchical (tree) view of processes and their ancestry.
- Automatic resource usage updates in a background thread.

### 5. Device Manager 🔌
- Manage USB, Bluetooth, Camera, Microphone, and Wi-Fi devices.
- Some actions require administrator privileges on Windows.

### 6. Logs Analytics 📊
- Read and parse JSON-based logs.
- Filter logs by date, level, script, module, or message (regex).
- Live logs feature for tailing a log file in real-time.
- Bar chart of logs per hour (Plotly).
- Color-coded stat cards for total logs, info, warnings, errors.

---

## Prerequisites ⚙️

- **Python 3.8+**
- **Flet 0.28+**
  ```bash
  pip install flet==0.28.0
  ```
- **pandas**
  ```bash
  pip install pandas
  ```
- **Plotly**
  ```bash
  pip install plotly
  ```
- **psutil**
  ```bash
  pip install psutil
  ```
- (Optional) Admin privileges on Windows for some device manager tasks.

---

## Installation 🚀

1. Clone the repository:
   ```bash
   git clone https://github.com/YourUsername/Intelligent-Task-Manager.git
   cd Intelligent-Task-Manager
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

   Or install them individually as listed above.

3. (Optional) Run with admin privileges for device management features on Windows.

---

## Project Structure 🗂️

```plaintext
Intelligent-Task-Manager/
│
├── Applications/
│   ├── integrated.py            # Main entry point integrating all modules
│   ├── proc_mon.py               # Process Monitoring
│   ├── network_monitor.py        # Network Monitoring
│   ├── Scheduled_processes.py    # Scheduled Processes
│   ├── proc_chain.py             # Process Chain Tracker
│   ├── device_manager.py         # Device Manager UI
│   ├── logs_analytics.py         # Logs Analytics
│
├── assets/
│   ├── Background.png
│   ├── logo.png
│
├── requirements.txt
├── README.md
└── ...
```

### Key Modules

- **integrated.py**: Main desktop app integrating all tabs.
- **logs_analytics.py**: Builds the "Logs" tab with live updates.
- **device_manager.py**: Controls USB, Bluetooth, Wi-Fi, Camera, and Microphone.
- **proc_mon.py**, **network_monitor.py**, **Scheduled_processes.py**, **proc_chain.py**: Specialized modules.

---

## Usage 🧩

1. Launch the main integrated app:
   ```bash
   python Applications/integrated.py
   ```

2. Tabs Overview:
   - **Process Monitor**: CPU/memory usage, status, alerts.
   - **Network Connections**: Live IPv4/IPv6 stats, network logs.
   - **Scheduled Processes**: Distribution of system vs. non-system processes.
   - **Process Chains**: Tree view of processes.
   - **Device Manager**: Control hardware devices.
   - **System Logs**: Load and analyze JSON-based logs.

---

## Configuration 🛠️

- **Paths**: Update `self.base_path` inside `integrated.py` if assets location changes.
- **Colors**: Modify `self.dark_bg`, `self.dark_card`, etc., to customize the app theme.
- **Refresh Rates**: Adjust `time.sleep(3)` intervals in background threads for faster/slower updates.

---

## Troubleshooting 🧹

- No chart appearing? 📊 Ensure Flet 0.28+ and Plotly are correctly installed.
- Permission errors on Windows? 🛡️ Try running the app as Administrator.
- Process/Network metrics missing? 🔍 Some readings require elevated permissions.
- Logs not loading? 📄 Ensure JSON logs have valid keys (timestamp, level, etc.).

---

## License 📝

This project is licensed under the **MIT License**. See the `LICENSE` file for full details.

---

## Final Notes 🎯

- Always keep your `requirements.txt` up-to-date.
- For best results, use Python 3.9+ with the latest version of Flet.
- Maintain clean and structured logs for best analytics results!

---

> _Give the project a ⭐ if you like it!_


