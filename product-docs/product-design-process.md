# Product & Design Process

## Overview

This document covers the unified process of defining product features and designing user experiences. For solo founders and small teams, feature definition and design are often the same process - you're figuring out what to build and how users will interact with it.

This process ensures that product and design decisions are based on user needs, validated through research and testing, and iterated based on feedback.

## Core Principles

### Understand Users First

- Start with user research to understand needs, goals, and behaviors
- Use [user research frameworks](user-research-discovery.md) to gather insights
- Build empathy through direct user contact
- Don't assume you know what users need

### Define Problems Before Solutions

- Clearly identify the problem you're solving
- Understand who has this problem and why it matters
- Define success outcomes, not just features
- Validate that the problem is worth solving

### Design for Users, Not Yourself

- Design solutions that solve real user problems
- Prioritize user goals over personal preferences
- Test assumptions with users before committing
- Be willing to change based on user feedback

### Validate with Data

- Validate feature assumptions with data before building
- Use user research to understand problems
- Use experiments (A/B tests, prototype tests) to validate solutions
- Don't build based on hunches alone - test first

### Iterate Based on Feedback

- Product and design work is iterative, not one-time
- Test early and often
- Use feedback to improve
- Don't wait for perfection before testing

### Measure Success by User Outcomes

- Success is measured by how well solutions solve user problems
- Focus on user outcomes, not just features or visual appeal
- Use [usability evaluation](../design-docs/usability-evaluation.md) to measure design effectiveness
- Link work to [product metrics](metrics-success-criteria.md)

## Product & Design Process Framework

### Phase 1: Research and Understand

**Goal:** Understand users, their needs, and the problem space

**Activities:**
- Conduct [user research](user-research-discovery.md) (interviews, surveys, observation)
- Understand user goals and pain points
- Identify user personas or segments
- Map user journeys and workflows
- Understand context of use
- Identify problems worth solving

**Outputs:**
- User research findings
- User personas or profiles
- User journey maps
- Problem statements
- Product & Design Brief (see [Product & Design Brief Template](templates/product-design-brief-template.md))

### Phase 2: Define and Ideate

**Goal:** Define the problem clearly and explore solution approaches

**Activities:**
- Synthesize research findings
- Define the problem clearly (who has it, why it matters)
- Define success outcomes (what success looks like)
- Generate multiple solution ideas
- Explore different approaches
- Consider constraints and requirements

**Outputs:**
- Clear problem definition
- Success criteria and metrics
- Solution concepts or ideas
- Initial sketches or wireframes
- Product direction

### Phase 3: Design and Prototype

**Goal:** Create detailed product and design solutions

**Activities:**
- Develop detailed product requirements
- Create prototypes (low-fidelity to high-fidelity)
- Design [information architecture](../design-docs/information-architecture.md)
- Design [interactions](../design-docs/interaction-design.md)
- Consider [accessibility](../dev-docs/accessibility-inclusivity.md) requirements
- Document functional and non-functional requirements

**Outputs:**
- Product requirements documentation
- Design mockups or prototypes
- Design specifications
- [Design system documentation](../design-docs/templates/design-system-documentation-template.md) (if applicable)
- User stories and acceptance criteria

### Phase 4: Test and Validate

**Goal:** Validate solutions with users and data

**Activities:**
- Conduct [usability testing](../design-docs/usability-evaluation.md)
- Run experiments (A/B tests, prototype tests) to validate solutions
- Gather user feedback
- Identify usability issues
- Measure effectiveness
- Compare alternatives

**Outputs:**
- Usability test results
- Experiment results
- User feedback
- Identified issues and priorities
- Validation data

### Phase 5: Iterate and Improve

**Goal:** Refine solutions based on feedback and data

**Activities:**
- Address usability issues
- Refine based on feedback
- Test improvements
- Continue iterating until solutions meet user needs
- Update requirements and designs as you learn

**Outputs:**
- Improved solutions
- Updated prototypes
- Final specifications
- Updated requirements

## Feature Definition

### What is a Feature?

