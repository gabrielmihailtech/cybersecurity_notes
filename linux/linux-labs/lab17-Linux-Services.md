# Lab 17 - Linux Services

Commands:

- service --status-all
- service <service_name> status
- ps aux
- grep

Learned:

- Services are background programs that provide system functionality.
- Services can be running or stopped.
- Service status can be checked using the service command.
- Running services usually have associated processes.
- Processes can be verified using ps and grep.
- Services are important during SOC investigations because they may indicate legitimate activity or persistence mechanisms.

Examples:

List all services:

```bash
service --status-all
```

Status Indicators:

```text
[ + ] Service is running
[ - ] Service is stopped
```

Observed Examples:

Running:

```text
dbus
chrony
```

Stopped:

```text
cron
apport
```

Check a specific service:

```bash
service cron status
```

Observed Result:

```text
Active: inactive (dead)
```

Meaning:

```text
The cron service is currently stopped.
```

Investigate related processes:

```bash
ps aux | grep cron
```

Observed Result:

```text
grep --color=auto cron
```

Explanation:

- The only visible process was the grep command itself.
- No active cron process was running.
- This confirmed the service status reported as inactive.

Important Concepts:

Service:

```text
Background process managed by the operating system.
```

Examples:

```text
cron
dbus
chrony
```

Service Status Check:

```bash
service <service_name> status
```

Example:

```bash
service cron status
```

Process Verification:

```bash
ps aux | grep <service_name>
```

Example:

```bash
ps aux | grep cron
```

SOC Use Cases:

Check running services:

```bash
service --status-all
```

Verify suspicious service activity:

```bash
service <service_name> status
```

Confirm whether a service has a running process:

```bash
ps aux | grep <service_name>
```

Investigate persistence mechanisms:

```text
cron jobs
background services
scheduled tasks
```

Key Takeaways:

- Services provide background functionality in Linux.
- Not all installed services are running.
- service --status-all quickly shows service status.
- service <name> status provides detailed information.
- ps aux | grep helps verify whether a service process is active.
- A service marked as inactive may have no corresponding running process.
- Service analysis is useful during Linux troubleshooting and SOC investigations.
