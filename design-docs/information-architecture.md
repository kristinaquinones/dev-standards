# Information Architecture

## Overview

Information architecture (IA) is the framework for organizing and structuring information in a way that helps users find what they need and understand how to navigate. Good IA makes products intuitive and easy to use.

## Core Principles

### User-Centered Organization

- Organize information based on how users think, not how you think
- Use [user research](../product-docs/user-research-discovery.md) to understand user mental models
- Group related information together
- Make relationships between information clear

### Clear Navigation

- Users should always know where they are
- Users should be able to find what they're looking for
- Navigation should be consistent and predictable
- Provide multiple ways to find information when appropriate

### Progressive Disclosure

- Show the most important information first
- Hide complexity until users need it
- Don't overwhelm users with too much information at once
- Reveal details progressively as users explore

### Scalable Structure

- Design structures that can grow
- Plan for future content and features
- Use consistent patterns that can be repeated
- Keep structure simple enough to maintain

## IA Frameworks

### Content Organization

**Hierarchical Structure:**
- Organize content in a tree structure
- Main categories at the top level
- Subcategories nested underneath
- Useful for organizing large amounts of content

**Flat Structure:**
- All content at the same level
- Simple navigation, no nesting
- Useful for small products or focused features
- Can become unwieldy as content grows

**Hub and Spoke:**
- Central hub with multiple spokes
- Users start at hub, navigate to specific areas
- Useful for products with distinct functional areas
- Each spoke can have its own structure

**Matrix:**
- Multiple ways to access the same content
- Users can filter or browse by different dimensions
- Useful for content that fits multiple categories
- More complex to design and maintain

### Navigation Patterns

**Top Navigation:**
- Horizontal navigation at the top of the page
- Good for main sections or categories
- Limited by screen width
- Common for websites and web apps

**Side Navigation:**
- Vertical navigation on the side
- Can accommodate more items
- Good for complex products with many sections
- Takes up screen space

**Tab Navigation:**
- Tabs for switching between views
- Good for related content or functions
- Limited number of tabs (usually 3-7)
- Common in mobile and desktop apps

**Breadcrumbs:**
- Shows path from home to current page
- Helps users understand where they are
- Useful for deep hierarchies
- Doesn't replace main navigation

**Search:**
- Allows users to find content directly
- Essential for large amounts of content
- Complements navigation, doesn't replace it
- Should be easy to find and use

### Labeling and Naming

**Clear Labels:**
- Use language users understand
- Avoid jargon or internal terminology
- Be consistent with labeling
- Test labels with users to ensure clarity

**Descriptive Names:**
- Names should clearly indicate what's inside
- Use specific names over generic ones
- Consider user mental models when naming
- Keep names concise but descriptive

## IA Design Process

### Step 1: Understand Content and Users

**Content Audit:**
- List all content and features
- Understand what information exists
- Identify content relationships
- Determine what's most important

**User Research:**
- Understand how users think about information
- Identify user mental models
- Learn what users are looking for
- Use [user research methods](../product-docs/user-research-discovery.md)

### Step 2: Organize Information

**Grouping:**
- Group related content together
- Use card sorting (with users) to understand groupings
- Create logical categories
- Consider multiple ways to organize

**Hierarchy:**
- Determine what's most important
- Create clear hierarchy of information
- Balance depth vs. breadth
- Keep hierarchy shallow when possible (3-4 levels max)

### Step 3: Design Navigation

**Navigation Structure:**
- Choose navigation pattern(s) that fit your content
- Design main navigation
- Plan secondary navigation if needed
- Consider mobile vs. desktop differences

**Navigation Labels:**
- Write clear, descriptive labels
- Test labels with users
- Keep labels consistent
- Use familiar terms when possible

### Step 4: Test and Refine

**Usability Testing:**
- Test if users can find information
- Test navigation structure
- Identify confusion or problems
- Use [usability testing methods](usability-evaluation.md)

**Iterate:**
- Fix problems identified in testing
- Refine organization based on feedback
- Simplify if structure is too complex
- Test again to verify improvements

## IA Patterns

### Common Structures

**Dashboard Pattern:**
- Overview page with key information
- Links to detailed views
- Good for products with multiple functions
- Users start here, navigate to specifics

**Wizard Pattern:**
- Step-by-step process
- Clear progress indication
- Good for complex tasks or onboarding
- Users move forward through steps

**Master-Detail Pattern:**
- List view with detail view
- Users select from list, see details
- Good for content browsing
- Common in mobile apps

**Filter and Browse:**
- Users filter content by criteria
- Browse filtered results
- Good for large content collections
- Multiple filters can be combined

## IA Best Practices

- **Start with User Mental Models**: Organize information how users think about it
- **Keep It Simple**: Don't create complex structures when simple works
- **Be Consistent**: Use consistent patterns throughout
- **Test with Users**: Don't assume your organization makes sense to users
- **Plan for Growth**: Design structures that can scale
- **Provide Multiple Paths**: Give users different ways to find information

## Common Pitfalls

**Organizing by Internal Structure:**
- Organizing based on how your team works, not how users think
- Solution: Use user research to understand mental models

**Too Many Levels:**
- Creating deep hierarchies that are hard to navigate
- Solution: Keep hierarchy shallow (3-4 levels max)

**Inconsistent Patterns:**
- Using different navigation patterns in different areas
- Solution: Establish patterns and use them consistently

**Ignoring Mobile:**
- Designing only for desktop, ignoring mobile constraints
- Solution: Consider mobile from the start, test on mobile

## Related Topics

- [User Research & Discovery](../product-docs/user-research-discovery.md) - Understanding user mental models
- [Product & Design Process](../product-docs/product-design-process.md) - Unified product and design process
- [Interaction Design](interaction-design.md) - Designing interactions
- [Usability Evaluation](usability-evaluation.md) - Testing IA
- [Product & Design Brief Template](../product-docs/templates/product-design-brief-template.md) - Documenting IA decisions

