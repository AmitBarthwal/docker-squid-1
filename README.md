[![](https://images.microbadger.com/badges/image/b4tman/squid.svg)](https://microbadger.com/images/b4tman/squid "Get your own image badge on microbadger.com")

# docker-squid

Docker Squid container based on Alpine Linux.

Automated builds of the image are available on [Dockerhub](https://hub.docker.com/r/b4tman/squid).

> **Note**: [armhf](https://github.com/b4tman/docker-squid/tree/armhf) image is based on **experimental** [armhf/alpine](https://hub.docker.com/r/armhf/alpine/) image. 

# Quick Start

Just launch container:

```bash
docker run -p 3128:3128 b4tman/squid
```

or use [docker-compose](https://docs.docker.com/compose/):

```bash
wget https://raw.githubusercontent.com/b4tman/docker-squid/master/docker-compose.yml
docker-compose up
```

# Configuration

## Environment variables:

- **SQUID_CONFIG_FILE**: Specify the configuration file for squid. Defaults to `/etc/squid/squid.conf`.


## Example:

```bash
docker run -p 3128:3128 \
	--env='SQUID_CONFIG_FILE=/etc/squid/my-squid.conf' \
	--volume=/srv/docker/squid/squid.conf:/etc/squid/my-squid.conf:ro \
	b4tman/squid
```

This will start a squid container with your config file `/srv/docker/squid/squid.conf`. 
