# DirBuster

## Overview

DirBuster is a legacy, multi-threaded Java-based application used to brute-force directories and file names on web servers. It is best known for its graphical user interface (GUI), making it beginner-friendly while still providing powerful directory and file enumeration capabilities during web application reconnaissance.

---

## Purpose / Uses

- **Directory and File Enumeration** – Discover hidden directories and files on a web server.
- **Recursive Content Discovery** – Automatically scan newly discovered directories for additional content.
- **Sensitive File Discovery** – Locate backup files, configuration files, and hidden scripts.
- **Web Application Reconnaissance** – Identify unlinked resources that may expose sensitive information.

---

## Installation

### Kali Linux

✅ **Preinstalled in Kali Linux**

Verify installation:

```bash
dirbuster
```

If not installed:

```bash
sudo apt update
sudo apt install dirbuster -y
```

---

## Basic Commands

### 1. Launch DirBuster

```bash
dirbuster
```

**Explanation**

Launches the graphical user interface.

---

### 2. Start a Scan (Command Line)

```bash
dirbuster -u http://target.com -l /path/to/wordlist.txt
```

**Explanation**

- `-u` – Specifies the target URL.
- `-l` – Specifies the wordlist to use.
- Performs directory and file brute-forcing against the target.

---

### 3. Common GUI Workflow

1. Open DirBuster.
2. Enter the target URL.
3. Select a wordlist.
4. Configure threads if required.
5. Click **Start** to begin scanning.

---

## Example Usage

### Scan a Website

```bash
dirbuster -u http://example.com -l /usr/share/dirbuster/wordlists/directory-list-2.3-medium.txt
```

**Expected Output**

```
Found Directory: /admin
Found Directory: /backup
Found File: config.php
Found File: robots.txt
```

---

## Screenshot

```markdown
![DirBuster Screenshot](../screenshots/dirbuster.png)
```

---

## Advantages

- Beginner-friendly graphical interface.
- Supports recursive directory discovery.
- Includes built-in wordlists.
- Multi-threaded scanning improves performance over single-threaded tools.
- Useful for discovering hidden web content.

---

## Limitations

- Java-based application consumes more system resources.
- Slower than modern tools such as Gobuster and FFUF.
- GUI-focused design makes automation less convenient.
- Development is largely inactive compared to newer alternatives.

---

## References

- Official DirBuster Repository
- Kali Linux Tools Documentation
- OWASP Web Application Testing Guide