A feature is a capability that delivers value to users and advances product goals. Features should be:
- **User-focused**: Solves a real user problem or creates value
- **Aligned**: Supports product strategy and strategic goals
- **Scoped**: Clearly defined boundaries and outcomes
- **Measurable**: Success criteria and metrics defined upfront using the [SMART goals framework](metrics-success-criteria.md#smart-goals-framework)

### Feature Definition Process

The feature definition process is integrated into the Product & Design Process above. Key steps:

1. **Identify the Problem**: What user need or strategic goal does this address?
2. **Define the Outcome**: What success looks like (not just the feature itself)
3. **Explore Solutions**: Consider multiple approaches before committing
4. **Validate Assumptions**: Validate feature assumptions with data before building. For example, if user research suggests users want a feature, design an experiment (A/B test, prototype test, or small launch) to measure actual impact rather than building the full feature based on research alone
5. **Scope the Feature**: Define what's in and out of scope
6. **Document Requirements**: Capture what needs to be built

**From Hunches to Features:**

Hunches about user needs can inform feature ideas, but validate with data - use user research to understand the problem, then experiments to validate the solution before committing to build.

## Requirements Documentation

### Types of Requirements

**Functional Requirements:**
- What the feature should do
- User interactions and behaviors
- Product rules and logic
- Data handling and validation

**Non-Functional Requirements:**
- Performance expectations
- Security and privacy considerations
- Accessibility requirements
- Scalability and reliability needs

**Design Requirements:**
- User experience expectations
- Visual design guidelines
- Interaction patterns
- Responsive behavior
- Information architecture

### Requirements Best Practices

- **Be Specific**: Avoid vague or ambiguous language
- **Focus on "What" and "Why"**: Leave "how" to implementation teams
- **Include Context**: Explain the problem being solved
- **Define Success**: How will we know this is successful?
- **Validate with Data**: When possible, validate requirements with data - use user research, experiments, or analytics to confirm assumptions before building
- **Document Constraints**: Technical, strategic, or user constraints
- **Keep It Current**: Update requirements as you learn

## User Stories

### User Story Format

User stories follow a simple template:

```
As a [type of user],
I want to [perform an action],
So that [I achieve a benefit].
```

**Example:**
```
As a project manager,
I want to filter tasks by assignee,
So that I can quickly see what each team member is working on.
```

### User Story Components

**User Persona:**
- Who is this for? Be specific about the user type
- Consider different user segments and their needs

**Action:**
- What can the user do? Use clear, action-oriented language
- Focus on user goals, not implementation details

**Benefit:**
- Why does this matter? Connect to user value or product outcome
- Helps prioritize and validate the story's importance

### Acceptance Criteria

Each user story should include acceptance criteria that define "done":

- **Specific**: Clear and unambiguous
- **Testable**: Can be verified as complete
- **User-focused**: Written from user perspective
- **Complete**: Covers happy path and edge cases

**Example:**
```
Given I am on the task list page
When I select a filter option from the "Filter by Assignee" dropdown
Then I see only tasks assigned to that person
And the filter dropdown shows the selected assignee
And I can clear the filter to see all tasks again
```

### User Story Best Practices

- **Keep Stories Small**: One story should be completable in a single sprint
- **Write from User Perspective**: Focus on user value, not technical implementation
- **Include Context**: Link stories to features and strategic goals
- **Define Done**: Clear acceptance criteria prevent ambiguity
- **Prioritize**: Not all stories are equally important

### Story Splitting

When stories are too large, split them:

**By User Flow:**
- Break into steps of a user journey
- Each story represents a complete step

**By User Type:**
- Different stories for different user personas
- Same feature, different user needs

**By Data Variations:**
- Different stories for different data scenarios
- Example: "As a user with no history" vs "As a user with existing data"

**By Platform/Device:**
- Separate stories for web, mobile, desktop
- When platform differences are significant

## Applying the Framework

### For Solo Founders and Small Teams

**Start Simple:**
- You don't need to do all phases for every feature
- Focus on research, design, and testing phases
- Skip formal documentation when you can
- Use lightweight methods (quick user interviews, simple prototypes)

**Prioritize:**
- Research before designing (understand users first)
- Test before building (validate solutions early)
- Iterate based on feedback (don't assume solutions are perfect)

**Practical Approach:**
- Talk to 3-5 users before designing
- Create simple prototypes (sketches, wireframes, or clickable mockups)
- Test with 3-5 users before finalizing
- Run small experiments to validate solutions
- Iterate based on what you learn

### When to Use Each Phase

**Always Do:**
- Research: Understand users before designing
- Testing: Validate solutions with users

**Do When Needed:**
- Ideation: When exploring new solutions or features
- Detailed Design: When you have a clear direction
- Iteration: When solutions don't meet user needs

**Skip When:**
- You're making small, incremental improvements
- You have strong evidence the solution will work
- Time or resources are extremely limited (but still test)

## Integration with Development

### Handoff Process

- Share requirements, user stories, and design specifications with engineering
- Provide context and answer questions
- Collaborate on technical feasibility and trade-offs
- Use [design handoff templates](../design-docs/templates/design-handoff-template.md) for clear communication
- Stay involved during implementation for clarifications

### Collaboration

- Work with engineering on technical constraints and possibilities
- Partner with design on user experience and interaction design (or do both yourself)
- Align with stakeholders on scope and priorities
- Communicate changes and updates as you learn

## Best Practices

- **Start with Users**: Always begin with user research
- **Test Early**: Don't wait for perfect solutions to test
- **Iterate Based on Data**: Use user feedback and data to improve
- **Keep It Simple**: Focus on solving user problems, not complex features
- **Measure Impact**: Track how solutions affect user outcomes
- **Validate Assumptions**: Use experiments to validate, not just research

## Common Pitfalls

**Skipping Research:**
- Designing without understanding users
- Solution: Always do some user research before designing

**Building Based on Hunches:**
- Building features without validating solutions
- Solution: Use experiments to validate solutions before building

**Designing in Isolation:**
- Not testing solutions with users
- Solution: Test solutions early and often

**Ignoring Feedback:**
- Not iterating based on user feedback
- Solution: Be willing to change based on what you learn

**Over-Designing:**
- Creating complex solutions when simple would work
- Solution: Start simple, add complexity only when needed

## Related Topics

- [User Research & Discovery](user-research-discovery.md) - Understanding users
- [Product Strategy & Vision](product-strategy-vision.md) - Aligning with strategy
- [Prioritization Frameworks](prioritization-frameworks.md) - Deciding what to build
- [Information Architecture](../design-docs/information-architecture.md) - Organizing information
- [Interaction Design](../design-docs/interaction-design.md) - Designing interactions
- [Usability Evaluation](../design-docs/usability-evaluation.md) - Testing solutions
- [Accessibility & Inclusivity](../dev-docs/accessibility-inclusivity.md) - Accessibility requirements
- [Templates](templates/) - Product and design templates

