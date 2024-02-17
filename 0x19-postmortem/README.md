# Cloud Storage Outage Postmortem

## Issue Summary

- **Duration:** The outage occurred from February 15, 2024, 10:00 PM to February 16, 2024, 2:00 AM (UTC).
- **Impact:** The service experiencing downtime was our cloud storage solution, affecting approximately 30% of our users. Users reported inability to upload/download files and experienced slow response times.
- **Root Cause:** The outage was caused by a misconfiguration in the network routing tables, leading to traffic congestion and packet loss within our data center.

## Timeline

- **February 15, 2024, 10:15 PM (UTC):** Issue detected through monitoring alerts indicating unusually high latency in storage requests.
- **February 15, 2024, 10:30 PM (UTC):** Engineering team notified and began investigation into potential causes, initially suspecting backend server overload.
- **February 15, 2024, 11:00 PM (UTC):** Misleadingly focused on optimizing database queries as a potential solution, without significant improvement in service availability.
- **February 15, 2024, 11:30 PM (UTC):** Issue escalated to network operations team as additional monitoring revealed abnormal network behavior.
- **February 16, 2024, 12:00 AM (UTC):** Network team identified misconfigured routing tables causing internal network congestion.
- **February 16, 2024, 1:30 AM (UTC):** Corrective measures implemented to restore proper routing configurations.
- **February 16, 2024, 2:00 AM (UTC):** Service fully restored and confirmed by monitoring systems.

## Root Cause and Resolution

- **Root Cause:** Misconfigured network routing tables led to traffic congestion within the data center, causing packet loss and increased latency in storage requests.
- **Resolution:** Network operations team reconfigured the routing tables to optimize traffic flow and alleviate congestion. Additionally, measures were put in place to improve monitoring of network configurations to catch similar issues early.

## Corrective and Preventative Measures

- **Improvements/Fixes:**
  - Enhance network configuration management practices to prevent misconfigurations.
  - Implement more granular monitoring for network traffic patterns and latency.
  - Develop better incident response protocols for escalating network-related issues promptly.
- **Tasks:**
  1. Conduct a thorough review of network configuration management processes.
  2. Implement automated checks to detect and prevent similar misconfigurations.
  3. Enhance documentation and training for network operations team regarding routing table management.
  4. Schedule regular audits of network infrastructure to identify potential vulnerabilities.
  5. Review incident response procedures to ensure efficient escalation and resolution of network issues.
