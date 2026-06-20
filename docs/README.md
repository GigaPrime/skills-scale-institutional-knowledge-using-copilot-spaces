# OctoAcme Project Management Docs

This README provides an overview of OctoAcme's project management processes and links to detailed process documents in this folder.

## Overview of OctoAcme Project Management Processes

OctoAcme follows a structured, five-phase project lifecycle designed to balance iterative delivery with clear governance. Projects begin with **Initiation**, where a lightweight one-pager validates business need, aligns stakeholders, and confirms go/no-go decisions. Once approved, teams move to **Planning**, where work is broken into shippable increments with prioritized backlogs, dependencies mapped, and milestones defined. The **Execution** phase emphasizes daily standups, small pull requests (≤400 lines), automated CI/CD checks, and regular demos. **Release & Deployment** is tightly controlled with pre-release checklists, smoke tests, and documented rollback plans. Finally, **Retrospectives** capture learnings and convert them into tracked action items, embedding continuous improvement into the culture.

### Core Principles

- **Customer-first**: Prioritize customer value and usability
- **Iterative delivery**: Deliver small, testable increments
- **Clear ownership**: Each project has a named Project Manager (PM) and Product Manager (PdM)
- **Data-informed decisions**: Measure impact and iterate based on evidence
- **Psychological safety**: Encourage feedback and learning

### Key Roles

OctoAcme operates with clear, distributed ownership across four primary personas:

- **Project Managers**: Coordinate schedules, risks, and communications—maintaining risk registers and ensuring transparent status reporting
- **Product Managers**: Own the vision, prioritize the backlog, and measure success metrics through data-driven decisions
- **Developers**: Implement features, write tests, and collaborate on design and technical risk mitigation
- **QA/Testing**: Validate acceptance criteria and quality gates

### Communication & Risk Management

Weekly syncs between PM and Product Manager form the backbone of coordination, supplemented by twice-weekly standups and monthly stakeholder updates. OctoAcme maintains a formal **Risk Register** (ID, Description, Impact, Likelihood, Owner, Mitigation, Status) reviewed at each weekly sync. Risks are escalated through three levels: team-level triage in standups → PM escalation to Product Lead and dependent teams → sponsor-level escalation for business-impacting issues.

### Quality Assurance & Delivery Standards

Quality is embedded throughout execution via unit tests for new logic, integration tests, and end-to-end smoke tests before release. All pull requests require at least one approval and must pass automated CI/CD checks (tests, linting, security scanning). Acceptance criteria are clearly defined during planning, and a formal **Definition of Done** gates what qualifies for release. Pre-release requirements include passing security scans, drafted release notes, and a documented rollback plan.

---

## Process Documents

- **[Project Management Overview](octoacme-project-management-overview.md)** — Introduction to OctoAcme's approach, roles, key artifacts, and lifecycle
- **[Project Initiation Guide](octoacme-project-initiation.md)** — Steps to validate and authorize work, align stakeholders, and create a lightweight plan
- **[Project Planning](octoacme-project-planning.md)** — Turn an approved initiative into an actionable plan and backlog for delivery
- **[Execution & Tracking](octoacme-execution-and-tracking.md)** — Guidance for managing day-to-day execution and tracking progress toward milestones
- **[Risks & Communication](octoacme-risks-and-communication.md)** — How to identify, manage, and communicate risks and dependencies
- **[Release & Deployment](octoacme-release-and-deployment.md)** — Standardized process for releasing features to production with reduced risk
- **[Retrospective & Continuous Improvement](octoacme-retrospective-and-continuous-improvement.md)** — Capture learnings and convert them into actionable improvements
- **[Roles & Personas](octoacme-roles-and-personas.md)** — Detailed definitions of typical roles and responsibilities

---

## Quick Start for New Team Members

1. Start here to understand OctoAcme's core project management principles and team structure
2. Reference the specific process document relevant to your current project phase
3. Use checklists and templates provided in each document to ensure consistency
4. Review the Risk Register and escalation paths in **Risks & Communication** for handling blockers
