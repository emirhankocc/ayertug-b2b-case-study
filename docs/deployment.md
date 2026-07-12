# Deployment

## Infrastructure

- Ubuntu server
- Plesk
- Node.js
- Docker
- Cloudflare DNS and CDN
- Cloudflare R2 object storage

## Deployment Flow

1. Application source is prepared for production.
2. Environment variables are configured securely.
3. Applications are built separately.
4. Backend and frontend services are deployed.
5. Reverse proxy and SSL settings are configured.
6. Health checks and logs are reviewed.

## Production Considerations

- Secrets are excluded from the repository.
- Database backups are required.
- Asset storage is separated from the application server.
- Logs are monitored during deployments.
- Staging validation is performed before production changes.
