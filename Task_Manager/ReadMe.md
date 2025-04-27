---

# Process Monitoring Script 🖥️

This **Python** script monitors system processes in real-time, logging detailed process information to both **CSV** and **NDJSON** files. It detects and alerts for various anomalies, including:

- Ghost Ancestry 👻
- Too Many Children 👶
- Deep Process Chains 🌳
- High Spawn Rate 🚀
- Unauthorized Elevated Privileges 🔐
- Anomalous Priority Changes 📈

---

## Features ✨

1. **Real-Time Monitoring** ⏱️  
   Monitors system processes at configurable intervals.

2. **CSV & NDJSON Logging** 📄  
   - CSV: `process_monitor_log.csv`
   - NDJSON: `logs/process_monitor.ndjson`

3. **Anomaly Detection** 🚨  
   - Unauthorized privilege escalation.
   - Suspicious process chain depth.
   - Priority and spawn rate changes.

4. **Cross-Platform Support** 🖥️  
   Works on Windows, Linux, and macOS.

5. **Graceful Shutdown** 🛑  
   Handles `SIGINT` and `SIGTERM` signals cleanly.

---

## Requirements ⚙️

- **Python 3.6+**
- **psutil** library  
  ```bash
  pip install psutil
  ```
- Optional: Admin/root privileges for deeper monitoring.

---

## Installation & Setup 🚀

```bash
pip install psutil
```

---

## Configuration ⚙️

Adjust constants inside the script:
- `MONITOR_INTERVAL`
- `MAX_SPAWN_RATE`
- `MAX_CHILD_PROCESSES`
- `MAX_TREE_DEPTH`
- `PRIVILEGE_CHANGE_FLAG`
- `PRIORITY_CHANGE_FLAG`

---

## Running the Script ▶️

```bash
python process_monitor.py
```

Or make it executable (Linux/macOS):

```bash
chmod +x process_monitor.py
./process_monitor.py
```

---

## Output 📂

- Console: Real-time alerts.
- CSV File: Process logs.
- NDJSON Log: Structured JSON entries.

---

## Stopping the Script ✋

- `Ctrl + C` (SIGINT)
- `kill` (SIGTERM on Linux/macOS)

---

# Log Parser 📚

A **Python GUI** (built with **PyQt5**) for viewing and analyzing **NDJSON** logs interactively.

---

## Features ✨

1. **GUI-Based Log Analysis** 🖥️  
2. **Advanced Filtering & Search** 🔎  
3. **Continuous Log File Polling** 🔄  
4. **Dark Theme with Level-Based Coloring** 🌑  
5. **Export Filtered Logs to CSV/JSON** 📄

---

## Requirements ⚙️

- **Python 3.6+**
- **PyQt5**  
  ```bash
  pip install PyQt5
  ```
- **pandas**  
  ```bash
  pip install pandas
  ```

---

## Installation 🚀

```bash
pip install PyQt5 pandas
```

---

## Running the Application ▶️

```bash
python log_parser_gui.py
```

---

## Usage 📚

- Load `.ndjson` or `.log` file.
- Apply quick filters, regex searches, and timeline sliders.
- Automatically updates when new log entries appear.
- Export filtered results.

---

## Known Limitations ⚠️

- Large files may slow down GUI.
- Log lines must be valid JSON.
- Regex needs to be properly formatted.

---

# Intelligent Task Manager 🧠

A GUI-based **Task Manager** built with **Tkinter** for:

- Monitoring running processes
- Killing processes by PID
- Tracking system resource usage
- Structured event logging (NDJSON)

---

## Features ✨

1. **Process Management** 🛠️  
2. **Resource Monitor (CPU, RAM, Disk)** 📈  
3. **Settings Toggles (Camera/Mic)** 🎛️  
4. **Rotating NDJSON Logs** 🗂️  
5. **Dark Themed UI** 🌑

---

## Requirements ⚙️

- **Python 3.6+**
- **psutil**  
  ```bash
  pip install psutil
  ```

---

## Installation 🚀

```bash
pip install psutil
```

---

## Running the Application ▶️

```bash
python IntelligentTaskManager.py
```

---

## Logging Schema 📑

Each NDJSON log entry example:

```json
{
  "timestamp": "2024-04-10 14:12:36",
  "level": "INFO",
  "script": "__main__",
  "module": "IntelligentTaskManager",
  "funcName": "refresh_tasks",
  "lineNo": "123",
  "message": "Refreshing process list..."
}
```

---

## Known Limitations ⚠️

- Killing protected system processes may require admin/root access.
- Signature checking is Windows-specific.

---

## License 📝

This project is licensed under the **MIT License**.

---

> ⭐ _If you like this project, consider giving it a star! Contributions are welcome!_
