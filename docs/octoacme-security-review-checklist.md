# OctoAcme — Security Review Checklist

## Purpose
Ensure that features and systems are designed, developed, and deployed with security best practices, minimizing vulnerabilities and protecting customer data.

## When to Use
- During feature design and architecture planning
- Before code review and deployment
- When responding to security incidents
- During regular security audits and compliance reviews

## Security Review Levels

### Level 1: Standard Feature Review
**Required For**: All new features and significant changes  
**Reviewer**: Developer + automated security tools  
**Timeline**: As part of normal PR review process

### Level 2: Enhanced Security Review
**Required For**: Authentication, authorization, data handling, external integrations  
**Reviewer**: Security Lead or designated security champion  
**Timeline**: 1-2 business days

### Level 3: Comprehensive Security Assessment
**Required For**: New services, major architecture changes, compliance-critical features  
**Reviewer**: Security Lead + external security consultant (if needed)  
**Timeline**: 1-2 weeks

## Pre-Development Security Checklist

### Threat Modeling
- [ ] Assets and data flows identified
- [ ] Threat actors and attack vectors documented
- [ ] Security requirements defined (STRIDE analysis)
- [ ] Data classification completed (public, internal, confidential, restricted)
- [ ] Privacy implications assessed (PII, GDPR, CCPA considerations)

### Architecture Review
- [ ] Authentication and authorization approach defined
- [ ] Data encryption requirements specified (at rest and in transit)
- [ ] API security controls designed (rate limiting, input validation)
- [ ] Secure defaults configured
- [ ] Principle of least privilege applied

### Compliance & Regulatory
- [ ] Compliance requirements identified (SOC 2, GDPR, HIPAA, etc.)
- [ ] Data retention and deletion policies defined
- [ ] Audit logging requirements specified
- [ ] Consent and privacy notice requirements documented

## Development Security Checklist

### Secure Coding Practices
- [ ] Input validation implemented for all user inputs
- [ ] Output encoding applied to prevent XSS
- [ ] Parameterized queries used to prevent SQL injection
- [ ] No hardcoded secrets or credentials in code
- [ ] Error messages don't leak sensitive information
- [ ] Security headers configured (CSP, HSTS, X-Frame-Options, etc.)

### Authentication & Authorization
- [ ] Strong password requirements enforced (length, complexity)
- [ ] Multi-factor authentication (MFA) supported or required
- [ ] Session management secure (httpOnly, secure, sameSite cookies)
- [ ] Session timeout configured appropriately
- [ ] Authorization checks performed on all protected resources
- [ ] Role-based access control (RBAC) implemented correctly

### Data Protection
- [ ] Sensitive data encrypted at rest (AES-256 or equivalent)
- [ ] TLS 1.2+ enforced for data in transit
- [ ] PII and sensitive data minimized in logs
- [ ] Data masking applied in non-production environments
- [ ] Secure key management solution used (no keys in code)

### API Security
- [ ] API authentication required (OAuth, API keys, JWT)
- [ ] Rate limiting implemented to prevent abuse
- [ ] CORS policy configured appropriately
- [ ] Request size limits enforced
- [ ] API versioning strategy defined

### Dependencies & Supply Chain
- [ ] All dependencies scanned for known vulnerabilities
- [ ] Dependencies updated to latest secure versions
- [ ] License compliance verified
- [ ] Dependency sources trusted and verified
- [ ] Software Bill of Materials (SBOM) generated

## Testing & Validation Checklist

### Automated Security Testing
- [ ] Static Application Security Testing (SAST) run and passing
- [ ] Dynamic Application Security Testing (DAST) run on staging
- [ ] Dependency scanning completed (Dependabot, Snyk, etc.)
- [ ] Secrets scanning run (no credentials in code)
- [ ] Infrastructure as Code (IaC) security scan completed

### Manual Security Testing
- [ ] Authentication bypass attempts tested
- [ ] Authorization boundary testing completed
- [ ] Input validation tested with malicious inputs (SQLi, XSS, etc.)
- [ ] File upload security validated (type checking, size limits)
- [ ] Session management tested (fixation, hijacking)

### Security Test Cases
- [ ] Test with invalid/malicious inputs
- [ ] Test authorization with different user roles
- [ ] Test rate limiting and abuse scenarios
- [ ] Test error handling (no stack traces exposed)
- [ ] Test HTTPS enforcement and certificate validation

## Pre-Deployment Security Checklist

### Configuration Review
- [ ] Secrets managed via secure secret management system
- [ ] Environment variables properly configured
- [ ] Debug/verbose logging disabled in production
- [ ] Unnecessary services and ports disabled
- [ ] File permissions set appropriately

