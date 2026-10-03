# 🛡️ NetworkWalks Cybersecurity Internship – Week 4

This repository documents my **Week 4 practical work** completed during my Cybersecurity Internship at **NetworkWalks**.

The focus of this week was **Web Application Penetration Testing** through an authorized and controlled security assessment.

---

## 🔍 Week 4 — Web Application Penetration Testing

During this week, I followed a structured penetration-testing approach covering:

- Reconnaissance
- Web technology identification
- Directory and endpoint enumeration
- Authentication security testing
- SQL Injection testing
- Sensitive file exposure analysis
- PDF password-security testing
- Error disclosure analysis
- Directory listing review
- Risk assessment
- Security remediation recommendations

The assessment followed a black-box methodology, with testing performed under written authorization.

---

## 🎯 Assessment Objectives

The main objectives were to:

1. Identify the application's externally exposed attack surface.
2. Discover accessible directories and endpoints.
3. Assess authentication security.
4. Identify potential web application vulnerabilities.
5. Evaluate sensitive information exposure.
6. Assess password and document security.
7. Document security findings and their potential impact.
8. Provide appropriate remediation recommendations.

---

## 🔎 Reconnaissance & Enumeration

The assessment began with reconnaissance and enumeration to understand the target's externally visible infrastructure.

Activities included:

- Domain reconnaissance
- Web technology fingerprinting
- Port and service enumeration
- Directory discovery
- Endpoint enumeration
- Review of publicly accessible resources

### Tools Used

- **Nmap** — Port scanning and service enumeration
- **WhatWeb** — Web technology fingerprinting
- **Gobuster** — Directory and endpoint enumeration
- **WHOIS** — Domain reconnaissance
- **cURL** — HTTP request testing

---

## 💉 Web Application Security Testing

During testing of the authorized application, an **SQL Injection vulnerability affecting authentication** was identified.

The vulnerability allowed authentication controls to be bypassed in the controlled assessment environment.

### Finding

**F-01 — SQL Injection / Authentication Bypass**

**Risk:** Critical

The assessment identified insufficient protection of user-supplied input in the authentication functionality.

### Recommended Remediation

- Use prepared statements / parameterized queries.
- Validate user input on the server side.
- Follow secure coding practices.
- Apply the principle of least privilege to database accounts.
- Perform a broader code review of authentication and query-processing functionality.

---

## 📂 Sensitive File Exposure

Directory enumeration also identified an **exposed database backup file** within a publicly accessible directory.

### Finding

**F-02 — Exposed Database Backup**

**Risk:** Critical

The exposed backup contained sensitive organizational information.

### Recommended Remediation

- Remove sensitive backup files from the public web root.
- Store backups outside publicly accessible directories.
- Encrypt backups at rest.
- Regularly audit web directories for unintended file exposure.
- Establish secure backup-management procedures.

---

## 🔐 PDF Password Security Testing

The assessment also included testing of password-protected PDF documents obtained within the authorized environment.

### Finding

**F-03 — Weak PDF Password Protection**

**Risk:** High

Password-recovery techniques were used to assess the strength of the protection applied to the documents.

### Recommended Remediation

- Enforce strong and unique passwords.
- Avoid common or dictionary-based passwords.
- Use securely generated passwords.
- Prefer stronger modern encryption standards.
- Where possible, use authenticated application-based access instead of relying solely on document passwords.

---

## ⚠️ Error Disclosure

Testing also identified **verbose SQL/database error messages** being returned by the application.

### Finding

**F-04 — Verbose SQL Error Disclosure**

**Risk:** Medium

Detailed database errors can reveal useful technical information to an attacker and assist further vulnerability testing.

### Recommended Remediation

- Disable detailed error display in production.
- Return generic error messages to users.
- Log technical errors securely on the server.
- Avoid exposing database details in HTTP responses.

---

## 📁 Directory Listing

Directory listing was identified as another security weakness.

### Finding

**F-05 — Directory Listing Enabled**

**Risk:** Medium

Exposed directory listings can reveal application structure, files, backups, and other resources that should not be publicly browsable.

### Recommended Remediation

- Disable directory listing.
- Review publicly accessible directories.
- Remove unnecessary files from the web root.
- Conduct regular security configuration reviews.

---

## 📊 Findings Summary

| ID | Finding | Risk |
|---|---|---|
| F-01 | SQL Injection / Authentication Bypass | Critical |
| F-02 | Exposed Database Backup | Critical |
| F-03 | Weak PDF Password Protection | High |
| F-04 | Verbose SQL Error Disclosure | Medium |
| F-05 | Directory Listing Enabled | Medium |

The assessment report documents these five findings and their corresponding remediation recommendations.

---

## 🧰 Tools Used

| Tool | Purpose |
|---|---|
| Nmap | Port scanning & service enumeration |
| WhatWeb | Web technology fingerprinting |
| Gobuster | Directory enumeration |
| cURL | HTTP request testing |
| WHOIS | Domain reconnaissance |
| pdfcrack | Authorized PDF password-recovery testing |
| pdf2john | PDF hash extraction |
| Hashcat | Password/hash security testing |

These tools were used as part of the documented assessment methodology.

---

## 🛠️ Remediation & Reporting

A major part of Week 4 was not only identifying vulnerabilities, but also understanding how to communicate them professionally.

For each finding, I focused on:

- Vulnerability identification
- Risk classification
- Potential impact
- Evidence
- Remediation recommendations
- Prioritization

The assessment recommendations included prepared statements for SQL injection, secure backup storage, stronger document passwords, safer error handling, and disabling directory listing.

---

## 📚 Learning Outcomes

Through this week's practical work, I gained hands-on exposure to:

- Web application penetration-testing methodology
- Reconnaissance and enumeration
- Attack-surface discovery
- Authentication security testing
- SQL Injection identification
- Sensitive file exposure
- Password-security assessment
- Error disclosure analysis
- Security configuration review
- Vulnerability risk classification
- Penetration-testing reporting
- Security remediation planning

---

## 📂 Repository Structure

```text
NetworkWalks-Internship-Week4-Penetration-Testing/
│
├── README.md
│
├── reconnaissance/
│
├── enumeration/
│
├── web-security-testing/
│
├── password-security/
│
├── findings/
│
├── remediation/
│
└── screenshots/
```

> Add your actual screenshots/evidence to the relevant folders when uploading them.

---

## ⚠️ Ethical & Legal Notice

All testing documented in this repository was performed in an **authorized and controlled educational environment**.

No security testing should be performed against systems, applications, domains, or data without explicit permission from the owner.

Sensitive information, credentials, passwords, database backups, personal information, medical information, and other confidential client data should **not** be published in a public repository.

---

## 👨‍💻 Internship

**NetworkWalks Cybersecurity Internship**  
**Batch B083 — Week 4**

Special thanks to **Waqas Karim (CCIE)** for his guidance and support throughout the internship.
