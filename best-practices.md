# Mega Agentic Coding Best Practices Guide - SDLC v1.0

A consolidated reference of best practices combining insights from CLAUDE.md, astroHalal, workerHalal projects, and the comprehensive SDLC v1.0 framework for performance-first development and systematic failure prevention.

## 🎯 Core Principles

### 1. Structured Development
- **Session-Driven Work**: Every development task should be wrapped in a session
- **Sprint Categorization**: Use numbered sprint types for organization (1.x features, 2.x infrastructure, etc.)
- **Checkpoint Documentation**: Regular progress updates with meaningful categorization
- **Knowledge Preservation**: Document decisions, lessons learned, and gotchas

### 2. Test-Driven Development (TDD)
- **Environment Parity**: Development must match production environments
- **CORS Validation**: Test all deployment domains in integration tests
- **Progressive Testing**: Unit → Integration → E2E → Performance
- **Objective Verification**: Use automated tools over manual testing

### 3. Systematic Problem Solving (SDLC v1.0)
- **Emergency Response Protocol**: Follow structured debugging phases (CLAUDE.md)
- **Documentation First**: Record symptoms before investigating
- **Root Cause Focus**: Don't just fix symptoms, eliminate causes
- **Prevention Mindset**: Always include prevention measures
- **Three-Strike Rule**: Mandatory failure analysis after 3 failed attempts (failure-analysis-framework.md)

### 4. Performance-First Development (performance-standards.md)
- **Performance Budgets**: Define performance targets before development
- **Measurement-Driven**: All performance claims backed by measurements
- **User-Centric Metrics**: Focus on metrics impacting user experience
- **Mandatory Standards**: API < 500ms, Page load < 2s, DB queries < 100ms

## 🏃 Sprint Planning Best Practices

### Sprint Categorization System (SDLC v1.0)
Based on astroHalal/workerHalal patterns and enhanced with SDLC v1.0 framework:

#### 1.x - Feature Sprints
- **Purpose**: New functionality development
- **Duration**: 1-2 weeks
- **Naming**: `1.x-component-feature-description`
- **Requirements**: Design docs, acceptance criteria, user stories
- **Example**: `1.3-auth-oauth-integration`

#### 2.x - Infrastructure Sprints  
- **Purpose**: DevOps, deployment, architecture improvements
- **Duration**: 1-3 weeks
- **Naming**: `2.x-infrastructure-component`
- **Requirements**: Architecture diagrams, deployment plans, rollback procedures
- **Example**: `2.1-ci-cd-github-actions`

#### 3.x - Bug Fix Sprints
- **Purpose**: Issue resolution and patches
- **Duration**: 3-5 days
- **Naming**: `3.x-bug-area-description`
- **Requirements**: Root cause analysis, regression prevention, testing plan
- **Example**: `3.2-auth-cors-configuration`

#### 4.x - Research Sprints
- **Purpose**: Investigation, proof of concepts, technology evaluation
- **Duration**: 1-2 weeks
- **Naming**: `4.x-research-topic`
- **Requirements**: Research report, recommendations, decision criteria
- **Example**: `4.1-framework-nextjs-migration`

#### 5.x - Maintenance Sprints
- **Purpose**: Updates, refactoring, cleanup, dependency management
- **Duration**: 1 week
- **Naming**: `5.x-maintenance-area`
- **Requirements**: Impact assessment, rollback plan, testing verification
- **Example**: `5.3-dependencies-security-updates`

#### 9.x - Emergency Sprints
- **Purpose**: Critical fixes requiring immediate attention
- **Duration**: Hours to 1 day
- **Naming**: `9.x-emergency-description`
- **Requirements**: Incident report, immediate mitigation, post-mortem plan
- **Example**: `9.1-production-api-timeout`

### Sprint Planning Guidelines

1. **Clear Objectives**: Define specific, measurable goals
2. **Acceptance Criteria**: Document what "done" means
3. **Risk Assessment**: Identify potential blockers and mitigation
4. **Dependency Mapping**: Understand upstream/downstream dependencies
5. **Resource Planning**: Allocate appropriate time and skills
6. **Success Metrics**: Define how to measure success

## 🚀 SDLC v1.0 Framework Integration

### Core Framework Documents
- **SDLC.md**: Master framework with sprint structure and performance standards
- **performance-standards.md**: Mandatory performance requirements and optimization strategies
- **failure-analysis-framework.md**: Three-strike rule implementation and prevention strategies

### Session Management (Enhanced)
- **sprint-planning-session.md**: Comprehensive sprint kickoff with risk assessment
- **performance-optimization-session.md**: Performance baseline and optimization tracking
- **failure-analysis-session.md**: Three-strike failure analysis and prevention

