## Commands

pwd     # show current directory
ls      # list files
cd      # change directory
mkdir   # create directory
touch   # create empty file
cp      # copy file
mv      # move/rename file
rm      # delete file

cat     # display file content
head    # show first 10 lines
tail    # show last 10 lines
less    # view large files

grep    # search text
sort    # sort lines
uniq    # show unique values
wc -l   # count lines

## Important Concepts:

Relative Path

cd linux-lab   # Uses current location.

Absolute Path

cd /var/log   # Starts from root /.

Linux Directories:

/ -> root directory
/home -> users
/etc -> configuration files
/var/log -> logs

## Notes

- > overwrites file content
  Example: echo "test" > file.txt
- >> appends content
  Example: echo "test" >> file.txt
- Avoid spaces in folder names
- Pipe: |   # Passes output from one command to another.
  Example: grep "Failed" auth.log | wc -l   # Find failed logins and count them.

## SOC Examples

Search failed logins: grep "Failed" auth.log

Count failed logins: grep "Failed" auth.log | wc -l

Case-insensitive search: grep -i "failed" auth.log

Unique IPs: sort ips.txt | uniq

Count IP occurrences: sort ips.txt | uniq -c

## Lessons Learned

## Path Types

Relative Path

cd linux-lab

Uses current location.

Absolute Path

cd /var/log

Starts from root (/).

---

## Important Linux Directories

/         -> root directory
/home     -> users
/etc      -> configuration files
/var/log  -> logs
