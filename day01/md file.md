
# Linux Interview Questions

## 1. What is the difference between a hard link and a soft link in Linux?

### Answer:
- Hard link points directly to inode
- Soft link (symbolic link) points to file path
- Hard links cannot cross file systems
- Soft links can cross file systems
- Deleting original file:
  - hard link still works
  - soft link breaks

---

## 2. Explain the Linux file permissions model.

### Answer:
Linux permissions are divided into:
- User (owner)
- Group
- Others

Permission types:
- `r` → read
- `w` → write
- `x` → execute

Example:

```bash
-rwxr-xr--
```
- Owner → rwx
- Group → r-x
- Others → r--

---

## 3. Difference between `grep`, `egrep`, and `fgrep`.

### Answer:
- `grep` → basic pattern search
- `egrep` → extended regular expressions
- `fgrep` → fixed string search (no regex)

Examples:

```bash
grep "error" file.txt
egrep "error|warning" file.txt
fgrep "hello.world" file.txt
```

---

## 4. What is the difference between `kill`, `killall`, and `pkill`?

### Answer:
- `kill` → terminate process using PID
- `killall` → terminate processes by exact name
- `pkill` → terminate processes using pattern matching

Examples:

```bash
kill 1234
killall nginx
pkill java
```

---

## 5. Explain `stdin`, `stdout`, and `stderr` in Linux.

### Answer:
- `stdin` → standard input → file descriptor 0
- `stdout` → standard output → file descriptor 1
- `stderr` → standard error → file descriptor 2

Examples:

```bash
command > output.txt
command 2> error.txt
command > output.txt 2>&1
```

- `>` redirects stdout
- `2>` redirects stderr
- `2>&1` combines both
