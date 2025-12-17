# OctoAcme Personas

This document defines typical roles and responsibilities used in OctoAcme project docs and exercises.

---

## Developers

### Role Summary
Developers design, build, test, and deliver software components. They collaborate with product and project leads to implement features that meet acceptance criteria and quality standards.

### Responsibilities
- Implement features and fixes to meet acceptance criteria
- Write and maintain tests and documentation
- Participate in design and code reviews
- Assist in estimating and planning work
- Help identify technical risks and propose mitigations

### Goals
- Deliver reliable, maintainable code
- Reduce cycle time from idea to production
- Maintain high test coverage and observability

### Typical Communication
- Daily standups and sprint planning
- PR descriptions and code review comments
- Technical design docs when needed

---

## Product Managers

### Role Summary
Product Managers define what should be built to deliver customer and business value. They own the product vision, prioritize the backlog, and measure outcomes.

### Responsibilities
- Define problem statements and success metrics
- Prioritize the roadmap and backlog
- Collaborate with stakeholders and engineering on trade-offs
- Validate solutions through user research and metrics

### Goals
- Maximize customer value and impact
- Make clear, data-driven prioritization decisions
- Ensure product-market fit and usability

### Typical Communication
- Weekly alignment with PM and engineering leads
- Roadmap updates and stakeholder briefings
- Acceptance criteria and feature specs

---

## Project Managers

### Role Summary
Project Managers coordinate delivery activities, manage schedules, risks, and communications. They enable the team to deliver on commitments efficiently.

### Responsibilities
- Create and maintain project plans and timelines
- Manage risks, dependencies, and resource constraints
- Facilitate meetings (kickoff, planning, retrospectives)
- Ensure consistent project documentation and status reporting
- Coordinate cross-team and stakeholder communication

### Goals
- Deliver projects on time and within scope
- Minimize unplanned work and escalations
- Maintain transparency and alignment across stakeholders

### Typical Communication
- Weekly status updates and stakeholder reports
- Risk registers and decision logs
- Coordination via project boards and meeting facilitation

---

## UX Designer

### Role Summary
UX Designers ensure that products are intuitive, accessible, and delightful for users. They conduct research, create wireframes and prototypes, and work closely with Product Managers and Developers to validate designs and improve the user experience.

### Responsibilities
- Conduct user research and usability testing to inform design decisions
- Create wireframes, mockups, and interactive prototypes
- Define and maintain design systems and UI component libraries
- Collaborate with Product Managers to understand user needs and pain points
- Work with Developers to ensure designs are implemented accurately
- Conduct accessibility audits and ensure WCAG compliance
- Participate in feature planning and provide design estimates

### Goals
- Deliver user-centered designs that meet accessibility standards
- Reduce friction in user workflows and improve task completion rates
- Maintain design consistency across the product
- Validate designs through user testing before development begins

### Typical Communication
- Design review sessions with Product and Engineering teams
- User research findings and usability test reports
- Design specs and handoff documentation in tools like Figma or Sketch
- Participation in sprint planning to discuss design feasibility

### Interactions with Other Roles
- **Product Managers**: Collaborate on feature requirements and user stories; validate solutions through research
- **Developers**: Provide design specifications; review implementation for design accuracy; answer questions during development
- **Support/Customer Success**: Gather feedback on user pain points; understand common support requests to improve UX
- **Security Lead**: Ensure security features (e.g., authentication flows) are user-friendly

---

## DevOps Engineer

### Role Summary
DevOps Engineers build and maintain the infrastructure, CI/CD pipelines, and monitoring systems that enable reliable, scalable, and secure software delivery. They bridge development and operations to automate deployments and improve system reliability.

### Responsibilities
- Design and maintain CI/CD pipelines for automated testing and deployment
- Manage infrastructure as code (IaC) using tools like Terraform or CloudFormation
- Monitor system health, performance, and security; respond to incidents
- Implement and maintain containerization and orchestration (Docker, Kubernetes)
- Automate operational tasks and reduce manual intervention
- Ensure disaster recovery plans and backup strategies are in place
- Collaborate with Security Lead on compliance and vulnerability management

