# 🧠 PHASE 7 — INVESTIGATION

## 🔍 Analysis Results

- **Attacker IP:** 192.168.0.86
- **Target Account:** Administrator  
- **Number of Attempts:** High volume of failed login attempts detected  
- **Successful Login:** Yes
- **Time Pattern:** Continuous rapid login attempts over a short duration, consistent with brute-force attack behavior  

## 📊 Observation

The attack shows a clear brute-force pattern with repeated authentication attempts from a single source targeting the Administrator account.
## 📊 Detailed Investigation Insights

### 🔐 Attack Behavior
The attacker performed a brute-force attack by continuously attempting multiple password combinations against the Administrator account. The pattern of repeated failures indicates automated attack activity.

---

### 🌐 Source Analysis
All login attempts originated from a single IP address (192.168.0.85), confirming that the attack was launched from a controlled source (Kali Linux attacker machine).

---

### ⏱️ Time-Based Pattern
The login attempts were generated rapidly within short time intervals, showing a clear automated attack pattern rather than manual login attempts.

---

### 🎯 Target Analysis
The attack specifically targeted the Administrator account, which is a high-privilege account, making it a critical security risk.

---

### 🚨 Indicators of Compromise (IOCs)

- Multiple Event ID 4625 logs (failed logins)  
- Repeated login attempts from a single IP  
- Possible Event ID 4624 (successful login)  
- High frequency of authentication requests  

---

### 🧠 Attack Classification
This activity is classified as a **Brute Force Attack**, where attackers try multiple password combinations to gain unauthorized access.

---

### 🔍 Log Evidence

The detection was based on Windows Security logs collected by Wazuh:

- Event ID 4625 → Failed login attempts  
- Event ID 4624 → Successful login  

---

### ⚠️ Security Weakness Identified

- No account lockout policy enabled  
- Weak or guessable passwords  
- Lack of multi-factor authentication (MFA)  

---

### 🛡️ Recommended Improvements

- Enable account lockout after multiple failed attempts  
- Use strong password policies  
- Enable MFA for all administrative accounts  
- Monitor login attempts continuously using SIEM tools  
