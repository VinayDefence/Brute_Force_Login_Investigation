# 📊 PHASE 4 — ENABLE LOGGING (VERY IMPORTANT)
## 👉 Run on BOTH Windows machines (11 and server)
## Open PowerShell (Admin):
```
$ auditpol /set /category:"Logon/Logoff" /success:enable /failure:enable
```
## ✅ Verify:
```
$ auditpol /get /category:"Logon/Logoff"
```
![Enable-logging](screenshots/enable_logon_logoff.png)

## Why this matters for Wazuh
•	Wazuh agent collects Windows Event Logs via the <localfile> configuration in ossec.conf.

•	Without enabling this, login events won’t appear, so alerts on failed logins or brute-force attempts won’t trigger.


## 💡 Optional: Enable other useful security logs
•	Account Management:
```
$ auditpol /set /category:"Account Management" /success:enable /failure:enable
```
•	Policy Change:
```
$ auditpol /set /category:"Policy Change" /success:enable /failure:enable
```
### Ater that check the Account Management & Policy change Status

![Enable-Account&Policy](screenshots/Account_policy.png)


•	This ensures Wazuh can detect user creation, privilege changes, and security policy changes.
