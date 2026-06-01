# User stories

## Overview

User stories are short, simple descriptions of a feature or capability told from the perspective of the person who needs it. They help teams stay focused on user value rather than technical implementation, and serve as the primary unit of work for defining what to build.

This document covers how to write, structure, split, and manage user stories as part of the [Product & Design Process](product-design-process.md).

## Core format

User stories follow a simple three-part template:

```
As a [type of user],
I want to [perform an action],
So that [I achieve a benefit].
```

Each part serves a specific purpose:

| Part | Purpose | Example |
|------|---------|---------|
| As a [user] | Identifies who benefits | As a project manager |
| I want to [action] | Describes the desired capability | I want to filter tasks by assignee |
| So that [benefit] | Explains the value or outcome | So that I can quickly see what each team member is working on |

**Full example:**
```
As a project manager,
I want to filter tasks by assignee,
So that I can quickly see what each team member is working on.
```

See the [User Story Template](templates/user-story-template.md) for a reusable format.

## Story components

### User persona

Be specific about who the user is:

- Reference a defined user segment or persona when available
- Avoid vague terms like "a user" or "an admin" — add context: "a first-time user," "a team admin with 10+ members"
- Different user types may need separate stories even for the same feature

### Action

Describe what the user wants to do:

- Use clear, action-oriented language: "filter," "export," "schedule," "view"
- Focus on the user's goal, not the technical implementation
- Avoid implementation details: say "save my progress" not "trigger an autosave API call"

### Benefit

Explain why the action matters:

- Connect to a user outcome or product goal
- Helps with prioritization — stories with unclear benefits are hard to justify
- Can surface misaligned assumptions before work begins

## Acceptance criteria

Every user story should include acceptance criteria that define what "done" means. Good acceptance criteria are:

- **Specific**: Clear and unambiguous
- **Testable**: Can be verified as complete or not
- **User-focused**: Written from the user's perspective
- **Complete**: Cover the happy path and relevant edge cases

### Checklist format

```
- [ ] Criteria 1
- [ ] Criteria 2
- [ ] Criteria 3
```

**Example:**
```
- [ ] Filter dropdown appears in the task list header
- [ ] User can select one assignee at a time to filter by
- [ ] Filtered list shows only tasks assigned to the selected person
- [ ] Filter selection persists if the user navigates away and returns
- [ ] User can clear the filter to see all tasks again
```

### Given/When/Then format (optional)

For more complex stories, use structured scenarios:

```
Given [a context or starting condition]
When [an action is taken]
Then [the expected result]
```

**Example:**
```
Given I am on the task list page
When I select an assignee from the "Filter by Assignee" dropdown
Then I see only tasks assigned to that person
And the dropdown displays the selected assignee name
And I can clear the filter to see all tasks again
```

Use this format when stories have multiple flows or conditional behavior.

## Story sizing and splitting

### Keep stories small

A user story should be completable within a single sprint. If a story is too large:

- It becomes hard to estimate
- Progress is opaque until the very end
- Scope creep risk increases

### Story splitting patterns

When a story is too large, split it using one of these patterns:

**By user flow:**
Split a multi-step journey into individual steps. Each story represents a complete, deliverable step.
```
Original: "As a user, I want to complete checkout, so that I can purchase items."
Split:
  - "As a user, I want to review my cart before purchasing, so that I can confirm my order."
  - "As a user, I want to enter my payment details, so that I can complete my purchase."
  - "As a user, I want to receive a confirmation email, so that I know my order was placed."
```

**By user type:**
Different personas with different needs get separate stories, even for the same feature.
```
  - "As a guest user, I want to check out without an account, so that I can buy quickly."
  - "As a registered user, I want my saved address to pre-fill at checkout, so that I can save time."
```

**By data variation:**
Write separate stories when behavior differs based on the user's data or state.
```
  - "As a user with no purchase history, I want to see popular products, so that I can discover items to buy."
  - "As a returning user, I want to see personalized recommendations, so that I can find items relevant to me."
```

**By platform or device:**
Separate stories for web, mobile, or desktop when platform differences are significant enough to warrant distinct work.

**By functional slice:**
Deliver a minimal version first, then enhance.
```
  - "As a user, I want to filter tasks by a single assignee, so that I can narrow my view."
  - "As a user, I want to filter tasks by multiple assignees at once, so that I can see work across a subset of the team."
```

## Prioritization

Not all stories are equally important. Consider:

- **User impact**: How many users benefit and how significantly?
- **Strategic alignment**: Does this story support current product goals?
- **Effort**: How much work is required relative to the value delivered?
- **Dependencies**: Does this story block or enable other work?

Use a [prioritization framework](prioritization-frameworks.md) (Kano, MoSCoW, or Value vs Effort) to compare stories objectively.

## Validation before building

User stories based on assumptions should be validated before committing to build:

1. **Validate the problem**: Use [user research](user-research-discovery.md) to confirm the problem is real and significant
2. **Validate the solution**: Run a small experiment (prototype test, A/B test, or limited launch) to confirm the story delivers the expected benefit
3. **Update or discard**: If validation reveals the story doesn't solve the right problem, update or remove it — don't build based on invalidated assumptions

## Managing stories

### Story states

Track stories through a clear lifecycle:

| State | Meaning |
|-------|---------|
| Backlog | Identified but not yet prioritized or refined |
| Refined | Well-written, sized, and ready for sprint planning |
| In progress | Actively being worked on |
| In review | Complete; awaiting review or QA |
| Done | Meets all acceptance criteria; shipped or released |

### Story relationships

Stories often relate to one another:

- **Epics**: Group related stories under a larger feature or theme
- **Dependencies**: Note when one story must be completed before another can begin
- **Conflicts**: Flag when two stories make competing assumptions

## Best practices

- **Write from the user's perspective**: Focus on what users need, not what's technically interesting
- **One story, one need**: Avoid compound stories with "and" in the action ("I want to filter *and* sort")
- **Include context**: Link stories to the feature, goal, or initiative they support
- **Define done upfront**: Write acceptance criteria before starting work, not after
- **Revisit regularly**: Stories in the backlog can become stale — review and update them as you learn
- **Collaborate**: Stories are best written with input from design, engineering, and users — not in isolation

## Common pitfalls

**Vague user types:**
"As a user" tells you nothing. Be specific about who and why.

**Missing benefits:**
"I want to export data" — why? What does the user do with the export? The benefit clarifies priority and success criteria.

**Solution-first stories:**
"As a user, I want a dropdown filter" describes implementation. Write "I want to narrow results by category" and let design and engineering decide the interface.

**Too large to ship:**
If a story can't be completed in a sprint, split it. Large stories hide progress and increase risk.

**No acceptance criteria:**
Without defined acceptance criteria, "done" is subjective and leads to rework.

## Related topics

- [Product & Design Process](product-design-process.md) - Where user stories fit in the product workflow
- [User Research & Discovery](user-research-discovery.md) - Validating the problems behind user stories
- [Prioritization Frameworks](prioritization-frameworks.md) - Deciding which stories to build first
- [Metrics & Success Criteria](metrics-success-criteria.md) - Linking stories to measurable outcomes
- [Templates](templates/) - Reusable templates
  - [User Story Template](templates/user-story-template.md)
  - [Product & Design Brief Template](templates/product-design-brief-template.md)
