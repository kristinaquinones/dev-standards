# Prioritization Frameworks

## Overview

Prioritization frameworks help product teams make objective decisions about what to build next. This document covers Kano Model, MoSCoW, and Value vs Effort matrix approaches.

## Framework selection

Choose frameworks based on:
- **Decision Type**: Feature prioritization vs. requirement prioritization vs. roadmap planning
- **Stakeholder Context**: Who needs to understand and agree on priorities
- **Data Availability**: What information you have about value and effort
- **Time Horizon**: Short-term tactical vs. long-term strategic decisions

## Kano model

### Overview

The Kano Model categorizes features based on their impact on user satisfaction, helping identify which features will delight users vs. which are expected.

### Feature Categories

**Basic (Must-Have):**
- Expected by users; absence causes dissatisfaction
- Not a differentiator, but required for competitiveness
- Example: Secure login, data backup, basic search

**Performance (Linear):**
- More is better; satisfaction increases with quality/quantity
- Direct correlation between investment and satisfaction
- Example: Page load speed, search accuracy, storage capacity

**Delight (Excitement):**
- Unexpected features that create delight when present
- Not expected, so absence doesn't cause dissatisfaction
- Can become performance or basic over time
- Example: AI-powered recommendations, one-click checkout

**Indifferent:**
- Features users don't care about either way
- Don't invest here

**Reverse:**
- Features that decrease satisfaction
- Avoid these

### Using Kano Model

1. **Identify Features**: List features or requirements to evaluate
2. **Survey Users**: Ask functional (with) and dysfunctional (without) questions
3. **Categorize**: Map features to Kano categories
4. **Prioritize**: Focus on Basic first, then Performance, then Delight
5. **Revisit**: Features evolve; re-categorize as market matures

### Kano Questions

**Functional (with feature):**
"How would you feel if the product had [feature]?"
- Like
- Expect it
- Neutral
- Live with it
- Dislike

**Dysfunctional (without feature):**
"How would you feel if the product did not have [feature]?"
- Like
- Expect it
- Neutral
- Live with it
- Dislike

## MoSCoW Prioritization

### Overview

MoSCoW categorizes requirements into four priority levels, useful for scoping work within time or resource constraints.

### Categories

**Must Have (M):**
- Critical requirements; product fails without them
- Non-negotiable for the release
- Typically 60% of requirements

**Should Have (S):**
- Important but not critical
- Significant value if included
- Can be deferred if necessary
- Typically 20% of requirements

**Could Have (C):**
- Nice to have; lower priority
- Included if time/resources allow
- Can be moved to future releases
- Typically 20% of requirements

**Won't Have (W):**
- Explicitly out of scope for this release
- May be considered for future work
- Prevents scope creep

### Using MoSCoW

1. **List Requirements**: All potential requirements for the release
2. **Categorize**: Assign M, S, C, or W to each
3. **Validate Distribution**: Ensure realistic split (typically 60/20/20)
4. **Negotiate**: If too many Must Haves, re-evaluate or adjust scope
5. **Communicate**: Clearly document what's in each category

### MoSCoW Best Practices

- **Be Realistic**: Not everything can be Must Have
- **Involve Stakeholders**: Get input from users, stakeholders, and technical teams
- **Revisit Regularly**: Priorities change as you learn
- **Document Rationale**: Explain why items are in each category

## Value vs Effort Matrix

### Overview

The Value vs Effort matrix helps prioritize work by comparing expected value against required effort, identifying quick wins and strategic investments.

### Quadrants

**Quick Wins (High Value, Low Effort):**
- High impact, easy to implement
- Prioritize these first
- Build momentum and demonstrate value
- Example: Fixing critical bugs, removing friction

**Strategic Investments (High Value, High Effort):**
- Significant impact but requires substantial work
- Plan carefully and allocate resources
- May span multiple releases
- Example: Major platform improvements, new product lines

**Fill-Ins (Low Value, Low Effort):**
- Easy to do but limited impact
- Do when you have spare capacity
- Don't prioritize over higher-value work
- Example: Minor UI improvements, nice-to-have features

**Time Sinks (Low Value, High Effort):**
- Avoid these
- High effort with little return
- Reconsider or significantly reduce scope
- Example: Over-engineered solutions, features nobody uses

### Using Value vs Effort Matrix

1. **List Initiatives**: Features, improvements, or projects to evaluate
2. **Estimate Value**: Consider user value, product impact, strategic alignment
3. **Estimate Effort**: Consider development time, complexity, dependencies
4. **Plot on Matrix**: Place each item in the appropriate quadrant
5. **Prioritize**: Quick Wins → Strategic Investments → Fill-Ins (avoid Time Sinks)
6. **Validate**: Get input from team on estimates
7. **Revisit**: Update as you learn more about value and effort

### Estimating Value

Consider:
- User impact and satisfaction
- Outcome metrics (revenue, retention, acquisition)
- Strategic alignment
- Competitive advantage
- Risk mitigation

**Data-Driven Value Estimation:**

Value estimates should be based on data (user research, analytics, experiments) rather than assumptions. Instead of assuming a feature is high-value, use user research to understand demand, then run a small experiment to measure actual impact.

### Estimating Effort

Consider:
- Development complexity
- Time required
- Resource availability
- Technical dependencies
- Design and research needs

## Combining frameworks

### When to Use Multiple Frameworks

- **Kano + Value vs Effort**: Understand user satisfaction AND resource requirements
- **MoSCoW + Value vs Effort**: Scope a release AND prioritize within that scope
- **All Three**: Comprehensive prioritization for major planning

### Framework Limitations

- **Kano**: Requires user research; categories can shift over time
- **MoSCoW**: Can be subjective; "Must Have" can expand without discipline
- **Value vs Effort**: Estimates can be inaccurate; value may be hard to quantify

**Reducing Subjectivity:**

Subjectivity in prioritization frameworks can be reduced by using data to inform estimates. Base value and effort estimates on user research, analytics, and experiments rather than intuition or assumptions.

## Best practices

- **Use Data**: Base prioritization on data, research, and evidence - not hunches, opinions, or 'feeling' something is right. Hunches can generate hypotheses (e.g., 'I think users want feature X'), but validate with user research and experiments before prioritizing
- **Validate Prioritization Decisions**: Validate prioritization decisions with data - use experiments, user research, and analytics to confirm value estimates. Example: If you think feature A is more valuable than feature B, design an experiment to test both and measure actual user behavior
- **Involve Stakeholders**: Get input from users, stakeholders, and technical teams
- **Be Transparent**: Share prioritization rationale with the team
- **Revisit Regularly**: Priorities change as context and learning evolve
- **Balance**: Mix quick wins with strategic investments
- **Say No**: Use frameworks to gracefully decline lower-priority requests

## Related topics

- [Product Strategy & Vision](product-strategy-vision.md) - Strategic context for prioritization
- [Roadmap Planning](roadmap-planning.md) - Using prioritization to build roadmaps
- [Product & Design Process](product-design-process.md) - Prioritizing features and requirements
- [Stakeholder Management](stakeholder-management.md) - Communicating priorities to stakeholders

