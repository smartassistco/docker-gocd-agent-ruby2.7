# GoCD Agent with Ruby 2.7 Docker Image

[![dockeri.co](https://dockeri.co/image/smartassist/gocd-agent-ruby2.7)](https://hub.docker.com/r/smartassist/gocd-agent-ruby2.7)

[![Docker Build Status](https://github.com/smartassistco/docker-gocd-agent-ruby2.7/actions/workflows/docker-image.yml/badge.svg)](https://github.com/smartassistco/docker-gocd-agent-ruby2.7/actions/workflows/docker-image.yml)

[GoCD Agent on Debian 10](https://hub.docker.com/r/gocd/gocd-agent-debian-10) with the latest version of Ruby 2.7 added to
it.

## Usage

- To use in your docker-compose.yml:

```yaml
version: "3.8"

services:
  gocd-agent-ruby2.7:
    image: smartassist/gocd-agent-ruby2.7:v21.3.0
    restart: unless-stopped
    env_file: .env
```

- To modify further, reference in your Dockerfile:

```dockerfile
FROM smartassist/gocd-agent-ruby2.7:v21.3.0
```

## Contents

- [GoCD's official Debian 10 agent's Dockerfile](https://hub.docker.com/r/gocd/gocd-agent-debian-10)
- [Docker's official Ruby 2.7 Dockerfile](https://github.com/docker-library/ruby/raw/master/2.7/buster/Dockerfile)
- [Buildpack Dependencies](https://github.com/docker-library/buildpack-deps/raw/master/debian/buster/Dockerfile)
- [Docker's official Node 16 Dockerfile](https://github.com/nodejs/docker-node/raw/main/16/buster/Dockerfile)

## Versions

| Runtime    | Version |
|------------|---------|
| OS      | Debian 10 (Buster)  |
| GoCD agent | 21.3.0 |
| Ruby       | 2.7.5  |
| Node       | 16.13.0  |

## Building

- Update versions in `generate.sh`
- Run `bash generate.sh`
