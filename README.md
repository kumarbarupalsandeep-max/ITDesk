# ITDesk — IT Help Desk & Service Management Research

> **Research status:** Initial research brief v1.0 — foundation for deeper competitor, UX, technical, and validation research. Product recommendations below are original proposals, not claims about an already-built product.

**Owner / Content Creator:** Sandeep Barupal  
**Copyright:** © 2026 Sandeep Barupal. All rights reserved, except third-party frameworks and resources explicitly identified and linked in the references.  
**Last reviewed:** 2026-10-30

## 1. Executive summary

An employee-facing service desk and agent workspace for incidents, service requests, knowledge, approvals, SLAs, assets, and service reporting.

## 2. Problem and opportunity

IT support becomes difficult to scale when requests arrive through scattered channels, ownership is unclear, and service levels cannot be measured consistently.

## 3. Target users

- Employees/requesters
- Service desk agents
- IT specialists and resolver groups
- Service owners and managers
- IT administrators

## 4. Proposed feature scope

- Request portal with categorized forms, attachments, status tracking, and requester updates.
- Incident records with impact, urgency, priority, assignment, timeline, and related incidents.
- Service request catalog with approval paths and fulfillment tasks.
- SLA calendars, business hours, pause rules, escalation, and breach alerts.
- Knowledge base with search, article ownership, review dates, and feedback.
- Queues, routing rules, team assignment, internal notes, and collision avoidance.
- Problem records, known errors, root-cause notes, and linked incidents.
- Change requests with risk, approvers, implementation plan, rollback plan, and evidence.
- Asset/CI linking, reports, CSAT, and audit logs.

## 5. Proposed page / module map

- Employee portal
- My requests
- Service catalog
- Knowledge base
- Agent queue
- Incident detail
- Request fulfillment
- Problem management
- Change calendar
- Assets and configuration items
- SLA dashboard
- Reports and administration

## 6. Technical architecture direction

- Use a ticket state machine with explicit allowed transitions and immutable activity history.
- Keep SLA calculation separate from UI and test time zones, holidays, pause conditions, and reassignment.
- Notification service should support templates, retries, deduplication, and user preferences.
- Model requester, assignee, group, service, asset, approval, and related-record relationships.

## 7. Security, privacy, and governance

- SSO/MFA, role-based and group-based access, and private internal notes.
- Attachment malware scanning and access-controlled downloads.
- Auditable permission changes, ticket exports, and admin actions.
- Retention policies and privacy controls for employee data.

## 8. Phased development roadmap

1. Phase 1: portal, tickets, queues, comments, assignment, and email/in-app notifications.
2. Phase 2: SLA engine, service catalog, approvals, and knowledge base.
3. Phase 3: problems, changes, assets, and reporting.
4. Phase 4: self-service automation and AI-assisted triage with agent confirmation.

## 9. Product differentiation hypotheses

1. **Clarity first:** show status, ownership, source of truth, last-updated time, and next action on every important record.
2. **Evidence and traceability:** connect decisions and recommendations to source records, timestamps, and audit history.
3. **Safe defaults:** least privilege, explicit confirmation for high-impact actions, reversible changes where possible, and useful empty/error states.
4. **Integration before duplication:** integrate with specialist systems when they are authoritative; do not silently create competing sources of truth.
5. **Progressive complexity:** provide a useful core workflow for small teams, then expose governance and scale features as needed.

These are hypotheses to validate through user interviews, competitor testing, and prototype usability tests; they are not proven market advantages.

## 10. Research questions to validate

- Which user segment has the most urgent and frequent problem?
- What are the top 3 existing workflows and where do users lose time or context?
- Which integrations are essential for a credible MVP, and which can remain links/imports?
- What data is sensitive, who can access it, and how long must it be retained?
- Which outcomes can be measured reliably without incentivizing harmful behavior?
- What is the smallest end-to-end workflow that delivers value in a real pilot?
- Which differentiators are important to users rather than merely impressive in a feature list?

## 11. MVP acceptance criteria

- A new user can understand the product purpose and reach the primary workflow without documentation.
- Core records have clear owners, statuses, timestamps, and history.
- Search, filters, pagination, empty states, loading states, validation, and error handling are defined.
- Role-based access is enforced server-side, not only hidden in the UI.
- Sensitive actions and integrations are auditable and use least privilege.
- Test coverage includes normal flow, invalid input, permission failures, integration failure, and recovery.
- Documentation clearly separates implemented functionality, planned functionality, and mock/demo data.

## 12. Risks and mitigations

| Risk | Mitigation |
|---|---|
| Building too much before validating demand | Interview target users and prototype one end-to-end workflow first |
| Feature overlap with mature tools | Differentiate by workflow clarity, integration, usability, or underserved segment |
| Incorrect or stale data | Display provenance, sync time, data quality warnings, and reconciliation status |
| Overprivileged integrations | Use least-privilege scopes, secure secrets storage, rotation, and audit logs |
| Misleading AI or analytics | Show evidence, confidence/limitations, and human review controls |
| Copying competitor expression or branding | Use independent naming, design system, wording, and implementation; use public references for learning only |

## 13. Reference sources

The links below are starting points for factual validation and further research. Product descriptions and recommendations in this file are original synthesis; the linked sources remain the property of their respective owners.

- [PeopleCert — ITIL](https://www.peoplecert.org/)
- [Atlassian ITSM guide](https://www.atlassian.com/itsm)
- [Atlassian incident management](https://www.atlassian.com/incident-management)
- [NIST incident response resources](https://csrc.nist.gov/projects/incident-response)

## 14. Next research deliverables

1. Competitor matrix: target segment, primary workflows, pricing model where publicly available, integrations, security posture, strengths, gaps, and source date.
2. UX teardown: onboarding, navigation, main workflow, error handling, accessibility, responsive behavior, and information architecture.
3. Detailed feature specification: user stories, acceptance criteria, permissions, data model, API contracts, and edge cases.
4. Architecture decision record: trade-offs, reliability, observability, security, deployment, backup, and recovery.
5. Validation plan: interview script, prototype tasks, measurable success criteria, and prioritized backlog.

---

**Disclaimer:** This document is research and product-planning material, not legal, financial, security, or compliance advice. Verify source content and applicable requirements before implementation.
