# Lab 15 - Advanced Log Analysis

Commands:

- grep
- sort
- uniq
- uniq -c
- wc -l
- tail
- journalctl

Learned:

- Logs can be searched for specific events
- Administrative activity can be identified through sudo entries
- Commands executed with sudo can be extracted from logs
- sort and uniq help identify repeated actions
- uniq -c helps count repeated events
- Recent activity can be analyzed using tail

Working Directory:

```bash
cd /var/log
```

Authentication Log:

```bash
auth.log
```

Investigations Performed:

Search for sudo activity:

```bash
grep "sudo" auth.log
```

Count sudo events:

```bash
grep "sudo" auth.log | wc -l
```

Search executed commands:

```bash
grep "COMMAND=" auth.log
```

Count executed commands:

```bash
grep "COMMAND=" auth.log | wc -l
```

Display commands in sorted order:

```bash
grep "COMMAND=" auth.log | sort
```

Display unique commands:

```bash
grep "COMMAND=" auth.log | sort | uniq
```

Count unique commands:

```bash
grep "COMMAND=" auth.log | sort | uniq -c
```

Investigate user activity:

```bash
grep "gmihail" auth.log
```

Count user-related events:

```bash
grep "gmihail" auth.log | wc -l
```

View latest log events:

```bash
tail -20 auth.log
```

SOC Investigation Concepts:

Who used administrative privileges?

```bash
grep "sudo" auth.log
```

What commands were executed?

```bash
grep "COMMAND=" auth.log
```

How many times was a command executed?

```bash
grep "COMMAND=" auth.log | sort | uniq -c
```

How active was a specific user?

```bash
grep "gmihail" auth.log | wc -l
```

Useful Command Combinations:

Search and count:

```bash
grep "text" file | wc -l
```

Search, sort and remove duplicates:

```bash
grep "text" file | sort | uniq
```

Search, sort and count occurrences:

```bash
grep "text" file | sort | uniq -c
```

Key Takeaways:

- auth.log is one of the most useful logs for Linux investigations
- sudo events reveal administrative activity
- grep is the primary tool for searching logs
- wc -l quickly counts matching events
- sort and uniq help identify repeated patterns
- tail is useful for reviewing recent activity
- Combining multiple commands provides powerful log analysis capabilities
