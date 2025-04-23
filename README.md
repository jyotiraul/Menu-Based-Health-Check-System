# System Health Check Script

## Overview
This is a **menu-based Bash script** that performs essential **system health checks** and sends a **comprehensive report via email** every four hours. It helps in monitoring disk usage, running services, memory usage, and CPU performance.

## Features
- **Check Disk Usage**: Displays available and used disk space.
- **Monitor Running Services**: Lists currently active services.
- **Assess Memory Usage**: Shows memory consumption.
- **Evaluate CPU Usage**: Monitors CPU performance.
- **Send Comprehensive Report via Email**: Gathers system data and sends a detailed report.
- **Automated Email Report Every Four Hours** (via `cron`).

## Prerequisites
Ensure your system meets the following requirements:
- **Linux (Ubuntu, CentOS, or any Unix-based system)**
- **Bash Shell**
- **mailx (for email functionality)**
- **sudo access**

## Automating the Report
To send the system health report every **four hours**, add a `cron` job:
```sh
crontab -e
```
Add the following line at the end:
```
0 */4 * * * /path/to/menu.sh --email
```
Save and exit.

##For mail 
install msmtp -sudo apt install msmtp msmtp-mta
```
vim ~/.msmtprc #give permission 600
```
#account default

#host smtp.gmail.com

#port 587

#from your_email@gmail.com

#user your_email@gmail.com

#password your_app_password_here   # Generate this via Gmail App Passwords

#tls on

#tls_starttls on

#auth on

#logfile ~/.msmtp.log

