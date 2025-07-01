Start a sprint planning session following SDLC v1.0 framework.

## Sprint Planning Session Creation Process:

1. **Generate Session Filename**: Create session file in `sessions/` using format:
   - `YYYY-MM-DD-HHMM-sprint-planning-[sprint-name].md`
   - Example: `2025-07-01-1400-sprint-planning-1.3-auth-oauth`

2. **Use Sprint Planning Template**: Initialize with `templates/sprint-planning-session.md`

3. **Sprint Categories** (SDLC v1.0 Framework):
   - **1.x - Feature Sprints**: New functionality development
   - **2.x - Infrastructure Sprints**: DevOps, deployment, architecture
   - **3.x - Bug Fix Sprints**: Issue resolution and patches
   - **4.x - Research Sprints**: Investigation, POCs, technology evaluation
   - **5.x - Maintenance Sprints**: Updates, refactoring, cleanup
   - **9.x - Emergency Sprints**: Critical fixes requiring immediate attention

4. **Session Initialization**: Populate template with:

```markdown
# Development Session - [Date Time] - sprint-planning - [sprint-name]

## Session Overview
- **Start Time**: [Current timestamp]
- **Session Type**: Sprint Planning
- **Estimated Duration**: 2-4 hours
- **Sprint Number**: [Sprint X.x]
- **Sprint Category**: [Category from above]
- **Team Members**: [List participants]

## Sprint Overview
- **Sprint Name**: [Descriptive sprint name]
- **Sprint Duration**: [Start date - End date]
- **Sprint Goal**: [Primary objective and deliverable]
- **Business Value**: [Expected business impact]

## SDLC v1.0 Integration
- **Performance Standards**: Reference performance-standards.md
- **Quality Gates**: Apply SDLC quality checkpoints
- **Failure Prevention**: Include three-strike analysis awareness
- **Knowledge Transfer**: Plan documentation and learning capture

[Continue with full sprint-planning-session.md template...]
```

5. **Pre-Planning Checklist**:
   - [ ] Review previous sprint retrospective
   - [ ] Check product backlog prioritization
   - [ ] Verify team capacity and availability
   - [ ] Ensure stakeholder alignment on goals
   - [ ] Confirm technical dependencies

6. **SDLC v1.0 Performance Standards Integration**:
   - Set performance budgets for sprint deliverables
   - Plan performance testing approach
   - Define performance success criteria
   - Reference performance-standards.md requirements

7. **Risk Assessment Framework**:
   - Technical risks with mitigation strategies
   - Timeline risks and contingency plans
   - Resource risks and backup options
   - Apply failure-analysis-framework.md patterns

After creating the session file, update `sessions/.current-session` to track the active session filename.

## Confirmation Message:
Confirm sprint planning session started with:
- Sprint number and category
- Sprint goal and expected duration
- Team participants and capacity
- Key deliverables and success criteria
- Reference to SDLC v1.0 framework compliance

## Available Commands During Sprint Planning:
- `/project:session-update` - Log planning progress and decisions
- `/project:session-end` - Complete planning with sprint summary
- `/project:session-help` - Access planning guidance and checklists

## SDLC v1.0 Best Practices:
- Follow performance-first development principles
- Include failure prevention measures in planning
- Plan for comprehensive knowledge transfer
- Set clear quality gates and success criteria
- Reference failure-analysis-framework.md for risk mitigation