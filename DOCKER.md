# Docker Setup for Medusa

## Background

While working with Medusa, I encountered and resolved a significant issue (#12163) where developers were unable to start their applications using `npm run dev`. The root cause was an interaction between the test files and the middleware.ts configuration that prevented proper backend-frontend communication.

## The Solution

This Docker setup provides a reliable way to run Medusa by:
1. Isolating the application environment
2. Ensuring proper service communication
3. Preventing test file interference

## Services Overview

The setup includes:

### Database (PostgreSQL)
- Port: 5432
- Credentials: postgres/postgres
- Database: medusa-db

### Redis Cache
- Port: 6379
- Handles caching and messaging

### Medusa Backend
- Port: 9000
- Configured to prevent test interference
- Proper environment variable setup

### Next.js Storefront
- Port: 8000
- Configured to connect with backend

## Quick Start

1. Copy the docker-compose.yml to your project root
2. Run:
```bash
docker compose up
```

## Service URLs

- Backend: http://localhost:9000
- Admin: http://localhost:9000/admin
- Storefront: http://localhost:8000

## Basic Commands

Start services:
```bash
docker compose up -d
```

Stop services:
```bash
docker compose down
```

## Need Help?

If you encounter any issues, check the service logs:
```bash
docker compose logs <service_name>
```

## Resources

- [Medusa Documentation](https://docs.medusajs.com/)
- [Docker Documentation](https://docs.docker.com/)



# What
- Added comprehensive Docker setup documentation
- Added production-ready docker-compose.yml configuration
- Fixed issue #12163 where npm run dev was failing due to test file interference

# Why
- Developers were unable to start applications using npm run dev
- Test files were interfering with application startup
- Middleware.ts configuration was preventing proper backend-frontend communication
- No clear Docker setup documentation existed

# How
- Created detailed Docker setup documentation with clear instructions
- Configured docker-compose.yml with proper service isolation
- Added environment variables to prevent test interference
- Implemented proper service communication setup

# Testing
The changes can be tested by:
1. Cloning the repository
2. Following the Docker setup instructions in DOCKER.md
3. Verifying that all services start correctly
4. Confirming that the application runs without test file interference