### Infrastructure Security
- [ ] Network security groups/firewalls configured
- [ ] Principle of least privilege applied to IAM roles
- [ ] Logging and monitoring configured
- [ ] Backup and disaster recovery tested
- [ ] Patch management process in place

### Deployment Security
- [ ] Deployment uses secure CI/CD pipeline
- [ ] Code signing or artifact verification enabled
- [ ] Rollback procedure tested and documented
- [ ] Monitoring alerts configured for security events
- [ ] Incident response plan reviewed and updated

## Post-Deployment Security Checklist

### Monitoring & Detection
- [ ] Security monitoring dashboards configured
- [ ] Alerts for suspicious activity configured (failed logins, etc.)
- [ ] Log aggregation and retention configured
- [ ] Vulnerability scanning scheduled (weekly/monthly)
- [ ] Penetration testing scheduled (annually or as needed)

### Incident Response Readiness
- [ ] Incident response playbook reviewed
- [ ] On-call rotation includes security contact
- [ ] Communication channels established
- [ ] Evidence preservation procedures documented

## Security Incident Response

### Severity Levels
- **CRITICAL**: Active breach, data exfiltration, ransomware
- **HIGH**: Vulnerability actively exploited, unauthorized access
- **MEDIUM**: Vulnerability identified but not exploited
- **LOW**: Informational findings, best practice recommendations

### Incident Response Steps
1. **Detect & Assess** (0-1 hour)
   - [ ] Confirm the incident and assess scope
   - [ ] Classify severity level
   - [ ] Notify Security Lead and on-call team
   
2. **Contain** (1-4 hours)
   - [ ] Isolate affected systems
   - [ ] Revoke compromised credentials
   - [ ] Block malicious traffic
   - [ ] Preserve evidence for investigation

3. **Eradicate** (4-24 hours)
   - [ ] Identify and remove root cause
   - [ ] Patch vulnerabilities
   - [ ] Restore from clean backups if needed

4. **Recover** (1-3 days)
   - [ ] Restore services to normal operation
   - [ ] Verify system integrity
   - [ ] Enhance monitoring

5. **Post-Incident Review** (within 1 week)
   - [ ] Document timeline and actions taken
   - [ ] Identify lessons learned
   - [ ] Update incident response playbook
   - [ ] Implement preventive measures

### Communication Protocol
- **Internal**: Notify engineering leadership, legal, and affected teams
- **External**: Coordinate with legal on customer/regulatory notification
- **Timeline**: Follow breach notification laws (e.g., 72 hours for GDPR)

## Vulnerability Management

### Vulnerability Disclosure
- [ ] Security policy published (security.txt or dedicated page)
- [ ] Responsible disclosure process documented
- [ ] Bug bounty program established (if applicable)
- [ ] Triage process for incoming reports defined

### Remediation SLAs
- **Critical**: 24 hours
- **High**: 7 days
- **Medium**: 30 days
- **Low**: 90 days or next release

### Patch Management
- [ ] Security patches tested in staging
- [ ] Emergency change process for critical patches
- [ ] Patch deployment communicated to stakeholders
- [ ] Verification testing completed post-patch

## Compliance Checklist

### SOC 2 Controls
- [ ] Access controls documented and enforced
- [ ] Change management process followed
- [ ] Encryption standards met
- [ ] Audit logs maintained and reviewed
- [ ] Background checks completed for personnel

### GDPR Requirements
- [ ] Data processing agreements in place
- [ ] Privacy policy updated
- [ ] Data subject rights supported (access, deletion, portability)
- [ ] Breach notification process established
- [ ] Data Protection Impact Assessment (DPIA) completed if needed

## Security Training & Awareness
- [ ] Secure coding training completed by developers
- [ ] Phishing awareness training for all employees
- [ ] Incident response drills conducted quarterly
- [ ] Security champions program active in engineering teams

## Security Metrics to Track
- Number of vulnerabilities by severity (CVSS score)
- Mean time to detect (MTTD) security incidents
- Mean time to remediate (MTTR) vulnerabilities
- Security test coverage (% of code covered by SAST)
- Compliance audit findings

## Resources
- **Security Policies**: [Link to security policy repository]
- **Vulnerability Database**: [Link to vuln tracking system]
- **Security Tools**: [Link to SAST/DAST/scanning tools]
- **Incident Response**: [Link to incident response playbook]
- **Compliance Docs**: [Link to compliance documentation]

## Related Documents
- [Roles and Personas](octoacme-roles-and-personas.md) — See Security Lead role definition
- [DevOps Checklist](octoacme-devops-checklist.md) — Deployment security controls
- [Risk Management & Communication](octoacme-risks-and-communication.md) — Risk management strategies
- [Execution and Tracking](octoacme-execution-and-tracking.md) — Security testing in CI/CD
