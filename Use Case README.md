# Resources
- Red Team: Caldera VM
- Blue Team: Wazuh-Cluster VM
- Victim: Ubuntu 20.04 VM (Agent Machine)

# Use Case 1
## Remote Agent Monitoring & Vulnerability Resolution

For my first use case, I will demonstrate the results showcasing the completion of configuring Wazuh to remotely monitor my Wazuh-Agents which was installed on my Ubuntu VM. I will also show how I resolved a "level 5 (critical)" vulnerability on this VM.

## Part 1: Installing Wazuh-Agent on Ubuntu 20.04 VM
To complete the installation of my Wazuh-Agent, I followed the instructions found in my "WazuhREADME.md". Once finishing the installation, I restarted the agent which allowed me to log in to my Wazuh-Dashboard showing the successful completion of enrolling my agent.

<img width="958" alt="image" src="https://github.com/bmcda37/IndependentResearch-SIEM/assets/157663194/2048633f-66a7-4fb5-ae1d-1ace5049cb32">

## Part 2: Querying for Vulnerabilities & Resolving PCI Alerts
<img width="958" alt="image" src="https://github.com/bmcda37/IndependentResearch-SIEM/assets/157663194/b661d6b3-b127-422d-a338-62442d13030e">

## PCI Top Alerts Needing Resolving
<img width="958" alt="image" src="https://github.com/bmcda37/IndependentResearch-SIEM/assets/157663194/fb094afd-2406-47b0-b198-c51f7aa59d18">


# Use Case 2

## Discritpion
For my second use case, I'll demonstrate the dashboard designed to display the number of failed login attempts for each user. To achieve this, I will be utilizing an OpenSearch visualization module within Wazuh. This will allow for the creation of a customized table. In constructing this table, I intend to include the following fields:

Time of data collection: This indicates when the rule was executed and data was gathered in the system.
Agent machine: This identifies the specific machine associated with the triggered alert.
Machine name: This provides an easily identifiable name for the machine.
Full log: This field contains detailed information regarding the account that the user attempted to access.
Additionally, at the bottom of the dashboard, you'll find a metric showcasing the total count of failed login attempts recorded during the selected time

## Value
This dashboard will add value to the organization by providing critical insights into security-related events such as failed login attempts. By visualizing data such as the time of data collection, agent machine, machine name, and the full log, the dashboard offers detailed information regarding the security event flagged. 

The below areas are in which I believe a SOC analyst or organization would gain value from this dashboard:

- Enhanced Visibility: It provides real-time visibility into security events, enabling quick identification and response to potential threats.

- Improved Incident Response: With detailed information on failed login attempts, security teams can promptly investigate and mitigate security incidents, reducing the organization's exposure to risk.

- Risk Mitigation: By monitoring and analyzing failed login attempts, the organization can proactively identify vulnerabilities and implement measures to strengthen security posture, minimizing the likelihood of successful unauthorized access.

- Operational Efficiency: The dashboard streamlines the monitoring and analysis process, allowing security teams to efficiently manage and prioritize security incidents, ultimately optimizing resource allocation and operational effectiveness.


## Failed Logon Attempts Visualization

<img width="958" alt="image" src="https://github.com/bmcda37/IndependentResearch-SIEM/assets/157663194/ba0aaa91-8e94-4655-8093-569c2c4cc5b0">




