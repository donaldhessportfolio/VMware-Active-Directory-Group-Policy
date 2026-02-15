## 🏢 Active Directory Group Policy Hardening Lab (Windows Server 2022)

In this lab, I implemented and tested multiple Group Policy Objects (GPOs) within a Windows Server 2022 Active Directory environment running in VMware. The goal was to simulate real-world enterprise policy enforcement by creating security-focused configurations that control authentication, endpoint behavior, and user restrictions.

Using the Group Policy Management Console (GPMC), I designed and deployed multiple domain-level policies that demonstrate foundational Active Directory administration and defensive security controls.

This lab focused on enforcing security baselines commonly used in enterprise environments, including password hardening, endpoint lockdown, and brute-force mitigation.

---

## 🔐 Password Policy Enforcement

Created a domain-level password policy to enforce stronger authentication standards across all domain users. This policy ensures consistent password hygiene and reduces the risk of weak credential exploitation.

**Key configurations:**
- Minimum password length: 12 characters  
- Password complexity enabled  
- Maximum password age: 90 days  

These controls simulate enterprise identity security baselines and align with common compliance frameworks.

![Password Policy 1](https://github.com/donaldhessportfolio/Active-Directory-Group-Policy/blob/main/Password-Policy.png)

---

## 🗂 Network Drive Mapping (User Preference GPO)

Configured a user-based Group Policy Preference to automatically map network drives upon login. This demonstrates centralized user environment configuration and scalable enterprise provisioning.

**Highlights:**
- User Configuration → Preferences → Drive Maps  
- Automatic network share mapping at login  
- Demonstrates policy vs. preference implementation differences  

![Drive Mapping 1](https://github.com/donaldhessportfolio/Active-Directory-Group-Policy/blob/main/Drive-Mapping.png)

---

## 🖼 Desktop Wallpaper Enforcement

Implemented a user policy to enforce a standardized desktop wallpaper across domain users. This demonstrates administrative enforcement of visual identity controls and policy immutability.

**Configuration path:**
User Configuration → Policies → Administrative Templates → Desktop

This policy ensures branding consistency and validates policy enforcement behavior.

### 📸 Screenshots
![Wallpaper Policy 1](./images/wallpaper-policy-1.png)

---

## 🚫 Control Panel Access Restriction

Created a restrictive user policy that prevents access to the Control Panel. This simulates enterprise endpoint hardening where administrative settings are locked down to reduce user misconfiguration risk.

**Policy impact:**
- Prevents unauthorized system modifications  
- Reduces attack surface from user tampering  
- Demonstrates administrative template enforcement  

### 📸 Screenshots
![Control Panel Restriction 1](./images/control-panel-1.png)

---

## 🔌 USB Storage Device Blocking

Implemented a computer-level policy to disable removable storage access, preventing data exfiltration and unauthorized device usage.

**Configuration path:**
Computer Configuration → Policies → Administrative Templates → System → Removable Storage Access

This simulates data loss prevention (DLP) and insider threat mitigation controls.

### 📸 Screenshots
![USB Blocking 1](./images/usb-block-1.png)

---

## 🔐 Account Lockout Policy (Brute Force Mitigation)

As a security-focused extension, I implemented an account lockout policy to simulate brute-force attack prevention and authentication monitoring.

**Policy settings:**
- Lockout threshold: 5 failed login attempts  
- Lockout duration configured  
- Reset counter configured  

I validated the policy by intentionally triggering failed login attempts from a domain-joined system and confirming account lockout behavior.

This demonstrates practical blue-team defensive configuration aligned with real SOC detection scenarios.

### 📸 Screenshots
![Lockout Policy 1](./images/lockout-1.png)

---

## 🧠 Skills Demonstrated

- Active Directory Administration  
- Group Policy Design & Deployment  
- Identity Security Hardening  
- Endpoint Restriction & Attack Surface Reduction  
- Brute Force Mitigation Strategies  
- Enterprise Policy Enforcement  

---

## 🔎 Future Enhancements

- Centralized logging with Windows Event Forwarding  
- SIEM ingestion for lockout detection  
- Privilege escalation simulations  
- Detection engineering for authentication abuse
