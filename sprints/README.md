# Sprint Documentation Guide

This directory contains all sprint-related documentation organized by status and sprint phases, following the SDLC v1.0 framework.

## Directory Structure

### Active Sprints
- `active/` - Currently in-progress sprints
  - Follow SDLC v1.0 framework for all sprint work
  - Each sprint has planning/ → implementation/ → retrospective/ structure

### Completed Sprints
- `completed/` - Finished sprints with comprehensive retrospectives
  - Complete documentation including lessons learned and knowledge transfer
  - Performance metrics and achievement analysis

### Backlog
- `backlog/` - Future work and planning
  - `product-backlog.md` - Prioritized feature backlog
  - `technical-debt.md` - Technical improvement items

## Sprint Structure

Following the SDLC v1.0 framework, each sprint directory follows this structure:

```
sprint-{number}-{name}/
├── planning/
│   ├── README.md           # Sprint overview and objectives
│   ├── prd.md             # Product requirements document
│   └── tasks.md           # Detailed task breakdown with estimates
├── implementation/
│   ├── task-{id}-{name}.md # Individual task documentation
│   ├── technical-specs.md  # Technical specifications and decisions
│   ├── performance-benchmarks.md # Performance targets and results
│   └── testing-guide.md    # Testing procedures and validation
└── retrospective/
    ├── completion-report.md # Final status and deliverables
    ├── retrospective.md     # Comprehensive sprint retrospective
    └── lessons-learned.md   # Key insights and process improvements
```

## Sprint Naming Convention

Based on proven patterns from battle-tested projects:

### Sprint Categories
- **1.x** - Feature Development Sprints
- **2.x** - Infrastructure & DevOps Sprints
- **3.x** - Bug Fix & Patch Sprints
- **4.x** - Research & Proof of Concept Sprints
- **5.x** - Maintenance & Optimization Sprints
- **9.x** - Emergency Response Sprints

### Naming Format
`sprint-{category}-{descriptive-name}`

Examples:
- `sprint-1.1-user-authentication`
- `sprint-2.3-ci-cd-pipeline`
- `sprint-3.2-cors-configuration-fix`
- `sprint-4.1-framework-evaluation`
- `sprint-5.2-dependency-updates`
- `sprint-9.1-production-outage`

## Sprint Framework Standards

### Performance Targets
Following SDLC v1.0 performance-first development:
- **API Response Time**: < 500ms end-to-end
- **Page Load Time**: < 2 seconds initial load
- **Database Queries**: < 100ms execution time
- **Build Time**: < 30 seconds for production builds

### Quality Gates
All sprints must meet these criteria before completion:
- [ ] All acceptance criteria met
- [ ] Performance benchmarks achieved
- [ ] Code review completed
- [ ] Documentation updated
- [ ] Tests passing (unit, integration, performance)
- [ ] Systematic debugging protocol followed for all issues

### Documentation Requirements
1. **Sprint Planning**: Clear objectives, success criteria, timeline
2. **Daily Progress**: Key decisions, blockers, solutions discovered
3. **Sprint Retrospective**: Comprehensive analysis with metrics and lessons
4. **Technical Documentation**: Architecture decisions, performance metrics
5. **Knowledge Transfer**: Context for next sprint, team learning artifacts

## Sprint Planning Template

Use this template when creating new sprints:

```markdown
# Sprint X.x: [Sprint Name] - Planning Document

## 🎯 Sprint Objectives
- **Primary Goal**: [Main deliverable/outcome]
- **Secondary Goals**: [Supporting objectives]
- **Success Criteria**: [Measurable outcomes]

## 📋 Product Backlog Items (PBI)
1. **PBI-01**: [Title] - [Priority: Critical/High/Medium/Low]
   - **User Story**: As a [user], I want [goal] so that [benefit]
   - **Acceptance Criteria**: [Specific, measurable requirements]
   - **Effort Estimate**: [Hours/days]
   - **Dependencies**: [Other tasks/external dependencies]

## 🛠️ Technical Approach
- **Architecture Decisions**: [Key technical choices]
- **Risk Assessment**: [Potential challenges and mitigation]
- **Performance Requirements**: [Specific metrics to achieve]
- **Quality Gates**: [Validation checkpoints]

## 📅 Timeline
- **Sprint Duration**: [Start date - End date]
- **Key Milestones**: [Major checkpoints]
- **Daily Standup**: [Time and format]
- **Sprint Review**: [Demo and validation session]
```

## Sprint Retrospective Template

Use this template for sprint completion:

```markdown
# Sprint X.x Retrospective - [Sprint Name]

**Date**: [Completion Date]  
**Duration**: [Actual sprint length]  
**Status**: ✅ COMPLETED / ⚠️ PARTIAL / ❌ FAILED  

## 🎯 Sprint Goals Achievement

### Primary Objectives
- [x] **Goal 1**: [Description] - [Status and notes]
- [x] **Goal 2**: [Description] - [Status and notes]
- [ ] **Goal 3**: [Description] - [Reason if not completed]

### Success Metrics
| Metric | Target | Achieved | Status |
|--------|--------|----------|--------|
| Performance | < 500ms API | [Actual] | [Status] |
| Feature Coverage | 100% requirements | [Actual] | [Status] |
| Code Quality | Zero critical issues | [Actual] | [Status] |

## 🏆 Major Wins
[Document significant achievements and successes]

## ⚠️ Challenges & Areas for Improvement
[Document challenges faced and improvement opportunities]

## 🎓 Key Learnings
[Document technical and process insights gained]

## 📋 Action Items for Future Sprints
[List specific actions for next sprint]
```

## Integrating with Sessions

All development work within sprints should use the session management framework:
- Start sessions with sprint context: `/project:session-start feature-[sprint-task]`
- Update progress regularly: `/project:session-update milestone "[achievement]"`
- End sessions with knowledge transfer: `/project:session-end`

## SDLC Framework Integration

This sprint documentation follows the SDLC v1.0 framework principles:

### Sprint Success Patterns
1. **Clear Objectives**: Sprints with specific, measurable goals
2. **Performance Focus**: Performance as first-class requirement
3. **Documentation Excellence**: Comprehensive documentation for knowledge transfer
4. **Systematic Debugging**: CLAUDE.md protocol for all technical issues
5. **Quality Gates**: Multiple validation checkpoints

### Three-Strike Rule
After 3 failed attempts at any sprint task:
1. Conduct formal failure analysis
2. Document root causes (technical, process, knowledge gaps)
3. Implement prevention measures
4. Update documentation and processes

### Knowledge Management
- **Session Documentation**: All development work documented in sessions/
- **Sprint Retrospectives**: Detailed analysis with metrics and lessons learned
- **Technical Documentation**: Architecture decisions and performance benchmarks
- **Process Improvements**: Continuous refinement based on sprint learnings

## Quick Reference

### Creating a New Sprint
1. Create directory: `sprints/active/sprint-X.x-[name]/`
2. Add planning documents using templates
3. Move to implementation phase during development
4. Complete with retrospective and move to completed/

### Sprint Status Transitions
- **Planning → Active**: When sprint starts
- **Active → Review**: When development complete
- **Review → Completed**: After retrospective and knowledge transfer
- **Any → Blocked**: If external dependencies prevent progress

### Performance Benchmarking
Track these metrics throughout the sprint:
- API response times (target: < 500ms)
- Database query performance (target: < 100ms)
- Frontend load times (target: < 2 seconds)
- Build performance (target: < 30 seconds)

---

**Framework Version**: SDLC v1.0  
**Last Updated**: July 1, 2025  
**Next Review**: After first sprint completion