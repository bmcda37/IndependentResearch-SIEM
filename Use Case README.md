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
## Failed Logon Attempts Visualization

My second use case will show the dashboard created to show each user's failed number of login attempts. To do this, we will use OpenSource's visualization platform, where I can create a custom table. When creating my table, I will want to show the time the rule ran and collected in the system, the agent machine, which is the machine that the alert is relating to, the machine name, so it's easier identifiable, and the full log which will give us the information regarding the account that the user was trying to access. At the bottom of the dashboard, you will also see where I created a metric showing the total number of failed login attempts over the selected time. 

Within Wazuh, 

<img width="958" alt="image" src="https://github.com/bmcda37/IndependentResearch-SIEM/assets/157663194/ba0aaa91-8e94-4655-8093-569c2c4cc5b0">




