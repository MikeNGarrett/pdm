### Title: [[phase]] [project]: [name of task or story]

---

## Summary

Brief description of the task or story. This should include the business purpose or user value (what this enables or solves), and any key context needed to understand the work.

---

## Definition of Done (DoD)

This task is considered done when:

- [ ] The implementation satisfies all stated **Acceptance Criteria**.
- [ ] The work has been **internally reviewed** by at least one team member other than the Implementer (e.g. code review, design review).
- [ ] The work has been **verified by QA** (for code/design stories).
- [ ] The work has been **merged into the main branch** (for dev tasks).
- [ ] The work has been **deployed to the test environment** (for dev tasks).
- [ ] The work has been **approved by stakeholders**, where required.

> _Design-specific DoD:_ Internal design review completed.  
> _Admin-specific DoD:_ Acceptance Criteria are met.  
> _Code-specific DoD:_ QA signoff and deployment steps complete.

---

## Acceptance Criteria (AC)

State all functional and non-functional requirements. Use Gherkin-style or bullet format.

### UI & Design

- [ ] Implementation follows the design system (layout, spacing, colors, fonts, interaction).
- [ ] A designer conducts a visual inspection and provides feedback.
- [ ] The final result aligns visually with related elements on the site.

### Functionality

- [ ] Users can [describe action or outcome].
- [ ] Handles edge cases like [describe specific edge cases or validation].

### Performance & Technical

- [ ] Loads in under [target time].
- [ ] Fully functional across Chrome, Firefox, Edge, and Safari (latest versions).
- [ ] Mobile, tablet, and desktop experiences are consistent.

### Accessibility & Usability

- [ ] Fully navigable with a keyboard.
- [ ] Screen reader support includes accurate labels, error announcements, and ARIA attributes.
- [ ] Meets WCAG 2.1 AA standards (contrast, focus states, labels, etc.).

### Testing & Deployment

- [ ] QA testing confirms that all criteria are met.
- [ ] No major bugs or regressions introduced.

---

## Implementation Notes (Optional)

Add technical considerations or implementation details specific to this task. This might include system interactions, technical constraints, known risks, or links to relevant documentation.

---

## Review Criteria (Optional)

Use this section to outline what reviewers should specifically look for (e.g. naming conventions, responsiveness, semantic markup, design fidelity, etc.).

---

## QA Testing Notes (Optional)

Provide guidance for QA, including required test data, user roles, or expected behavior in different environments.

---

## Dependencies / Prerequisites

- [ ] List any other tasks, approvals, or assets that must be completed or provided before work can begin.