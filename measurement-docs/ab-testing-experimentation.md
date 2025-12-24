# A/B testing & experimentation

## Overview

A/B testing and experimentation allow you to make data-driven decisions by comparing different versions of a product or feature to understand which performs better. Experiments help validate hypotheses, measure the true impact of changes, and avoid making decisions based on assumptions or correlation alone.

## Why experiment?

### The Problem with Observational Data

Simply observing data over time can be misleading:

- **Confounding Factors**: Many things change simultaneously, making it impossible to know what caused an outcome
- **Selection Bias**: Users who engage with a feature may be different from those who don't
- **External Events**: Market changes, seasonality, or other exogenous variables can influence results
- **Correlation vs. Causation**: Just because two things happen together doesn't mean one caused the other

### The Power of Experiments

Experiments, particularly those that measure incrementality, provide:

- **Causal Understanding**: Directly measure the impact of a specific change
- **Controlled Comparison**: Compare similar groups under controlled conditions
- **Confidence in Decisions**: Statistical rigor provides confidence in results
- **True Impact Measurement**: Understand the actual effect, not just correlation

## Experiment design principles

### 1. Start with a Hypothesis

Before designing an experiment, clearly state what you're testing:

- **Hypothesis Format**: "If we [make this change], then [this outcome] will [increase/decrease/change] because [reason]"
- **Be Specific**: Define the change and expected outcome clearly
- **Make it Testable**: Ensure you can measure whether the hypothesis is true or false

**Example:**
"If we add a progress indicator to the onboarding flow, then completion rates will increase by 15% because users will have clearer expectations about the process."

### 2. Define Success Metrics

Identify the metrics that will indicate success:

- **Primary Metric**: The main outcome you're trying to improve
- **Secondary Metrics**: Other important outcomes to monitor
- **Guardrail Metrics**: Metrics to ensure you're not causing harm

**Example:**
- Primary: Onboarding completion rate
- Secondary: Time to complete onboarding, user satisfaction
- Guardrail: Support ticket volume, error rates

### 3. Random Assignment

Randomly assign users to treatment and control groups:

- **Randomization**: Ensures groups are similar on average
- **Equal Distribution**: For solo devn and bootstrapped products, typically a 50/50 split is fine, but this can and will vary based on your hypothesis, existing baseline(s), and audience size
- **Consistent Assignment**: Users should stay in the same group throughout the experiment

### 4. Sample Size Planning

Determine how many users you need in your audience:

- **Statistical Power**: Probability of detecting an effect if it exists (typically 80% or higher)
- **Effect Size**: The minimum difference you want to detect
- **Significance Level**: Probability of false positive (typically 5%)
- **Use Calculators**: Online tools can help calculate required sample size

### 5. Duration Planning

Run experiments long enough to capture meaningful data:

- **Statistical Significance**: Wait until you have enough data for valid conclusions
- **Weekly Patterns**: Account for day-of-week effects (weekends vs. weekdays)
- **Seasonal Effects**: Consider if timing matters (holidays, events, etc.)
- **Minimum Duration**: Typically at least 1-2 weeks, often longer

## Incrementality: Understanding True Impact

### What is Incrementality?

**Incrementality** measures the true, causal impact of a change or intervention. It answers the question: "What would have happened differently if we hadn't made this change?"

Incrementality is fundamentally different from simply observing data over time because it:

- **Establishes Causality**: Proves that the change caused the outcome, not just that they happened together
- **Controls for Confounding**: Accounts for other factors that might influence results
- **Measures Net Effect**: Shows the actual additional value created by the change
- **Provides Confidence**: Uses statistical methods to quantify uncertainty

### Why Incrementality Matters

**The Problem with Observed Data Over Time:**

Imagine you launch a new feature and see a 20% increase in user engagement. You might conclude the feature caused the increase. But consider:

