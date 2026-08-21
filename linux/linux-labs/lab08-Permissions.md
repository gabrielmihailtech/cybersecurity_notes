# Lab 08 - Linux Permissions

Commands:

- ls -l
- chmod +x
- chmod -x
- chmod 644
- chmod 755
- chmod 600
- chmod 700

Learned:

- Linux permissions are divided into:
  - owner
  - group
  - others

- Permission types:
  - r = read
  - w = write
  - x = execute

- First character meanings:
  - - = file
  - d = directory

Examples:

-rw-r--r--

Owner:
- read
- write

Group:
- read

Others:
- read

---

-rwxr-xr-x

Owner:
- read
- write
- execute

Group:
- read
- execute

Others:
- read
- execute

Numeric Permissions:

r = 4
w = 2
x = 1

Examples:

rwx = 7
rw- = 6
r-x = 5
r-- = 4

Common Permission Sets:

644

rw-r--r--

- Owner: read, write
- Group: read
- Others: read

Commonly used for files.

---

755

rwxr-xr-x

- Owner: read, write, execute
- Group: read, execute
- Others: read, execute

Commonly used for scripts and directories.

---

600

rw-------

- Owner: read, write
- Group: no access
- Others: no access

Commonly used for sensitive files.

---

700

rwx------

- Owner: read, write, execute
- Group: no access
- Others: no access

Commonly used for private scripts.

---

777

rwxrwxrwx

- Everyone can read
- Everyone can write
- Everyone can execute

Security Risk:
- Generally not recommended

Lab Exercises:

Check permissions:

ls -l script.sh

Add execute permission:

chmod +x script.sh

Remove execute permission:

chmod -x script.sh

Set permissions to 644:

chmod 644 script.sh

Set permissions to 755:

chmod 755 script.sh

Set permissions to 600:

chmod 600 script.sh

Set permissions to 700:

chmod 700 script.sh

Key Takeaways:

- ls -l displays permissions
- chmod changes permissions
- x controls execution
- 644 is common for files
- 755 is common for scripts and directories
- 600 and 700 are used for sensitive content
- 777 should generally be avoided
