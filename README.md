# Vulnerability Management Lab with Tenable: A Practical Guide

Welcome to the **Vulnerability Management Lab with Tenable**! This repository contains the resources and steps from a hands-on lab that demonstrates the fundamentals of vulnerability management using Tenable’s vulnerability scanning tools. This lab is a good approach to deepen my understanding of vulnerability management and how to use it effectively to secure systems.

---

### Lab Architecture and Overview
This lab is designed to be cloud-based and accessible from my computer. The lab provides actionable skills for my cybersecurity journey, with practical steps to enhance my resume and boost my job prospects. The Tenable Vulnerability Management cloud console was used as the main operating interface and the Tenable Scan Engine as well as the Scan Target were both hosted on Microsoft Azure virtual machines.

<img width="931" alt="image" src="https://github.com/user-attachments/assets/2853aed3-0092-4b4c-be3e-a67cd8dfd9f5" />

---

### Key Concepts Covered
- **Introduction to Vulnerability Management**:
  - What is software vulnerability management?
  - Understanding vulnerabilities, scan engines, and remediation.
  - Overview of compliance standards like DISA/STIG, CIS, etc.

- **Hands-On Steps**:
  - Setting up a virtual machine (VM) for scanning.
  - Configuring a Tenable vulnerability scanner.
  - Performing compliance checks (e.g., DISA/STIG).
  - Identifying vulnerabilities and compliance issues.
  - Creating and remediating vulnerabilities.
  - Observing results and documenting remediation efforts.

- **Tools Used**:
  - Azure (for VM setup with free credits).
  - Tenable Vulnerability Management (free trial available).
  - LogN Pacific Cyber Range (optional, preconfigured environment).

---

### Lab Workflow

**Environment Setup**:
   - Configure a VM in Azure.
   - Prepare the VM for vulnerability scanning.
     <img width="1161" height="681" alt="image" src="https://github.com/user-attachments/assets/161f9563-7b1d-4d9b-b50c-3e9e14bf9599" />


**Scan Configuration**
   - Configure a credentialed Tenable scan to look for all the basic vulnerabilities + *DISA Windows 10 STIG v3r2*

     <img width="815" height="444" alt="image" src="https://github.com/user-attachments/assets/99d41dc5-cc78-44c4-8f2a-dad14229aed9" />

     <img width="1486" height="830" alt="image" src="https://github.com/user-attachments/assets/135c6591-37f6-4ef2-8e6e-6836f838cd42" />



**Initial Scan**:
   - Perform an initial vulnerability and compliance baseline scan.
   - Review and analyze scan results including failed STIGs. For this lab, we will focus on the following STIGs to Fail/Remediate:
     - STIG ID WN10-AU-000505 (Increase size of Security Event Log) - Initial Fail
     - STIG ID WN10-SO-000025 (Rename Guest Account) - Initial Fail
     - STIG ID WN10-SO-000010 (Disable Guest Account) - Initial Pass

     <img width="1690" alt="image" src="https://github.com/user-attachments/assets/b4393be5-5f17-4b86-8ad2-54216531ef07" />
     <img width="1690" alt="image" src="https://github.com/user-attachments/assets/89eae55d-5a6b-405e-8095-6d68caa68f96" />
     <img width="1690" alt="image" src="https://github.com/user-attachments/assets/30a36968-bdb5-4815-9153-56d0e12caebf" />



**Simulate Vulnerabilities**:
   - Introduce vulnerabilities such as outdated software (Firefox v110) or misconfigured settings (Enabled Guest Account)
     - Intentionally FAIL: STIG ID WN10-SO-000010 by enabling the Guest Account
   - Perform a second scan to detect changes.
     ![image](https://github.com/user-attachments/assets/46f0d7c2-fb90-4014-86e1-8f8528a167f5)

**Remediation**:
   - Fix vulnerabilities and compliance issues (e.g., uninstall outdated software, modify registry settings to increase security event log size, disable Guest account, rename Guest account, fully update Windows).
   - Perform a final scan to confirm remediation.
     
**Document Results**:
   
   <img width="790" alt="image" src="https://github.com/user-attachments/assets/415caeeb-31e5-4bbd-b516-babfd7a66e2e" />
   
   - Scan 1: You can see the initial vulnerability baseline with the first scan
   - Scan 2: A spike occurred when we introduced a deprecated version of Firefox
   - Scan 3: A dip in vulnerabilities is observed after removing Firefox
   - Scan 4: A final dip takes place after fully updating Windows

---

### Why This Lab?
This lab not only provides hands-on experience with vulnerability management but also equips you with practical skills that can enhance your cybersecurity resume. By completing the lab, you'll gain familiarity with:
- Real-world vulnerability identification and remediation.
- Compliance frameworks such as DISA/STIG.
- Effective use of Tenable’s tools.

---
