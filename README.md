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

⚙️ How It Works<br>
1️⃣ User Configures:
Log directory (default: /var/log)<br>
Days to keep logs (default: 7)<br>
Days to keep backups (default: 30)<br>


2️⃣ Archiving Process:<br>
Finds logs older than specified days<br>
Compresses them into:<br>
archive/logs_archive_YYYYMMDD_HHMMSS.tar.gz<br>
Deletes original logs after archiving<br>
Deletes old backup archives beyond retention limit<br>

📥 Installation
Clone the repository:<br>
git clone https://github.com/your-username/log-archiver.git<br>
cd log-archiver<br>
Make the script executable:<br>
chmod u+x log-archive.sh<br>

▶️ Usage<br>
Run the script:<br>
./log-archive.sh<br>
You will see an interactive menu:<br>

1. Specify Log Directory<br>
2. Specify Number of Days to Keep Logs<br>
3. Specify Number of Days to Keep Backup Archives<br>
4. Run Log Archiving Process<br>
5. Exit<br>
🕒 Setup Cron Job (Optional)<br>

The script can automatically add itself to cron:<br>
0 2 * * * /usr/local/bin/log-archive.sh<br>
This runs daily at 2:00 AM.<br>

To manually install:<br>
sudo mv log-archive.sh /usr/local/bin/<br>
crontab -e<br>

Add:
0 2 * * * /usr/local/bin/log-archive.sh


🔍 Technologies Used<br>
Bash Scripting<br>
Linux File System Commands<br>
find<br>
tar<br>
cron<br>
Shell Functions & Case Statements<br>


🧠 Concepts Demonstrated<br>
Automation<br>
Log rotation strategy<br>
System maintenance scripting<br>
Production-style cleanup policies<br>
Cron scheduling<br>
Safe file handling using -print0<br>

🛡 Example Use Case<br>
This script can be used in:<br>
Linux servers<br>
Cloud VM instances<br>
DevOps environments<br>
Personal log cleanup automation<br>
Academic system scripting projects<br>


