# logTracker
Automated Log Archiver (Bash Script)  Overview  This project is a menu-driven Bash automation script that:  Archives old log files  Compresses them into .tar.gz  Deletes old logs after archiving  Cleans up old backup archives  Optionally schedules daily execution via cron  It simulates a real-world DevOps log rotation 

Features
🗃️ Custom selected log directory
⏳ Configurable length of time to retain logs for
⏱️ Configurable length of time to retain log backup archives for
📦 Automatic compression of log archives to .tar file format
🧹 Clean up of old log files
🕒 cron job to automate the daily execution of the script
📝 Maintain an archive activity log

⚙️ How It Works
1️⃣ User Configures:
Log directory (default: /var/log)
Days to keep logs (default: 7)
Days to keep backups (default: 30)


2️⃣ Archiving Process:
Finds logs older than specified days
Compresses them into:
archive/logs_archive_YYYYMMDD_HHMMSS.tar.gz
Deletes original logs after archiving
Deletes old backup archives beyond retention limit

📥 Installation
Clone the repository:
git clone https://github.com/your-username/log-archiver.git
cd log-archiver
Make the script executable:
chmod u+x log-archive.sh

▶️ Usage
Run the script:
./log-archive.sh
You will see an interactive menu:

1. Specify Log Directory
2. Specify Number of Days to Keep Logs
3. Specify Number of Days to Keep Backup Archives
4. Run Log Archiving Process
5. Exit
🕒 Setup Cron Job (Optional)

The script can automatically add itself to cron:
0 2 * * * /usr/local/bin/log-archive.sh
This runs daily at 2:00 AM.

To manually install:
sudo mv log-archive.sh /usr/local/bin/
crontab -e

Add:
0 2 * * * /usr/local/bin/log-archive.sh


🔍 Technologies Used
Bash Scripting
Linux File System Commands
find
tar
cron
Shell Functions & Case Statements


🧠 Concepts Demonstrated
Automation
Log rotation strategy
System maintenance scripting
Production-style cleanup policies
Cron scheduling
Safe file handling using -print0

🛡 Example Use Case
This script can be used in:
Linux servers
Cloud VM instances
DevOps environments
Personal log cleanup automation
Academic system scripting projects


