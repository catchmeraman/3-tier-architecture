# Self-Service 3-tier Environment Provisioning Using Docker MCP Catalog

## Overview

This project demonstrates how to use a Docker MCP catalog to provision a 3-tier microservices architecture using Docker Compose.

## Components

- Frontend: NGINX or React App
- Backend: Node.js API
- Database: PostgreSQL

## Steps to Deploy

1. Clone the repository:
    ```bash
    git clone <repo-url>
    cd docker_mcp_3tier_catalog
    ```

2. Modify the `.env` file with your custom configuration.

3. Deploy the stack using Docker Compose:
    ```bash
    docker compose --env-file .env -f docker-compose.yml up -d
    ```

4. Access your services:
    - Frontend: `http://localhost:8080`
    - Backend API: `http://localhost:3000`
    - Database: runs in background

## Clean Up

```bash
docker compose down -v
```

## Security Tips

- Do not commit `.env` with secrets to Git.
- Use Docker secrets or Vault for production deployments.
- Limit port exposure and run containers as non-root.