### Goals
- Achieve high deployment frequency with low change failure rate
- Minimize mean time to recovery (MTTR) for incidents
- Maintain 99.9%+ uptime for production systems
- Reduce operational toil through automation

### Typical Communication
- Incident reports and postmortems
- Infrastructure change proposals and runbooks
- Performance and monitoring dashboards
- On-call rotation schedules and escalation procedures

### Interactions with Other Roles
- **Developers**: Provide CI/CD support; troubleshoot build and deployment issues; collaborate on performance optimization
- **Project Managers**: Communicate deployment schedules and infrastructure constraints; report on reliability metrics
- **Security Lead**: Implement security controls; coordinate vulnerability remediation; manage secrets and access controls
- **Support/Customer Success**: Provide incident status updates; investigate production issues reported by customers

---

## Support/Customer Success Representative

### Role Summary
Support/Customer Success Representatives serve as the primary point of contact between customers and the product team. They resolve customer issues, gather product feedback, and ensure customers achieve their desired outcomes with the product.

### Responsibilities
- Respond to customer inquiries via email, chat, or ticketing systems
- Troubleshoot and resolve technical issues or escalate to Engineering
- Document common issues and maintain knowledge base articles
- Gather and relay customer feedback to Product and Engineering teams
- Track customer health metrics and identify at-risk accounts
- Conduct onboarding and training sessions for new customers
- Advocate for customer needs in product planning discussions

### Goals
- Maintain high customer satisfaction (CSAT) and Net Promoter Scores (NPS)
- Reduce average resolution time for support tickets
- Increase product adoption and feature utilization
- Proactively identify and prevent customer churn

### Typical Communication
- Support ticket responses and resolution summaries
- Weekly customer feedback reports to Product and Engineering
- Escalation emails for critical bugs or feature requests
- Customer onboarding materials and training documentation

### Interactions with Other Roles
- **Product Managers**: Share customer feedback and feature requests; validate that new features solve customer problems
- **Developers**: Escalate bugs with reproduction steps; request clarification on product behavior
- **UX Designer**: Report usability issues and confusion points from customer interactions
- **DevOps Engineer**: Coordinate on incident communication; understand system status during outages

---

## Security Lead

### Role Summary
Security Leads ensure that products are designed, built, and operated with security best practices. They identify vulnerabilities, define security requirements, and work across teams to implement controls that protect customer data and company assets.

### Responsibilities
- Conduct threat modeling and security reviews for new features
- Perform or coordinate security testing (SAST, DAST, penetration testing)
- Define and enforce security policies and compliance requirements
- Respond to security incidents and coordinate remediation efforts
- Manage vulnerability disclosure and patching processes
- Provide security training and guidance to development teams
- Monitor for security threats and maintain security tooling

### Goals
- Minimize security vulnerabilities in production systems
- Ensure compliance with relevant standards (SOC 2, GDPR, etc.)
- Reduce mean time to remediate (MTTR) for security issues
- Foster a security-aware culture across the organization

### Typical Communication
- Security review reports and threat models
- Vulnerability assessments and remediation plans
- Security incident postmortems
- Security training materials and best practice guides

### Interactions with Other Roles
- **Developers**: Review code for security issues; provide guidance on secure coding practices; approve security-sensitive changes
- **DevOps Engineer**: Collaborate on infrastructure security; manage access controls and secrets; implement security monitoring
- **Product Managers**: Advise on security implications of feature decisions; help prioritize security work
- **Project Managers**: Report on security posture; communicate compliance timelines and security project status

---

## How these personas are used in the exercise
- Use these persona definitions to frame scenarios and sample interactions in the Skills Exercise.
- Each persona can be used as a persona prompt for Copilot Spaces to shape role-specific guidance.

