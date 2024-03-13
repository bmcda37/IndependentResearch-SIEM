# Wazuh Cluster

## Purpose
For this project, I will be using Wazuh as my SIEM tool. Wazuh provides a general installation guide at ``` ```; however, you will need to make changes to the configuration files which will be discussed in this README. The completed config files showing my specific configurations will be attached in the single-node folder within this repository.

## Config for VUlnerabilities
```
<vulnerability-detector>
    <enabled>yes</enabled>
    <interval>5m</interval>
    <min_full_scan_interval>6h</min_full_scan_interval>
    <run_on_start>yes</run_on_start>

    <!-- Ubuntu OS vulnerabilities -->
    <provider name="canonical">
      <enabled>yes</enabled>
      <os>trusty</os>
      <os>xenial</os>
      <os>bionic</os>
      <os>focal</os>
      <os>jammy</os>
      <update_interval>1h</update_interval>
    </provider>

    <!-- Debian OS vulnerabilities -->
    <provider name="debian">
      <enabled>yes</enabled>
      <os>buster</os>
      <os>bullseye</os>
      <os>bookworm</os>
      <update_interval>1h</update_interval>
    </provider>
```

# Wazuh Components

## Wazuh Manager

## Wazuh Indexer

## Wazuh Dashboard
