## 🖼️ 1. Wazuh Dashboard Overview

![Wazuh Dashboard Overview](screenshots/wazuh/wazuh_dashboard0.png)
#### This image shows the main dashboard of :contentReference[oaicite:0]{index=0} displaying overall security events. It provides a summary of alerts, agent status, and system activity. This confirms that the Wazuh manager is running and collecting logs.
## 🖼️ 2. Active Agents Status
![Active Agents](screenshots/wazuh/wazuh_active_agents2.png)

#### This image displays the list of connected agents. It confirms that Windows systems are successfully connected to the Wazuh manager. Active agents are required for collecting and analyzing logs from endpoints.
## 🖼️ 3. Security Events View
![Security Events in Wazuh](screenshots/wazuh/wazuh_dashboard1.png)

#### This image shows the detailed event logs collected from Windows systems. It includes timestamps, event IDs, usernames, and source IP addresses for analysis.
## 🖼️ 4. Failed Login Attempt (Event ID 4625)
![Failed Login Detection (Event ID 4625)](screenshots/wazuh/wazuh_failedlogins3.png)

#### This image shows failed login attempts detected in Wazuh. Event ID 4625 indicates unsuccessful login attempts, which are generated during the brute-force attack.
## 🖼️ 5. Successful Login (Event ID 4624)
![Successful Login Detection (Event ID 4624)](screenshots/wazuh/wazuh_success_login4.png)

#### This image displays successful login events. Event ID 4624 indicates a valid login, helping differentiate between normal and suspicious activity.

## 🖼️ 6. Attack Logs with Source IP
![Attack Source Identification](screenshots/wazuh/wazuh_ip5.1.png)
![Attack Source Identification](screenshots/wazuh/wazuh_ip5.2.png)
#### This image highlights the source IP address of the attacker (Kali Linux). Wazuh helps identify where the attack originated, which is critical for incident response.

## 🖼️ 7. Exploring the MITRE ATTACK
![Mitre Attack](screenshots/wazuh/wazuh_mitreattack6.png)
