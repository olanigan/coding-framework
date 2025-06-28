Manage and enforce project-specific rules and guidelines integration with session management system.

## Rules Management Functions:

### Command Usage:
- `/project:session-rules init` - Initialize project rules system
- `/project:session-rules check` - Validate current session against project rules
- `/project:session-rules enforce [rule-category]` - Apply specific rule category
- `/project:session-rules update [rule-file]` - Update specific rule file
- `/project:session-rules audit` - Comprehensive rules compliance audit

## Project Rules System Structure:

### Rules Directory Structure:
```
.rules/
├── project.md           # Project-specific guidelines
├── sdlc.md             # Software Development Lifecycle rules
├── architecture.md     # Architecture and design patterns
├── testing.md          # Testing standards and requirements
├── security.md         # Security guidelines and requirements
├── deployment.md       # Deployment and infrastructure rules
├── documentation.md    # Documentation standards
└── cloudflare.md       # Platform-specific rules (if applicable)
```

## Rules Initialization:

When initializing rules system (`/project:session-rules init`):

1. **Detect Existing Rules**: Check for `.rules` directory and existing rule files
2. **Create Missing Structure**: Generate standard rule file templates
3. **Project Type Detection**: Identify project framework and platform
4. **Rule Template Selection**: Choose appropriate templates based on project type

### Default Project Rules Template:
```markdown
# Project-Specific Development Rules

## Project Overview
- **Project Name**: [Auto-detected from package.json or directory]
- **Project Type**: [Frontend/Backend/Fullstack/Library/CLI]
- **Framework**: [React/Vue/Angular/Next.js/Astro/etc.]
- **Platform**: [Web/Mobile/Desktop/Server/Cloudflare Workers]

## Sprint Management Rules

### Sprint Categorization
- **Feature Sprints (1.x)**: New functionality development
  - Naming: `1.x-feature-description`
  - Duration: 1-2 weeks
  - Requirements: Design docs, acceptance criteria
  
- **Infrastructure Sprints (2.x)**: DevOps and architecture
  - Naming: `2.x-infrastructure-component`
  - Duration: 1-3 weeks
  - Requirements: Architecture diagrams, deployment plans
  
- **Bug Fix Sprints (3.x)**: Issue resolution
  - Naming: `3.x-bug-category`
  - Duration: 3-5 days
  - Requirements: Root cause analysis, regression prevention
  
- **Research Sprints (4.x)**: Investigation and proof of concepts
  - Naming: `4.x-research-topic`
  - Duration: 1-2 weeks
  - Requirements: Research report, recommendations
  
- **Maintenance Sprints (5.x)**: Updates and cleanup
  - Naming: `5.x-maintenance-area`
  - Duration: 1 week
  - Requirements: Impact assessment, rollback plan
  
- **Emergency Sprints (9.x)**: Critical fixes
  - Naming: `9.x-emergency-description`
  - Duration: Hours to 1 day
  - Requirements: Incident report, immediate mitigation

### Task Naming Conventions
- **Feature Tasks**: `feat: descriptive action in present tense`
- **Bug Fixes**: `fix: resolve specific issue description`
- **Infrastructure**: `infra: infrastructure component or update`
- **Documentation**: `docs: documentation area or update`
- **Testing**: `test: testing area or coverage improvement`
- **Refactoring**: `refactor: component or system being refactored`

## Development Standards

### Session Management
- **Session Naming**: Use sprint type prefix in session names
- **Checkpoint Frequency**: Update session every 2-4 hours of work
- **Documentation Required**: All significant decisions must be documented
- **Knowledge Transfer**: Each session must include lessons learned

### Code Quality Requirements
- **Linting**: Must pass project linting standards
- **Type Checking**: TypeScript projects require clean type checking
- **Testing**: Minimum test coverage requirements
- **Performance**: Performance budgets and monitoring
- **Security**: Security scanning and vulnerability assessment

### Git and Version Control
- **Branch Naming**: Follow sprint/task naming conventions
- **Commit Messages**: Conventional commits format required
- **Pull Requests**: Template and review requirements
- **Code Review**: Minimum reviewer requirements

## Technology Stack Rules
[Project-specific technology guidelines]

## Architecture Patterns
[Architectural decisions and patterns]

## Testing Requirements
[Testing standards and coverage requirements]

## Deployment Rules
[Deployment procedures and requirements]

## Security Guidelines
[Security requirements and best practices]
```

## Rules Compliance Checking:

When checking rules compliance (`/project:session-rules check`):

1. **Session Compliance**:
   - Session naming follows project conventions
   - Required documentation sections are present
   - Sprint alignment and categorization
   - Knowledge transfer completeness

