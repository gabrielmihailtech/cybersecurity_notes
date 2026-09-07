# Lab 20 - Bash Scripting Basics

Commands:

- nano
- chmod
- echo
- date
- cat

Learned:

- Bash scripts automate commands.
- Scripts are stored in .sh files.
- The shebang identifies the interpreter used to run the script.
- Variables can store values and system information.
- Scripts can access environment variables.
- Scripts can execute standard Linux commands.

Creating a Script:

Create a file:

```bash
nano script1.sh
```

Basic Script:

```bash
#!/bin/bash

echo "Hello Gabriel"
```

Important Concept:

Shebang:

```bash
#!/bin/bash
```

Meaning:

```text
Run this script using Bash.
```

Make Script Executable:

```bash
chmod 755 script1.sh
```

Verify Permissions:

```bash
ls -l script1.sh
```

Observed Example:

```text
-rwxr-xr-x
```

Run Script:

```bash
./script1.sh
```

Output:

```text
Hello Gabriel
```

Using Variables:

Script:

```bash
#!/bin/bash

NAME="Gabriel"

echo "Hello $NAME"
```

Output:

```text
Hello Gabriel
```

Using Environment Variables:

Script:

```bash
#!/bin/bash

echo "Current user: $USER"
```

Output:

```text
Current user: gmihail
```

Display Date and Time:

Script:

```bash
#!/bin/bash

echo "Current date:"
date
```

Output Example:

```text
Current date:
Mon Sep 07 2026
```

SOC Information Script:

Script:

```bash
#!/bin/bash

echo "User: $USER"
echo "Home: $HOME"
echo "Shell: $SHELL"
```

Output Example:

```text
User: gmihail
Home: /home/gmihail
Shell: /bin/bash
```

Important Concepts:

Create Variable:

```bash
NAME="Gabriel"
```

Display Variable:

```bash
echo $NAME
```

Display Current User:

```bash
echo $USER
```

Display Home Directory:

```bash
echo $HOME
```

Display Shell:

```bash
echo $SHELL
```

Run Script:

```bash
./script1.sh
```

SOC Use Cases:

Display system information:

```bash
echo $USER
echo $HOME
echo $SHELL
```

Automate repetitive commands:

```bash
log searches
system checks
daily tasks
```

Key Takeaways:

- Bash scripts automate tasks.
- The shebang tells Linux which interpreter to use.
- chmod makes scripts executable.
- Variables store reusable values.
- Environment variables can be accessed inside scripts.
- Scripts can combine multiple Linux commands.
- Basic Bash scripting is useful for SOC automation and administration tasks.
