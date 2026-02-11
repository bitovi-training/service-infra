# service-infra

Docker Compose setup for running the core microservices locally.

## Services
- **order-service**: http://localhost:8100
- **product-service**: http://localhost:8200
- **loyalty-service**: http://localhost:8300
- **user-service**: http://localhost:8400

## Requirements
- Docker + Docker Compose v2

## Start all services
```bash
docker compose up -d --build
```

## Start a subset
```bash
docker compose up -d --build order-service product-service
```

## Stop services
```bash
docker compose down
```

## Environment variables
These are wired in `docker-compose.yml` and match service defaults:
- **order-service**: `PRODUCT_SERVICE_URL`, `LOYALTY_SERVICE_URL`, `PORT`
- **loyalty-service**: `ORDER_SERVICE_URL`, `USER_SERVICE_URL`, `PORT`
- **product-service**: `PORT`
- **user-service**: `PORT`

## Related docs
- `../order-service/README.md`
- `../product-service/README.md`
- `../loyalty-service/README.md`
- `../user-service/README.md`
