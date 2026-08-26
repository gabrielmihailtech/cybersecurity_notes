# Lab 10 - Linux Processes

Commands:

- ps
- ps aux
- top
- grep
- kill

Learned:

- A process is a running program
- Each process has a unique PID (Process ID)
- ps displays running processes
- ps aux displays detailed process information
- top provides real-time process monitoring
- grep can be combined with ps to find specific processes
- kill terminates a process using its PID

Examples:

Display running processes:

```bash
ps
```

Example Output:

```text
PID TTY          TIME CMD
381 pts/0    00:00:00 bash
4834 pts/0   00:00:00 ps
```

Display detailed process information:

```bash
ps aux
```

Useful Fields:

- USER = process owner
- PID = Process ID
- %CPU = CPU usage
- %MEM = Memory usage
- COMMAND = running program

Real-time process monitoring:

```bash
top
```

Exit:

```text
q
```

Find bash processes:

```bash
ps aux | grep bash
```

Observed Example:

```text
381 bash
453 bash
675 bash
```

Create a temporary process:

```bash
sleep 300
```

Stop process:

```text
Ctrl + C
```

Run a process in the background:

```bash
sleep 300 &
```

Observed Example:

```text
[1] 4915
```

Find the process:

```bash
ps aux | grep sleep
```

Observed Example:

```text
4915 sleep 300
```

Terminate a process:

```bash
kill 4915
```

Verify termination:

```bash
ps aux | grep sleep
```

Process Investigation Notes:

PID = Process ID

Example:

```text
4915 sleep 300
```

- 4915 = PID
- sleep = process name
- 300 = parameter

Important Observation:

The grep process receives a new PID every time it is executed.

Examples:

```text
4894 grep bash
4926 grep sleep
4946 grep sleep
```

Reason:

Each command execution creates a new process.

The PID changes because:

```text
grep bash
```

and

```text
grep sleep
```

are separate processes.

Key Takeaways:

- ps shows running processes
- ps aux provides detailed information
- top monitors processes in real time
- PID uniquely identifies a process
- grep helps locate specific processes
- kill stops a process using its PID
- Background processes can be started with &
- A new process receives a new PID when started
