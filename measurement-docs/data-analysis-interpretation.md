# Data analysis & interpretation

## Overview

Data analysis transforms raw data into actionable insights. This document covers analysis techniques, interpretation pitfalls, and how to communicate findings effectively through dashboards and reports.

## Analysis techniques

### Exploratory Analysis

**Purpose:** Understand your data before formal analysis

**Approaches:**
- **Summary Statistics**: Mean, median, mode, distributions
- **Visualizations**: Histograms, scatter plots, time series
- **Segmentation**: Break data into groups (by user type, feature, time period)
- **Pattern Recognition**: Look for trends, anomalies, clusters

**When to Use:**
- Initial data exploration
- Hypothesis generation
- Understanding data quality
- Identifying areas for deeper analysis

### Comparative Analysis

**Purpose:** Compare groups or time periods

**Approaches:**
- **Before/After**: Compare metrics before and after a change
- **Cohort Analysis**: Compare groups of users over time
- **A/B Test Analysis**: Compare treatment and control groups (see [A/B Testing & Experimentation](ab-testing-experimentation.md))
- **Benchmarking**: Compare against industry standards or past performance

**When to Use:**
- Evaluating impact of changes
- Understanding user segments
- Measuring progress toward goals
- Identifying best and worst performers

### Trend Analysis

**Purpose:** Understand how metrics change over time

**Approaches:**
- **Time Series**: Track metrics over days, weeks, months
- **Seasonality Detection**: Identify recurring patterns
- **Growth Rates**: Calculate percentage changes
- **Moving Averages**: Smooth out noise to see trends

**When to Use:**
- Monitoring product health
- Understanding user behavior patterns
- Forecasting future performance
- Identifying anomalies

### Funnel Analysis

**Purpose:** Understand where users drop off in a process

**Approaches:**
- **Conversion Rates**: Calculate % completing each step
- **Drop-off Points**: Identify where most users leave
- **Time Analysis**: How long users spend at each step
- **Segment Comparison**: Compare funnels for different user groups

**When to Use:**
- Optimizing user flows
- Identifying friction points
- Improving conversion rates
- Understanding user journeys

## Interpretation pitfalls

### Correlation vs. Causation

**The Problem:**
Just because two things happen together doesn't mean one causes the other.

**Example:**
- Ice cream sales and drowning deaths both increase in summer
- Correlation exists, but ice cream doesn't cause drowning
- The real cause: More people swimming in summer

**How to Avoid:**
- Use experiments to establish causality (see [A/B Testing & Experimentation](ab-testing-experimentation.md))
- Consider alternative explanations
- Look for confounding factors
- Don't assume correlation means causation

### Selection Bias

**The Problem:**
The group you're analyzing may not represent the whole population.

**Example:**
- Analyzing only users who completed onboarding
- Missing insights about why others didn't complete
- Results don't apply to all users

**How to Avoid:**
- Analyze all relevant groups, not just successful ones
- Consider why some users might be excluded
- Use random sampling when possible
- Be explicit about who is included/excluded

### Survivorship Bias

**The Problem:**
Focusing only on what succeeded, ignoring what failed.

**Example:**
- Only analyzing successful features
- Missing lessons from failed features
- Overestimating success rates

**How to Avoid:**
- Include failed attempts in analysis
- Analyze both successes and failures
- Consider the full picture, not just winners

### Confirmation Bias

**The Problem:**
Interpreting data to confirm what you already believe.

**Example:**
- Looking for evidence that supports your hypothesis
- Ignoring evidence that contradicts it
- Cherry-picking data points

**How to Avoid:**
- Start with questions, not answers
- Actively look for disconfirming evidence
- Consider alternative explanations
- Be open to being wrong

### Sample Size Issues

**The Problem:**
Drawing conclusions from too few data points.

**Example:**
- Analyzing 10 users and generalizing to all users
- Results may not be representative
- High variability in small samples

**How to Avoid:**
- Ensure adequate sample sizes
- Use statistical methods to assess reliability
- Be cautious about generalizing from small samples
- Consider confidence intervals

