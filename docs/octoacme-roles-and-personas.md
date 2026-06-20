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

## How these personas are used in the exercise
- Use these persona definitions to frame scenarios and sample interactions in the Skills Exercise.
- Each persona can be used as a persona prompt for Copilot Spaces to shape role-specific guidance.

---

## Proposed Additions — Additional Personas & Roles (recommended)

To close ownership gaps for cross-cutting activities (releases, observability, docs, security, coordination), consider adding the following personas. For each persona below we include a short responsibilities list and how they typically interact with existing roles.

1. Release Manager
- Responsibilities
  - Owns release coordination and gating (schedules, approvals, rollback plans, release notes).
  - Validates that release criteria are met (CI, security scans, acceptance tests).
  - Coordinates deployment windows and cross-team readiness.
- Interactions
  - PM / PdM: aligns on release scope and timing.
  - Developers: checks PR readiness and deployment artifacts.
  - QA Lead: confirms acceptance and smoke test completion.
  - Support / On-call: communicates post-release monitoring expectations.
- Example decision point
  - Approves/releases only when release checklist items (tests, rollbacks, monitoring) are completed.

2. Delivery Lead
- Responsibilities
  - Focuses on day-to-day delivery execution for a release or program.
  - Removes blockers, manages cross-team dependencies, and tracks delivery progress.
  - Maintains short-term delivery plan and ensures sprint objectives are met.
- Interactions
  - PM/PdM: communicates status and re-prioritizes work as needed.
  - Developers and QA: facilitates handoffs and mitigations for blockers.
  - Stakeholders: provides frequent status updates and escalation.
- Example decision point
  - Reassigns or escalates tasks when a dependency threatens a milestone.

3. QA Lead / Test Coordinator
- Responsibilities
  - Owns test strategy, test planning, and verification for releases.
  - Ensures test coverage, defines acceptance test suites, and coordinates manual/automation effort.
  - Manages test environments and release gating criteria related to quality.
- Interactions
  - Developers: ensures code is testable and coordinates on test fixes.
  - Release Manager: signals gating (pass/fail) for releases.
  - PM: confirms acceptance criteria and risk areas.
- Example decision point
  - Declares that a release cannot proceed due to critical test failures.

4. Technical Writer / Documentation Owner
- Responsibilities
  - Produces and maintains user-facing documentation, runbooks, and release notes.
  - Ensures docs are updated as features change, and that migration/upgrade notes are clear.
- Interactions
  - PdM: gathers requirements for user-facing content.
  - Developers: obtains implementation details and API changes.
  - Support: collects common customer questions to improve docs.
- Example decision point
  - Signs off on publishable release notes and user-facing how-to guides.

5. Observability Engineer (or Monitoring Owner)
- Responsibilities
  - Ensures metrics, dashboards, alerts, and SLOs are defined and implemented for new features.
  - Validates that monitoring and logging are adequate for production support and incident response.
- Interactions
  - Developers: specifies instrumentation and logging requirements.
  - PM: aligns on SLOs and KPIs.
  - On-call/Support: tunes alerts and runbooks to reduce noise.
- Example decision point
  - Requires added telemetry before a feature goes to production to meet SLAs.

6. Security Liaison
- Responsibilities
  - Coordinates security reviews, threat modeling, and vulnerability remediation.
  - Ensures compliance with security policies and coordinates with central Security team.
- Interactions
  - Developers: helps prioritize and verify fixes for findings.
  - PM: informs risk decisions and release gating when security impacts exist.
  - Security team: sequences scans and remediation.
- Example decision point
  - Holds a release if a high-severity vulnerability is discovered and unresolved.

7. Product Ops (optional)
- Responsibilities
  - Bridges product, data, and operations to run experiments, manage feature flags, and analyze feature adoption.
  - Manages release toggles and rollout strategies (canary, feature-flag rollouts).
- Interactions
  - PdM: sets rollout strategy.
  - Developers: implements feature-flag controls.
  - Analytics/Observability: tracks adoption and experiments.
- Example decision point
  - Approves a canary rollout or a broader rollout based on metric signals.

8. UX Researcher / Designer (if not already specified)
- Responsibilities
  - Owns user research, usability studies, and design validation.
  - Ensures designs are validated before significant investment and that accessibility standards are met.
- Interactions
  - PdM: aligns on user goals and measurement.
  - Developers: hands off design assets and accessibility requirements.
  - QA: coordinates on accessibility and usability verification.
- Example decision point
  - Requires additional usability testing before user-visible changes are released.

---

## How to adopt these additions
- Add short responsibility paragraphs for each persona in this document (as above).
- Add an "Interactions" matrix mapping new roles to existing roles (PM, PdM, Developers, QA, Stakeholders).
- For immediate clarity, include two short scenarios at the end of this doc showing "Who owns X?" (e.g., "Who approves a release?" "Who owns post-release monitoring?") and map roles to actions.
- Update the issue template default dropdown options (if desired) to include the new persona doc or references.
- Acceptance criteria for the doc update:
  - Each proposed persona has a responsibilities section and interaction notes.
  - Two illustrative scenarios added.
  - PR links the change to issue #1 and lists reviewers.
