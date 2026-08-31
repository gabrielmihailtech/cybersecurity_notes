# Lab 13 - Archives and Compression

Commands:

- tar -cvf
- tar -tvf
- tar -xvf
- tar -czvf
- tar -xzvf
- mkdir
- touch
- ls

Learned:

- tar can create archives containing multiple files
- tar can display the contents of an archive
- tar can extract archived files
- gzip compression can be combined with tar
- .tar files are archives
- .tar.gz files are compressed archives
- Linux administrators and DFIR analysts frequently encounter archive files

Lab Setup:

Create working directory:

```bash
mkdir backup_test
cd backup_test
```

Create sample files:

```bash
touch file1.txt
touch file2.txt
touch file3.txt
```

Verify files:

```bash
ls
```

Observed Files:

```text
file1.txt
file2.txt
file3.txt
```

Create TAR Archive:

```bash
tar -cvf backup.tar file1.txt file2.txt file3.txt
```

Options:

```text
c = create
v = verbose
f = file
```

Verify archive:

```bash
ls
```

Observed:

```text
backup.tar
```

View Archive Contents:

```bash
tar -tvf backup.tar
```

Options:

```text
t = list contents
v = verbose
f = file
```

Observed Contents:

```text
file1.txt
file2.txt
file3.txt
```

Extract Archive:

Create extraction directory:

```bash
mkdir extracted
```

Extract:

```bash
tar -xvf backup.tar -C extracted
```

Options:

```text
x = extract
C = extract into specified directory
```

Verify extraction:

```bash
ls extracted
```

Observed:

```text
file1.txt
file2.txt
file3.txt
```

Create Compressed Archive:

```bash
tar -czvf backup.tar.gz file1.txt file2.txt file3.txt
```

Options:

```text
c = create
z = gzip compression
v = verbose
f = file
```

Verify:

```bash
ls
```

Observed:

```text
backup.tar
backup.tar.gz
```

Extract Compressed Archive:

Create directory:

```bash
mkdir extracted_gz
```

Extract:

```bash
tar -xzvf backup.tar.gz -C extracted_gz
```

Verify:

```bash
ls extracted_gz
```

Observed:

```text
file1.txt
file2.txt
file3.txt
```

Troubleshooting Encountered:

Command entered incorrectly:

```bash
tar -xvf backup.tar -c extracted
```

Error:

```text
You may not specify more than one '-Acdtrux'
```

Reason:

```text
-c = create
-x = extract
```

Both options cannot be used together.

Correct command:

```bash
tar -xvf backup.tar -C extracted
```

Important Concepts:

TAR Archive:

```text
backup.tar
```

Compressed TAR Archive:

```text
backup.tar.gz
```

Common TAR Options:

```text
c = create
t = list contents
x = extract
z = gzip compression
v = verbose
f = archive file
C = extraction directory
```

Key Takeaways:

- tar is one of the most common archive utilities in Linux
- Archives can contain multiple files and directories
- gzip compression reduces archive size
- tar -tvf allows inspection of archive contents before extraction
- tar -xvf extracts archives
- tar -czvf creates compressed archives
- tar -xzvf extracts compressed archives
- Archive handling is useful in Linux administration, DFIR, backups, and incident investigations
