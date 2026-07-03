# Knockpy (Subdomain Enumeration Tool)

## Overview

Knockpy is an open-source Python-based subdomain enumeration tool used to discover subdomains associated with a target domain. It combines passive reconnaissance techniques with active DNS brute-forcing to identify hidden subdomains, perform DNS zone transfer (AXFR) checks, and detect wildcard DNS configurations during the reconnaissance phase of penetration testing.

---

## Purpose / Uses

- **Subdomain Enumeration** – Discover subdomains associated with a target domain.
- **DNS Brute-Forcing** – Identify hidden hosts using custom or built-in wordlists.
- **DNS Zone Transfer (AXFR) Testing** – Check for misconfigured DNS servers that allow zone transfers.
- **Wildcard DNS Detection** – Detect and filter wildcard DNS records to reduce false positives.

---

## Installation

### Kali Linux

✅ **Preinstalled in Kali Linux**

Verify installation:

```bash
knockpy --help
```

If not installed:

```bash
sudo apt update
sudo apt install knockpy -y
```

---

## Basic Commands

### 1. Display Help

```bash
knockpy --help
```

**Explanation**

Displays all available command-line options.

---

### 2. Enumerate Subdomains

```bash
knockpy example.com
```

**Explanation**

- `example.com` – Target domain for subdomain enumeration.

---

### 3. Enumerate Using a Custom Wordlist

```bash
knockpy example.com -w /path/to/wordlist.txt
```

**Explanation**

- `example.com` – Target domain.
- `-w` – Specifies a custom wordlist for brute-forcing subdomains.

---

## Example Usage

### Scan a Target Domain

```bash
knockpy example.com
```

**Expected Output**

```
Target: example.com

Found Subdomains:
www.example.com
mail.example.com
vpn.example.com
dev.example.com

Wildcard DNS: Not Detected
Zone Transfer: Failed
```

---

## Screenshot

```markdown
![Knockpy Screenshot](../screenshots/knockpy.png)
```

---

## GitHub Repository

**Official GitHub**

https://github.com/guelfoweb/knock

**Documentation**

https://github.com/guelfoweb/knock

**Kali Tools Page**

https://www.kali.org/tools/knockpy/

---

## Advantages

- Fast and lightweight Python-based tool.
- Supports passive and active subdomain enumeration.
- Performs DNS zone transfer (AXFR) testing.
- Detects wildcard DNS records automatically.
- Supports custom wordlists for targeted enumeration.

---

## Limitations

- Active brute-forcing can generate noticeable DNS traffic.
- Enumeration quality depends on the supplied wordlist.
- Some passive sources may become unavailable over time.
- Large scans may take longer on domains with extensive DNS infrastructure.

---

## References

- Official Knockpy GitHub Repository
- Kali Linux Tools Documentation
- OWASP Web Security Testing Guide
- DNS Reconnaissance Best Practices