### Time Period Bias

**The Problem:**
Results from one time period may not apply to others.

**Example:**
- Analyzing only holiday season data
- Results may not apply to rest of year
- Seasonal effects can mislead

**How to Avoid:**
- Analyze multiple time periods
- Account for seasonality
- Consider external events
- Use appropriate comparison periods

### Decision by Intuition

**The Problem:**
Making decisions based on hunches without data validation.

**Example:**
- "I feel like users want this feature" without checking user research or running an experiment
- Changing a design based on "it looks better" without measuring impact
- Prioritizing work based on stakeholder opinions without validating with data

**How to Avoid:**
- Treat hunches as hypotheses and validate with data before deciding
- Use user research to understand problems, then experiments to validate solutions
- Base decisions on data analysis, not feelings or opinions alone

## Turning data into insights

### The Analysis Process

1. **Start with Questions**: What do you need to know?
2. **Gather Relevant Data**: Collect data that answers your questions
3. **Clean and Prepare**: Ensure data quality
4. **Analyze**: Apply appropriate techniques
5. **Interpret**: What do the results mean?
6. **Validate**: Check for errors and alternative explanations
7. **Communicate**: Share insights clearly

### Validating hunches with data

If you have a hunch or intuition about user behavior, use data analysis to validate it. For example, if you think users are dropping off at a specific step, analyze funnel data to confirm. If you believe a feature is underused, check analytics before making changes. Don't make decisions based on feelings alone - let data validate or invalidate your hypotheses.

### Asking the Right Questions

**Good Questions:**
- Specific and answerable
- Lead to actionable insights
- Consider context and constraints
- Focus on "why" and "what if"

**Poor Questions:**
- Too vague ("Is our product good?")
- Not answerable with available data
- Leading or biased
- Focus only on "what" without "why"

### Validating Insights

Before acting on insights, validate:

- **Statistical Validity**: Are results statistically significant?
- **Practical Significance**: Is the effect large enough to matter?
- **Consistency**: Do results hold across segments and time periods?
- **Alternative Explanations**: Could something else explain the results?
- **Reproducibility**: Can you replicate the analysis?

### Actionable Insights

Good insights should:

- **Answer a Question**: Address a specific need
- **Be Clear**: Easy to understand
- **Lead to Action**: Suggest what to do next
- **Be Timely**: Available when decisions need to be made
- **Be Reliable**: Based on sound analysis

## Dashboard & Reporting Principles

### Dashboard Design

**Purpose of Dashboards:**
- Monitor key metrics at a glance
- Track progress toward goals
- Identify issues quickly
- Support decision-making

**Design Principles:**

**1. Focus on What Matters**
- Include only the most important metrics
- Avoid clutter and information overload
- Prioritize actionable metrics

**2. Use Appropriate Visualizations**
- **Time Series**: Line charts for trends over time
- **Comparisons**: Bar charts for comparing categories
- **Distributions**: Histograms for understanding spread
- **Relationships**: Scatter plots for correlations
- **Parts of Whole**: Pie charts (sparingly) or stacked bars

**3. Make It Scannable**
- Use clear labels and titles
- Group related metrics together
- Use color consistently (e.g., green = good, red = bad)
- Highlight important information

**4. Provide Context**
- Show targets or benchmarks
- Include time comparisons (vs. last week, last month)
- Add annotations for important events
- Explain what metrics mean

**5. Keep It Current**
- Update automatically when possible
- Show data freshness (last updated timestamp)
- Ensure data is accurate and reliable

### Reporting Best Practices

**Report Structure:**

**1. Executive Summary**
- Key findings in 2-3 sentences
- Most important metrics
- Recommended actions

**2. Key Metrics**
- Primary metrics with context
- Trends and changes
- Comparisons to goals or benchmarks

**3. Detailed Analysis**
- Supporting data and analysis
- Segment breakdowns
- Deeper dives into important areas

**4. Insights and Recommendations**
- What the data means
- What actions to take
- What to investigate next

