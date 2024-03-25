# My Changes
Note these are not the original configuration of yml files from Wazuh. I customized the scripts to work for my home lab. I added the agent.conf file and the insert within the file. Within the Wazuh_Cluster.conf file, I added the vulnerability scanning configuration which is outlined in my Wazuh README.md explaining the steps I took and reasoning behind each step. Within the docker-compose.yml file I added the configurations for my twinggate connector which utilizes ZTNO which allows me to access my Wazuh Cluster remotely.

# Deploy Wazuh using Docker for single-node configuration

This deployment is defined in the `docker-compose.yml` file with one Wazuh manager container, one Wazuh indexer container, and one Wazuh dashboard container. It can be deployed by following these steps: 

1) Increase max_map_count on your host (Linux). This command must be run with root permissions:
```
$ sysctl -w vm.max_map_count=262144
```
2) Next you will want to ``` cd /wazuh-docker/single-node ``` to run the certificate creation script. This will generate your self-signed certs:
```
$ docker-compose -f generate-indexer-certs.yml run --rm generator
```
3) Start the environment with docker-compose:

 You will want to run your Docker-Compose in the background:
```
$ docker-compose up -d
```

Once you run the docker-compose file, you will begin to see the Docker containers images being pulled. You will also see the volumes being created for each docker container along with the additional API volumes created such as filebeat.