- Did engagement increase because of the feature, or because of a marketing campaign that happened at the same time?
- Would engagement have increased anyway due to seasonal trends?
- Are the users engaging with the feature different from those who aren't (selection bias)?
- Did external events (news, competitor changes) influence the results?

Without incrementality, you can't answer these questions. You're left with correlation, not causation.

**How Incrementality Solves This:**

By comparing a treatment group (users who see the change) to a control group (users who don't), incrementality:

1. **Controls for External Factors**: Both groups experience the same external events, so differences are due to the change
2. **Eliminates Selection Bias**: Random assignment ensures groups are similar
3. **Measures True Impact**: The difference between groups is the actual effect of the change
4. **Quantifies Uncertainty**: Statistical methods tell you how confident you can be in the result

### Example: Incrementality vs. Observed Data

**Scenario:** You add a "Save for Later" button to your product and want to measure its impact on user retention.

**Observed Data Approach (Misleading):**
- Look at retention rates before and after launching the feature
- Before feature launch: 40% Day 30 retention
- After feature launch: 44% Day 30 retention
- **Observed Change: +4 percentage points**
- Conclude: "The feature increased retention by 4 percentage points, for 10% improvement overall."

**The Problem:**
- A major marketing campaign launched the same week as the feature
- It's the holiday season (typically 3-4% higher retention)
- Your product was featured in a popular newsletter (brought in higher-quality users)
- You can't tell: Did retention increase because of the feature, or despite it?

**Incrementality Approach (Reveals the Truth):**
- Randomly assign users: 50% see the feature (treatment), 50% don't (control)
- Both groups experience the same marketing campaign, seasonality, and newsletter traffic
- After 30 days, measure retention in both groups
- Treatment group: 44% retention
- Control group: 44% retention
- **Incremental Impact: 0 percentage points, 0% change** (no statistically significant difference)

**Why This Matters:**
- **Observed data suggested a 4% increase** - you might have invested more in this feature
- **Incrementality shows 0% impact** - the feature didn't actually improve retention
- The observed increase was due to marketing, seasonality, and better user quality
- Without incrementality, you'd make decisions based on false conclusions
- You can now focus resources on features that actually drive retention

**The Key Insight:**
Observed data showed retention increased, but incrementality revealed the feature had no effect. The increase was caused by external factors that affected both groups equally. Only by comparing treatment and control groups can you isolate the true impact of your change.

### Statistical Concepts

**Causality vs. Correlation:**

- **Correlation**: Two things happen together, but one doesn't necessarily cause the other
  - Example: Ice cream sales and drowning deaths both increase in summer (correlated, but ice cream doesn't cause drowning)
- **Causality**: One thing directly causes another
  - Example: Adding a feature (cause) leads to increased engagement (effect)
- **Experiments Establish Causality**: By controlling conditions, experiments prove cause and effect

**Statistical Significance:**

Think of it like this: You test a new button color and see more clicks. Is that because the color is better, or just random luck? Statistical significance helps you decide.

- **P-value**: The chance that your result happened by luck alone (like seeing more clicks just by random chance, not because the change actually worked)
- **Significance Threshold**: Usually 5% (0.05) - if the chance is less than 5%, we say it's "significant" (probably not luck)
- **What It Means**: A low p-value means "this probably wasn't just luck"
- **Remember**: Significance tells you something happened, but not whether it matters much

**Confidence Intervals:**

Instead of saying "the effect is exactly 5%," we say "the effect is probably between 3% and 7%."

- **Range of Values**: The likely range where the true effect actually is
- **Example**: "5% increase, with 95% confidence it's between 3% and 7%"
- **What It Means**: We're pretty sure (95% sure) the real effect is somewhere in that range
- **Wider Range**: Less certainty - happens when your data is all over the place (e.g., in your test group, some users clicked 10 times while others clicked 0 times - that's messy, hard-to-predict data). You'll need more users or more consistent behavior to narrow it down.
- **Narrow Range**: More certainty - happens when your data is consistent and predictable (e.g., in your test group, most users clicked 4-6 times with very few outliers - that's clean, reliable data). With consistent behavior, you can be more confident about the true effect.

**When Results Aren't Significant (This Can Be Useful Too!):**

Lack of statistical significance or high variance isn't always a failure - it can tell you important things:

- **No Effect Found**: If your test shows no significant difference, that's valuable information. Maybe the change doesn't matter, or you need a bigger change to see results. Example: Testing button color and finding no difference suggests users don't care about that color choice - you can stop worrying about it and focus elsewhere.

- **High Variance Reveals Problems**: If your data is all over the place, that might indicate a real issue. Example: If some users complete onboarding in 2 minutes while others take 2 hours, the high variance tells you your onboarding experience is inconsistent - that's a problem worth fixing, even if the average looks fine.

**Using Calculators:**

You don't need to calculate these by hand! Use online calculators to:

- **Calculate Sample Size**: Figure out how many users you need for your experiment
  - [Statsig Sample Size Calculator](https://www.statsig.com/sample-size-calculator) - Calculate required sample size
  - [Evan's Awesome A/B Tools](https://www.evanmiller.org/ab-testing/sample-size.html) - Sample size calculator
  - [Optimizely Sample Size Calculator](https://www.optimizely.com/sample-size-calculator/) - Experiment planning tool

- **Calculate Statistical Significance**: Check if your results are significant
  - [Statsig Significance Calculator](https://www.statsig.com/significance-calculator) - Test statistical significance
  - [AB Testguide](https://abtestguide.com/calc/) - A/B test calculator
  - [VWO A/B Test Significance Calculator](https://vwo.com/ab-split-test-significance-calculator/) - Significance testing

**Quick Rule of Thumb:**
- If your p-value is below 0.05 (5%), your result is probably real, not luck
- If your confidence interval doesn't include zero, you likely have a real effect
- When in doubt, use a calculator or ask someone with statistical expertise

### Common Pitfalls and Misconceptions

**Pitfall 1: Stopping Too Early**

- **Problem**: Ending an experiment as soon as you see a positive result
- **Why It's Wrong**: Early results can be due to chance (regression to the mean)
     - **Example**: After 3 days, your test shows a 10% improvement and looks "significant." You stop and launch. But by day 7 (your planned end date), that improvement has shrunk to 2% and is no longer significant.
     - Early results often look better (or worse) than they really are because you haven't reached enough participants yet, or you're measuring before users have had enough time to complete the action you're tracking (e.g., measuring 7-day retention after only 3 days).
- **Solution**: Wait for statistical significance and run for planned duration

**Pitfall 2: Peeking at Results**

- **Problem**: Checking results multiple times and stopping when you like what you see
- **Why It's Wrong**: Increases false positive rate (multiple comparisons problem)
     - A well-designed experiment with a clear plan from the start doesn't require multiple checks. The experiment design already accounts for the sample size and duration needed. Trust the process, buddy.
- **Solution**: Decide on analysis plan upfront, stick to it 

**Pitfall 3: Ignoring Secondary Metrics**

- **Problem**: Focusing only on primary metric, ignoring negative effects elsewhere
- **Why It's Wrong**: A feature might improve one metric but harm others
     - e.g. in email marketing, focusing only on email opens and clicks, and not once looking at unsubscribe rate
- **Solution**: Monitor guardrail metrics and secondary outcomes

**Pitfall 4: Confusing Statistical and Practical Significance**

- **Problem**: A result is statistically significant but practically meaningless
- **Why It's Wrong**: A 0.5% improvement might be significant but not worth the effort
     - For some products, a 0.5% improvement might be worth +$100k ARR, and for others, this might be worth +$1k ARR. Whether or not it's worth it then depends on your product/organizational goals and the cost these changes. Will you get +$1k for something that'll cost +$5k to maintain? Or is the one time cost of implementation sub $500?
- **Solution**: Consider effect size and practical importance, not just p-values

**Pitfall 5: Assuming Correlation is Causation**

- **Problem**: Seeing patterns in observational data and assuming they're causal
- **Why It's Wrong**: Many factors could explain the pattern
- **Solution**: Use experiments to establish causality

**Pitfall 6: Not Accounting for Multiple Comparisons**

- **Problem**: Testing many things and finding "significant" results by chance
- **Why It's Wrong**: The more tests you run, the more likely false positives.
     - If you test 20 different button colors, even if none actually work, you'll likely find 1 "significant" result just by chance (5% of 20 = 1 false positive).
     - **Another Example**: You test 10 different headlines for your landing page simultaneously. One shows a 15% improvement with p < 0.05, so you launch it. But you've essentially run 10 tests - the chance of at least one false positive is now ~40%, not 5%. That "winning" headline might not actually be better.
- **Solution**: The simplest approach is to test one thing at a time. If you must test multiple things, be more strict about what counts as "significant" (e.g., require stronger evidence when testing 10 things vs. 1 thing). Many analytics tools can handle this automatically - just be aware that testing many things at once increases the chance of false positives.

### When to Use Incrementality

Use incrementality measurement when:

- **Making Important Decisions**: Changes that significantly impact users or product direction
- **Validating Hypotheses**: Testing whether a change actually works as expected
- **Measuring ROI**: Understanding the true value of an investment
- **Avoiding False Conclusions**: When observational data could be misleading

Consider simpler approaches when:

- **Exploratory Analysis**: Early stage research and discovery
- **Low-Stakes Decisions**: Minor changes with minimal impact
- **Resource Constraints**: When experiments aren't feasible
- **Clear Patterns**: When observational data is very clear and consistent

## Experiment types (in practice)

**Reality Check:** People use "A/B test" to mean any experiment that compares groups. A/B, A/B/N (testing multiple variants), and split tests are all the same thing - comparing different versions to see which performs better. Don't get hung up on terminology.

### What You're Actually Testing

| What You're Testing | What to Call It | When to Use |
|---------------------|-----------------|-------------|
| **One change** (button text, color, headline) | A/B test | 90% of your experiments - start here |
| **Multiple variants** (3-4 different headlines) | A/B/N test (or just "A/B test") | When you have several options and want to test them all at once |
| **Multiple elements together** (headline + image + button) | Multivariate test | Rarely needed - usually better to test elements separately first |
| **Entire experience** (new onboarding flow vs. old) | Split test (or just "A/B test") | Major changes where you're testing a completely different approach |

### Practical Guidance

**Default to Simple A/B Tests:**
- Test one change at a time
- Easier to understand what actually worked
- Faster to get results
- Less chance of false positives
- **Use this for**: Almost everything - button changes, copy, colors, single feature tweaks

**Split Tests Are Just Big A/B Tests:**
- Same methodology, bigger scope
- Testing completely different experiences
- **Use this for**: New user flows, major feature launches, complete redesigns

**When to Test Multiple Variants (A/B/N):**
- You have 3-4 clear options and can't decide
- You want to test them all simultaneously
- You have enough traffic to support multiple groups
- **Use this for**: Testing several headline options, multiple CTA button texts, different value propositions

**Skip Multivariate Tests (Usually):**
- They're complex and require huge sample sizes
- Hard to know which element actually caused the result
- Better to test elements one at a time
- **Only use when**: You genuinely need to understand how elements interact (rare)

**The Difference Between Multiple Variant (A/B/N) and Multivariate:**

| Aspect | Multiple Variant (A/B/N) | Multivariate |
|--------|-------------------------|--------------|
| **What you're testing** | Multiple versions of ONE thing | Multiple things at the SAME time |
| **Example** | 3 different headlines or landing pages | Headline + image + button (all together) |
| **Complexity** | Simple - just more variants (3 headlines = 3 versions) | Complex - testing combinations (3 elements with 3 variants each = 27 combinations to test) |
| **Sample size needed** | Moderate (more variants = more users) | Very large (exponential combinations) |
| **What you learn** | Which variant is best | How elements interact with each other, which combination is best |
| **When to use** | You have several options for one element | You need to understand element interactions |

**Quick Rule:** A/B/N = testing 3-4 different headlines. Multivariate = testing headline + image + button together to see if they work better in combination.

**Bottom Line:** Start with simple A/B tests. If you need to test multiple options, use A/B/N, which literally just means there are variants. Save multivariate tests for when you really need to understand interactions. Don't overthink the terminology - focus on what you're trying to learn.

## Experiment checklist

### Before Launching

- [ ] Clear hypothesis defined
- [ ] Success metrics identified (primary, secondary, guardrails)
- [ ] Sample size calculated
- [ ] Duration planned
- [ ] Randomization method confirmed
- [ ] Analysis plan documented
- [ ] Stakeholders aligned on approach

### During Experiment

- [ ] Monitor for technical issues
- [ ] Check data quality regularly
- [ ] Avoid peeking at results (or use proper methods if you must)
- [ ] Document any unexpected events
- [ ] Ensure experiment is running as designed

### After Experiment

- [ ] Wait for planned duration (unless stopping early is justified)
- [ ] Check statistical significance
- [ ] Analyze primary and secondary metrics
- [ ] Review guardrail metrics for negative effects
- [ ] Document findings and learnings
- [ ] Make decision based on results
- [ ] Share results with stakeholders
- [ ] Plan follow-up experiments if needed

## Real-World Examples

### Example 1: Feature Launch

**Hypothesis:** Adding social sharing will increase user engagement

**Experiment Design:**
- Treatment: Users see social sharing buttons
- Control: Users don't see social sharing buttons
- Metric: Weekly active users
- Duration: 4 weeks

**Results:**
- Treatment: 45% weekly active users
- Control: 42% weekly active users
- Incremental Impact: +3 percentage points (statistically significant)

**Decision:** Launch feature to all users

### Example 2: Pricing Test

**Hypothesis:** Lowering price by 20% will increase revenue through higher volume

**Experiment Design:**
- Treatment: 20% lower price
- Control: Current price
- Metric: Total revenue
- Duration: 8 weeks (to account for purchase cycles)

**Results:**
- Treatment: Higher volume, but lower revenue overall
- Incremental Impact: -5% revenue (statistically significant)

**Decision:** Keep current pricing

### Example 3: Onboarding Optimization

**Hypothesis:** Shorter onboarding will improve completion rates

**Experiment Design:**
- Treatment: 3-step onboarding
- Control: 5-step onboarding
- Metrics: Completion rate, time to value, Day 7 retention
- Duration: 2 weeks

**Results:**
- Completion rate: Higher in treatment (+8%)
- Time to value: Faster in treatment
- Day 7 retention: Lower in treatment (-2%)

**Decision:** Launch shorter onboarding, but add nurture messaging to improve retention

## Common mistakes to avoid

1. **Not Having a Control Group**: Can't measure incrementality without comparison
2. **Sample Size Too Small**: Results won't be reliable or generalizable
3. **Running Too Short**: Not capturing full user behavior cycles
4. **Testing Too Many Things at one time**: Hard to understand what caused results
5. **Ignoring Statistical Significance**: Making decisions on noise, not signal
6. **Only Looking at Primary Metric**: Missing negative effects elsewhere
7. **Stopping When You Like Results**: Increases false positive rate
8. **Not Documenting Learnings**: Missing opportunities to build knowledge
9. **Assuming Results Generalize**: What works for one segment may not work for others
10. **Not Planning Follow-ups**: One experiment rarely tells the full story

## Frameworks

### Statistical Significance Framework

**The Basics: When Results Are Significant**

Think of it like this: You need enough evidence to be confident your change actually worked, not just got lucky.

- **P-value is low** (usually below 0.05): The chance this happened by luck is small - probably not random
- **Confidence interval doesn't include zero**: The effect is likely real (not zero), even if you're not sure exactly how big
- **You had enough users**: Too few users = unreliable results (like asking 3 people and thinking you know what everyone thinks)
- **You ran it long enough**: Let the experiment finish - early results can be misleading

**Minimum Detectable Effect (MDE) - Plan Before You Test**

MDE is the smallest improvement you can reliably detect with your experiment. It's like asking: "How small of a difference can I actually see with my sample size?"

- **Small MDE** (e.g., 1%): You can detect tiny changes, but you need LOTS of users
- **Larger MDE** (e.g., 10%): You can detect bigger changes with fewer users
- **Why it matters**: If your MDE is 10% but your actual change is only 2%, you might miss it even if it's real. You need to plan your experiment to detect the size of change you care about.

**Example:** You want to detect a 5% improvement in sign-ups. Your MDE calculator says you need 10,000 users per group. If you only have 1,000 users, you can't reliably detect a 5% change - you'd need a bigger change (like 15%) to see it.

**Planning Your Experiment:**
1. Decide what size change matters to you (your MDE)
2. Use a sample size calculator with MDE to figure out how many users you need
3. Run the experiment for the full planned duration
4. Check if results are significant AND if the effect size is meaningful

**When to Be Cautious:**
- P-value just below threshold (e.g., 0.049) - might be borderline
- Wide confidence intervals - less certain about the true effect
- Small sample size - results might not be reliable
- Multiple comparisons made - higher chance of false positives

**Effect Size - Does It Actually Matter?**

Statistical significance tells you an effect exists, but effect size tells you if it matters:

- **Small Effect:** Noticeable but may not be worth the effort (e.g., 0.5% improvement that costs more to maintain)
- **Medium Effect:** Meaningful improvement worth implementing (e.g., 5% improvement that's easy to maintain)
- **Large Effect:** Significant improvement, high priority to implement (e.g., 20% improvement that transforms the experience)

**The Bottom Line:** Results are significant when you have enough evidence (low p-value, good sample size, full duration) AND the change is big enough for you to actually detect (MDE) AND the effect size is meaningful for your goals. Use a sample size calculator that includes MDE to plan your experiment properly.

### Experiment Design Framework

Use this framework to design experiments that deliver clear, actionable results. Each step should align with SMART goals (Specific, Measurable, Achievable, Relevant, Time-bound) - see [SMART Goals Framework](../../product-docs/metrics-success-criteria.md#smart-goals-framework) for details.

1. **Question**: What are we trying to learn? (SMART: Specific, Relevant)
2. **Hypothesis**: What do we think will happen? (SMART: Specific, Achievable)
3. **Design**: How will we test it? (SMART: Achievable - can we actually run this?)
4. **Metrics**: What will we measure? (SMART: Measurable, Time-bound)
5. **Analysis**: How will we interpret results? (SMART: Measurable - clear success criteria)
6. **Decision**: What will we do based on results? (SMART: Relevant - ties to goals)

**Example Using SMART Goals:**

- **Question**: Will a shorter onboarding increase completion rates?
- **Hypothesis**: Reducing onboarding from 5 steps to 3 will increase completion by 15%
- **Design**: A/B test with 50/50 split, 2-week duration, 5,000 users per group
- **Metrics**: Completion rate (primary), time to complete (secondary), Day 7 retention (guardrail)
- **Analysis**: Significant if p < 0.05 AND completion rate increases by at least 10%
- **Decision**: Launch if significant improvement; iterate if no change; investigate if retention drops

## Related topics

- [Analytics Strategy](analytics-strategy.md) - Planning what to measure and why
- [Data Analysis & Interpretation](data-analysis-interpretation.md) - Analyzing experiment results
- [Metrics & Success Criteria](../../product-docs/metrics-success-criteria.md) - Defining success metrics for experiments