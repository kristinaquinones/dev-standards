# Design Handoff Template

**Feature/Component:** [Name]  
**Designer:** [Name]  
**Date:** [Date]  
**Status:** [Draft / Ready for Review / Approved]

## Overview

**What is this?**
[Brief description of what's being designed]

**Where does it live?**
[Where in the product this appears]

**Related Features:**
[Links to related features or components]

## Design Specifications

### Visual Design

**Layout:**
[Description of layout, dimensions, spacing]

**Colors:**
- [Color name]: [Hex code] - [Usage]
- [Color name]: [Hex code] - [Usage]

**Typography:**
- [Text element]: [Font, size, weight, color]
- [Text element]: [Font, size, weight, color]

**Spacing:**
- [Element spacing]: [Value]
- [Element spacing]: [Value]

### Components Used

[List of design system components or custom components used]

- [Component 1]: [Variant/State]
- [Component 2]: [Variant/State]

### Assets

**Images/Icons:**
- [Asset name]: [Location/link]
- [Asset name]: [Location/link]

**Export Specifications:**
- Format: [PNG, SVG, etc.]
- Size/Resolution: [Specifications]

## Interactions

### User Actions

**Action 1: [Action Name]**
- Trigger: [How user initiates]
- Feedback: [What happens]
- Result: [What changes or happens next]

**Action 2: [Action Name]**
- Trigger: [How user initiates]
- Feedback: [What happens]
- Result: [What changes or happens next]

### States

**Default State:**
[How it looks normally]

**Hover State:**
[How it looks on hover]

**Active/Focus State:**
[How it looks when active or focused]

**Loading State:**
[How it looks while loading]

**Error State:**
[How it looks when there's an error]

**Empty State:**
[How it looks when there's no content]

### Transitions

**Animation/Transition:**
- [What animates]: [Duration, easing]
- [What animates]: [Duration, easing]

## Responsive Behavior

**Mobile (< 768px):**
[How design adapts for mobile]

**Tablet (768px - 1024px):**
[How design adapts for tablet]

**Desktop (> 1024px):**
[How design adapts for desktop]

## Accessibility Requirements

[See [Accessibility & Inclusivity](../../dev-docs/accessibility-inclusivity.md) for detailed requirements]

**Keyboard Navigation:**
- [Navigation requirements]

**Screen Reader:**
- [ARIA labels, roles, descriptions needed]

**Color Contrast:**
- [Contrast requirements]

**Focus Indicators:**
- [Focus state requirements]

## Edge Cases

**Empty States:**
[What to show when there's no data]

**Error States:**
[What to show when errors occur]

**Loading States:**
[What to show while loading]

**Long Content:**
[How to handle long text or content]

**Multiple Items:**
[How to handle many items]

## Technical Notes

**Dependencies:**
- [Technical dependency 1]
- [Technical dependency 2]

**Constraints:**
- [Technical constraint 1]
- [Technical constraint 2]

**Questions for Development:**
- [Question 1]
- [Question 2]

## Example

**Feature:** Task Filtering  
**What is this?** Filter dropdown for task list

**Layout:**
- Dropdown in task list header, right-aligned
- Width: 200px
- Spacing: 16px from search box

**Colors:**
- Background: #FFFFFF
- Text: #333333
- Border: #CCCCCC
- Hover: #F5F5F5

**Interactions:**
- Click dropdown: Opens list of assignees
- Select assignee: Filters task list, shows selected assignee in dropdown
- Clear filter: Button appears when filter is active, clears filter on click

**States:**
- Default: Dropdown shows "All" or selected assignee
- Open: Dropdown shows list of assignees
- Filtered: Task list shows only filtered tasks, clear button visible

**Accessibility:**
- Keyboard: Tab to focus, Enter to open, Arrow keys to navigate, Enter to select
- Screen Reader: "Filter by assignee, dropdown, currently showing [name]"
- Focus: Clear focus indicator on dropdown and options

## Related Topics

- [Interaction Design](../interaction-design.md) - Interaction design frameworks
- [Accessibility & Inclusivity](../../dev-docs/accessibility-inclusivity.md) - Accessibility requirements
- [Design System Documentation Template](design-system-documentation-template.md) - Component documentation

