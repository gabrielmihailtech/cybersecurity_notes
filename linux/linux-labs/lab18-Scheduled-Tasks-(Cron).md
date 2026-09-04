# Lab 18 - Scheduled Tasks (Cron)

Commands:

- crontab -l
- sudo crontab -l
- ls /etc/cron*

Learned:

- Cron is the Linux scheduling service.
- Cron can automatically execute commands and scripts.
- User-specific scheduled tasks are stored in crontab.
- System-wide scheduled tasks are stored in cron directories.
- Cron is often used for maintenance, backups, updates, and automation.
- Cron can also be abused as a persistence mechanism by attackers.

Examples:

Display current user's scheduled tasks:

```bash
crontab -l
```

Observed Result:

```text
no crontab for gmihail
```

Meaning:

```text
The user gmihail does not have any scheduled tasks configured.
```

Display root scheduled tasks:

```bash
sudo crontab -l
```

Observed Result:

```text
no crontab for root
```

Meaning:

```text
The root user does not have any scheduled tasks configured.
```

View system cron directories:

```bash
ls /etc/cron*
```

Observed Directories:

```text
/etc/cron.daily
/etc/cron.hourly
/etc/cron.weekly
/etc/cron.monthly
/etc/cron.yearly
```

Observed Tasks:

Daily Tasks:

```text
apport
apt-compat
dpkg
logrotate
man-db
```

Weekly Tasks:

```text
man-db
```

Important Concepts:

Cron Job:

```text
A scheduled command or script that runs automatically.
```

Example:

```text
0 2 * * * backup.sh
```

Meaning:

```text
Run backup.sh every day at 02:00.
```

Common Cron Locations:

Hourly Tasks:

```text
/etc/cron.hourly
```

Daily Tasks:

```text
/etc/cron.daily
```

Weekly Tasks:

```text
/etc/cron.weekly
```

Monthly Tasks:

```text
/etc/cron.monthly
```

Yearly Tasks:

```text
/etc/cron.yearly
```

SOC Investigation Use Cases:

Check user scheduled tasks:

```bash
crontab -l
```

Check root scheduled tasks:

```bash
sudo crontab -l
```

Inspect system scheduled tasks:

```bash
ls /etc/cron*
```

Look for suspicious scripts:

```text
backup.sh
update_users.sh
unknown_script.sh
```

Possible Indicators:

```text
Unauthorized persistence
Malware execution
Repeated scheduled activity
```

Key Takeaways:

- Cron is used to automate tasks in Linux.
- Scheduled tasks may exist for users or the entire system.
- Cron directories contain automatically executed scripts.
- Cron is commonly checked during SOC and DFIR investigations.
- Unexpected cron jobs may indicate persistence mechanisms.
- System maintenance tasks often use cron.
