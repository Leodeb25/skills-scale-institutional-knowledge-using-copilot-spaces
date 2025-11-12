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
UX Designers create intuitive, user-centered experiences by conducting research, designing interfaces, and validating solutions with users. They collaborate closely with Product Managers and Developers to ensure features are both valuable and usable.

### Responsibilities
- Conduct user research and usability testing
- Create wireframes, prototypes, and high-fidelity designs
- Define interaction patterns and information architecture
- Collaborate with developers to ensure design implementation fidelity
- Maintain design system components and guidelines
- Advocate for accessibility and inclusive design practices

### Goals
- Deliver intuitive, accessible user experiences
- Reduce user friction and increase task completion rates
- Ensure consistency across product touchpoints
- Balance user needs with technical and business constraints

### Typical Collaboration Points
- **With Product Managers**: Align on user needs, feature priorities, and success metrics
- **With Developers**: Review design feasibility, provide implementation guidance, and validate UI/UX in code reviews
- **With QA Automation Engineers**: Define acceptance criteria for UI/UX quality and collaborate on automated visual regression tests
- **With Support Lead**: Gather user feedback and pain points to inform design improvements

---

## Tech Lead

### Role Summary
Tech Leads provide technical leadership and architectural guidance for the engineering team. They ensure code quality, scalability, and maintainability while mentoring developers and making key technical decisions.

### Responsibilities
- Define technical architecture and design patterns
- Review critical code changes and technical designs
- Mentor developers on best practices and code quality
- Evaluate and recommend technologies, tools, and frameworks
- Identify and mitigate technical risks and debt
- Facilitate technical discussions and decision-making
- Ensure engineering standards and practices are followed

### Goals
- Maintain high code quality and system reliability
- Enable team velocity through solid architecture
- Foster technical growth and knowledge sharing
- Balance technical excellence with delivery timelines

### Typical Collaboration Points
- **With Developers**: Provide code review, architectural guidance, and mentorship
- **With Product Managers**: Translate business requirements into technical solutions and provide feasibility estimates
- **With Project Managers**: Identify technical dependencies, risks, and realistic timelines
- **With QA Automation Engineers**: Define testing strategies and review test architecture

---

## QA Automation Engineer

### Role Summary
QA Automation Engineers design and implement automated testing strategies to ensure product quality and reliability. They create test frameworks, maintain test suites, and collaborate with developers to catch issues early in the development cycle.

### Responsibilities
- Design and maintain automated test frameworks and infrastructure
- Write automated tests (unit, integration, end-to-end, performance)
- Implement CI/CD testing pipelines and quality gates
- Collaborate with developers on testability and test coverage
- Identify and report bugs with clear reproduction steps
- Monitor test results and investigate flaky or failing tests
- Advocate for quality best practices and shift-left testing

### Goals
- Maximize test coverage and reduce manual testing effort
- Catch defects early in the development lifecycle
- Enable fast, confident deployments through reliable automation
- Improve overall product quality and stability

### Typical Collaboration Points
- **With Developers**: Review code for testability, pair on test implementation, and debug test failures
- **With Tech Lead**: Align on testing strategy, test architecture, and quality standards
- **With UX Designer**: Define acceptance criteria for UI/UX testing and implement automated visual tests
- **With Project Managers**: Report on quality metrics, test coverage, and readiness for release

---

## Support Lead

### Role Summary
Support Leads manage customer support operations and serve as the voice of the customer within the organization. They triage issues, coordinate resolution efforts, and provide insights to improve product quality and user experience.

### Responsibilities
- Manage support ticket queue and escalation process
- Triage and prioritize customer issues
- Coordinate with engineering on bug fixes and workarounds
- Document known issues and resolution procedures
- Analyze support trends to identify product improvement opportunities
- Provide customer feedback to Product and UX teams
- Create and maintain customer-facing documentation and knowledge base

### Goals
- Minimize customer issue resolution time
- Improve customer satisfaction and retention
- Reduce support ticket volume through product improvements
- Ensure clear communication between customers and product teams

### Typical Collaboration Points
- **With Product Managers**: Share customer feedback, pain points, and feature requests to inform roadmap
- **With Developers**: Report bugs with reproduction steps and collaborate on troubleshooting
- **With UX Designer**: Provide insights on usability issues and user confusion patterns
- **With Project Managers**: Coordinate on release communications and support readiness

---

## Collaboration Scenarios

### Scenario 1: Planning Phase - Tech Lead and QA Automation Engineer Align on Testing Strategy

**Context**: During sprint planning for a new payment processing feature.

**Interaction**:
1. **Tech Lead** reviews the feature architecture with the team and identifies critical paths that need thorough testing (e.g., payment validation, transaction rollback, error handling).
2. **QA Automation Engineer** proposes a testing approach:
   - Unit tests for payment validation logic (Developer-owned)
   - Integration tests for payment gateway interactions (QA-owned)
   - End-to-end tests for complete checkout flow (QA-owned)
   - Performance tests for concurrent transactions (QA-owned)
