# theHarvester

## Overview

theHarvester is a powerful open-source OSINT (Open Source Intelligence) reconnaissance tool written in Python. It gathers publicly available information such as email addresses, subdomains, hostnames, IP addresses, employee names, and other intelligence from numerous search engines, certificate transparency logs, and online data sources.

---

## Purpose / Uses

- **Email Harvesting** – Collect publicly exposed email addresses associated with a target domain.
- **Subdomain Discovery** – Identify subdomains and hostnames belonging to an organization.
- **Public Footprint Assessment** – Discover information exposed on public search engines and online services.
- **Reconnaissance** – Build an organization's external attack surface before security testing.

---

## Installation

### Kali Linux

✅ **Preinstalled in Kali Linux**

Verify installation:

```bash
theHarvester -h
```

If not installed:

```bash
sudo apt update
sudo apt install theharvester -y
```

---

## Basic Commands

### 1. Display Help

```bash
theHarvester -h
```

**Explanation**

Displays all available options and supported data sources.

---

### 2. Search Using All Sources

```bash
theHarvester -d example.com -b all
```

**Explanation**

- `-d` – Target domain.
- `-b` – Specifies the search source (`all`, `google`, `bing`, `crtsh`, `shodan`, etc.).

---

### 3. Search Using a Specific Source

```bash
theHarvester -d example.com -b crtsh
```

**Explanation**

Searches Certificate Transparency logs for subdomains.

---

## Example Usage

### Gather Public Information

```bash
theHarvester -d example.com -b all
```

**Expected Output**

```
Emails Found:
admin@example.com
support@example.com

Hosts Found:
mail.example.com
vpn.example.com
dev.example.com

IPs:
192.168.x.x
```

---

## Screenshot

```markdown
![theHarvester Screenshot](../screenshots/theharvester.png)
```

---

## GitHub Repository

**Official GitHub**

https://github.com/laramies/theHarvester

**Official Documentation**

https://github.com/laramies/theHarvester/wiki

**Kali Tools Page**

https://www.kali.org/tools/theharvester/

---

## Advantages

- Collects emails, subdomains, hosts, and IP addresses in one tool.
- Supports dozens of public data sources.
- Passive reconnaissance minimizes interaction with the target.
- Frequently updated with new modules.
- Widely used in penetration testing and bug bounty programs.

---

## Limitations

- Many advanced modules require API keys.
- Public search engines may impose rate limits or CAPTCHAs.
- Results depend on publicly available information.
- Some sources may change or become unavailable over time.

---

## References

- Official theHarvester Documentation
- theHarvester GitHub Repository
- Kali Linux Tools Documentation
- OWASP Web Security Testing Guide
