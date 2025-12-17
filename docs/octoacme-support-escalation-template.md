# OctoAcme — Customer Support Escalation Template

## Purpose
Provide a standardized process for escalating customer issues from Support to Engineering, Product, or other teams, ensuring efficient resolution and clear communication.

## When to Use
- Customer reports a critical bug or service outage
- Feature request has significant business impact or multiple customer requests
- Complex technical issue requires Engineering investigation
- Customer escalation requires leadership involvement

## Support Escalation Levels

### Level 1: Standard Support
**Handler**: Support/Customer Success Representative  
**Response Time**: Within 4 business hours  
**Resolution Target**: 1-2 business days

**Issue Types**:
- Common how-to questions
- Known issues with documented workarounds
- Account/billing inquiries
- Basic configuration assistance

### Level 2: Engineering Support
**Handler**: Engineering team via ticketing system  
**Response Time**: Within 1 business day  
**Resolution Target**: 3-5 business days

**Issue Types**:
- Confirmed bugs requiring code fixes
- Performance issues specific to customer environment
- Integration problems
- Data inconsistencies

### Level 3: Critical Escalation
**Handler**: Engineering Lead + Product Manager  
**Response Time**: Within 2 hours  
**Resolution Target**: Same day or emergency hotfix

**Issue Types**:
- Production outage affecting multiple customers
- Data loss or security incident
- Severe performance degradation
- Customer threatening to churn due to product issues

### Level 4: Executive Escalation
**Handler**: VP Engineering, VP Product, or CEO  
**Response Time**: Immediate  
**Resolution Target**: Immediate action plan

**Issue Types**:
- Strategic account at risk of churning
- Legal or compliance issues
- Major brand/reputation risk
- Contract-critical functionality broken

## Escalation Template

### Issue Summary
**Customer Name**: [Company/Contact name]  
**Account Tier**: [Free, Pro, Enterprise]  
**Reported By**: [Customer contact email/name]  
**Reported Date**: [YYYY-MM-DD]  
**Support Ticket ID**: [TICKET-12345]  
**Escalation Level**: [L1/L2/L3/L4]  
**Assigned To**: [Team/Person]

### Problem Description
[Clear, concise description of the issue from customer perspective]

**Impact**:
- Number of users affected: [#]
- Business impact: [e.g., cannot process orders, workflow blocked]
- Urgency: [High/Medium/Low]
- Financial impact (if known): [e.g., $X revenue blocked daily]

### Steps to Reproduce
1. [Step 1]
2. [Step 2]
3. [Step 3]

**Expected Behavior**: [What should happen]  
**Actual Behavior**: [What actually happens]

### Technical Details
**Environment**: [Production, Staging, etc.]  
**Browser/Client**: [e.g., Chrome 120, Mobile App v2.5]  
**User Role/Permissions**: [e.g., Admin, Standard User]  
**Relevant URLs**: [Link to affected pages]  
**Error Messages**: [Exact error text or screenshots]  
**Logs/Stack Traces**: [Attach or link to logs]

### Customer Context
**Account Value**: [Annual contract value if relevant]  
**Customer Health Score**: [Green/Yellow/Red]  
**Recent Interactions**: [Summary of recent support history]  
**Customer Sentiment**: [Frustrated, Understanding, Angry, etc.]  
**Renewal Date**: [If applicable and near-term]

### Investigation & Findings
**Initial Diagnosis**: [Support team's initial assessment]  
**Workaround Available**: [Yes/No — if yes, describe]  
**Root Cause (if known)**: [Technical explanation]  
**Related Issues**: [Links to similar tickets or known bugs]

### Requested Action
- [ ] Bug fix required
- [ ] Feature enhancement
- [ ] Configuration change
- [ ] Documentation update
- [ ] Escalation to leadership
- [ ] Other: [Specify]

**Proposed Timeline**: [Expected resolution date]  
**Priority Justification**: [Why this needs immediate attention]

### Communication Plan
**Customer Commitment**: [What was promised to customer]  
**Update Frequency**: [How often customer expects updates]  
**Next Update Due**: [YYYY-MM-DD HH:MM]  
**Point of Contact**: [Who is managing customer communication]

## Escalation Checklist

### Before Escalating to Engineering
- [ ] Attempted basic troubleshooting steps
- [ ] Searched knowledge base for similar issues
- [ ] Reproduced the issue (if possible)
- [ ] Gathered all relevant technical details
- [ ] Documented steps to reproduce clearly
- [ ] Checked for existing bug reports or feature requests
- [ ] Assessed business impact and urgency

### During Escalation
- [ ] Filled out escalation template completely
- [ ] Assigned to appropriate team/person
- [ ] Set priority and severity appropriately
- [ ] Notified customer that issue has been escalated
- [ ] Added to escalation tracking board
- [ ] Scheduled follow-up reminders

### After Resolution
- [ ] Verified fix with customer
- [ ] Updated knowledge base if new issue type
- [ ] Documented root cause and resolution
- [ ] Gathered customer feedback (CSAT score)
- [ ] Closed support ticket with summary
- [ ] Shared learnings with support team

## Feature Request Escalation

### Criteria for Product Team Review
- **Volume**: 5+ customers requesting same feature
- **Impact**: High-value customer requesting feature
- **Strategic**: Aligns with product roadmap direction
- **Competitive**: Required for competitive parity
- **Contract**: Promised in customer contract/negotiation

### Feature Request Template
**Feature Summary**: [Brief description]  
**Customer Use Case**: [What problem does this solve?]  
**Number of Requests**: [How many customers asked for this?]  
**Workaround Available**: [Yes/No — if yes, describe]  
**Business Impact**: [Revenue opportunity or retention risk]  
**Competitive Context**: [Do competitors have this feature?]

## Communication Templates

### Initial Escalation Email to Engineering
```
Subject: [ESCALATION] [L2/L3] - [Brief issue description] - [Customer Name]

Hi [Engineering Team],

We have an escalated customer issue that requires engineering investigation:

- Customer: [Name/Company]
- Issue: [One-line summary]
- Impact: [Business impact]
- Priority: [High/Medium]
- Ticket: [TICKET-12345]

Full details in the escalation template: [Link to ticket/document]

Please acknowledge and provide an initial assessment by [Date/Time].

Customer has been notified and expects an update by [Date/Time].

Thank you,
[Support Rep Name]
```

### Customer Update Template
```
Subject: Update on [Issue Summary] - Ticket #[12345]

Hi [Customer Name],

Thank you for your patience. Here's an update on your issue:

**Current Status**: [Under investigation / Fix in progress / Fix deployed]

**What we've found**: [Brief explanation]

**Next Steps**: [What will happen next]

**Expected Timeline**: [When customer can expect resolution]

I'll keep you updated with progress. Please don't hesitate to reach out if you have questions.

Best regards,
[Support Rep Name]
```

## Escalation Metrics to Track
- Average time to first response by escalation level
- Escalation volume by category (bug, feature, configuration)
- Customer satisfaction scores for escalated issues
- Re-escalation rate (issues escalated multiple times)
- Resolution time by escalation level

## Resources
- **Support Ticketing System**: [Link to Zendesk/Jira Service Desk]
- **Knowledge Base**: [Link to internal knowledge base]
- **Customer Health Dashboard**: [Link to customer success platform]
- **Engineering On-Call**: [Link to on-call schedule]

## Related Documents
- [Roles and Personas](octoacme-roles-and-personas.md) — See Support/Customer Success role definition
- [Risk Management & Communication](octoacme-risks-and-communication.md) — Communication strategies
- [Execution and Tracking](octoacme-execution-and-tracking.md) — Blocker escalation process