### Quality Gates Integration
All development work must pass these quality gates:
- [ ] **Performance Standards Met**: All performance-standards.md requirements achieved
- [ ] **Test Coverage**: Comprehensive testing (unit, integration, E2E, performance)
- [ ] **Code Quality**: Code review completed with no critical issues
- [ ] **Documentation Updated**: All changes documented and knowledge transferred
- [ ] **No Regressions**: No degradation in existing functionality
- [ ] **Acceptance Criteria**: All user story acceptance criteria verified

### Three-Strike Failure Prevention
When tasks fail 3 times, mandatory failure analysis includes:
1. **Root Cause Analysis**: Technical, process, and knowledge factors
2. **Prevention Strategy**: Immediate and long-term prevention measures
3. **Alternative Solution**: New approach with success criteria
4. **Knowledge Transfer**: Insights documented for team learning

**Reference**: failure-analysis-framework.md for complete process

### Performance-First Development Workflow
1. **Pre-Development**: Define performance budgets and baselines
2. **During Development**: Continuous performance monitoring
3. **Pre-Deployment**: Performance testing and validation
4. **Post-Deployment**: Real user monitoring and alerts

**Reference**: performance-standards.md for detailed requirements

## 🐛 Systematic Debugging Protocol

### Emergency Response Checklist (from CLAUDE.md)

#### Phase 1: Symptoms Analysis (5 minutes)
- **Document Impact**: User count affected, revenue impact, severity
- **Error Collection**: Gather all error messages, stack traces, logs
- **Timeline Establishment**: When did it start, what changed recently
- **Reproduction**: Can you reproduce the issue consistently

**Key Questions:**
- What were users trying to do?
- What should have happened vs. what actually happened?
- Is this affecting all users or specific segments?
- Are there any patterns (browser, device, location, time)?

#### Phase 2: Browser DevTools Analysis (10 minutes)
- **Network Tab**: Failed requests, HTTP status codes, CORS errors
- **Console Errors**: JavaScript errors, resource loading failures
- **Performance**: Timing issues, slow requests, memory leaks
- **Application State**: Cookies, local storage, service workers

**CORS Specific Checks:**
```bash
# Check preflight requests
# Look for Access-Control-Allow-Origin headers
# Verify request origin matches allowed origins
```

#### Phase 3: API Testing with CURL (10 minutes)
- **Direct API Validation**: Test endpoints independently of browser
- **CORS Header Testing**: Include origin headers in requests
- **Authentication Testing**: Verify tokens and permissions
- **Data Validation**: Check request/response formats

**CORS Testing Commands:**
```bash
# Test preflight
curl -H "Origin: https://app.domain.com" \
     -H "Access-Control-Request-Method: POST" \
     -H "Access-Control-Request-Headers: Content-Type,Authorization" \
     -X OPTIONS \
     https://api.domain.com/endpoint

# Test actual request
curl -H "Origin: https://app.domain.com" \
     -H "Content-Type: application/json" \
     -H "Authorization: Bearer token" \
     -X POST \
     -d '{"data": "test"}' \
     https://api.domain.com/endpoint
```

#### Phase 4: Configuration Review (15 minutes)
- **Environment Comparison**: Dev vs staging vs production configs
- **CORS Configuration**: Allowed origins, methods, headers
- **DNS and Infrastructure**: Domain resolution, SSL certificates
- **External Services**: Third-party service status and configuration

### Debugging Best Practices

1. **Progressive Approach**: Follow phases systematically
2. **Time Boxing**: Stick to time limits to avoid rabbit holes
3. **Documentation**: Record everything as you investigate
4. **Verification**: Always verify fixes work as expected
5. **Prevention**: Document how to prevent similar issues

## 📝 Session Management Excellence

### Session Naming Conventions
Format: `[timestamp]-[sprint-type]-[descriptive-name]`

Examples:
- `2025-01-15-1430-feature-oauth-integration`
- `2025-01-15-1630-bug-cors-misconfiguration`
- `2025-01-15-1830-infrastructure-docker-setup`

### Checkpoint Types and Usage

#### Milestone Checkpoints
- **When**: Major feature completion or significant progress
- **Documentation**: Achievement details, acceptance criteria met
- **Frequency**: At natural completion points

#### Daily Checkpoints
- **When**: End of working day or session
- **Documentation**: Summary of work done, next steps
- **Frequency**: At least once per day

#### Debug Checkpoints
- **When**: During or after debugging sessions
- **Documentation**: Root cause, solution, prevention measures
- **Frequency**: For each debugging effort

#### Blocker Checkpoints
- **When**: Encountering issues that prevent progress
- **Documentation**: Blocker description, impact, resolution plan
- **Frequency**: As soon as blockers are identified

### Session Quality Gates

Before ending any session:
- [ ] All goals documented with completion status
- [ ] Acceptance criteria verified and recorded
- [ ] Code quality metrics checked (linting, tests, coverage)
- [ ] Architecture decisions documented with rationale
- [ ] Knowledge transfer notes complete
- [ ] Follow-up tasks identified and prioritized

