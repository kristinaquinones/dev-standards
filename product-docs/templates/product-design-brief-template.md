# Product & Design Brief Template

**Feature/Project:** [Feature Name]  
**Date:** [Date]  
**Author:** [Your Name]

## Problem Statement

[What problem are we solving? Who has this problem? Why does it matter?]

## Goals

[What are we trying to achieve? Use SMART goals framework.]

**Primary Goal:**
[Main goal]

**Secondary Goals:**
- [Goal 1]
- [Goal 2]

## Target Users

**Primary Users:**
[Who is this for? Be specific.]

**User Context:**
[When, where, and how will users use this?]

**User Needs:**
- [Need 1]
- [Need 2]
- [Need 3]

## Success Criteria

[How will we measure success?]

**Metrics:**
- [Metric 1]: [Target]
- [Metric 2]: [Target]

**User Outcomes:**
- [Outcome 1]
- [Outcome 2]

**Note:** If this feature is based on a hunch, validate with user research or a small experiment first.

## Research Insights

[What did we learn from user research?]

**Key Insights:**
- [Insight 1]
- [Insight 2]

**User Quotes:**
- [Quote 1]
- [Quote 2]

## Solution

[What are we building? What will users be able to do?]

**Design Direction:**
[What is the proposed design approach?]

**Design Principles:**
- [Principle 1]
- [Principle 2]

**Design Considerations:**
- [Consideration 1]
- [Consideration 2]

## Requirements

### Functional Requirements
- [Requirement 1]
- [Requirement 2]
- [Requirement 3]

### Non-Functional Requirements
- [Performance requirements]
- [Security and privacy considerations]
- [Accessibility requirements - see [Accessibility & Inclusivity](../../dev-docs/accessibility-inclusivity.md)]
- [Scalability and reliability needs]

### Design Requirements
- [User experience expectations]
- [Visual design guidelines]
- [Interaction patterns]
- [Responsive behavior]

## User Stories

**Story 1:**
```
As a [type of user],
I want to [perform an action],
So that [I achieve a benefit].
```

**Acceptance Criteria:**
- [ ] [Criterion 1]
- [ ] [Criterion 2]

[Add more user stories as needed...]

## Out of Scope

[What's explicitly not included?]

## Constraints

**Technical Constraints:**
- [Constraint 1]
- [Constraint 2]

**Design Constraints:**
- [Constraint 1]
- [Constraint 2]

**Time Constraints:**
- [Constraint 1]

**Resource Constraints:**
- [Constraint 1]

## Assumptions & Risks

**Assumptions:**
- [Assumption 1]
- [Assumption 2]

**Risks:**
- [Risk 1 and mitigation]

**Important:** Validate assumptions with data (user research, experiments, analytics) before building. If this came from a hunch, document it as a hypothesis and validate first.

## Related Information

**User Research:**
[Link to user research findings]

**Related Designs:**
[Link to related design work or inspiration]

**Technical Specs:**
[Link to technical requirements]

## Example

**Feature:** Task Filtering

**Problem Statement:** Project managers struggle to find specific tasks in large task lists, making it time-consuming to check on individual work items.

**Goals:**
- Primary: Enable users to quickly filter tasks by assignee
- Secondary: Make filtering intuitive and discoverable

**Target Users:**
- Primary: Project managers managing teams of 5+ people
- Context: Using the product on desktop during work hours

**Success Criteria:**
- 80% of users use filter within 2 weeks
- Time to find a task reduced by 50%
- User satisfaction increases

**Solution:** Add filter dropdown to filter tasks by assignee.

**Design Direction:**
- Add filter dropdown in task list header
- Use familiar dropdown pattern
- Show selected filter clearly
- Make it easy to clear filter

**Requirements:**
- Filter dropdown in task list header
- Filter by single assignee or "All"
- Clear filter button
- Filter state persists during session
- Keyboard accessible
- Screen reader support

**User Story:**
```
As a project manager,
I want to filter tasks by assignee,
So that I can quickly see what each team member is working on.
```

**Acceptance Criteria:**
- [ ] Filter dropdown appears in task list header
- [ ] User can select an assignee to filter by
- [ ] Filtered list shows only tasks for selected assignee
- [ ] User can clear filter to see all tasks
- [ ] Filter is keyboard accessible
- [ ] Screen reader announces filter state

**Out of Scope:**
- Multi-select filtering
- Saved filter presets

**Constraints:**
- Must work with existing navigation
- Should be accessible (keyboard navigation, screen reader support)
- Limited to single-select filtering (this release)

## Related Topics

- [Product & Design Process](../product-design-process.md) - Process framework
- [User Research & Discovery](../user-research-discovery.md) - Understanding users
- [User Story Template](user-story-template.md) - User story format

