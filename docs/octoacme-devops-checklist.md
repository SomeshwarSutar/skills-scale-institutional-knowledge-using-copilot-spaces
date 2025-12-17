# OctoAcme — DevOps Deployment Checklist

## Purpose
Ensure deployments are executed safely, reliably, and with proper monitoring and rollback capabilities.

## When to Use
- Before any production deployment
- When setting up new services or infrastructure
- During incident response and emergency deployments

## Pre-Deployment Checklist

### Code & Build
- [ ] All automated tests passing in CI
- [ ] Code reviewed and approved by required reviewers
- [ ] Security scans completed (SAST, dependency vulnerabilities)
- [ ] Build artifacts versioned and tagged appropriately
- [ ] Release notes drafted with changes and known issues

### Infrastructure & Configuration
- [ ] Infrastructure changes reviewed and approved (IaC/Terraform plans)
- [ ] Configuration changes documented and peer-reviewed
- [ ] Environment variables and secrets properly configured
- [ ] Database migrations tested and rollback plan documented
- [ ] Resource capacity validated (CPU, memory, storage, network)

### Monitoring & Observability
- [ ] Key metrics and alerts configured for new features
- [ ] Logging instrumentation in place for debugging
- [ ] Dashboards updated to track deployment health
- [ ] Error tracking configured (e.g., Sentry, Rollbar)
- [ ] Performance monitoring enabled (APM tools)

### Communication & Coordination
- [ ] Deployment time scheduled and communicated to stakeholders
- [ ] On-call engineer identified and available during deployment
- [ ] Dependent teams notified of deployment (if applicable)
- [ ] Customer-facing communication prepared (if needed for downtime)
- [ ] Rollback plan documented and reviewed with team

## Deployment Execution Checklist

### Pre-Flight Checks
- [ ] Verify deployment window and change freeze status
- [ ] Confirm backup/snapshot of production data completed
- [ ] Review rollback procedure and ensure it's tested
- [ ] Set deployment status in communication channels (e.g., Slack)

### Deployment Steps
- [ ] Deploy to staging/canary environment first
- [ ] Run smoke tests on staging/canary deployment
- [ ] Monitor key metrics for 10-15 minutes in staging/canary
- [ ] Gradually roll out to production (if using progressive delivery)
- [ ] Monitor error rates, latency, and resource utilization
- [ ] Verify critical user flows are working as expected

### Post-Deployment Verification
- [ ] Smoke tests passed in production
- [ ] No spike in error rates or alerts triggered
- [ ] Key business metrics stable (e.g., transaction volume, API response times)
- [ ] User-facing features validated manually
- [ ] Documentation updated (runbooks, architecture diagrams)

## Rollback Checklist

### When to Rollback
- Error rates exceed 5% increase from baseline
- Critical functionality is broken
- Security vulnerability discovered in deployed version
- Performance degradation affects customer experience

### Rollback Steps
- [ ] Announce rollback decision to team and stakeholders
- [ ] Execute rollback procedure (revert deployment, restore database if needed)
- [ ] Verify previous version is running correctly
- [ ] Monitor for 15 minutes to confirm stability
- [ ] Document root cause and action items in incident report
- [ ] Schedule postmortem meeting within 24-48 hours

## Progressive Delivery Strategies

### Canary Deployment
- Deploy to small percentage of production traffic (e.g., 5%)
- Monitor for 15-30 minutes
- Gradually increase to 25%, 50%, 100% if metrics are healthy

### Blue-Green Deployment
- Deploy to parallel environment (green)
- Run validation tests on green environment
- Switch traffic from blue to green
- Keep blue environment available for quick rollback

### Feature Flags
- Deploy code with feature disabled
- Enable for internal users first
- Gradually roll out to user segments
- Monitor and adjust rollout speed based on metrics

## Incident Response

### Severity Levels
- **SEV1 (Critical)**: Complete service outage or data loss
- **SEV2 (High)**: Major feature broken, significant user impact
- **SEV3 (Medium)**: Minor feature issue, workaround available
- **SEV4 (Low)**: Cosmetic issue or minor bug

### Escalation Path
1. On-call DevOps Engineer investigates
2. Escalate to Engineering Lead if not resolved in 15 minutes (SEV1/2)
3. Escalate to Product/Engineering Director for business impact decisions
4. Involve Security Lead if security-related

## Deployment Metrics to Track
- Deployment frequency (daily, weekly)
- Lead time for changes (commit to production)
- Change failure rate (percentage of deployments causing incidents)
- Mean time to recovery (MTTR)

## Resources
- **Runbooks**: [Link to operational runbooks]
- **Infrastructure Docs**: [Link to architecture and IaC documentation]
- **Monitoring Dashboards**: [Link to Grafana/Datadog/CloudWatch]
- **On-Call Schedule**: [Link to PagerDuty/Opsgenie schedule]

## Related Documents
- [Roles and Personas](octoacme-roles-and-personas.md) — See DevOps Engineer role definition
- [Release and Deployment](octoacme-release-and-deployment.md) — Overall release process
- [Risk Management & Communication](octoacme-risks-and-communication.md) — Communication strategies
