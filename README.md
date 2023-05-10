# docker-compose-archive

## Introduction
This repository contains multiple docker-compose.yml files for popular services like traefik, portainer, and n8n. The docker-compose files are configured to work together and can be used to quickly spin up a development environment with these services.

## How to use
1. Clone this repository.
2. Navigate to the directory of the service you want to run (e.g., traefik).
3. Run `docker-compose up -d` to start the service.

### Note for localhost
For the domains specified in the `traefik.http.routers.[serviceName].rule=Host([URL])` section of the docker-compose file to work correctly on localhost, they need to be added to the `/etc/hosts` file. Here's an example of how to do it:

```
127.0.0.1 traefik.loc
127.0.0.1 whoami.loc
```

Replace `traefik.loc` and `whoami.loc` with the URLs specified in the `traefik.http.routers.[serviceName].rule=Host([URL])` section of the docker-compose file.

## Services
This repository currently contains docker-compose files for the following services:

- Traefik: A reverse proxy and load balancer that can be used to route incoming requests to the appropriate container.
- Portainer: A web-based container management UI.
- n8n: A workflow automation tool that allows you to create and manage workflows using a drag-and-drop interface.
