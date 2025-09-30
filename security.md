# Security Documentation

## Authentication
- JWT-based auth for APIs.
- Refresh tokens for session management.

## Authorization
- Role-based access control (user, admin).
- Endpoint protection via middleware.

## Data Protection
- Store passwords hashed (bcrypt, Argon2).
- Use HTTPS for all traffic.
- Sensitive environment variables in secrets store.

## Compliance
- GDPR: Right to delete, export user data.
- PCI DSS (payments): Never store raw card data.

## Common Vulnerabilities
- SQL Injection: Use parameterized queries.
- XSS: Input/output sanitization.
- CSRF: Use tokens for state-changing requests.

## Security Checklist
- [ ] Use HTTPS everywhere
- [ ] Validate all inputs
- [ ] Rotate secrets regularly
- [ ] Audit logs for admin actions