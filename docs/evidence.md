# Evidence

## Agents onboarded
- Screenshot: [01_agents_connected.png](screenshots/01_agents_connected.png)
- Shows: Windows + Linux agents are connected and reporting to Wazuh.

## SSH authentication monitoring
- Screenshot: [02_ssh_failed_password_archives.png](screenshots/02_ssh_failed_password_archives.png)
- Shows: Linux SSH failed logins are collected (auth.log) and searchable.

## OPNsense syslog forwarding
- Screenshot: [03_opnsense_remote_syslog.png](screenshots/03_opnsense_remote_syslog.png)
- Shows: OPNsense forwards syslog to SEC-SRV over UDP 514.

## Syslog arrival proof (SEC-SRV)
- Screenshot: [04_syslog_udp514_tcpdump.png](screenshots/04_syslog_udp514_tcpdump.png)
- Shows: packets arrive to UDP/514 on the Wazuh server.

## Firewall / IDS visibility in Wazuh
- Screenshot: [05_opnsense_logs_archives.png](screenshots/05_opnsense_logs_archives.png)
- Shows: OPNsense logs (filterlog / Suricata) are ingested into `wazuh-archives-*`.

## Custom rules
- Screenshot: [06_suricata_alerts_rule_100202.png](screenshots/06_suricata_alerts_rule_100202.png)
- Shows: `local_rules.xml` on SEC-SRV — rules 100200–100202 tag OPNsense syslog, firewall (`filterlog`) and Suricata events so they reach `wazuh-alerts-*`. File: [`rules/local_rules.xml`](../rules/local_rules.xml).
