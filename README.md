# n8n-railway

This repository contains the configuration for deploying n8n on Railway platform. n8n is a workflow automation platform that allows you to automate tasks across different services.

## Features

- n8n workflow automation platform
- PostgreSQL database for persistent storage
- Docker-based deployment
- Basic authentication enabled by default
- Railway platform integration

## Prerequisites

- Docker and Docker Compose
- Railway CLI (for deployment)
- Git

## Quick Start

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/n8n-railway.git
   cd n8n-railway
   ```

2. Start the services using Docker Compose:
   ```bash
   docker-compose up -d
   ```

3. Access n8n at `http://localhost:5555`
   - Default credentials:
     - Username: admin
     - Password: password

## Configuration

### Environment Variables

The following environment variables can be configured:

- `N8N_BASIC_AUTH_ACTIVE`: Enable/disable basic authentication
- `N8N_BASIC_AUTH_USER`: Username for basic authentication
- `N8N_BASIC_AUTH_PASSWORD`: Password for basic authentication
- `DB_TYPE`: Database type (postgresdb)
- `DB_POSTGRESDB_HOST`: PostgreSQL host
- `DB_POSTGRESDB_DATABASE`: Database name
- `DB_POSTGRESDB_USER`: Database user
- `DB_POSTGRESDB_PASSWORD`: Database password
- `PORT`: Port number for n8n (default: 5555)

### Database

The project uses PostgreSQL as the database backend. The database configuration is set up in the `docker-compose.yml` file with the following default settings:

- Database name: n8n
- Username: n8n
- Password: n8n_password
- Port: 5432

## Deployment to Railway

1. Install Railway CLI:
   ```bash
   npm i -g @railway/cli
   ```

2. Login to Railway:
   ```bash
   railway login
   ```

3. Link your project:
   ```bash
   railway link
   ```

4. Deploy your project:
   ```bash
   railway up
   ```

## Security Considerations

- Change the default credentials in production
- Use strong passwords
- Consider using Railway's secrets management for sensitive data
- Enable HTTPS in production

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.
