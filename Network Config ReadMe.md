# Configuration for Docker Compose, Docker Bridge Network, &  Port Forwarding

## Docker-Compose.yml File

For each service defined in your docker-compose.yml file, ensure you have defined your network for each service.
```
    networks:
      - custom-network
```

At the bottom of your docker-compose.yml file add the following lines of code:
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

## Port Fowarding Xcp-ng -> Host -> Docker-Compose

