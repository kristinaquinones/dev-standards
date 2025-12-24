# Metrics & success criteria

## Overview

Defining success metrics and criteria upfront ensures product work delivers intended outcomes. This document covers how to define, track, and use metrics effectively. For detailed analytics and measurement practices, see [measurement-docs/](../../measurement-docs/).

## Defining success

### Success Criteria

Success criteria define what "done" and "successful" means for product work. Use the **SMART goals framework** to ensure your criteria are well-defined.

### SMART Goals Framework

The SMART framework ensures your success criteria are actionable and measurable:

- **Specific**: Clear and unambiguous
- **Measurable**: Can be quantified or verified
- **Achievable**: Realistic given constraints
- **Relevant**: Aligned with product and strategic goals
- **Time-bound**: When will we evaluate success?

**Why SMART Goals Matter:**
- **Specific**: Vague goals lead to vague results. "Improve engagement" is unclear; "Increase daily active users by 20%" is specific.
- **Measurable**: If you can't measure it, you can't know if you succeeded. Define exactly how you'll measure success.
- **Achievable**: Unrealistic goals demotivate teams and set you up for failure. Set challenging but realistic targets.
- **Relevant**: Goals must connect to your product strategy and user needs, not just arbitrary metrics.
- **Time-bound**: Without a timeframe, there's no urgency or clear evaluation point. "By end of Q2" is better than "eventually."

**Example:**
- ❌ **Not SMART**: "Make onboarding better"
- ✅ **SMART**: "Increase onboarding completion rate from 60% to 75% within 3 months by reducing steps from 5 to 3"

For experiments, SMART goals are especially important - see [A/B Testing & Experimentation](../../measurement-docs/ab-testing-experimentation.md#experiment-design-framework) for how to apply SMART goals to experiment design.

### Types of Success Criteria

**User Outcomes:**
- User satisfaction or engagement
- Task completion rates
- Time to value
- User retention or growth

**Outcome Metrics:**
- Revenue impact
- Cost reduction
- Market share
- Customer acquisition

**Product Outcomes:**
- Feature adoption
- Usage frequency
- Error rates
- Performance improvements

## Metrics framework

### North Star Metric

A North Star Metric is the single metric that best captures the core value your product delivers.

**Characteristics:**
- Reflects user value creation
- Leads to desired outcomes
- Actionable by the product team
- Measurable and trackable

**Examples:**
- Daily active users (social network)
- Number of successful transactions (marketplace)
- Time saved per user (productivity tool)
- Content created per user (content platform)

### Metric Categories

**Leading Indicators:**
- Predict future outcomes
- Early signals of success or failure
- Example: User engagement, feature usage, satisfaction scores

**Lagging Indicators:**
- Reflect past performance
- Confirm whether goals were achieved
- Example: Revenue, retention, churn

**Input Metrics:**
- Activities and efforts
- What the team can directly control
- Example: Features shipped, tests run, research conducted

**Output Metrics:**
- Results and outcomes
- What we're trying to achieve
- Example: User growth, revenue, satisfaction

### Balanced Metrics

Avoid focusing on a single metric. Consider:

- **User Metrics**: Satisfaction, engagement, retention
- **Outcome Metrics**: Revenue, growth, efficiency
- **Quality Metrics**: Errors, performance, reliability
- **Team Metrics**: Velocity, delivery, collaboration

## Metric selection

### Choosing the Right Metrics

**Align with Goals:**
- Metrics should directly connect to product and strategic goals
- Different features may need different metrics
- Avoid vanity metrics that don't drive decisions

**Consider Context:**
- What decisions will this metric inform?
- Who needs to understand this metric?
- How will we act on this information?

**Ensure Measurability:**
- Can we actually measure this?
- Do we have the data infrastructure?
- How accurate and reliable is the data?

### Common Product Metrics

**Engagement:**
- Daily/Weekly/Monthly Active Users (DAU/WAU/MAU)
- Session frequency and duration
- Feature adoption rates
- User actions per session

**Retention:**
- Day 1, 7, 30 retention
- Cohort retention curves
- Churn rate
- Lifetime value

**Satisfaction:**
- Net Promoter Score (NPS)
- Customer Satisfaction (CSAT)
- User ratings and reviews
- Support ticket volume

**Outcome Metrics:**
- Revenue and revenue per user
- Conversion rates
- Customer acquisition cost (CAC)
- Lifetime value (LTV)

## Measurement planning

### Before Launch

1. **Define Success**: What does success look like?
2. **Identify Metrics**: Which metrics will indicate success?
3. **Set Targets**: What are the target values?
4. **Plan Measurement**: How will we collect and analyze data?
5. **Establish Baseline**: What's the current state?

### During Development

- **Track Progress**: Monitor metrics as features are built
- **Validate Assumptions**: Use data to test hypotheses
- **Adjust as Needed**: Pivot if metrics indicate issues

### After Launch

- **Measure Impact**: Compare actual results to targets
- **Analyze Results**: Understand what worked and why
- **Iterate**: Use insights to improve
- **Share Learnings**: Communicate results to stakeholders

## Using metrics

### Decision Making

- **Prioritization**: Use metrics to inform what to build next
- **Scoping**: Adjust scope based on expected impact
- **Trade-offs**: Make informed decisions about compromises

### Communication

- **Stakeholder Updates**: Share progress using metrics
- **Retrospectives**: Review what metrics tell us about outcomes
- **Planning**: Use historical metrics to inform future plans

### Avoiding Pitfalls

- **Vanity Metrics**: Avoid metrics that look good but don't drive decisions
- **Metric Myopia**: Don't optimize one metric at the expense of others
- **Correlation vs. Causation**: Understand what metrics actually indicate
- **Gaming Metrics**: Ensure metrics reflect real value, not manipulation

## Analytics and Measurement

For detailed guidance on:
- Analytics tools and implementation
- Data collection and analysis
- A/B testing and experimentation
- Advanced measurement techniques

See [measurement-docs/](../../measurement-docs/) for comprehensive measurement and analytics standards.

## Related topics

- [Product Strategy & Vision](product-strategy-vision.md) - Connecting metrics to strategic goals
- [Release Planning](release-planning.md) - Defining success for releases
- [Product & Design Process](product-design-process.md) - Including success criteria in feature definition
- [A/B Testing & Experimentation](../../measurement-docs/ab-testing-experimentation.md) - Using SMART goals in experiment design
- [measurement-docs/](../../measurement-docs/) - Detailed analytics and measurement practices