**5. Methodology**
- How data was collected
- Time period covered
- Any limitations or caveats

**Writing Effective Reports:**

- **Be Clear**: Use plain language, avoid jargon
- **Be Concise**: Get to the point quickly
- **Be Honest**: Acknowledge limitations and uncertainties
- **Be Actionable**: Focus on what to do, not just what happened
- **Be Visual**: Use charts and graphs to illustrate points

### Visualization Best Practices

**Choose the Right Chart Type:**

- **Line Charts**: Trends over time
- **Bar Charts**: Comparing categories
- **Pie Charts**: Parts of a whole (use sparingly, max 5-6 categories)
- **Scatter Plots**: Relationships between variables
- **Heatmaps**: Patterns in two dimensions
- **Tables**: Precise numbers, detailed comparisons

**Design Guidelines:**

- **Color**: Use consistently, ensure accessibility (colorblind-friendly)
- **Labels**: Clear, descriptive titles and axis labels
- **Scale**: Appropriate scale to show meaningful differences
- **Legends**: Clear and positioned appropriately
- **Annotations**: Add notes for important events or context

**Common Mistakes:**

- **Too Many Colors**: Hard to distinguish, confusing
- **Misleading Scales**: Exaggerating or minimizing differences
- **3D Charts**: Hard to read, often misleading
- **Chart Junk**: Unnecessary decorations that distract
- **Poor Labels**: Unclear what's being shown

### Simple Dashboard Examples

**Product Health Dashboard:**
- Key metrics: DAU, retention, error rate
- Trends: Week-over-week changes
- Alerts: When metrics cross thresholds
- Context: Comparison to previous period

**Feature Performance Dashboard:**
- Adoption: % of users using feature
- Engagement: How often feature is used
- Outcomes: Impact on key metrics
- Segments: Performance by user type

**Experiment Results Dashboard:**
- Treatment vs. Control: Side-by-side comparison
- Statistical Significance: P-values and confidence intervals
- Primary and Secondary Metrics: All relevant outcomes
- Timeline: Results over time

### Reporting Examples

**Weekly Product Report:**
- Summary: 3-5 key points
- Metrics: Top 5-10 metrics with trends
- Highlights: What went well
- Concerns: What needs attention
- Next Steps: Recommended actions

**Feature Launch Report:**
- Launch Summary: What was launched
- Adoption: How many users are using it
- Impact: Effect on key metrics
- Learnings: What we learned
- Next Steps: Iterations or follow-ups

**Experiment Report:**
- Hypothesis: What was tested
- Results: Treatment vs. control
- Statistical Analysis: Significance, confidence intervals
- Interpretation: What the results mean
- Recommendation: Launch, iterate, or abandon

## Checklists

### Analysis Checklist

- [ ] Clear question or objective defined
- [ ] Appropriate data collected
- [ ] Data quality verified
- [ ] Right analysis technique chosen
- [ ] Results interpreted correctly
- [ ] Alternative explanations considered
- [ ] Insights validated
- [ ] Findings documented

### Dashboard Checklist

- [ ] Focuses on most important metrics
- [ ] Uses appropriate visualizations
- [ ] Provides context (targets, comparisons)
- [ ] Is scannable and easy to understand
- [ ] Updates automatically or regularly
- [ ] Includes data freshness indicator
- [ ] Is accessible (colorblind-friendly, clear labels)
- [ ] Mobile-friendly if needed

### Report Checklist

- [ ] Executive summary included
- [ ] Key findings highlighted
- [ ] Data visualizations support points
- [ ] Context provided (comparisons, benchmarks)
- [ ] Limitations acknowledged
- [ ] Recommendations included
- [ ] Methodology documented
- [ ] Clear and actionable

## Related topics

- [Analytics Strategy](analytics-strategy.md) - Planning what to analyze
- [A/B Testing & Experimentation](ab-testing-experimentation.md) - Using experiments for causal analysis
- [Metrics & Success Criteria](../../product-docs/metrics-success-criteria.md) - Defining metrics to analyze

