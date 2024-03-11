# Configuration of Docker Compose, Docker Bridge Network, &  Port Forwarding

## Purpose

Our Docker-Compose.yml file is located at ```/wazuh-docker/single-node``` . Once within our directory, we will be able to run the ```docker-compose up -d```
cmd to run all the containers outlined in our compose.

Docker Compose allows us to group our containers within one network which is created by Docker. Within this group, the docker containers can be ran together while allowing them to communicate with each other. This is beneficial for our Wazuh cluster since we will need the Wazuh Manager, Wazuh Indexer, and Wazuh Dashboard to send/recieve data.








## Docker-Compose.yml File

For each service defined in your docker-compose.yml file, ensure you have defined your network for each service.
```
    networks:
      - custom-network
```

After defining the services for your docker-compose, add the following to the bottom of your docker-compose.yml file:
```
networks:
  custom-network:
    driver: bridge
    ipam:
      driver: default
      config:
        - subnet: <enter your subnet for your network>
```

## Docker Bridge Network
When defining my bridge network, I chose to do so in my docker-compose file. 

*    Note: By configuring the network this way, the 'custom-network' will only be created when docker-compose is running and will not be listed in 'network ls' if compose is not running.

```
networks:
  custom-network:
    driver: bridge
    ipam:
      driver: default
      config:
        - subnet: <ip of subnet for your network>
```

## Port Fowarding (Xcp-ng -> Host -> Docker-Compose)

