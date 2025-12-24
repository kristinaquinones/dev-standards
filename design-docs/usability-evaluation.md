# Usability Evaluation

## Overview

Usability evaluation helps you understand how well your designs work for users. This document covers frameworks for evaluating usability, identifying problems, and measuring design effectiveness.

## Core Principles

### Test with Real Users

- Test with people who represent your target users
- Don't test with team members or people familiar with the product
- Test early and often, not just at the end
- Even testing with 3-5 users reveals most problems

### Focus on Tasks, Not Features

- Test whether users can complete tasks
- Don't just show features and ask if they like them
- Give users realistic tasks to complete
- Observe what users actually do, not just what they say

### Measure What Matters

- Focus on task completion, not just opinions
- Measure time to complete tasks
- Track errors and confusion
- Use [analytics](../measurement-docs/analytics-strategy.md) to complement usability testing

### Iterate Based on Findings

- Use findings to improve designs
- Prioritize problems by severity and frequency
- Test improvements to verify they work
- Don't assume one round of testing is enough

## Usability Evaluation Frameworks

### Heuristic Evaluation

**What It Is:**
A framework for evaluating designs against usability principles (heuristics). Can be done without users, but is most effective with user testing.

**Heuristics:**
1. **Visibility of System Status**: Users should know what's happening
2. **Match Between System and Real World**: Use language and concepts users understand
3. **User Control and Freedom**: Users should be able to undo and escape
4. **Consistency and Standards**: Follow conventions and be consistent
5. **Error Prevention**: Prevent errors when possible
6. **Recognition Rather Than Recall**: Make options visible, don't require memory
7. **Flexibility and Efficiency**: Support both novice and expert users
8. **Aesthetic and Minimalist Design**: Don't include unnecessary elements
9. **Help Users Recognize, Diagnose, and Recover from Errors**: Clear error messages
10. **Help and Documentation**: Provide help when needed (but design should be self-explanatory)

**How to Use:**
- Review design against each heuristic
- Identify violations of heuristics
- Prioritize problems by severity
- Use findings to improve design

### Usability Testing

**What It Is:**
Observing users interact with your design to complete tasks. The most effective way to identify usability problems.

**Types of Usability Testing:**

**Moderated Testing:**
- You observe and guide users
- Can ask questions during testing
- More control over the session
- Requires your time during testing

**Unmodestated Testing:**
- Users test on their own
- You review recordings or results later
- Less control but more scalable
- Users may need clearer instructions

**Remote Testing:**
- Test with users anywhere
- Use screen sharing or recording tools
- More flexible scheduling
- May miss some context

**In-Person Testing:**
- Test with users in person
- Can observe body language and context
- More natural interaction
- Requires coordination

### Usability Testing Process

**Step 1: Plan the Test**
- Define what you want to learn
- Create realistic tasks for users
- Identify target users
- Plan test structure and questions
- Use [Usability Testing Plan Template](templates/usability-testing-plan-template.md)

**Step 2: Recruit Users**
- Find 3-5 users who represent your target audience
- Don't use team members or people familiar with the product
- Consider incentives for participation
- Schedule test sessions

**Step 3: Conduct Tests**
- Give users realistic tasks to complete
- Observe without leading or helping
- Ask follow-up questions
- Take notes on problems and observations

**Step 4: Analyze Results**
- Identify common problems
- Prioritize issues by severity and frequency
- Look for patterns across users
- Document findings clearly

**Step 5: Improve Design**
- Address identified problems
- Prioritize fixes by impact
- Test improvements to verify they work
- Iterate as needed

## Usability Metrics

### Task Completion

**Completion Rate:**
- Percentage of users who complete tasks successfully
- Higher is better
- Track for each task
- Identify which tasks are problematic

**Time to Complete:**
- How long users take to complete tasks
- Compare to baseline or target time
- Longer times may indicate problems
- Consider user experience, not just speed

### Errors

**Error Rate:**
- Number of errors users make
- Types of errors (wrong action, confusion, etc.)
- Where errors occur
- How users recover from errors

**Error Severity:**
- How serious are the errors?
- Do errors prevent task completion?
- Can users recover easily?
- Prioritize severe errors

### User Satisfaction

**Subjective Ratings:**
- Ask users to rate ease of use
- Measure satisfaction with design
- Understand user preferences
- Complement objective metrics

**Qualitative Feedback:**
- What users say about the design
- What they found confusing
- What they liked or didn't like
- Use to understand why problems occur

## Evaluation Methods

### Task-Based Testing

**Process:**
- Give users specific tasks to complete
- Observe how they complete tasks
- Note problems, confusion, or errors
- Ask follow-up questions

**Example Tasks:**
- "Sign up for an account"
- "Find information about pricing"
- "Complete a purchase"
- "Update your profile settings"

### Think-Aloud Protocol

**Process:**
- Ask users to say what they're thinking
- Understand user thought process
- Identify confusion or uncertainty
- Reveal mental models

**Best Practices:**
- Remind users to keep talking
- Don't interrupt or lead
- Let users struggle (don't help immediately)
- Ask clarifying questions after

### A/B Testing

**Process:**
- Compare two design alternatives
- Measure which performs better
- Use [A/B testing frameworks](../measurement-docs/ab-testing-experimentation.md) for proper testing
- Test with real users in real contexts

**When to Use:**
- When you have two clear alternatives
- When you have enough users to test
- When you can measure clear outcomes
- For optimization, not initial design

## Prioritizing Usability Issues

### Severity

**Critical:**
- Prevents users from completing tasks
- Causes data loss or serious errors
- Affects many users
- Fix immediately

**Major:**
- Makes tasks difficult or confusing
- Causes frustration
- Affects some users
- Fix soon

**Minor:**
- Small annoyances or inconveniences
- Doesn't prevent task completion
- Affects few users
- Fix when possible

### Frequency

**High Frequency:**
- Many users encounter the problem
- Happens often during testing
- Fix high-frequency problems first

**Low Frequency:**
- Few users encounter the problem
- Rare occurrence
- Still fix, but lower priority

## Usability Evaluation Best Practices

- **Test Early**: Don't wait for perfect designs
- **Test Often**: Regular testing catches problems early
- **Test with Real Users**: Team members aren't representative
- **Focus on Tasks**: Test whether users can accomplish goals
- **Measure Objectively**: Use metrics, not just opinions
- **Iterate Based on Findings**: Use results to improve designs

## Common Pitfalls

**Testing Too Late:**
- Waiting until design is complete to test
- Solution: Test early with simple prototypes

**Testing with Wrong Users:**
- Testing with team members or non-representative users
- Solution: Test with real target users

**Leading Users:**
- Helping users or asking leading questions
- Solution: Observe without helping, ask neutral questions

**Ignoring Findings:**
- Not using test results to improve designs
- Solution: Prioritize and fix identified problems

**Testing Too Little:**
- Only testing once or with too few users
- Solution: Test regularly with 3-5 users per round

## Related Topics

- [Product & Design Process](../product-docs/product-design-process.md) - Unified product and design process
- [User Research & Discovery](../product-docs/user-research-discovery.md) - Understanding users
- [A/B Testing & Experimentation](../measurement-docs/ab-testing-experimentation.md) - Comparing designs
- [Analytics Strategy](../measurement-docs/analytics-strategy.md) - Measuring user behavior
- [Usability Testing Plan Template](templates/usability-testing-plan-template.md) - Test planning template

