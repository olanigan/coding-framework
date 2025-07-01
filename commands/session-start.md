Start a new development session following SDLC v1.0 framework with integrated sprint planning and performance-first development.

## Session Creation Process:

1. **Generate Session Filename**: Create session file in `sessions/` using format:
   - With name: `YYYY-MM-DD-HHMM-[sprint-type]-[descriptive-name].md`
   - Without name: `YYYY-MM-DD-HHMM.md`
   
   **Sprint Type Categories** (SDLC v1.0 Framework):
   - `feature` - New functionality development (Sprint 1.x)
   - `infrastructure` - DevOps, deployment, configuration (Sprint 2.x)
   - `bug` - Bug fixes and patches (Sprint 3.x)
   - `research` - Spike, analysis, proof of concept (Sprint 4.x)
   - `maintenance` - Updates, dependencies, cleanup (Sprint 5.x)
   - `emergency` - Critical fixes requiring immediate attention (Sprint 9.x)
   - `sprint-planning` - Sprint kickoff and planning sessions
   - `performance` - Performance optimization work
   - `failure-analysis` - Three-strike rule failure analysis

2. **Session File Structure**: Initialize with comprehensive sections:

```markdown
# Development Session - [Date Time] - [Sprint Type] - [Name]

## Session Overview
- **Start Time**: [Timestamp]
- **Sprint Type**: [Category]
- **Estimated Duration**: [Ask user]
- **Priority Level**: [High/Medium/Low]
- **Related Sprint**: [If applicable]

## Goals & Acceptance Criteria
[Prompt user for specific, measurable goals]
- [ ] [Goal 1 with clear acceptance criteria]
- [ ] [Goal 2 with clear acceptance criteria]
- [ ] [Goal 3 with clear acceptance criteria]

## Pre-Development Checklist (SDLC v1.0)
- [ ] **Environment Setup**: Verify development environment parity
- [ ] **CORS Configuration**: Confirm all deployment domains configured
- [ ] **Test Suite**: Ensure tests are passing before starting
- [ ] **Branch Strategy**: Confirm working on correct branch
- [ ] **Dependencies**: Check for any pending updates or conflicts
- [ ] **Performance Baseline**: Document current performance metrics
- [ ] **Quality Gates**: Review applicable quality checkpoints

## Architecture & Approach
[Document planned approach and architecture decisions]

## TDD Setup (if applicable)
- [ ] **Test Environment**: Configure test database/environment
- [ ] **Testing Strategy**: Define test scenarios and coverage
- [ ] **CORS Testing**: Plan cross-origin request testing
- [ ] **Mock Services**: Identify external services to mock

## Progress Log
[Updates will be added here during development]

## Debugging Protocol Checkpoints (CLAUDE.md Integration)
- [ ] **Symptoms Analysis**: Document any issues encountered (5min)
- [ ] **Browser DevTools**: Check Network tab for failed requests (10min)
- [ ] **API Testing**: Direct CURL testing with proper headers (10min)
- [ ] **Configuration Review**: CORS settings, environment differences (15min)
- [ ] **Three-Strike Awareness**: Track failed attempts for failure analysis

## Session Rules & Guidelines
[Project-specific rules will be referenced here]

## Dependencies & External Services
[Document any external dependencies or services involved]

## Risk Assessment
[Identify potential risks and mitigation strategies]
```

3. **Project Rules Integration**: Check for project-specific rules:
   - Look for `.rules` directory and reference applicable guidelines
   - Check for `CLAUDE.md` and integrate relevant best practices
   - Apply descriptive naming conventions from project standards

4. **Environment Verification**: Perform initial checks:
   - Verify git repository status and branch
   - Check for existing session conflicts
   - Validate development environment setup
   - Confirm CORS configurations if web development

5. **Sprint Planning Integration**: If this is part of a larger sprint:
   - Reference existing sprint documentation
   - Link to relevant backlog items
   - Identify dependencies on other tasks
   - Set realistic time estimates

After creating the session file, update `sessions/.current-session` to track the active session filename.

## Confirmation Message:
Confirm the session has started with:
- Session name and estimated duration
- Sprint type and priority level
- Key goals and acceptance criteria
- Remind user of available commands:
  - `/project:session-update` - Log progress and checkpoint
  - `/project:session-debug` - Systematic debugging protocol
  - `/project:session-sprint` - Sprint management features
  - `/project:session-sprint-planning` - Start sprint planning session
  - `/project:session-performance` - Start performance optimization session
  - `/project:session-failure-analysis` - Start failure analysis session
  - `/project:session-end` - Complete session with delivery docs

## SDLC v1.0 Best Practices Integration:
- Use descriptive commit messages referencing the session
- Update session regularly at key checkpoints
- Document any unexpected discoveries or issues
- Maintain environment parity throughout development
- Test CORS configurations on all target domains
- Follow performance-first development (performance-standards.md)
- Apply three-strike rule for failure prevention
- Include quality gates and knowledge transfer sections
- Reference failure-analysis-framework.md for systematic learning