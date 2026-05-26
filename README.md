# LabGard
...

# LabGard Pro | Advanced Client-Server Terminal Monitor

LabGard Pro is a Python-based smart lab management system developed for real-time monitoring and control of computer labs. The system gathers and analyzes hardware performance data, presents insights through a centralized dashboard, and enables administrators to enforce application and web access policies across multiple devices. By integrating data collection, analysis, and automation, LabGuard Pro aligns with the principles of Artificial Intelligence & Data Science through intelligent decision support and resource optimization.

## 🚀 Key Features

* **Real-Time Terminal Monitoring:** Dynamically tracks active client nodes, capturing hostnames, real-time CPU utilization, and RAM allocation metrics.
* **Automated Threat & Violation Enforcement:** Continuously audits client process trees. Instantly terminates unauthorized applications (`.exe`) and forces target window closure upon detecting blacklisted browser keywords (e.g., streaming, gaming, or social media handles).
* **Two-Tier Compliance Logic:** Implements a graceful enforcement policy. The first infraction displays a transient system warning; a secondary breach activates an uncompromising, full-screen hardware lock overlay.
* **Centralized Security Orchestration:** Administrators can monitor violations globally from a live-updating Flask dashboard and issue encrypted remote unlock clearances to restore hijacked student terminals.
* **Self-Healing Database Initialization:** Features automated schema execution that dynamically provisions relational MySQL tables (`pc_logs`, `violation_history`) upon backend boot.

## 🛠️ Tech Stack

* **Backend / Server Architecture:** Python, Flask, MySQL, MySQL-Connector
* **Client Monitoring & Automation:** Python, `psutil` (Process Management), `pygetwindow` (OS Window Automation), `requests`
* **Frontend Interface:** Responsive HTML5, CSS3 (Glassmorphism UI, Dark/Light Mode Engine), JavaScript (Asynchronous Polling)
* **GUI Subsystem:** Tkinter (Custom OS-level security overlay)

---

## 🏗️ System Architecture

```text
  [ Student Client Node ]                               [ Admin Control Server ]
  +-------------------------+                           +------------------------+
  |  - Process Auditor      | -- HTTP POST (Metrics) -> |  - Flask Core Engine   |
  |  - Active Window Closer |                           |  - Dashboard View Engine|
  |  - Security Lock UI     | <- HTTP GET (Pin/State) - |  - MySQL Schema Matrix |
  +-------------------------+                           +------------------------+   copy and paste into readme ok
