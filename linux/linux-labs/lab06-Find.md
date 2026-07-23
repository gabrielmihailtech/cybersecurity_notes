# Lab 06 - Find

Commands:

- find
- find -name
- find -type f
- find -type d

Learned:

- find searches files and directories
- -name searches by filename
- -type f shows files only
- -type d shows directories only
- find can search recursively

Examples:

find . -name "*.txt"

find . -name "*.log"

find . -name "auth.log"

find . -type f

find . -type d

find /var/log -name "*.log"

find . -name "*.txt" | wc -l

Notes:

- "." represents the current directory
- Permission denied is normal for protected directories
