# Lab 14 - Text Processing

Commands:

- cat
- sort
- uniq
- uniq -c
- tr
- wc -l

Learned:

- sort organizes lines alphabetically
- uniq removes duplicate lines
- uniq -c counts occurrences of unique values
- tr transforms characters and text
- wc -l counts lines in a file
- Combining commands with pipes allows efficient text analysis

Lab Setup:

Create user list:

```bash
cat > users.txt
```

Content:

```text
admin
root
admin
guest
root
administrator
guest
```

Display file contents:

```bash
cat users.txt
```

Sort Data:

```bash
sort users.txt
```

Observed Example:

```text
admin
admin
administrator
guest
guest
root
root
```

Display Unique Values:

```bash
sort users.txt | uniq
```

Observed Example:

```text
admin
administrator
guest
root
```

Count Occurrences:

```bash
sort users.txt | uniq -c
```

Observed Example:

```text
2 admin
1 administrator
2 guest
2 root
```

Create IP List:

```bash
cat > iplist.txt
```

Content:

```text
192.168.1.10
192.168.1.20
10.0.0.1
192.168.1.10
192.168.1.20
192.168.1.10
```

Display Unique IP Addresses:

```bash
sort iplist.txt | uniq
```

Observed Example:

```text
10.0.0.1
192.168.1.10
192.168.1.20
```

Count IP Occurrences:

```bash
sort iplist.txt | uniq -c
```

Observed Example:

```text
1 10.0.0.1
3 192.168.1.10
2 192.168.1.20
```

Text Transformation:

Create sample text:

```bash
echo "linux soc analyst" > text.txt
```

Display content:

```bash
cat text.txt
```

Convert to uppercase:

```bash
cat text.txt | tr 'a-z' 'A-Z'
```

Observed Output:

```text
LINUX SOC ANALYST
```

Count Lines:

Count lines in users.txt:

```bash
wc -l users.txt
```

Count lines in iplist.txt:

```bash
wc -l iplist.txt
```

Important Concepts:

Sort Data:

```bash
sort filename
```

Remove Duplicates:

```bash
sort filename | uniq
```

Count Unique Values:

```bash
sort filename | uniq -c
```

Transform Text:

```bash
tr 'a-z' 'A-Z'
```

Count Lines:

```bash
wc -l filename
```

SOC Use Cases:

Count IP occurrences:

```bash
sort iplist.txt | uniq -c
```

Identify unique users:

```bash
sort users.txt | uniq
```

Count unique usernames:

```bash
sort users.txt | uniq -c
```

Normalize text formatting:

```bash
tr 'a-z' 'A-Z'
```

Key Takeaways:

- sort prepares data for analysis
- uniq identifies unique values
- uniq -c provides occurrence counts
- tr transforms text between formats
- wc -l counts lines quickly
- sort | uniq -c is one of the most useful command combinations for SOC investigations
- Text processing is essential when analyzing logs, user activity, IP addresses, and events
``
