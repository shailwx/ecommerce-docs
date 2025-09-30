# Monitoring and Observability

## Health Endpoints
- Each microservice should expose `/health` or `/ready` endpoints for status checks.

## Logging
- Use structured logging (JSON format recommended).
- Log levels: INFO, WARN, ERROR, DEBUG.

## Metrics
- Track API latency, request counts, error rates per endpoint.
- Expose metrics via `/metrics` (for Prometheus or similar).

## Alerting
- Define alerts for high error rate, downtime, or resource exhaustion.
- Integrate with tools like PagerDuty, Opsgenie, or email.

## Dashboards
- Use Grafana or similar to visualize key metrics.
- Example dashboards: API latency, error rates, service uptime.

## Example Health Response
```json
{
  "status": "ok",
  "uptime": "72h",
  "version": "1.0.3"
}
```