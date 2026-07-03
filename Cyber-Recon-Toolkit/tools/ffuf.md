# Fuzz Faster U Fool(FFUF) 

## Overview
ffuf (Fuzz Faster U Fool) is a ultra-fast, command-line web fuzzing tool written in Go. Security professionals, penetration testers, and bug bounty hunters use it to discover hidden elements on web servers by rapidly throwing a list of words (a wordlist) at a target URL
ffuf automates web infrastructure discovery through four primary use cases:Directory and File Busting: Finding hidden folders or files (e.g., searching for ://site.com to discover ://site.com or ://site.com).Subdomain Enumeration: Discovering unlinked subdomains (e.g., checking ://target.com to find ://target.com or ://target.com).Vhost Discovery: Identifying virtual hosts hosted on the same IP address by fuzzing the HTTP Host header.Parameter Fuzzing: Identifying hidden GET or POST parameters that might be vulnerable to exploitation (e.g., ://site.com)

---

## Purpose / Uses

- Purpose 1 : Directory and File Enumeration
- Purpose 2 : Subdomain and Virtual Host (Vhost) Discovery
- Purpose 3 : Authentication Brute-Forcing

---

## Installation

### Kali Linux

- ✅ Preinstalled in Kali Linux
OR
- Installation command
Verify if it is already installed
```bash
ffuf -v
``` 
```bash
sudo apt update && sudo apt install ffuf -y
```

---

## Basic Commands

### Command 1

```bash
ffuf -u http://target.com -w /path/to/wordlist.txt
```

-u: Specifies the target URL.
-w: Specifies the path to the wordlist (common lists include SecLists)

---

## Screenshot

> Uploaded screenshot as:

```
../screenshots/ffuf.png
```

Display it using:

```markdown
![Tool Screenshot](../screenshots/fuff.png)
```

---

## Advantages

- Extreme Speed: Written in Go, it features efficient multi-threading to send thousands of requests per second.
- Flexible Fuzzing: You can place the FUZZ keyword anywhere—in the URL, the request body, or HTTP headers.

---

## Limitations

- No Built-in Wordlists: It is completely useless without an external wordlist file (like SecLists).
- Network Bottlenecks: Can easily outrun your local bandwidth or overwhelm the target server's capacity

---

## References

- Official Documentation
- GitHub Repository
- Kali Tool page 
