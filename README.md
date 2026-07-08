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

     <img width="1422" height="596" alt="image" src="https://github.com/user-attachments/assets/b3db6184-cfff-4a45-91f3-19ccc87137c9" />
     <img width="1419" height="794" alt="image" src="https://github.com/user-attachments/assets/11e9c9e5-08b7-4b17-82dc-beb1da91a549" />
     <img width="1424" height="580" alt="image" src="https://github.com/user-attachments/assets/d201edc3-03da-472b-bb74-88308e06696e" />




**Simulate Vulnerabilities**:
   - Introduce vulnerabilities such as outdated software (Firefox v110) or misconfigured settings (Enabled Guest Account)
     - Intentionally FAIL: STIG ID WN10-SO-000010 by enabling the Guest Account
    
     <img width="745" height="527" alt="image" src="https://github.com/user-attachments/assets/9432df95-d7ba-4680-8ad8-789cf2716075" />

 
   - Perform a second scan to detect changes.

<img width="1428" height="464" alt="image" src="https://github.com/user-attachments/assets/034e80da-68ec-435d-b867-7bfef5ec2da3" />
<img width="1071" height="152" alt="image" src="https://github.com/user-attachments/assets/5f9a2390-cabe-4b38-9842-f215f66aa336" />


    

**Remediation**:
   - Fix vulnerabilities and compliance issues (e.g., uninstall outdated software (**use appwiz.cpi to delete fastly Firefox**), modify registry settings to increase security event log size, disable Guest account, rename Guest account, fully update Windows).

<img width="1367" height="435" alt="image" src="https://github.com/user-attachments/assets/c4718765-bc97-4273-a8e2-d0b4dd999bf5" />
<img width="595" height="127" alt="image" src="https://github.com/user-attachments/assets/2789afc0-9ebe-4f1a-b817-67408b110446" />
<img width="788" height="438" alt="image" src="https://github.com/user-attachments/assets/c2e85bb9-add9-48c0-832a-a3026f70f8d6" />


<img width="1423" height="303" alt="image" src="https://github.com/user-attachments/assets/87cb424a-5284-429d-9f71-f03207163d9a" />
<img width="153" height="82" alt="image" src="https://github.com/user-attachments/assets/786e6b35-d7e5-4ee8-b331-bb5352648107" />




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