2. **Code Quality Compliance**:
   - Linting and formatting standards
   - Type checking (if applicable)
   - Test coverage requirements
   - Performance criteria

3. **Process Compliance**:
   - Git workflow adherence
   - Documentation standards
   - Review requirements
   - Deployment checklist

**Compliance Report Format**:
```markdown
### Rules Compliance Report - [Timestamp]

#### Session Compliance
- **Naming Convention**: ✅ Follows sprint type pattern
- **Documentation**: ⚠️ Missing architecture decisions section
- **Sprint Alignment**: ✅ Properly categorized as feature sprint
- **Knowledge Transfer**: ✅ Lessons learned documented

#### Code Quality
- **Linting**: ✅ All files pass linting checks
- **Type Checking**: ❌ 3 type errors found in src/components/
- **Test Coverage**: ⚠️ 78% coverage, target is 80%
- **Performance**: ✅ Bundle size within limits

#### Process Compliance
- **Git Workflow**: ✅ Feature branch from main
- **Commit Messages**: ✅ Conventional commits format
- **Documentation**: ⚠️ API documentation needs update
- **Review Process**: ✅ PR template followed

#### Violations Found
1. **Type Errors** (High Priority):
   - File: src/components/UserProfile.tsx:45
   - Issue: Property 'email' is possibly undefined
   - Action: Add null check or optional chaining

2. **Test Coverage** (Medium Priority):
   - Coverage: 78% (target: 80%)
   - Missing: Integration tests for payment flow
   - Action: Add payment integration tests

#### Recommendations
- Fix type errors before session completion
- Add missing integration tests
- Update API documentation with new endpoints
```

## Rule Enforcement:

When enforcing specific rules (`/project:session-rules enforce [rule-category]`):

### Available Rule Categories:
- **naming**: Enforce naming conventions
- **testing**: Apply testing requirements
- **security**: Security guidelines compliance
- **performance**: Performance standards
- **documentation**: Documentation requirements
- **git**: Git workflow enforcement

### Enforcement Actions:
1. **Automated Fixes**: Apply automated corrections where possible
2. **Warning Generation**: Flag violations that require manual attention
3. **Blocker Identification**: Identify issues that prevent session completion
4. **Guidance Provision**: Provide specific steps to achieve compliance

## Integration with Session Commands:

### Session Start Integration:
- Automatically apply project rules to new sessions
- Generate rule-compliant session templates
- Validate sprint categorization
- Check for rule file updates

### Session Update Integration:
- Validate updates against naming conventions
- Check code quality requirements
- Verify documentation standards
- Assess compliance with process rules

### Session End Integration:
- Comprehensive rules compliance audit
- Generate compliance report
- Identify rule violations for future improvement
- Update project rules based on lessons learned

## Rules Maintenance:

### Rule File Updates:
- Track changes to rule files
- Version control for rule modifications
- Team notification of rule changes
- Migration guides for rule updates

### Continuous Improvement:
- Collect feedback on rule effectiveness
- Identify common rule violations
- Suggest rule improvements based on session patterns
- Update rules based on project evolution

## Platform-Specific Rules Integration:

### Cloudflare Workers Projects:
- Worker-specific development patterns
- Durable Objects best practices
- KV storage guidelines
- Environment configuration rules

### Frontend Framework Rules:
- React/Vue/Angular specific patterns
- Component architecture guidelines
- State management rules
- Performance optimization requirements

### Backend Service Rules:
- API design guidelines
- Database interaction patterns
- Security implementation requirements
- Monitoring and logging standards

## Rule Templates by Project Type:

### Next.js/React Projects:
- Component naming and structure
- State management patterns
- API route conventions
- Performance optimization rules

### Astro Projects:
- Island architecture guidelines
- Static site generation rules
- Component hydration patterns
- Build optimization requirements

### Node.js Backend:
- API design standards
- Error handling patterns
- Database interaction rules
- Security implementation guidelines

## Custom Rule Definition:

Allow projects to define custom rules:

```markdown
## Custom Project Rules

### Database Interaction
- All database queries must use prepared statements
- Connection pooling required for production
- Query timeout limits: 5 seconds for reads, 10 seconds for writes

### API Design
- RESTful resource naming required
- JSON schema validation for all endpoints
- Rate limiting implementation mandatory
- API versioning strategy must be followed

### Component Architecture
- Maximum component file size: 200 lines
- Props interface must be exported
- Component must have TypeScript documentation
- Unit tests required for complex logic
```

## Rules Violation Handling:

### Severity Levels:
- **Critical**: Blocks session completion
- **High**: Requires immediate attention
- **Medium**: Should be addressed before delivery
- **Low**: Improvement opportunity

### Resolution Guidance:
- Specific steps to fix violations
- Links to relevant documentation
- Code examples and templates
- Tool recommendations