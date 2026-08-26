# Lab 09 - Linux Logs

Commands:

- cd /var/log
- pwd
- ls
- head
- tail
- grep
- wc -l
- journalctl

Log Files Explored:

- auth.log
- syslog
- kern.log
- journal

Learned:

- /var/log stores system log files
- auth.log contains authentication and sudo events
- syslog contains general system activity
- grep can be used to search for specific events
- wc -l can be used to count matching events
- journalctl displays events from the system journal

Examples:

Navigate to log directory:

```bash
cd /var/log
pwd
```

List available log files:

```bash
ls
```

View first 10 log entries:

```bash
head auth.log
```

View last 10 log entries:

```bash
tail auth.log
```

Search for sudo activity:

```bash
grep "sudo" auth.log
```

Count sudo-related events:

```bash
grep "sudo" auth.log | wc -l
```

Search for a specific user:

```bash
grep "gmihail" auth.log
```

Count user-related events:

```bash
grep "gmihail" auth.log | wc -l
```

Count opened sessions:

```bash
grep "session opened" auth.log | wc -l
```

Count closed sessions:

```bash
grep "session closed" auth.log | wc -l
```

View recent system events:

```bash
journalctl -n 20
```

Observations:

Session Opened Events:

```bash
grep "session opened" auth.log | wc -l
```

Result:

```text
10
```

Session Closed Events:

```bash
grep "session closed" auth.log | wc -l
```

Result:

```text
8
```

User Activity:

```bash
grep "gmihail" auth.log | wc -l
```

Result:

```text
13
```

Sudo Activity:

```bash
grep "sudo" auth.log | wc -l
```

Result:

```text
9
```

Examples Found:

```text
sudo: pam_unix(sudo:session): session opened for user root
```

```text
sudo: pam_unix(sudo:session): session closed for user root
```

```text
sudo: gmihail : COMMAND=/usr/bin/grep Failed auth.log
```

Key Takeaways:

- Log analysis is a core SOC analyst activity
- auth.log is useful for investigating authentication events
- grep helps find relevant events quickly
- wc -l provides fast event counts
- tail is often more useful than head during investigations because it shows the most recent activity
- journalctl can be used to review recent system events
- Sudo usage can be traced through auth.log
