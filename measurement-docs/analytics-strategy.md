# Analytics strategy

## Overview

Analytics strategy defines how an organization collects, analyzes, and uses data to make informed product and strategic decisions. A well-defined analytics strategy ensures that data collection is purposeful, metrics are meaningful, and insights drive action.

## Core principles

### Purpose-Driven Data Collection

- **Collect with Intent**: Only collect data that answers specific questions or supports decision-making
- **Avoid Data Hoarding**: More data isn't always better; focus on actionable insights
- **Respect User Privacy**: Balance data needs with privacy expectations and regulations
- **Plan for Analysis**: Design data collection with analysis in mind. You should already be prepared with the **questions** you want to answer before you begin data collection or experiment design.

### Metrics That Matter

- **Outcome-Focused**: Measure what matters, not just activity
- **Actionable**: Metrics should inform decisions, not just report status
- **Balanced**: Consider user metrics, outcome metrics, and quality metrics together
- **Contextual**: Metrics need context to be meaningful; compare against baselines and goals

### Data-Driven Decision Making

- **Evidence Over Opinion**: Hunches and intuition can generate hypotheses, but they must be validated with data through experiments or analysis before making decisions. For example, if you have a hunch that changing a button color will improve clicks, design an A/B test to validate rather than making the change based on intuition alone
- **Statistical Rigor**: Understand the difference between correlation and causation
- **Incrementality**: Use experiments to test hypotheses and understand the true impact of a change or intervention.
- **Action on Insights**: Data is only valuable if it leads to action

**Treating Hunches as Hypotheses:**

Treat hunches as hypotheses to test: User research suggests users want feature X → Form hypothesis 'Feature X will improve retention' → Design experiment to measure impact → Make decision based on data, not the initial hunch.

## Analytics strategy framework

### 1. Define Objectives

**Strategic Objectives:**
- What outcomes are we trying to achieve?
- How will analytics support these outcomes?
- What decisions need data to be made?

**Product Objectives:**
- What product goals align with strategic objectives?
- Which user behaviors indicate success?
- What product questions need answers?

**Analytics Objectives:**
- What data do we need to answer key questions?
- What metrics will indicate progress?
- How will we measure success?

### 2. Identify Key Questions

Before collecting data, identify the questions you need to answer:

- **Strategic Questions**: Long-term direction and priorities
- **Tactical Questions**: Feature-level decisions and optimizations
- **Operational Questions**: Day-to-day monitoring and health checks

**Example Questions:**
- Are users finding value in our product?
- Which features drive retention?
- What's causing users to churn?
- How can we improve conversion rates?
- Is our product performing as expected?

### 3. Design Data Collection

**What to Collect:**
- User actions and behaviors
- Product performance metrics
- Product outcomes
- Contextual data (user attributes, session info, etc.)

**How to Collect:**
- **Event Tracking**: User actions (clicks, views, conversions)
- **Page/Screen Tracking**: Navigation and content consumption
- **User Attributes**: Demographics, segments, preferences
- **Product Metrics**: Performance, errors, technical health
- **Outcome Metrics**: Revenue, subscriptions, transactions

**Collection Best Practices:**
- **Consistent Naming**: Use clear, consistent event and property names
- **Documentation**: Document what each event means and when it fires
- **Validation**: Ensure data quality through testing and validation
- **Privacy Compliance**: Follow privacy regulations and best practices

### 4. Define Metrics

**Metric Categories:**

**User Engagement Metrics:**
- Active users (DAU, WAU, MAU)
- Session frequency and duration
- Feature adoption and usage
- User actions per session

**Retention Metrics:**
- Day 1, 7, 30 retention
- Cohort retention curves
- Churn rate
- Lifetime value

**Product Health Metrics:**
- Error rates
- Performance metrics (load time, response time)
- Feature usage and adoption
- User satisfaction scores

**Outcome Metrics:**
- Revenue and revenue per user
- Conversion rates
- Customer acquisition cost (CAC)
- Lifetime value (LTV)

**Metric Definition Best Practices:**
- **Clear Definitions**: Document exactly what each metric measures
- **Calculation Methods**: Specify how metrics are calculated
- **Data Sources**: Identify where metric data comes from
- **Update Frequency**: Define how often metrics are updated
- **Ownership**: Assign owners responsible for metric accuracy

### 5. Establish Measurement Infrastructure

