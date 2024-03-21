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




