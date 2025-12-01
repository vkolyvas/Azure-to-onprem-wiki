# Wazuh – Installation & Configuration
Wazuh is an open-source SIEM and threat detection platform.\
\
**Installation**
1. Deploy Wazuh Indexer, Manager, and Dashboard using the all in one script (example version):
bash
```
curl -s https://packages.wazuh.com/4.7/wazuh-install.sh | bash
```
**Configuration**
- Add agents from the Wazuh dashboard.
- Apply security policies and detection rules.
- Integrate log sources (syslog, Windows event logs, cloud providers, etc.).
