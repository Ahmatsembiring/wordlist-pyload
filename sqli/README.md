# 💉 SQL Injection (SQLi) Payloads & Cheatsheet

> 🛡️ Curated collection of SQL injection payloads for penetration testing, bug bounty hunting, CTFs, and security education.

⚠️ **ETHICAL USE ONLY**  
All payloads in this repository are intended for **authorized security testing** and **educational purposes**. Using these against systems without explicit written permission is illegal and violates cybersecurity laws worldwide.

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](../LICENSE)
[![Category: SQLi](https://img.shields.io/badge/Category-SQLi-orange.svg)](./)
[![Payloads](https://img.shields.io/badge/Payloads-150+-green.svg)](./payloads/)

---

## 📑 Table of Contents

- [🔍 Overview](#-overview)
- [📂 Repository Structure](#-repository-structure)
- [🗃️ Database-Specific Payloads](#️-database-specific-payloads)
- [🛠️ Usage Examples](#️-usage-examples)
- [🔎 Detection & Testing Guide](#-detection--testing-guide)
- [🛡️ Mitigation Strategies](#️-mitigation-strategies)
- [🤝 Contributing](#-contributing)
- [📜 License](#-license)

---

## 🔍 Overview

SQL Injection occurs when untrusted input is directly concatenated into SQL queries without proper sanitization. This allows attackers to:
- 🔐 Bypass authentication
- 👁️ Extract sensitive data
- ✏️ Modify/Delete database records
- 🖥️ Achieve Remote Code Execution (in specific configurations)

| Type | Mechanism | When to Use |
|------|-----------|-------------|
| **In-Band (Union)** | Uses `UNION SELECT` to merge results | Output is reflected in response |
| **In-Band (Error)** | Leverages verbose DB errors | Debug mode enabled / detailed errors |
| **Blind (Boolean)** | Infers data via TRUE/FALSE responses | No direct output, but page behavior changes |
| **Blind (Time)** | Infers data via response delays (`SLEEP`, `WAITFOR`) | No visual differences in response |
| **Out-of-Band (OOB)** | Exfiltrates via DNS/HTTP callbacks | No direct response channel available |

---

## 📂 Repository Structure