## 🔧 Environment & Configuration Management

### Environment Parity Rules
1. **Configuration Management**: Use environment variables for all config
2. **Dependency Versions**: Lock dependency versions across environments
3. **Feature Flags**: Use feature flags for environment-specific features
4. **Data Consistency**: Use representative data in staging
5. **Monitoring Alignment**: Same monitoring and alerting across environments

### CORS Configuration Best Practices
1. **Domain Whitelist**: Explicitly list allowed origins (never use *)
2. **Method Specification**: Only allow necessary HTTP methods
3. **Header Control**: Restrict allowed headers to required ones
4. **Credentials Handling**: Be explicit about credential support
5. **Testing Coverage**: Test CORS for all deployment domains

### Environment Testing Checklist
- [ ] Local development environment matches production
- [ ] All environment variables documented and configured
- [ ] CORS configured for all deployment domains
- [ ] SSL certificates valid and properly chained
- [ ] Database connections tested and performant
- [ ] External service integrations verified
- [ ] Monitoring and logging configured
- [ ] Error handling tested across environments

## 📋 Code Quality Standards

### Naming Conventions
Following astroHalal/workerHalal patterns:

#### Files and Directories
- **Components**: `PascalCase` for React components
- **Utilities**: `camelCase` for utility functions
- **Constants**: `UPPER_SNAKE_CASE` for constants
- **Directories**: `kebab-case` for directory names

#### Git Workflow
- **Branches**: `[sprint-type]/[description]` (e.g., `feature/oauth-integration`)
- **Commits**: Conventional commits format
  - `feat:` for new features
  - `fix:` for bug fixes
  - `docs:` for documentation
  - `refactor:` for code refactoring
  - `test:` for adding tests

### Testing Standards
1. **Unit Tests**: Minimum 80% coverage for business logic
2. **Integration Tests**: All API endpoints tested
3. **E2E Tests**: Critical user journeys covered
4. **Performance Tests**: Load testing for key scenarios
5. **Security Tests**: Vulnerability scanning and penetration testing

### Code Review Requirements
1. **Automated Checks**: All CI/CD checks must pass
2. **Peer Review**: At least one team member approval
3. **Documentation**: README and code comments updated
4. **Testing**: New code includes appropriate tests
5. **Security**: Security implications reviewed

## 🚀 Deployment & Delivery

### Pre-Deployment Checklist
- [ ] All tests passing in CI/CD pipeline
- [ ] Security scan completed with no critical issues
- [ ] Performance benchmarks met
- [ ] Database migrations tested and reversible
- [ ] Environment configuration verified
- [ ] Monitoring and alerting configured
- [ ] Rollback plan documented and tested
- [ ] Stakeholder approval obtained

### Deployment Strategy
1. **Blue-Green Deployment**: Zero-downtime deployments
2. **Feature Flags**: Gradual rollout with instant rollback
3. **Database Migrations**: Backward-compatible changes first
4. **Monitoring**: Real-time monitoring during deployment
5. **Verification**: Automated and manual verification post-deployment

### Post-Deployment Actions
- [ ] Health checks verified
- [ ] Performance metrics within expected ranges
- [ ] Error rates monitored for 24 hours
- [ ] User feedback collection active
- [ ] Documentation updated
- [ ] Team retrospective scheduled

## 📚 Knowledge Management

### Documentation Standards
1. **Decision Records**: Document architectural decisions with rationale
2. **API Documentation**: Keep API docs current with code changes
3. **Runbooks**: Operational procedures for common tasks
4. **Troubleshooting Guides**: Common issues and solutions
5. **Onboarding Docs**: Guide for new team members

### Knowledge Transfer Practices
1. **Session Documentation**: Comprehensive session summaries
2. **Code Comments**: Explain "why" not just "what"
3. **Pair Programming**: Share knowledge through collaboration
4. **Team Presentations**: Regular knowledge sharing sessions
5. **External Documentation**: Blog posts and conference talks

## 🔍 Monitoring & Observability (SDLC v1.0 Enhanced)

### Key Metrics to Track
1. **Application Performance**: Response time, throughput, error rate (performance-standards.md)
2. **Infrastructure Health**: CPU, memory, disk, network usage
3. **Business Metrics**: User engagement, conversion rates, revenue
4. **Security Events**: Failed logins, suspicious activities
5. **Development Velocity**: Deployment frequency, lead time, MTTR
6. **Quality Metrics**: Code coverage, technical debt, performance regression
7. **Learning Metrics**: Failure analysis effectiveness, prevention success rate

