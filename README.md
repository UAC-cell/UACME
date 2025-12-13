# UACME (version 3.7.2)

Defeating Windows User Account Control by abusing built-in Windows AutoElevate behavior (UAC Bypass).
This project demonstrates multiple UAC bypass techniques and serves as an educational resource for understanding Windows security mechanisms.

> ⚠️ **Warning**: This tool demonstrates security vulnerabilities that could be exploited maliciously. Use responsibly and only in controlled environments.

# System Requirements

* **Operating Systems:** Windows 7 / 8 / 8.1 / 10 / 11 (including Windows 11 25H2)
* **User Account:** Administrator account with UAC enabled (default settings)
* **UAC Configuration:** Default (standard)

---

# Updated Behavior

## 📦 Release Versions

### **UACME 3.7.1**

UACME 3.7.1
Overview

This release introduces significant internal restructuring. All previous UACME operations have been consolidated into Method 43, simplifying the project’s architecture and standardizing behavior across all supported techniques.

What’s New

Unified Operation Model:
All functionality has been merged into Method 43, reducing complexity and improving maintainability.

Cleaner Codebase:
Consolidation removes duplicated logic from older methods and prepares the project for future updates.

Improved Stability:
Some internal fixes and optimizations tied to the method unification.

Note

Older methods remain in the codebase for reference but are no longer active in this release.

### **UACME 3.7**

* Method updates and behavioral consistency improvements.

### **UACME 3.6**

* Expanded support for additional UAC bypass mechanisms.

*(Add more release tags as needed)*

---

## 🔍 Overview

UACME is a Windows security research project focused on **User Account Control (UAC) bypass techniques**, **AutoElevate abuse**, and **privilege escalation behavior** across Windows versions. This repository provides:

* Proof‑of‑concept UAC bypass implementations
* Research on AutoElevate executable behavior
* Documentation of privilege escalation vectors
* Source code examples for security testing and auditing
* Updated method 43 (UACME 3.7.1) unified bypass model

UACME is widely referenced in:

* Windows security research
* Malware analysis reports
* Red-team tooling studies
* Reverse‑engineering and infosec training

Use this project for **educational**, **research**, and **defensive** purposes only.

---

## 📝 Usage

This project is for:

* Security researchers
* Malware analysts
* Reverse engineers
* Windows internals enthusiasts

**Do not use this for illegal activity.**

---

## 📚 Research & Discussion Resources

* Windows Internals communities
* Security Stack Exchange
* Reverse engineering forums
* GitHub Issues / Discussions
* Specialized infosec Discord servers and Reddit communities

---

## 📥 Download Statistics

GitHub does not show repository download counts, but it **does** show release asset download numbers under:

**Releases → (Select Release) → Assets → Download Count**

---

## 📄 License

Research and educational use only. Follow applicable laws.

```
UACME 3.7.1
Overview

This release introduces significant internal restructuring. All previous UACME operations have been consolidated into Method 43, simplifying the project’s architecture and standardizing behavior across all supported techniques.

What’s New

Unified Operation Model:
All functionality has been merged into Method 43, reducing complexity and improving maintainability.

Cleaner Codebase:
Consolidation removes duplicated logic from older methods and prepares the project for future updates.

Improved Stability:
Some internal fixes and optimizations tied to the method unification.

Note

Older methods remain in the codebase for reference but are no longer active in this release.
```

---

## 📘 Research-Focused README Summary

UACME is a Windows security research project dedicated to analyzing **User Account Control (UAC)**, **AutoElevate behavior**, and **local privilege escalation mechanics** across modern Windows versions. Rather than serving as an offensive toolkit, UACME is designed to help researchers, reverse engineers, and defenders understand *why* UAC bypasses occur, *how* Microsoft mitigates them, and *where* architectural weaknesses still exist.

Version **3.7.2** represents a major simplification of the codebase. All previously scattered bypass implementations have been consolidated into a single, unified execution path (**Method 43**), making the project easier to audit, maintain, and study.

---

## 🔎 Comparison: UACME 3.7.x vs Older Versions

| Aspect           | Older UACME Versions           | UACME 3.7.2                  |
| ---------------- | ------------------------------ | ---------------------------- |
| Method selection | Manual `method_number` per OS  | Single unified **Method 43** |
| Code structure   | Multiple duplicated code paths | Centralized logic            |
| Maintainability  | Difficult to audit             | Significantly improved       |
| Windows 11 25H2  | Unreliable / failing           | Fully supported              |
| Research clarity | Fragmented                     | Consistent behavior          |
| Legacy methods   | Actively used                  | Retained for reference only  |

---

## 🧠 Method 43 — Research-Oriented Explanation

Method 43 represents a consolidation of multiple historical UAC bypass techniques into a **single execution flow** that reliably demonstrates AutoElevate abuse under default UAC settings.

From a research perspective, Method 43 is valuable because:

* It demonstrates how **trusted AutoElevate binaries** interact with COM objects and system components.
* It highlights how **UAC design trade-offs** prioritize usability over strict isolation for administrative users.
* It provides a consistent test case across Windows versions, reducing OS-specific branching.

Rather than introducing new bypass primitives, Method 43 focuses on *behavioral consistency* — making it easier for analysts to:

* Trace token elevation behavior
* Study mitigation changes between Windows releases
* Compare security responses across Windows 7 → Windows 11 25H2

---