3. **Tech Lead** and **QA Automation Engineer** discuss testability requirements:
   - Tech Lead ensures the payment service exposes test-friendly interfaces
   - QA Engineer sets up test data fixtures and mock payment gateway
4. **Tech Lead** commits to code review requirements: all payment-related PRs must include tests and pass QA's automated suite.
5. **Project Manager** adds "QA test automation setup" as a dependency in the project plan with estimated effort from QA Engineer.

**Outcome**: Clear testing strategy documented, test automation work included in sprint planning, and quality gates defined before feature completion.

### Scenario 2: Delivery Phase - UX Designer, Support Lead, and Product Manager Collaborate on Release Readiness

**Context**: Final week before launching a redesigned user dashboard.

**Interaction**:
1. **UX Designer** completes final design QA in staging environment and reports minor UI inconsistencies to developers via annotated screenshots.
2. **Support Lead** raises concern: "We're seeing confusion in beta user feedback about the new navigation. Do we have updated help docs?"
3. **Product Manager** facilitates alignment meeting:
   - UX Designer walks through the new navigation structure and shares design rationale
   - Support Lead provides specific user confusion examples from beta feedback
   - Team decides on two quick fixes:
     - UX Designer adds tooltips for key navigation items
     - Support Lead drafts FAQ and updates help center articles
4. **Product Manager** adjusts release timeline by 2 days to accommodate changes and support documentation.
5. **Support Lead** creates internal training materials for support team based on UX Designer's walkthrough.
6. **Project Manager** updates deployment checklist to include "Support team training completed" as pre-release gate.

**Outcome**: Release is delayed slightly but launches with better UX and support readiness, reducing potential post-launch support burden.

---

## Role Onboarding Checklist

This section helps new team members quickly understand their role and ramp up effectively. Each role owner should complete the relevant checklist during their first 1-2 weeks.

### General Onboarding (All Roles)
- [ ] Review OctoAcme project management overview and principles
- [ ] Understand the project lifecycle (initiation → planning → execution → release → retrospective)
- [ ] Meet with Project Manager to understand current projects and priorities
- [ ] Get access to project boards, repositories, and communication channels
- [ ] Review recent retrospective notes to understand team learnings

### Developer Onboarding
- [ ] Complete development environment setup
- [ ] Review coding standards and PR review process
- [ ] Shadow a senior developer on code review
- [ ] Complete first code contribution (small bug fix or documentation update)
- [ ] Attend sprint planning and daily standup

### Product Manager Onboarding
- [ ] Review product roadmap and current priorities
- [ ] Meet with key stakeholders and understand their needs
- [ ] Review success metrics and how they are measured
- [ ] Shadow customer research session or review recent user feedback
- [ ] Participate in backlog grooming with development team

### Project Manager Onboarding
- [ ] Review active project charters and timelines
- [ ] Understand risk management process and current risk register
- [ ] Meet with stakeholders to understand communication preferences
- [ ] Review project tracking tools and reporting templates
- [ ] Facilitate first team meeting (standup or weekly sync)

### UX Designer Onboarding
- [ ] Review design system and component library
- [ ] Understand design tool access and file organization
- [ ] Meet with Product Manager to understand user personas and use cases
- [ ] Review recent user research findings and usability test results
- [ ] Shadow or conduct first usability testing session
- [ ] Collaborate with a developer on design implementation review

### Tech Lead Onboarding
- [ ] Review system architecture documentation
- [ ] Understand tech stack, frameworks, and architectural decisions
- [ ] Review recent technical design documents and ADRs (Architecture Decision Records)
- [ ] Meet with developers to understand current technical challenges
- [ ] Conduct first architecture review or code review session
- [ ] Identify technical debt and discuss prioritization with Product Manager

### QA Automation Engineer Onboarding
- [ ] Set up test automation environment and tools
- [ ] Review existing test frameworks and test suite structure
- [ ] Understand CI/CD pipeline and quality gates
- [ ] Review test coverage reports and identify gaps
- [ ] Shadow manual QA session to understand test scenarios
- [ ] Write first automated test and integrate with CI pipeline
- [ ] Review bug reporting process and collaborate with developer on bug triage

### Support Lead Onboarding
- [ ] Get access to support ticketing system and customer communication channels
- [ ] Review support documentation, FAQs, and knowledge base
- [ ] Shadow experienced support team member on ticket resolution
- [ ] Understand escalation process and SLA expectations
- [ ] Meet with Product and UX teams to understand product roadmap
- [ ] Review common customer issues and known bugs
- [ ] Conduct first customer interaction and document resolution

---

## How these personas are used in the exercise
- Use these persona definitions to frame scenarios and sample interactions in the Skills Exercise.
- Each persona can be used as a persona prompt for Copilot Spaces to shape role-specific guidance.
- Reference specific roles in project documentation (see [octoacme-project-initiation.md](octoacme-project-initiation.md), [octoacme-project-planning.md](octoacme-project-planning.md), and [octoacme-execution-and-tracking.md](octoacme-execution-and-tracking.md)) to clarify responsibilities throughout the project lifecycle.