### Alerting Best Practices
1. **Actionable Alerts**: Only alert on issues requiring immediate action
2. **Alert Fatigue**: Avoid too many low-priority alerts
3. **Escalation Paths**: Clear escalation procedures for different severities
4. **Context Information**: Include relevant context in alert messages
5. **Alert Documentation**: Document what each alert means and how to respond

## 🎓 Continuous Improvement

### Retrospective Framework
1. **What Went Well**: Celebrate successes and effective practices
2. **What Could Improve**: Identify areas for enhancement
3. **Action Items**: Specific, measurable improvements to implement
4. **Experiments**: New practices to try in next iteration
5. **Metrics**: How to measure improvement success

### Learning Culture
1. **Blameless Post-Mortems**: Focus on system improvements, not individual blame
2. **Experiment Mindset**: Encourage trying new approaches
3. **Knowledge Sharing**: Regular team learning sessions
4. **External Learning**: Conference attendance, course enrollment
5. **Documentation**: Capture and share learnings

## 🚨 Emergency Response

### Incident Response Roles
1. **Incident Commander**: Coordinates response, communicates with stakeholders
2. **Technical Lead**: Leads technical investigation and resolution
3. **Communications Lead**: Manages internal and external communications
4. **Subject Matter Expert**: Provides specialized knowledge as needed

### Communication Templates

#### Initial Alert
```
🚨 INCIDENT: [Brief Description]
Severity: [Critical/High/Medium/Low]
Impact: [User impact description]
Started: [Time]
Incident Commander: [Name]
Updates: [Communication channel]
```

#### Status Update
```
📊 INCIDENT UPDATE: [Brief Description]
Current Status: [Investigation/Mitigation/Resolved]
Actions Taken: [What has been done]
Next Steps: [What's happening next]
ETA: [Expected resolution time]
```

#### Resolution Notice
```
✅ INCIDENT RESOLVED: [Brief Description]
Root Cause: [Brief root cause]
Fix Applied: [What was fixed]
Total Downtime: [Duration]
Post-Mortem: [When post-mortem will be conducted]
```

### Post-Incident Actions
1. **Immediate**: Verify resolution and monitor for recurrence
2. **24 Hours**: Conduct blameless post-mortem
3. **1 Week**: Implement prevention measures
4. **1 Month**: Review effectiveness of improvements

---

## 🎯 Quick Reference

### Daily Checklist (SDLC v1.0)
- [ ] Check current sprint status and priorities
- [ ] Review yesterday's session summary and performance metrics
- [ ] Start session with appropriate sprint type (reference SDLC.md)
- [ ] Apply performance-first development principles
- [ ] Update session at checkpoint intervals with quality gates
- [ ] Track any task failures for three-strike analysis
- [ ] End session with comprehensive summary and knowledge transfer
- [ ] Plan tomorrow's work based on session insights and performance data

### Weekly Checklist (SDLC v1.0)
- [ ] Review sprint progress and velocity against performance standards
- [ ] Conduct code quality audit with performance regression analysis
- [ ] Update project documentation and knowledge base
- [ ] Review and address technical debt with failure analysis insights
- [ ] Plan next sprint based on current learnings and performance data
- [ ] Assess any three-strike situations and schedule failure analysis

### Monthly Checklist (SDLC v1.0)
- [ ] Conduct team retrospective with SDLC framework effectiveness review
- [ ] Review and update best practices based on failure analysis findings
- [ ] Analyze development velocity trends and performance metrics
- [ ] Update project roadmap with performance and quality priorities
- [ ] Celebrate team achievements and learning from systematic improvement
- [ ] Review performance-standards.md and failure-analysis-framework.md effectiveness

---

*"Excellence is not an act, but a habit. We are what we repeatedly do."* - Aristotle

## 📚 SDLC v1.0 Framework References

### Core Documents
- **[SDLC.md](./SDLC.md)**: Master framework document with sprint structure and development standards
- **[performance-standards.md](./performance-standards.md)**: Mandatory performance requirements and optimization strategies
- **[failure-analysis-framework.md](./failure-analysis-framework.md)**: Three-strike rule implementation and systematic learning

### Session Templates
- **[templates/sprint-planning-session.md](./templates/sprint-planning-session.md)**: Comprehensive sprint kickoff template
- **[templates/performance-optimization-session.md](./templates/performance-optimization-session.md)**: Performance work template
- **[templates/failure-analysis-session.md](./templates/failure-analysis-session.md)**: Three-strike failure analysis template

### Commands Integration
- **[commands/session-sprint-planning.md](./commands/session-sprint-planning.md)**: Sprint planning session command
- **[commands/session-performance.md](./commands/session-performance.md)**: Performance optimization session command
- **[commands/session-failure-analysis.md](./commands/session-failure-analysis.md)**: Failure analysis session command

This best practices guide integrates with the complete SDLC v1.0 framework and should be updated regularly based on team learnings, failure analysis insights, and performance optimization discoveries.