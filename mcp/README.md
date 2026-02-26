# MCP

## Environment URL

https://mcp.hyperplane.dev

## Accessible?

yes

## Airgapped (Y/N)



## Steps to access Kubernetes

SSH access managed via public key auth. To get access:
1. Generate an SSH key pair if you don't have one
2. Give Yiran your public key (`.pub` file) to be added to the server
3. SSH credentials are stored in 1Password:
   - **MCP SSH Access**: [Open in 1Password](https://shakudo.1password.com/app#/vaults/zwgd3omhtwxsdakm7cd64iqwpa/items/or4ztyacvacsjs76mdey2arv4i)
   - `op://[Client admin] MCP/MCP SSH Access/username` — ubuntu
   - `op://[Client admin] MCP/MCP SSH Access/hostname` — server IP
   - `op://[Client admin] MCP/MCP SSH Access/port` — SSH port
4. Once added: `ssh ubuntu@<host> -p <port>` (retrieve host+port from 1Password above)
5. Find the kubeconfig and `scp` it to your machine

## Steps to access Dashboard

Login via 1Password: https://shakudo.1password.com/app#/vaults/zwgd3omhtwxsdakm7cd64iqwpa/items/or4ztyacvacsjs76mdey2arv4i

## Infrastructure provider

Latitude (Shakudo managed)

## Who manages the infra/cloud

Shakudo

## Shakudo Version

v3.48.0

## Stack Components

GraphQL, Grafana, Alertmanager, Qdrant, Langfuse V3, n8n, LiteLLM, Open Web UI, Open Web UI 1, Neo4j, Minio

## Last updated on (stack components)

Dec 10, 2025

## If changes, tag Shahzad/Chandan



## Applications



## Notes



## Who to ask

Yijie, Shabbir

## GPU available



## Backup enabled? What is backed up? and How?

No back up

## GPU config (VRAM?)


