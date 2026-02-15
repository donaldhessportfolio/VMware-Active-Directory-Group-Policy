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

### 📸 Screenshots
![Password Policy 1](./images/password-policy-1.png)
![Password Policy 2](./images/password-policy-2.png)
![Password Policy 3](./images/password-policy-3.png)
![Password Policy 4](./images/password-policy-4.png)
![Password Policy 5](./images/password-policy-5.png)

---

## 🗂 Network Drive Mapping (User Preference GPO)

Configured a user-based Group Policy Preference to automatically map network drives upon login. This demonstrates centralized user environment configuration and scalable enterprise provisioning.

**Highlights:**
- User Configuration → Preferences → Drive Maps  
- Automatic network share mapping at login  
- Demonstrates policy vs. preference implementation differences  

### 📸 Screenshots
![Drive Mapping 1](./images/drive-mapping-1.png)
![Drive Mapping 2](./images/drive-mapping-2.png)
![Drive Mapping 3](./images/drive-mapping-3.png)
![Drive Mapping 4](./images/drive-mapping-4.png)
![Drive Mapping 5](./images/drive-mapping-5.png)

---

## 🖼 Desktop Wallpaper Enforcement

Implemented a user policy to enforce a standardized desktop wallpaper across domain users. This demonstrates administrative enforcement of visual identity controls and policy immutability.

**Configuration path:**
User Configuration → Policies → Administrative Templates → Desktop

This policy ensures branding consistency and validates policy enforcement behavior.

### 📸 Screenshots
![Wallpaper Policy 1](./images/wallpaper-policy-1.png)
![Wallpaper Policy 2](./images/wallpaper-policy-2.png)
![Wallpaper Policy 3](./images/wallpaper-policy-3.png)
![Wallpaper Policy 4](./images/wallpaper-policy-4.png)
![Wallpaper Policy 5](./images/wallpaper-policy-5.png)

---

## 🚫 Control Panel Access Restriction

Created a restrictive user policy that prevents access to the Control Panel. This simulates enterprise endpoint hardening where administrative settings are locked down to reduce user misconfiguration risk.

**Policy impact:**
- Prevents unauthorized system modifications  
- Reduces attack surface from user tampering  
- Demonstrates administrative template enforcement  

### 📸 Screenshots
![Control Panel Restriction 1](./images/control-panel-1.png)
![Control Panel Restriction 2](./images/control-panel-2.png)
![Control Panel Restriction 3](./images/control-panel-3.png)
![Control Panel Restriction 4](./images/control-panel-4.png)
![Control Panel Restriction 5](./images/control-panel-5.png)

---

## 🔌 USB Storage Device Blocking

Implemented a computer-level policy to disable removable storage access, preventing data exfiltration and unauthorized device usage.

**Configuration path:**
Computer Configuration → Policies → Administrative Templates → System → Removable Storage Access

This simulates data loss prevention (DLP) and insider threat mitigation controls.

### 📸 Screenshots
![USB Blocking 1](./images/usb-block-1.png)
![USB Blocking 2](./images/usb-block-2.png)
![USB Blocking 3](./images/usb-block-3.png)
![USB Blocking 4](./images/usb-block-4.png)
![USB Blocking 5](./images/usb-block-5.png)

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
![Lockout Policy 2](./images/lockout-2.png)
![Lockout Policy 3](./images/lockout-3.png)
![Lockout Policy 4](./images/lockout-4.png)
![Lockout Policy 5](./images/lockout-5.png)

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
