# Dockerized Pihole
This YAML files creates a docker container that has its own IP address on your network with a  macvlan configuration. 

## Requirements

* docker-compose
* docker

## Installation
1. Make sure you are in the same directory as the docker-compose.yml file.
2. Execure the below commands

```bash
docker-compose -f docker-compose.yml up -d --build
```

Tear down
```bash
docker-compose down -v
```
3. Navigate to`http://ipv4_address/admin` page and log in with the `WEBPASSWORD.`

4. Once that is up and running, point your router, phone, laptop, etc, at the new IP address as your DNS server.

## Customization
To ensure that the YAML file best conforms to your network please change the `ipv4_address`, `ServerIP`, `WEBPASSWORD`, and `parent:interface` before running the above commands. 

Note: Works best when your physical network interface can support multiple mac address. Feel free to swap that out with an ipvlan. 

for more information please see https://github.com/pi-hole/docker-pi-hole/#running-pi-hole-docker
