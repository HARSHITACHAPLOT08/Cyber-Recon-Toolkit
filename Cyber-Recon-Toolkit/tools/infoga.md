# Infoga (Email Information Gathering)

## Overview

Infoga is an open-source OSINT tool written in Python that gathers publicly available email addresses and related information from multiple online sources. It is commonly used during the reconnaissance phase of a penetration test to collect email accounts associated with a target domain and assess their exposure in public data sources.

---

## Purpose / Uses

- **OSINT Email Harvesting** – Collect email addresses associated with a target domain.
- **Credential Leak Auditing** – Check whether discovered email addresses have appeared in known data breaches.
- **Domain Reconnaissance** – Identify an organization's publicly exposed email infrastructure.
- **Information Gathering** – Gather passive intelligence without directly interacting with the target system.

---

## Installation

### Kali Linux

❌ **Not Preinstalled in Kali Linux**

Verify installation:

```bash
infoga -h
```

If not installed:

```bash
git clone https://github.com/m4ll0k/Infoga.git
cd Infoga
pip3 install -r requirements.txt
```

Run the tool:

```bash
python3 infoga.py -h
```

---

## Basic Commands

### 1. Display Help

```bash
python3 infoga.py -h
```

**Explanation**

Displays all available options and modules.

---

### 2. Search Emails from All Sources

```bash
python3 infoga.py -d target.com -s all
```

**Explanation**

- `-d` – Specifies the target domain.
- `-s` – Specifies the search engine or source (`all`, `google`, `bing`, etc.).

---

## Example Usage

### Gather Email Addresses

```bash
python3 infoga.py -d example.com -s all
```

**Expected Output**

```
Target Domain : example.com

Emails Found:
admin@example.com
support@example.com
contact@example.com

Checking public information...
Done.
```

---

## Screenshot

```markdown
![Infoga Screenshot](../screenshots/infoga.png)
```

---

## GitHub Repository

**Official GitHub**

https://github.com/m4ll0k/Infoga

**Documentation**

https://github.com/m4ll0k/Infoga

---

## Advantages

- Collects email addresses from multiple public sources.
- Performs passive reconnaissance without directly interacting with the target.
- Helps identify publicly exposed organizational email accounts.
- Open-source and easy to customize.

---

## Limitations

- Search engines may apply rate limits or CAPTCHAs.
- Some modules may stop working if third-party services change.
- Results depend on publicly available information.
- Project maintenance and compatibility may vary over time.

---

## References

- Official Infoga GitHub Repository
- OWASP Web Security Testing Guide
- OSINT Framework Documentation
