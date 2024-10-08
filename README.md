# 🖥️ Automated System Health Checker

A Python-based tool that automates system performance monitoring, including CPU usage, memory consumption, disk space, and network connectivity. This tool sends alerts via email or Slack when predefined thresholds are exceeded, helping system administrators maintain continuous performance.

## 🚀 Features

- **🔍 CPU Monitoring**: Monitors CPU usage and triggers alerts when the usage exceeds a set threshold.
- **💾 Memory and Disk Monitoring**: Tracks memory consumption and disk space, notifying you when critical levels are reached.
- **🌐 Network Connectivity Check**: Periodically checks network latency to ensure connectivity.
- **📧 Alerts**: Sends notifications via email or Slack for real-time monitoring updates.
- **🔄 Scheduled Tasks**: Can be scheduled to run at regular intervals using cron jobs or task schedulers.

## 🛠️ Tech Stack

- **🐍 Python**: Core language used for scripting and automation.
- **📡 SNMP (Optional)**: Retrieves system metrics (if required).
- **📬 SMTP**: For email notifications.
- **🔧 Cron Jobs**: Automates periodic system health checks.
- **📊 Matplotlib**: Optional for generating reports/graphs for performance metrics.

## ⚙️ Getting Started

### Prerequisites

- Python 3.x
- Slack API or SMTP credentials for notifications

### Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/system-health-checker.git
    cd system-health-checker
    ```

2. Install dependencies:
    ```bash
    pip install -r requirements.txt
    ```

3. Set environment variables for email or Slack notifications:
    ```bash
    export EMAIL_USER="your-email@example.com"
    export EMAIL_PASS="your-email-password"
    export SLACK_WEBHOOK_URL="your-slack-webhook-url"
    ```

4. Run the system checker manually:
    ```bash
    python3 system_health.py
    ```

5. (Optional) To schedule automated checks using cron:
    ```bash
    crontab -e
    # Add the following line to run the checker every hour
    0 * * * * /usr/bin/python3 /path/to/system_health.py
    ```

## Example Metrics Tracked

- **CPU Usage**
- **Memory Utilization**
- **Disk Space**
- **Network Latency and Uptime**

## 📑 Project Structure

```plaintext
system-health-checker/
│
├── health_checker.py   # Core script for system monitoring
├── alerts.py           # Handles notifications via email or Slack
├── config.py           # Configuration for thresholds and settings
├── requirements.txt    # Python dependencies
└── README.md           # Project documentation (this file)
