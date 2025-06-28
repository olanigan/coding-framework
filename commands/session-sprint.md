Manage sprint planning and coordination for development sessions with integrated project management capabilities.

## Sprint Management Functions:

### Command Usage:
- `/project:session-sprint create [sprint-name]` - Create new sprint with backlog
- `/project:session-sprint status` - View current sprint status and progress
- `/project:session-sprint update [notes]` - Update sprint progress and milestones
- `/project:session-sprint tasks` - Manage sprint tasks and priorities
- `/project:session-sprint complete` - Complete sprint with retrospective

## Sprint Creation Process:

When creating a new sprint (`/project:session-sprint create [sprint-name]`):

1. **Sprint Classification**: Determine sprint type based on astroHalal/workerHalal patterns:
   - **Feature Sprint** (1.x series): New functionality development
   - **Infrastructure Sprint** (2.x series): DevOps, deployment, architecture
   - **Bug Fix Sprint** (3.x series): Bug fixes and patches
   - **Research Sprint** (4.x series): Spikes, analysis, proof of concepts
   - **Maintenance Sprint** (5.x series): Updates, refactoring, cleanup
   - **Emergency Sprint** (9.x series): Critical fixes and hotfixes

2. **Sprint File Generation**: Create `sprints/[sprint-type]-[YYYY-MM-DD]-[name].md`

```markdown
# Sprint [Number] - [Type] - [Name]
**Created**: [Timestamp]
**Sprint Type**: [Classification]
**Estimated Duration**: [Duration]
**Priority Level**: [High/Medium/Low]

## Sprint Overview
### Objectives
- [ ] [Primary objective with acceptance criteria]
- [ ] [Secondary objective with acceptance criteria]
- [ ] [Tertiary objective with acceptance criteria]

### Success Metrics
- **Functional**: [Measurable functional outcomes]
- **Technical**: [Technical quality metrics]
- **Business**: [Business value delivered]

## Sprint Backlog

### High Priority Tasks
- [ ] **[Task ID]**: [Task description]
  - **Effort**: [Story points/hours]
  - **Assignee**: [Developer/Team]
  - **Dependencies**: [Blocking/blocked by]
  - **Acceptance Criteria**: [Clear criteria]

### Medium Priority Tasks
- [ ] **[Task ID]**: [Task description]
  - **Effort**: [Story points/hours]
  - **Dependencies**: [Blocking/blocked by]

### Low Priority Tasks (Nice to Have)
- [ ] **[Task ID]**: [Task description]
  - **Effort**: [Story points/hours]

## Technical Architecture

### Architecture Decisions
- **Decision**: [What needs to be decided]
- **Options**: [Available approaches]
- **Recommendation**: [Preferred approach and rationale]

### Technology Stack
- **Frontend**: [Technologies and frameworks]
- **Backend**: [Technologies and frameworks]
- **Database**: [Database technologies]
- **Infrastructure**: [Deployment and hosting]
- **Testing**: [Testing frameworks and approaches]

## Environment & Configuration

### Development Environment
- [ ] **Local Setup**: Environment parity verified
- [ ] **CORS Configuration**: All domains configured
- [ ] **Test Data**: Representative data available
- [ ] **External Services**: Mocks/staging configured

### Deployment Pipeline
- [ ] **Staging Environment**: Configured and tested
- [ ] **Production Environment**: Ready for deployment
- [ ] **CI/CD Pipeline**: Automated testing and deployment
- [ ] **Monitoring**: Logging and alerting configured

## Risk Assessment

### Technical Risks
- **Risk**: [Description]
  - **Probability**: [High/Medium/Low]
  - **Impact**: [High/Medium/Low]
  - **Mitigation**: [Mitigation strategy]

### Project Risks
- **Risk**: [Description]
  - **Mitigation**: [Mitigation strategy]

## Sprint Timeline

### Week 1
- [ ] [Milestone 1]
- [ ] [Milestone 2]

### Week 2
- [ ] [Milestone 3]
- [ ] [Milestone 4]

## Quality Assurance

### Testing Strategy
- [ ] **Unit Tests**: [Coverage targets and approach]
- [ ] **Integration Tests**: [API and service testing]
- [ ] **E2E Tests**: [User journey testing]
- [ ] **Performance Tests**: [Load and stress testing]
- [ ] **Security Tests**: [Security scanning and validation]

### Code Quality
- [ ] **Linting**: Automated code style checking
- [ ] **Type Checking**: Static type analysis
- [ ] **Code Review**: Peer review process
- [ ] **Documentation**: Code and API documentation

## Sprint Progress Log
[Updates will be added here during sprint execution]

## Dependencies & External Coordination
- **Upstream Dependencies**: [What we're waiting for]
- **Downstream Dependencies**: [What others are waiting for]
- **External Teams**: [Coordination needed]
- **Third-party Services**: [External integrations]

## Retrospective Planning
- **What to Measure**: [Key metrics for retrospective]
- **Feedback Channels**: [How to collect feedback]
- **Improvement Areas**: [Areas to focus on]
```

