*****Linux Cheat Sheet*****

---NAVIGATION

*pwd

Purpose: Display the current working directory.

When I use it: When I need to know my current location in the filesystem.

Example:

pwd

Output:

/home/name/linux-lab


*ls

Purpose: List files and directories.

When I use it: When I want to see the contents of the current directory.

Example:
ls


Output:

auth.log
users.txt
script.sh


*cd dir

Purpose: Change directory/ enter directory.

When I use it: When navigating through the Linux filesystem.

Example:

cd /var/log

*cd ..
Purpose: go to parent directory/ go back to previous directory

*cd ~
Purpose: go to home directory


---FILES

*mkdir
mkdir logs

Purpose: Create a directory.

When I use it: When organizing files into folders.

*touch
touch auth.log

Purpose: Create an empty file.

When I use it: When creating a new file quickly.


*cp
cp auth.log backup.log

Purpose: Copy files.

When I use it: Before modifying or deleting important files.


*mv
mv file1.txt file2.txt

Purpose: Move or rename files.

When I use it: When organizing files or changing filenames.


*rm
rm file.txt

Purpose: Delete files.

When I use it: When removing unnecessary files.


---READING FILES


*cat
cat auth.log

Purpose: Display the entire file content.

When I use it: When viewing small files.

Output:
Failed password for admin
Accepted password for user


*head
head auth.log

Purpose: Display the first 10 lines.

When I use it: When checking the beginning of a file.


*tail
tail auth.log

Purpose: Display the last 10 lines.

When I use it: When reviewing recent log entries.


*tail -f
tail -f auth.log

Purpose: Monitor a file in real time.

When I use it: When monitoring live log activity.


*Exit:

Ctrl + C


*less
less auth.log

Purpose: Read large files interactively.

When I use it: When files are too large for cat.


*Exit:

*q

---SEARCH and FILTERING


*grep
grep "admin" auth.log

Purpose: Search text inside files.

When I use it: When searching logs for users, IPs, errors, or events.

Output:

Failed password for admin


*grep -i
grep -i "failed" auth.log

Purpose: Search text without case sensitivity.

When I use it: When capitalization may vary.


*wc -l
wc -l auth.log

Purpose: Count lines.

When I use it: When measuring file size or counting events.

Output:

24 auth.log


*Pipe
*|

Purpose: Send output from one command to another.

When I use it: When combining commands.

Example:

grep "Failed" auth.log | wc -l

Meaning:

Find all Failed entries and count them.


---SORTING and COUNTING


*sort
sort users.txt


Purpose: Sort lines alphabetically.

When I use it: Before using uniq.

*uniq
sort users.txt | uniq

Purpose: Show unique values.

When I use it: To remove duplicates.


*uniq -c
sort users.txt | uniq -c

Purpose: Count occurrences of unique values.

When I use it: To identify frequently occurring users, IPs, or events.

Output:
2 admin
1 administrator
2 guest
2 root


---FINDING FILES


*find
find . -name "*.txt"

Purpose: Search for files and directories.

When I use it: When I know the name or extension but not the location.


*find by exact name
find . -name "auth.log"

Purpose: Find a specific file.


*find files only
find . -type f

Purpose: Display files only.


*find directories only
find . -type d

Purpose: Display directories only.


---USERS and GROUPS


*whoami
whoami

Purpose: Display the current user.

Output:

name


*id
id

Purpose: Display user ID, group ID, and memberships.

When I use it: When checking permissions and group membership.


*groups
groups

Purpose: Display the groups the user belongs to.


*/etc/passwd
cat /etc/passwd | head

Purpose: View system users.


---PERMISSIONS


*ls -l
ls -l

Purpose: Display file permissions.

Output:
-rwxr-xr-x


*chmod +x
chmod +x script.sh

Purpose: Add execute permission.

When I use it: Before running scripts.

*chmod -x
chmod -x script.sh

Purpose: Remove execute permission.

*chmod 644
chmod 644 file.txt

Purpose: Owner can read/write. Others can read.

Result:

-rw-r--r--


*chmod 755
chmod 755 script.sh

Purpose: Owner has full access. Others can read and execute.

Result:

-rwxr-xr-x


*chmod 600
chmod 600 secret.txt

Purpose: Only owner has access.

Result:

-rw-------


*chmod 700
chmod 700 script.sh

Purpose: Only owner can read, write, and execute.

Result:

-rwx------

---LOGS


*View authentication log
tail auth.log

Purpose: Check recent authentication events.


*Search sudo activity
grep "sudo" auth.log

Purpose: View privilege escalation activity.


*Count sudo events
grep "sudo" auth.log | wc -l

Purpose: Count sudo-related events.


*journalctl
journalctl -n 20

Purpose: View recent system events.


---PROCESSES


*ps
ps

Purpose: Display running processes.


*ps aux
ps aux

Purpose: Display detailed process information.


*top
top

Purpose: Monitor processes in real time.


*Exit:
q


*Find a process
ps aux | grep bash

Purpose: Search for a specific process.


*kill
kill PID

Purpose: Terminate a process.

Example:

kill 4915


--SYSTEM MONITORING


*df -h
df -h

Purpose: Display disk usage.


*free -h
free -h

Purpose: Display memory and swap usage.


*du -sh
du -sh .

Purpose: Display total directory size.


*uname -a
uname -a

Purpose: Display kernel and system information.


---NETWORKING


*ip addr
ip addr

Purpose: Display IP addresses.


*ip link
ip link

Purpose: Display network interfaces.


*ss -tuln
ss -tuln

Purpose: Display listening ports and services.


*ss -tulpn
sudo ss -tulpn

Purpose: Display listening ports with associated processes.


*ping
ping 8.8.8.8

Purpose: Test network connectivity.


*ip route
ip route

Purpose: Display routing information and default gateway.

Output Example:

default via 172.20.32.1 dev eth0


-->Linux Directories to Remember

/          -> root
/home      -> user directories
/etc       -> configuration files
/var/log   -> log files


