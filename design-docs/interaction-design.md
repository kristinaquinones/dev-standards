# Interaction Design

## Overview

Interaction design focuses on how users interact with products and how products respond to user actions. This document covers frameworks for designing effective, intuitive interactions.

## Core Principles

### Clear Affordances

- Make it obvious what users can interact with
- Use visual cues (buttons look clickable, links look clickable)
- Follow conventions users expect
- Don't make users guess what's interactive

### Immediate Feedback

- Provide feedback for every user action
- Feedback should be immediate and clear
- Show loading states for actions that take time
- Confirm important actions before executing

### Error Prevention and Recovery

- Prevent errors when possible
- Design to make errors less likely
- Provide clear error messages when errors occur
- Make it easy to recover from errors

### Consistency

- Use consistent interaction patterns
- Similar actions should work similarly
- Follow platform conventions when applicable
- Build user expectations through consistency

## Interaction Patterns

### Common Interactions

**Click/Tap:**
- Primary interaction for buttons and links
- Should be clearly indicated (button styling, hover states)
- Provide visual feedback on click/tap
- Use for primary actions

**Hover:**
- Reveal additional information or options
- Show that something is interactive
- Provide previews or tooltips
- Desktop-only interaction

**Drag and Drop:**
- For reordering, moving items
- Should be clearly draggable
- Provide visual feedback during drag
- Show drop zones clearly

**Form Input:**
- Text fields, checkboxes, radio buttons, selects
- Clear labels and placeholders
- Validation feedback
- Help users complete forms successfully

**Navigation:**
- Moving between pages or sections
- Should be clear where links go
- Provide feedback on current location
- Support browser back/forward

### Feedback Patterns

**Loading States:**
- Show when actions are processing
- Use progress indicators for longer operations
- Keep users informed about what's happening
- Don't leave users wondering if something is working

**Success Feedback:**
- Confirm when actions succeed
- Use clear, positive messaging
- Show what happened (e.g., "Item added to cart")
- Don't overdo it (not every action needs a celebration)

**Error Feedback:**
- Clearly explain what went wrong
- Explain how to fix the error
- Use helpful, not technical language
- Show errors near where they occurred

**Empty States:**
- Show helpful content when there's no data
- Explain what users can do
- Provide actions to get started
- Don't just show blank screens

## Interaction Design Framework

### Step 1: Identify User Actions

**What do users need to do?**
- List all actions users can take
- Understand user goals and tasks
- Identify primary vs. secondary actions
- Consider different user types and use cases

**How do users expect to do it?**
- Understand user mental models
- Consider platform conventions
- Look at similar products
- Use [user research](../product-docs/user-research-discovery.md) to understand expectations

### Step 2: Design Interactions

**Choose Interaction Patterns:**
- Select appropriate patterns for each action
- Consider context and constraints
- Balance familiarity with innovation
- Test patterns with users

**Design Feedback:**
- Plan feedback for each action
- Ensure feedback is immediate and clear
- Design loading and error states
- Consider success confirmations

**Design States:**
- Default state (how it looks normally)
- Hover/focus state (when user is about to interact)
- Active state (during interaction)
- Disabled state (when not available)
- Error state (when something goes wrong)

### Step 3: Test Interactions

**Usability Testing:**
- Test if interactions are clear and intuitive
- Verify feedback is helpful
- Check error handling
- Use [usability testing methods](usability-evaluation.md)

**Iterate:**
- Fix problems identified in testing
- Improve unclear interactions
- Refine feedback and states
- Test again to verify improvements

## Interaction Patterns by Context

### Forms

**Best Practices:**
- Clear labels and placeholders
- Inline validation (show errors as user types)
- Required field indicators
- Helpful error messages
- Progress indicators for multi-step forms

**Common Patterns:**
- Single column layout
- Group related fields
- Show character limits
- Auto-save when possible
- Clear submit buttons

### Lists and Tables

**Best Practices:**
- Sortable columns when helpful
- Filterable when there's lots of data
- Pagination or infinite scroll
- Clear row actions
- Responsive design for mobile

**Common Patterns:**
- Row selection (checkboxes)
- Row actions (hover or menu)
- Expandable rows for details
- Bulk actions for multiple items

### Modals and Overlays

**Best Practices:**
- Clear close button
- Escape key to close
- Focus trap (keyboard navigation stays in modal)
- Clear purpose and actions
- Don't overuse modals

**Common Patterns:**
- Confirmation dialogs
- Form modals
- Information overlays
- Full-screen modals for mobile

### Navigation

**Best Practices:**
- Clear current location
- Breadcrumbs for deep hierarchies
- Search when there's lots of content
- Consistent navigation patterns
- Mobile-friendly navigation

**Common Patterns:**
- Top navigation
- Side navigation
- Tab navigation
- Hamburger menu (mobile)

## Interaction Design Best Practices

- **Follow Conventions**: Use familiar patterns users expect
- **Provide Feedback**: Every action should have clear feedback
- **Prevent Errors**: Design to make errors less likely
- **Make Recovery Easy**: When errors happen, make it easy to fix
- **Test with Users**: Don't assume interactions are intuitive
- **Consider Context**: Design interactions for the context of use

## Common Pitfalls

**Hidden Interactions:**
- Making things interactive without clear indication
- Solution: Use clear visual cues and affordances

**No Feedback:**
- Actions happen without any indication
- Solution: Provide immediate, clear feedback for all actions

**Poor Error Handling:**
- Unclear error messages or no way to recover
- Solution: Write helpful error messages and make recovery easy

**Inconsistent Patterns:**
- Same action works differently in different places
- Solution: Establish patterns and use them consistently

## Related Topics

- [Product & Design Process](../product-docs/product-design-process.md) - Unified product and design process
- [Information Architecture](information-architecture.md) - Organizing content and navigation
- [Usability Evaluation](usability-evaluation.md) - Testing interactions
- [Accessibility & Inclusivity](../dev-docs/accessibility-inclusivity.md) - Accessible interactions
- [Design Handoff Template](templates/design-handoff-template.md) - Documenting interactions

