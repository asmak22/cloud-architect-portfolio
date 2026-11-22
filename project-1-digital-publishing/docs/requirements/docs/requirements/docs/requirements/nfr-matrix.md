
# ComixRus – Non-Functional Requirements Matrix

## Purpose

This document defines the non-functional requirements for the ComixRus digital publishing platform.

These requirements establish measurable expectations for performance, scalability, availability, security, reliability and maintainability.

The targets below are initial architectural assumptions for this learning project. They must be validated with business stakeholders.

## NFR Matrix

| ID | Category | Requirement | Proposed Target | Priority |
|---|---|---|---|---|
| NFR-01 | Performance | Customer-facing pages should load quickly. | 95% of page requests complete within 2 seconds under normal load. | High |
| NFR-02 | Performance | Comic sample content should be delivered efficiently. | Sample content begins loading within 3 seconds under normal conditions. | High |
| NFR-03 | Scalability | Platform must accommodate unpredictable traffic increases. | Support a tenfold increase in normal traffic without manual infrastructure provisioning. | High |
| NFR-04 | Availability | Customer-facing services should remain accessible. | Target 99.9% monthly availability. | High |
| NFR-05 | Security | Data must be protected in transit. | All external connections must use HTTPS with TLS. | High |
| NFR-06 | Security | Sensitive stored information must be protected. | Encrypt customer data and comic files at rest. | High |
| NFR-07 | Security | Users must only access authorised functionality. | Implement role-based access control for customers, writers, editors and administrators. | High |
| NFR-08 | Security | Payment information must be handled securely. | Use Stripe and PayPal hosted/tokenised payment flows; do not store raw card details. | High |
| NFR-09 | Reliability | Purchased comic entitlements must not be lost. | Successful purchases must be recorded durably and recoverably. | High |
| NFR-10 | Reliability | The platform should recover from major service failures. | Initial recovery targets: RTO of 4 hours and RPO of 1 hour. | High |
| NFR-11 | Maintainability | The platform must be manageable by a small technical team. | Infrastructure should be documented and automated where practical. | Medium |
| NFR-12 | Maintainability | Operational problems should be identifiable. | Centralised application logs, monitoring and alerting must be available. | High |
| NFR-13 | Accessibility | The website should be accessible to a broad audience. | Target WCAG 2.2 AA compliance. | High |
| NFR-14 | Cost | The platform should avoid unnecessary infrastructure costs. | Use managed services and scalable infrastructure, with cost monitoring and budget alerts. | Medium |

## Assumptions and Constraints

- Traffic may fluctuate significantly around new comic releases.
- Comic files may be relatively large and require efficient delivery.
- The business has a small technical operations team.
- Third-party payment providers handle sensitive card processing.
- The business requires permanent customer access to purchased comics.
- Initial recovery and performance targets are provisional and require validation.

## Outstanding Questions

- What is the expected number of concurrent visitors?
- What is the anticipated size of an average comic file?
- What is the expected monthly website availability requirement?
- How much data loss, if any, can the business tolerate?
- How quickly must the platform recover after a major outage?
- What is the monthly infrastructure budget?

## Architectural Implications

These NFRs will influence subsequent architectural decisions.

Examples:

- Performance: caching and content delivery.
- Scalability: horizontal scaling and managed services.
- Availability: multi-Availability Zone architecture.
- Security: identity management, encryption and least privilege.
- Reliability: durable storage, backups and recovery processes.
- Maintainability: infrastructure as code, monitoring and automation.
- Cost: consumption-based services and cost controls.

These are potential architectural approaches, not final design decisions.
