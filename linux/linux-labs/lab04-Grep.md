# Lab 04 - Grep

Commands:

- grep
- grep -i
- wc -l
- |

Learned:

- grep searches text inside files
- grep -i ignores case sensitivity
- wc -l counts lines
- Pipe (|) sends output from one command to another

Examples:

grep "admin" auth.log

grep "Failed" auth.log

grep -i "failed" auth.log

grep "Failed" auth.log | wc -l

grep "192.168.1.10" auth.log