## Sprint Status Monitoring:

When checking sprint status (`/project:session-sprint status`):

1. **Progress Overview**:
   - Sprint timeline and milestones
   - Task completion percentage
   - Blocked/at-risk items
   - Velocity tracking

2. **Current Sprint Health**:
   - On track/Behind/Ahead of schedule
   - Resource utilization
   - Quality metrics
   - Risk status

3. **Active Sessions**:
   - Current development sessions
   - Session alignment with sprint goals
   - Resource allocation

## Sprint Task Management:

When managing tasks (`/project:session-sprint tasks`):

1. **Task Prioritization**:
   - MoSCoW method (Must/Should/Could/Won't)
   - Story point estimation
   - Dependency mapping
   - Resource allocation

2. **Task Status Tracking**:
   - Not Started/In Progress/Review/Complete
   - Blocker identification and resolution
   - Effort estimation vs. actual
   - Quality gate compliance

## Sprint Updates:

When updating sprint progress (`/project:session-sprint update [notes]`):

1. **Progress Documentation**:
   - Milestone achievements
   - Task completions
   - Blocker resolutions
   - Risk updates

2. **Velocity Tracking**:
   - Story points completed
   - Time invested vs. estimated
   - Quality metrics
   - Team capacity utilization

## Sprint Completion:

When completing a sprint (`/project:session-sprint complete`):

1. **Sprint Retrospective**:
   - Goal achievement assessment
   - Quality metrics review
   - Process effectiveness analysis
   - Lessons learned documentation

2. **Delivery Documentation**:
   - Feature completeness report
   - Quality assurance summary
   - Deployment readiness checklist
   - Knowledge transfer documentation

3. **Next Sprint Planning**:
   - Carry-over tasks identification
   - Capacity planning for next sprint
   - Backlog refinement
   - Risk assessment update

## Integration with Session Commands:

- **Start Session**: Automatically link sessions to active sprint
- **Update Session**: Include sprint progress in session updates
- **End Session**: Update sprint status with session outcomes
- **Delivery Docs**: Generate sprint deliverables

## Best Practices Integration:

- **TDD Compliance**: Ensure test-first development
- **CORS Validation**: Verify cross-origin configurations
- **Environment Parity**: Maintain consistency across environments
- **Documentation**: Keep knowledge transfer current
- **Security**: Include security considerations in all tasks

## Sprint Naming Conventions:

Based on astroHalal/workerHalal patterns:
- **Feature Sprints**: `1.1-user-authentication`, `1.2-payment-integration`
- **Infrastructure**: `2.1-docker-setup`, `2.2-ci-cd-pipeline`
- **Bug Fixes**: `3.1-login-bug-fixes`, `3.2-performance-issues`
- **Research**: `4.1-framework-evaluation`, `4.2-architecture-analysis`
- **Maintenance**: `5.1-dependency-updates`, `5.2-code-cleanup`
- **Emergency**: `9.1-security-patch`, `9.2-production-hotfix`