# OctoAcme — Execution & Tracking

## Purpose
Guidance for managing day-to-day execution and tracking progress toward project milestones.

## Team Rhythm
- Daily standups (15 min) — focus on progress, blockers, dependencies
- Weekly delivery sync — show progress, updates, and flagged risks
- Demo/Review at the end of each sprint or milestone

## Workflows
- Use the project board (e.g., GitHub Projects) with columns: Backlog, Ready, In Progress, In Review, QA, Done
- Pull Request workflow:
  - Small PRs (<= 400 lines when possible)
  - Include issue link and acceptance criteria in PR description
  - Run automated tests and linting in CI before requesting review
  - Require at least one approval before merging (or team-defined policy)

## Quality & Testing
- Unit tests for new logic (Developer-owned)
- Integration tests where applicable (QA Automation Engineer-owned)
- End-to-end smoke tests for critical flows before release (QA Automation Engineer-owned)
- Security scanning in CI
- Manual QA for feature acceptance when needed
- UI/UX quality review by UX Designer
- Performance and load testing as defined with Tech Lead
- Automated test suite maintained and expanded by QA Automation Engineer

For testing strategy and responsibilities, see [roles-and-personas.md](octoacme-roles-and-personas.md).

## Reporting & Metrics
- Track velocity and burndown
- Monitor success metrics identified in the Project One-pager
- Use dashboards for key signals (errors, latency, usage)

## Blocker Escalation
- Level 1: Team-level triage in daily standup
- Level 2: PM escalates to Product Lead and dependent teams
- Level 3: Sponsor-level escalation for business-impacting issues

## Execution Checklist
- [ ] Branching and PR conventions documented in repo
- [ ] CI configured for tests and lint
- [ ] Regular demos scheduled
- [ ] Risk register updated weekly
- [ ] Quality gates defined and automated with QA Automation Engineer
- [ ] Design reviews scheduled with UX Designer for UI changes
- [ ] Tech Lead reviews architectural/technical changes
- [ ] Support Lead briefed on customer-impacting features
- [ ] All role owners actively participating in standups and reviews (see [roles-and-personas.md](octoacme-roles-and-personas.md))
