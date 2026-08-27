# Lab 11 - System Information & Disk Usage

Commands:

- df -h
- free -h
- du -h
- du -sh
- uname -a
- wc -l

Learned:

- df displays disk space usage
- free displays memory and swap usage
- du displays file and directory sizes
- uname displays system information
- wc -l counts lines in a file
- WSL presents Linux storage differently than a traditional Linux installation

Examples:

Display disk usage:

```bash
df -h
```

Useful Fields:

- Filesystem
- Size
- Used
- Available
- Use%

Observed Example:

```text
/dev/sdd
Size: 1007G
Used: 2.2G
Available: 954G
Use%: 1%
```

Display memory usage:

```bash
free -h
```

Observed Example:

```text
Mem: 7.6Gi
Swap: 2.0Gi
```

Display directory size:

```bash
du -h
```

Observed Result:

```text
16K .
```

Display total directory size summary:

```bash
du -sh
```

Observed Example:

```text
275M .
```

Note:

Some directories returned:

```text
Permission denied
```

This is normal when the user does not have access to certain folders.

Display kernel and system information:

```bash
uname -a
```

Observed Example:

```text
Linux DP-PM4
6.18.33.1-microsoft-standard-WSL2
x86_64 GNU/Linux
```

Count lines in a file:

```bash
wc -l auth.log
```

Observed Result:

```text
6 auth.log
```

Meaning:

```text
auth.log contains 6 lines
```

Command Summary:

Check disk space:

```bash
df -h
```

Check RAM and swap:

```bash
free -h
```

Check file/folder size:

```bash
du -h
```

Check total folder size:

```bash
du -sh
```

Check operating system details:

```bash
uname -a
```

Count lines:

```bash
wc -l filename
```

Key Takeaways:

- df -h is useful for checking available storage
- free -h is useful for checking memory usage
- du -h and du -sh help identify large directories
- uname -a provides Linux kernel and platform information
- wc -l quickly counts lines in files
- Permission denied errors can occur when accessing protected directories
- These commands are commonly used for troubleshooting and system monitoring
