# Independent Research using SIEM technologies and integrations
For my independent research study, I decided to configure a home SIEM lab using Wazuh. I am using the single-node option since I do not need more worker nodes for the volume of agents I will be installing. I leveraged various skills acquired from my undergraduate studies, internships, and personal research to build a comprehensive solution capable of addressing various use case scenarios.

## Key proficiencies involved in this project:
- Linux File System
- Utilizing tools such as scp, ssh
- Configuring Docker & Docker Compose configuration, along with managing containers using Portaniner 
- Networking Concepts: Subnetting, Firewall Configuration, Port Forwarding, Virtualization Management
- Zero Trust Network Architecture

## Technologies used within the project:
- Docker: Employed Docker Compose for hosting Wazuh Stack
- Wazuh Stack: Single-Node configuration consisting of Wazuh Manager, Wazuh Indexer, & Wazuh Dashboard
- XCP-ng: Server hosting VMs
- Virtual Machines: Kali Linux & Ubuntu
- Twingate (ZTNA Solution) for remote access
- Caldera- Threat simulation
- pfsense Firewall
