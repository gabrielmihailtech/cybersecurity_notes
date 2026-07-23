# Lab 05 - Sort and Uniq

Commands:

- sort
- uniq
- uniq -c

Created:

- ips.txt

Learned:

- sort arranges lines in order
- uniq removes duplicate lines
- uniq -c counts occurrences
- sort is often used before uniq

Examples:

sort ips.txt

sort ips.txt | uniq

sort ips.txt | uniq -c

Results:

1 10.0.0.1
3 192.168.1.10
2 192.168.1.20