**Analytics Tools:**
- Choose tools that fit your needs and scale
- Consider integration with existing systems
- Plan for data export and portability
- Ensure tools support your privacy requirements

**Data Pipeline:**
- How data flows from collection to analysis
- Data storage and retention policies
- Data transformation and aggregation
- Access controls and security

**Governance:**
- Who can access what data
- How data quality is maintained
- Documentation and training requirements
- Compliance and audit processes

## Data collection & instrumentation

### Event Tracking Strategy

**Event Naming Conventions:**
- Use consistent naming patterns (e.g., `action_object`: `click_button`, `view_page`)
- Include context in event names or properties
- Document event schemas
- Version events when they change

**Event Properties:**
- Include relevant context (user type, feature, location, etc.)
- Use consistent property names and types
- Avoid PII (personally identifiable information) when possible
- Document all properties

**Common Event Types:**
- **Page/Screen Views**: Track navigation and content consumption
- **User Actions**: Clicks, form submissions, feature usage
- **Conversion Events**: Purchases, subscriptions, conversions
- **Error Events**: Track errors and issues
- **Performance Events**: Measure load times and performance

### Instrumentation Best Practices

**Implementation:**
- Instrument early in development, not as an afterthought
- Test instrumentation before and after deployment
- Validate data quality regularly
- Monitor for missing or incorrect data

**Maintenance:**
- Keep instrumentation up to date as products evolve
- Remove tracking for deprecated features
- Document changes to event schemas
- Regularly audit data collection

**Privacy Considerations:**
- Minimize data collection to what's necessary
- Obtain proper consent where required
- Anonymize or pseudonymize data when possible
- Follow privacy regulations (GDPR, CCPA, etc.)

## Metrics definition

### Defining Meaningful Metrics

**Start with Questions:**
- What question does this metric answer?
- What decision will this metric inform?
- How will we act on this metric?

**Define Clearly:**
- **What**: Exactly what is being measured
- **Why**: Why this metric matters
- **How**: How it's calculated
- **When**: When it's measured and updated
- **Who**: Who owns and uses this metric

### Metric Frameworks

**North Star Metric:**
- The single metric that best captures product value
- Should reflect user value creation
- Leads to desired outcomes
- Actionable by the product team

**Leading vs. Lagging Indicators:**
- **Leading Indicators**: Predict future outcomes (engagement, feature usage)
- **Lagging Indicators**: Reflect past performance (revenue, retention)

**Input vs. Output Metrics:**
- **Input Metrics**: Activities and efforts (features shipped, tests run)
- **Output Metrics**: Results and outcomes (user growth, revenue)

### Metric Health

**Quality Checks:**
- Are metrics accurate and reliable?
- Are they updated on schedule?
- Do stakeholders understand what they mean?
- Are they driving decisions?

**Common Issues:**
- **Vanity Metrics**: Look good but don't drive decisions
- **Misleading Metrics**: Don't reflect actual value or outcomes
- **Over-Reliance**: Relying on single metrics without context
- **Under-Utilization**: Collecting metrics but not using them

## Analytics strategy in practice

### Planning Analytics for New Features

1. **Define Success**: What does success look like for this feature?
2. **Identify Metrics**: Which metrics will indicate success?
3. **Plan Instrumentation**: What events need to be tracked?
4. **Set Baselines**: Establish baseline metrics before launch
5. **Monitor and Iterate**: Track metrics after launch and iterate based on learnings

### Using Analytics for Decision Making

1. **Ask Questions**: Start with the question, not the data
2. **Gather Data**: Collect relevant data to answer the question
3. **Analyze**: Look for patterns, trends, and insights
4. **Validate**: Use experiments to validate insights when possible
5. **Act**: Make decisions based on data and insights
6. **Measure Impact**: Track whether decisions achieved desired outcomes

### Common Pitfalls

- **Analysis Paralysis**: Collecting too much data without acting on it
- **Correlation vs. Causation**: Assuming correlation means causation
- **Vanity Metrics**: Focusing on metrics that look good but don't matter
- **Missing Context**: Using metrics without understanding context
- **Ignoring Qualitative Data**: Relying only on quantitative metrics

## Related topics

- [A/B Testing & Experimentation](ab-testing-experimentation.md) - Using experiments to validate insights and make decisions
- [Data Analysis & Interpretation](data-analysis-interpretation.md) - Analyzing data and drawing insights (includes dashboard and reporting principles)
- [Data Governance](data-governance.md) - Privacy, data quality, and governance practices

