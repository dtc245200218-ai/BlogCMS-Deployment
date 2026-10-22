# Blog/CMS Deployment

WordPress CMS deployed with Docker Compose.

## Services
WordPress, MySQL, phpMyAdmin, Nginx, Prometheus, Grafana, Loki and Promtail.

## Start
1. Configure .env using .env.example and set strong passwords.
2. Validate: docker compose config --quiet
3. Start: docker compose up -d

## Local URLs
- Blog via Nginx: http://localhost:8082
- WordPress: http://localhost:8090
- phpMyAdmin: http://localhost:8091
- Prometheus: http://localhost:9090
- Grafana: http://localhost:3000

## LogQL examples
{service_name=~".+"}
{service_name=~".+"} |~ "(?i)error"
{service_name=~".+"} |~ "(?i)info"

Never commit .env or real credentials.
