# Development Session - [Date Time] - feature - [descriptive-name]

## Session Overview
- **Start Time**: [Timestamp]
- **Sprint Type**: Feature Development
- **Estimated Duration**: [2-4 hours]
- **Priority Level**: [High/Medium/Low]
- **Related Sprint**: [Sprint number if applicable]

## Goals & Acceptance Criteria
- [ ] **Primary Goal**: [Specific, measurable goal with clear acceptance criteria]
- [ ] **Secondary Goal**: [Additional goal if applicable]
- [ ] **Technical Goal**: [Technical implementation goal]
- [ ] **Performance Goal**: [Performance targets - API < 500ms, UI < 2s load]

## Pre-Development Checklist
- [ ] **Environment Setup**: Verify development environment parity
- [ ] **CORS Configuration**: Confirm all deployment domains configured
- [ ] **Test Suite**: Ensure tests are passing before starting
- [ ] **Branch Strategy**: Feature branch created from main/develop
- [ ] **Dependencies**: Check for any pending updates or conflicts
- [ ] **Performance Baseline**: Current performance metrics documented

## Architecture & Approach
### Design Decisions
- **Pattern**: [Architecture pattern to follow]
- **Components**: [Components to create/modify]
- **Data Flow**: [How data will flow through the system]
- **State Management**: [State management approach]

### Technical Approach
- **Implementation Strategy**: [Step-by-step approach]
- **Code Organization**: [How code will be structured]
- **Reusability**: [Reusable components/utilities to create]
- **Performance Considerations**: [Optimization strategies]

## TDD Setup
- [ ] **Test Strategy**: Define test scenarios and expected outcomes
- [ ] **Unit Tests**: Plan unit test coverage for new components
- [ ] **Integration Tests**: Identify integration points to test
- [ ] **E2E Tests**: User journey tests to implement
- [ ] **Test Data**: Prepare test data and mocks

## Progress Log
### [Time] - Initial Setup
- Environment configured and verified
- Dependencies installed and up to date
- Test suite running successfully

### [Time] - Implementation Start
- [Progress notes will be added here]

## Debugging Protocol Checkpoints (CLAUDE.md)
If any issues arise, follow systematic debugging protocol:

- [ ] **Symptoms Analysis**: Document any issues encountered (5min)
  - User impact assessment
  - Error frequency analysis
  - Recent deployment correlation

- [ ] **Browser DevTools**: Check Network tab for failed requests (10min)
  - Console error analysis
  - Failed request identification
  - CORS pattern detection

- [ ] **API Testing**: Direct CURL testing with proper headers (10min)
  - Backend log verification
  - Server response isolation
  - Database query validation

- [ ] **Configuration Review**: CORS settings, environment differences (15min)
  - Environment variable verification
  - Framework-specific settings

## Session Rules & Guidelines
### Coding Standards
- Follow project ESLint/Prettier configuration
- Use TypeScript for type safety
- Implement proper error handling
- Add comprehensive JSDoc comments

### Git Workflow
- Commit frequently with descriptive messages
- Use conventional commits format
- Keep commits atomic and focused
- Reference session documentation in commit messages

### Performance Requirements
- API endpoints: < 500ms response time
- Page load: < 2 seconds
- Component render: < 100ms
- Database queries: < 100ms

## Dependencies & External Services
- **NPM Packages**: [List any new packages to be added]
- **APIs**: [External APIs to integrate]
- **Services**: [Third-party services involved]

## Risk Assessment
- **Technical Risks**: [Potential technical challenges]
- **Timeline Risks**: [Factors that could delay completion]
- **Mitigation**: [How to address identified risks]
- **Three-Strike Rule**: If any task fails 3 times, conduct formal failure analysis

## Quality Gates
- [ ] **Functionality**: All acceptance criteria met
- [ ] **Performance**: Performance targets achieved
- [ ] **Code Quality**: Code review passed
- [ ] **Testing**: All tests passing
- [ ] **Documentation**: Component documentation updated
- [ ] **Accessibility**: WCAG compliance verified

## Knowledge Transfer Notes
[Important insights for future developers will be documented here]
- **Architecture Decisions**: [Key technical choices and rationale]
- **Performance Optimizations**: [Techniques used and results]
- **Common Issues**: [Problems encountered and solutions]
- **Best Practices**: [Patterns that worked well]

## Session Completion Checklist
- [ ] **Code Complete**: All functionality implemented
- [ ] **Tests Passing**: All automated tests passing
- [ ] **Performance Verified**: Meets performance requirements
- [ ] **Documentation Updated**: README and component docs current
- [ ] **Branch Ready**: Ready for PR/merge
- [ ] **Knowledge Captured**: Key learnings documented

## Next Steps
[Action items for continuation will be listed here]
- **Immediate**: [Tasks to complete in next session]
- **Follow-up**: [Related tasks for future sessions]
- **Dependencies**: [What other work depends on this]