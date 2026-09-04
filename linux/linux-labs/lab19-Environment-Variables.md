# Lab 19 - Environment Variables

Commands:

- env
- echo $USER
- echo $HOME
- echo $SHELL
- echo $PATH
- which

Learned:

- Environment variables store information used by Linux and applications.
- Variables can contain user information, paths, shell settings, and configuration data.
- The PATH variable determines where Linux searches for commands.
- The which command identifies the real location of executables.

Examples:

Display environment variables:

```bash
env
```

Important Variables:

```text
HOME
USER
SHELL
PATH
```

Display current user:

```bash
echo $USER
```

Observed Result:

```text
gmihail
```

Display home directory:

```bash
echo $HOME
```

Observed Result:

```text
/home/gmihail
```

Display current shell:

```bash
echo $SHELL
```

Observed Result:

```text
/bin/bash
```

Display PATH variable:

```bash
echo $PATH
```

Observed:

```text
Multiple directories separated by :
```

Purpose:

```text
Linux searches these directories when executing commands.
```

Find executable location:

```bash
which ls
```

Observed Result:

```text
/usb/bin/ls
```

Meaning:

```text
Linux found the ls command in /usr/bin.
```

Important Variables:

USER

```bash
echo $USER
```

Purpose:

```text
Displays the current user.
```

HOME

```bash
echo $HOME
```

Purpose:

```text
Displays the user's home directory.
```

SHELL

```bash
echo $SHELL
```

Purpose:

```text
Displays the active shell.
```

PATH

```bash
echo $PATH
```

Purpose:

```text
Displays directories searched for executable commands.
```

SOC Use Cases:

Identify user executing commands:

```bash
echo $USER
```

Verify shell environment:

```bash
echo $SHELL
```

Investigate command locations:

```bash
which command
```

Review search paths:

```bash
echo $PATH
```

Key Takeaways:

- Environment variables store important system information.
- USER identifies the logged-in user.
- HOME identifies the user's working area.
- SHELL identifies the command interpreter.
- PATH determines where commands are located.
- which helps identify the actual executable being used.
- Environment variables are commonly referenced in Linux scripts and investigations.
