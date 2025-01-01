# Docker Healthchecks Repository

This repository contains a collection of healthchecks designed for use with Docker Compose files. Each healthcheck ensures that your containers are running optimally and can quickly recover in case of issues.

## Features

- **Custom Healthchecks**: Ready-to-use scripts for monitoring container health.
- **Wide Compatibility**: Designed to work seamlessly with various containers.
- **Easy Integration**: Drop-in healthcheck commands for Docker Compose services.

## Usage

To use a healthcheck, simply add the corresponding healthcheck script to your container's `docker-compose.yml` file. Here's an example:

```yaml
services:
  my-service:
    image: my-image
    healthcheck:
      test: ["CMD", "healthcheck-script.sh"]
      interval: 30s
      timeout: 10s
      retries: 3