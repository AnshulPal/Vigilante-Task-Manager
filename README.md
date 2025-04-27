# 🧪 Intelligent Task Manager

## 📚 Introduction

The **Intelligent Task Manager** is an advanced Python-based tool designed to provide extensive functionalities for monitoring, analyzing, and securing system processes and network activity. It enhances system performance, security, and privacy by incorporating a powerful suite of modules that:

- Track process hierarchies with precise details
- Monitor network traffic and active connections
- Scan running files for potential threats
- Manage and control audio-visual device access seamlessly

This project integrates external services like MetaDefender and uses advanced threat detection methods, making it an indispensable resource for users, developers, IT administrators, and privacy enthusiasts alike.

---

# 📊 1. Process and Network Monitoring

This Python script logs detailed process and network connection information and saves the collected data into a well-structured CSV file on your desktop for thorough analysis.

## 🔄 Features
- Logs process details including PID, CPU/memory usage, privileges, and parent process information
- Tracks associated network connections: IP addresses, ports, and statuses
- Monitors active processes and logs their start and end times accurately
- Outputs all collected data into an easy-to-analyze CSV format

## 📅 Requirements
- **OS**: Windows
- **Python**: 3.6+
- **Libraries**: `psutil`, `wmi`

## 🔧 Installation
```bash
pip install psutil wmi
```

## 📗 Running the Script
1. Open `process_network_logger.py`
2. Modify the monitoring duration if needed
3. Run:
```bash
python 1process_and_network_monitoring.py
```
4. Find the output file: `full_process_network_info.csv` on your desktop

## 📊 How It Works
- **Privilege Detection**: Uses Windows APIs (admin rights needed)
- **Network Connection Retrieval**: Utilizes `psutil`
- **Data Collection**: Captures CPU, memory, I/O, runtime, and privileges
- **Output**: Detailed CSV export for complete visibility

---

# 🔍 2. Process Chain and Monitoring

This module monitors and manages process chains efficiently and can terminate child processes exceeding a specified threshold.

## 🔄 Features
- Monitors processes continuously and tracks process trees
- Executes customizable actions when specific processes are detected
- Displays clean and organized process tree structures

## 📅 Requirements
- **OS**: Windows
- **Python**: 3.12.5
- **Library**: `psutil`

## 🔧 Installation
```bash
pip install psutil
```

## 📗 Running the Script
1. Edit `process_chain_tracker.py` to specify processes and associated actions
2. Run:
```bash
python process_chain_tracker.py
```
3. Press `Ctrl+C` anytime to stop and display the tracked tree

## 👁️ Example Output
```
Process 'Code.exe' (PID: 1234) detected.
    Process 'ChildProcess1.exe' (PID: 5678)
        Process 'GrandChildProcess.exe' (PID: 91011)
```

---

# 📻 3. Microphone and Camera Control and Monitoring Tool

This tool provides real-time control over microphone and camera device access, along with monitoring capabilities to ensure your privacy is never compromised.

## 🔄 Features
- Enable or disable system-wide microphone and camera access instantly
- Combined control to toggle both devices with a single action
- Real-time monitoring using `pycaw` and `psutil`
- Reset options to restore default settings effortlessly
- Intuitive Tkinter-based GUI with dynamic updates every 5 seconds

## 📅 Requirements
- **OS**: Windows 10+
- **Python**: 3.8+
- **Libraries**: `tkinter`, `ctypes`, `subprocess`, `psutil`, `pycaw`

## 🔧 Installation
```bash
pip install psutil pycaw
```

## 📗 How to Run
```bash
python mic_cam_control.py
```

## 🔍 Key Points
- Requires administrative rights
- GUI allows intuitive control over devices
- Dynamic status updates keep you informed

---

# 📡 4. MetaDefender File Scanner

A powerful scanner that interacts with the MetaDefender Cloud API to detect potential threats in currently running executable files.

## 🔄 Features
- Uploads files for deep cloud scanning
- Uses round-robin technique for API key management
- Scan history avoids redundant checks

## 📅 Requirements
- **Python Modules**: `psutil`, `requests`, `os`, `time`, `json`

## 🔧 Installation
```bash
pip install psutil requests
```

## 📗 Setup
- Obtain API keys from [MetaDefender](https://metadefender.opswat.com/)
- Add them into the `API_KEYS` list in the script

## 📗 How to Run
```bash
python meta_defender_scan.py
```

---

# 🛡️ 5. IP Threat Analysis

This real-time network monitoring tool captures packets and performs multi-method threat detection on IP addresses.

## 🔄 Features
- Live packet capture
- IP analysis using Bloom Filter, Google Safe Browsing API, and reputation checks
- Logs results into user-friendly CSV format
- Automatically updates blocklists every 24 hours

## 📅 Requirements
- **Python**: 3.12.5
- **Libraries**: `scapy`, `requests`, `pybloom_live`, `msvcrt`

## 🔧 Installation
```bash
pip install scapy requests pybloom-live
```

## 📗 How to Run
```bash
ip_threat_analysis.ipynb
```

## 📃 CSV Format
| IP | Reputation | Method Flags | Time |
|----|------------|--------------|------|

---

# 📚 6. USB and Audio Device Monitor

Lists all currently connected USB devices and audio devices in your system using WMI.

## 🔄 Features
- Lists all connected USB devices
- Lists all detected audio devices
- Lightweight and easy to deploy

## 📅 Requirements
- **OS**: Windows
- **Python**: 3.12.5+
- **Library**: `wmi`

## 🔧 Installation
```bash
pip install wmi
```

## 📗 How to Run
```bash
python device_monitor.py
```

---

# 👁️ 7. Active Window Input Tracker

This script tracks and stores user keyboard inputs for each active window separately, offering an organized overview of typing activities.

## 🔄 Features
- Real-time key logging for active windows
- Organizes typed inputs by window title
- Handles space, backspace, and special keys gracefully

## 📅 Requirements
- **Python**: 3.12.5
- **Libraries**: `keyboard`, `pygetwindow`

## 🔧 Installation
```bash
pip install keyboard pygetwindow
```

## 📗 How to Run
```bash
python keylogger.ipynb
```

---

# 🎉 Conclusion

The **Intelligent Task Manager** is your all-in-one system monitoring, privacy, and threat detection solution.

With modules handling:

- Process and network tracking
- File scanning for threats
- Real-time microphone and camera control
- IP threat detection
- USB/audio device monitoring
- Keyboard input tracking

You are empowered to maintain complete control over your digital environment!



