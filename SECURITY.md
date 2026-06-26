# Security Policy

## Supported Versions

| Version | Supported |
|---------|-----------|
| 1.x.x | ✅ Active support |
| < 1.0 | ❌ No longer supported |

## Reporting a Vulnerability

**Please do NOT open a public GitHub issue for security vulnerabilities.**

### Responsible Disclosure Process

1. **Email**: Send details to `security@aegis-fraud.ai`
2. **PGP Key**: Available at `https://aegis-fraud.ai/.well-known/security.txt`
3. **Response Time**: We acknowledge within 24 hours
4. **Resolution Target**: Critical issues patched within 7 days

### What to Include

- Description of the vulnerability
- Steps to reproduce
- Potential impact assessment
- Suggested fix (if any)

### Scope

**In scope:**
- AEGIS backend API (FastAPI)
- Authentication and authorization bypass
- SQL injection, XSS, CSRF
- Secrets exposure in logs or responses
- Insecure deserialization
- Dependency vulnerabilities (CVSSv3 ≥ 7.0)

**Out of scope:**
- Social engineering attacks
- Physical security
- Third-party services (Kafka, PostgreSQL, etc.)
- DoS/DDoS without security impact

## Security Features

### Authentication
- JWT with RS256 (access) and HS256 (refresh)
- Refresh token rotation on every use
- Account lockout after 5 failed attempts (30-minute lockout)
- Optional TOTP MFA support

### API Security
- Rate limiting: 1,000 req/min default, 10 req/15min for auth
- Request signing for webhook callbacks
- Input validation via Pydantic v2 strict mode
- SQL injection prevention via SQLAlchemy ORM

### Data Security
- AES-256 encryption at rest for sensitive fields
- TLS 1.3 for all in-transit data
- Secrets managed via environment variables + HashiCorp Vault
- PII masking in logs

### Audit Logging
- Immutable audit trail for all API operations
- Log tampering detection via hash chaining
- Retained for 90 days (configurable)

### Dependency Scanning
- `safety check` in CI/CD for known CVEs
- `bandit` for Python security anti-patterns
- `trivy` image scanning for container vulnerabilities
- Dependabot alerts enabled

## Security Hall of Fame

We thank the following researchers for responsible disclosure:

*(No disclosures yet — be the first!)*
