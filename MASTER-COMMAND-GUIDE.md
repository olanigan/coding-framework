# Master Command Usage Guide 🎯 - SDLC v1.0
*The Complete Reference for SDLC v1.0 Framework Session Management*

> **Use this guide to determine which commands to use in any development scenario with performance-first development and systematic failure prevention**

## 🚀 Quick Start Decision Tree

### 1. **First Question: What's the project state?**

```
Is this a NEW project?
├── YES → Go to [New Project Setup](#new-project-setup)
└── NO → Is this an EXISTING project?
    ├── YES → Go to [Existing Project Assessment](#existing-project-assessment)
    └── EMERGENCY → Go to [Emergency Response](#emergency-response)
```

### 2. **Second Question: What are you trying to do?**

```
What's your goal today?
├── Start development work → [Development Sessions](#development-sessions)
├── Fix a bug or issue → [Bug Fixing Workflow](#bug-fixing-workflow)  
├── Research/investigate → [Research Sessions](#research-sessions)
├── Infrastructure work → [Infrastructure Sessions](#infrastructure-sessions)
├── Maintenance tasks → [Maintenance Sessions](#maintenance-sessions)
├── Sprint planning → [Sprint Planning Sessions](#sprint-planning-sessions)
├── Performance optimization → [Performance Sessions](#performance-sessions)
├── Failure analysis → [Failure Analysis Sessions](#failure-analysis-sessions)
└── Emergency fix → [Emergency Response](#emergency-response)
```

---

## 📊 Project State Assessment Matrix

### New Project Setup

**Scenario**: Starting a brand new project from scratch

**Commands to Use**:
```bash
# 1. Initialize the session system
/project:session-rules init

# 2. Start your first session
/project:session-start feature-project-initialization

# 3. Create your first sprint
/project:session-sprint create feature-foundation-setup

# 4. Update progress as you work
/project:session-update milestone "Project structure created"

# 5. End session with comprehensive docs
/project:session-end
```

**What this does**:
- Creates `.rules/` directory with project guidelines
- Sets up session management structure
- Establishes sprint planning foundation
- Documents initial architecture decisions

---

### Existing Project Assessment

**Scenario**: Working on a project that already exists but may not have session management

**Step 1: Assess Current State**
```bash
# Check if project has session system
# Look for: commands/, sessions/, .rules/, templates/

# If missing → Initialize
/project:session-rules init

# If present → Check compliance
/project:session-rules check
```

**Step 2: Determine Project Phase**
```bash
# If project has active development
/project:session-sprint status

# If no active sprint
/project:session-sprint create [appropriate-type]

# If unclear what to work on
/project:session-current  # Check if there's an active session
```

**Step 3: Start Appropriate Session**
```bash
# Based on what you need to do:
/project:session-start [type]-[description]
```

---

## 🔄 Development Workflow Scenarios

### Scenario 1: Brand New Project (Day 1)

**Commands Sequence**:
```bash
# 1. Project initialization
/project:session-rules init

# 2. Create foundation sprint
/project:session-sprint create 1.1-foundation-project-setup

# 3. Start development session
/project:session-start feature-project-foundation

# 4. Work and update regularly
/project:session-update milestone "Package.json and basic structure complete"
/project:session-update daily "Core dependencies installed and configured"

# 5. End session
/project:session-end

# 6. Complete sprint when foundation is done
/project:session-sprint complete
```

### Scenario 2: Existing Project, No Session System

**Commands Sequence**:
```bash
# 1. Assess and initialize
/project:session-rules init

# 2. Check project compliance
/project:session-rules check

# 3. Start with assessment session
/project:session-start research-codebase-analysis

# 4. Document findings
/project:session-update milestone "Codebase analysis complete"
/project:session-update review "Architecture documented, technical debt identified"

# 5. End analysis session
/project:session-end

# 6. Plan sprint based on findings
/project:session-sprint create [appropriate-type-based-on-analysis]

# 7. Start actual development work
/project:session-start [type]-[specific-task]
```

### Scenario 3: Project in Progress, Joining Mid-Development

**Commands Sequence**:
```bash
# 1. Understand current state
/project:session-current  # Check if there's an active session
/project:session-list     # Review recent sessions
/project:session-sprint status  # Check current sprint

# 2. Review project rules
/project:session-rules check

# 3. Start your session aligned with current sprint
/project:session-start [sprint-aligned-task]

# 4. Update progress
/project:session-update milestone "Onboarding complete, ready to contribute"
```

### Scenario 4: Emergency Production Issue

**Commands Sequence**:
```bash
# 1. Start emergency session immediately
/project:session-start emergency-[brief-description]

# 2. Begin systematic debugging (5-phase SDLC v1.0)
/project:session-debug start "[detailed issue description]"

# 3. Follow 5-phase debugging protocol
/project:session-debug symptoms    # Phase 1: Symptoms Analysis (5 min)
/project:session-debug browser     # Phase 2: Browser DevTools (10 min)
/project:session-debug api         # Phase 3: API Testing (10 min)
/project:session-debug config      # Phase 4: Configuration Review (15 min)
                                   # Phase 5: Solution & Documentation

# 4. Document solution and prevention
/project:session-debug complete "[solution description]"

# 5. End emergency session
/project:session-end

# 6. Create follow-up sprint if needed
/project:session-sprint create 9.x-emergency-follow-up
```

---

## 🎯 Task-Specific Command Selection

### Development Sessions

**Feature Development (SDLC v1.0)**:
```bash
# Check sprint alignment first
/project:session-sprint status

# Start feature session
/project:session-start feature-[component-name]

# Document performance baseline
/project:session-update milestone "Performance baseline documented"

# Regular updates with performance checks
/project:session-update milestone "[achievement]"
/project:session-update daily "[progress summary] - Performance: API [X]ms, Page [Y]ms"

# Validate performance standards before completion
/project:session-update review "Performance standards verified: ✅ API < 500ms, ✅ Page < 2s"

# Before ending, check delivery readiness
/project:session-delivery status

# End with comprehensive docs
/project:session-end
```

**Performance Standards Compliance (Mandatory)**:
- Document performance baseline before development
- Monitor performance continuously during development
- Validate all standards met before completion
- No performance regressions allowed

**Bug Fixing Workflow**:
```bash
# Start bug session
/project:session-start bug-[issue-description]

# If debugging needed (5-phase SDLC v1.0 protocol)
/project:session-debug start "[issue details]"
/project:session-debug symptoms    # Phase 1: 5 min
/project:session-debug browser     # Phase 2: 10 min
/project:session-debug api         # Phase 3: 10 min  
/project:session-debug config      # Phase 4: 15 min
/project:session-debug complete "[solution]"  # Phase 5: Solution & Prevention

# Update with fix details
/project:session-update debug "Root cause: [cause], Fix: [solution]"

# End session
/project:session-end
```

**Research Sessions**:
```bash
# Start research session
/project:session-start research-[topic]

# Document findings as you learn
/project:session-update milestone "[key discovery]"
/project:session-update review "[evaluation results]"

# Create research delivery doc
/project:session-delivery create research

# End with recommendations
/project:session-end
```

**Infrastructure Sessions**:
```bash
# Start infrastructure session
/project:session-start infrastructure-[component]

# Document architecture decisions
/project:session-update integration "[system integration complete]"
/project:session-update deployment "[deployment pipeline working]"

# Check delivery readiness
/project:session-delivery status

# End session
/project:session-end
```

**Maintenance Sessions**:
```bash
# Start maintenance session
/project:session-start maintenance-[area]

# Check current compliance
/project:session-rules check

# Update progress
/project:session-update daily "[dependencies updated, X vulnerabilities fixed]"

# End session
/project:session-end
```

### Sprint Planning Sessions (SDLC v1.0)

**When to Use**: Sprint kickoff, planning sessions, sprint retrospectives

```bash
# Start sprint planning session
/project:session-sprint-planning [sprint-name]

# Example: /project:session-sprint-planning 1.3-auth-oauth-integration

# During planning
/project:session-update milestone "Sprint backlog prioritized"
/project:session-update review "Team capacity and velocity confirmed"

# Complete sprint planning
/project:session-end
```

**What this does**:
- Creates comprehensive sprint planning documentation
- Sets performance goals and quality gates
- Plans risk mitigation and failure prevention
- Defines sprint success criteria and metrics

### Performance Sessions (SDLC v1.0)

**When to Use**: Performance optimization, meeting performance standards, performance emergencies

```bash
# Start performance optimization session
/project:session-performance [optimization-target]

# Example: /project:session-performance api-response-optimization

# Document baseline metrics
/project:session-update milestone "Performance baseline documented"

# Track optimization progress
/project:session-update debug "Found N+1 query causing 800ms response time"

# Validate improvements
/project:session-update milestone "API response time reduced to 300ms"

# End session
/project:session-end
```

**Performance Standards (Mandatory)**:
- API Response Time: < 500ms end-to-end
- Page Load Time: < 2 seconds initial load
- Database Query Time: < 100ms execution
- Component Render: < 100ms for interactive elements

### Failure Analysis Sessions (SDLC v1.0)

**When to Use**: Three-strike rule triggered (task failed 3 times)

**MANDATORY Trigger Conditions**:
- Same task fails 3 times despite different approaches
- Sprint objectives not met for 3 consecutive sprints
- Same type of bug/issue occurs 3 times
- Performance standards missed 3 times for same component

```bash
# STOP all related work immediately when three-strike rule triggered

# Start failure analysis session
/project:session-failure-analysis [failed-task-description]

# Example: /project:session-failure-analysis oauth-integration-attempts

# Document all failed attempts
/project:session-update milestone "All 3 attempts documented and analyzed"

# Root cause analysis
/project:session-update review "Technical, process, and knowledge factors identified"

# Prevention strategy
/project:session-update milestone "Prevention measures and alternative approach defined"

# End session
/project:session-end
```

**What this does**:
- Systematic root cause analysis (technical, process, knowledge factors)
- Prevention strategy development (immediate and long-term)
- Alternative solution approach with success criteria
- Knowledge transfer and team learning

---

## 🔍 Diagnostic Questions & Command Selection

### "I don't know what command to use"

**Ask yourself these questions**:

1. **Is this the first time touching this project?**
   - YES → `/project:session-rules init` then assess
   - NO → Continue to next question

2. **Is there an emergency/production issue?**
   - YES → `/project:session-start emergency-[issue]`
   - NO → Continue to next question

3. **Am I starting new work or continuing existing work?**
   - NEW → Check sprint status first: `/project:session-sprint status`
   - CONTINUING → Check current session: `/project:session-current`

4. **What type of work am I doing?**
   - FEATURE → `/project:session-start feature-[name]`
   - BUG → `/project:session-start bug-[issue]`
   - RESEARCH → `/project:session-start research-[topic]`
   - INFRASTRUCTURE → `/project:session-start infrastructure-[component]`
   - MAINTENANCE → `/project:session-start maintenance-[area]`

### "The project seems messy/unorganized"

```bash
# 1. First, assess current state
/project:session-rules check

# 2. Start analysis session
/project:session-start research-project-assessment

# 3. Document findings
/project:session-update review "Technical debt analysis complete"

# 4. Plan improvement sprint
/project:session-sprint create 5.x-project-cleanup

# 5. End analysis session
/project:session-end
```

### "I'm getting errors/bugs"

```bash
# 1. Start debug-focused session
/project:session-start bug-[error-description]

# 2. Begin systematic debugging
/project:session-debug start "[detailed error description]"

# 3. Follow the 5-phase SDLC v1.0 protocol
/project:session-debug symptoms    # Phase 1: Symptoms Analysis (5 min)
/project:session-debug browser     # Phase 2: Browser DevTools (10 min)  
/project:session-debug api         # Phase 3: API Testing (10 min)
/project:session-debug config      # Phase 4: Configuration Review (15 min)
                                   # Phase 5: Solution & Documentation

# 4. Document solution
/project:session-debug complete "[solution implemented]"

# 5. End session
/project:session-end
```

---

## 📋 Quick Reference Checklists

### Starting Any Session Checklist
- [ ] Is there an active session? (`/project:session-current`)
- [ ] What sprint are we in? (`/project:session-sprint status`)
- [ ] Are project rules up to date? (`/project:session-rules check`)
- [ ] What type of work am I doing? (Choose appropriate session type)
- [ ] Do I have clear goals for this session?

### During Development Checklist
- [ ] Am I updating the session regularly? (Every 2-4 hours)
- [ ] Am I using appropriate checkpoint types?
- [ ] Am I documenting decisions and rationale?
- [ ] Am I following project rules and guidelines?
- [ ] Am I tracking progress toward acceptance criteria?

### Before Ending Session Checklist
- [ ] Are all goals documented with completion status?
- [ ] Have I checked code quality? (`/project:session-rules check`)
- [ ] Is delivery documentation needed? (`/project:session-delivery status`)
- [ ] Are there follow-up tasks to document?
- [ ] Have I captured lessons learned?

### Emergency Response Checklist
- [ ] Start emergency session immediately
- [ ] Follow systematic debugging protocol
- [ ] Document everything as you investigate
- [ ] Don't skip phases - follow the time-boxed approach
- [ ] Document root cause and prevention measures
- [ ] Plan follow-up work if needed

---

## 🎓 Master Prompt for AI Agents

> **Copy this section to use as a master prompt for any AI coding agent**

```
You are an expert development agent using the SDLC v1.0 Framework with performance-first development and systematic failure prevention.

BEFORE starting any coding work, ALWAYS:

1. ASSESS PROJECT STATE:
   - New project? → `/project:session-rules init` first
   - Existing project? → `/project:session-rules check` to assess compliance
   - Emergency? → `/project:session-start emergency-[issue]` immediately

2. CHECK CURRENT CONTEXT:
   - Active session? → `/project:session-current`
   - Active sprint? → `/project:session-sprint status`
   - Project rules? → `/project:session-rules check`

3. SELECT APPROPRIATE SESSION TYPE (SDLC v1.0):
   - New feature → `feature-[component-name]`
   - Bug fix → `bug-[issue-description]`
   - Research → `research-[topic]`
   - Infrastructure → `infrastructure-[component]`
   - Maintenance → `maintenance-[area]`
   - Sprint planning → `/project:session-sprint-planning [sprint-name]`
   - Performance optimization → `/project:session-performance [target]`
   - Failure analysis → `/project:session-failure-analysis [task]` (three-strike rule)
   - Emergency → `emergency-[issue]`

4. FOLLOW SESSION WORKFLOW:
   - Start: `/project:session-start [type]-[descriptive-name]`
   - Update: `/project:session-update [checkpoint-type] "[description]"` every 2-4 hours
   - Debug if needed: `/project:session-debug` protocol (symptoms→browser→api→config)
   - End: `/project:session-end` with comprehensive documentation

5. USE 5-PHASE DEBUGGING PROTOCOL FOR ANY ISSUES (SDLC v1.0):
   - Start: `/project:session-debug start "[issue description]"`
   - Phase 1: `/project:session-debug symptoms` (5 min - user impact, error frequency)
   - Phase 2: `/project:session-debug browser` (10 min - network tab, console errors)
   - Phase 3: `/project:session-debug api` (10 min - CURL testing, backend logs)
   - Phase 4: `/project:session-debug config` (15 min - CORS, environment differences)
   - Phase 5: `/project:session-debug complete "[solution]"` (solution & prevention)

6. MAINTAIN QUALITY (SDLC v1.0 STANDARDS):
   - Check compliance: `/project:session-rules check` regularly
   - Document decisions and rationale in updates
   - Use appropriate checkpoint types (milestone, daily, debug, blocker, etc.)
   - Ensure CORS validation and environment parity
   - Follow TDD practices when applicable
   - PERFORMANCE FIRST: Monitor API < 500ms, Page < 2s, DB < 100ms continuously
   - THREE-STRIKE AWARENESS: Track failed attempts, trigger failure analysis after 3 failures
   - QUALITY GATES: Validate all standards before completion

7. DELIVERY FOCUS:
   - Check readiness: `/project:session-delivery status`
   - Generate docs: `/project:session-delivery create [type]`
   - Publish when ready: `/project:session-delivery publish`

REMEMBER: Every significant development activity should be wrapped in a session following SDLC v1.0 framework. Sessions provide context, ensure performance-first development, implement systematic failure prevention, and preserve knowledge for future work.

SDLC v1.0 FRAMEWORK REFERENCES:
- Master Framework: SDLC.md
- Performance Standards: performance-standards.md (MANDATORY compliance)
- Failure Analysis: failure-analysis-framework.md (three-strike rule)
- Best Practices: best-practices.md (enhanced with SDLC patterns)
```

---

## 🎯 "What's Next?" Status Assessment (SDLC v1.0)

### Quick Status Check Commands
**Run these commands when you're unsure what to do next:**

```bash
# 1. Check if there's an active session
/project:session-current

# 2. Check current sprint status
/project:session-sprint status

# 3. Check framework compliance
/project:session-rules check

# 4. List recent sessions for context
/project:session-list
```

### Decision Matrix: What Should I Do Next?

#### Scenario 1: No Active Session
```
Current State: No active session found
Next Action: Start appropriate session type
Commands: /project:session-start [type]-[description]
```

#### Scenario 2: Active Session Exists
```
Current State: Session active for [X] hours
Next Actions:
- Continue work: Resume development on current session
- Update progress: /project:session-update [checkpoint-type] "[status]"
- End session: /project:session-end (if work complete)
```

#### Scenario 3: No Active Sprint
```
Current State: No active sprint
Next Actions:
- Plan new sprint: /project:session-sprint-planning [sprint-name]
- Create sprint: /project:session-sprint create [type]
```

#### Scenario 4: Sprint Active, Work Available
```
Current State: Sprint [X] active with pending tasks
Next Action: Start task-aligned session
Commands: /project:session-start [sprint-aligned-task]
```

#### Scenario 5: Performance Issues Detected
```
Current State: Performance standards not met
Next Action: Performance optimization session
Commands: /project:session-performance [optimization-target]
```

#### Scenario 6: Three-Strike Rule Triggered
```
Current State: Task failed 3 times
Next Action: MANDATORY failure analysis
Commands: 
1. STOP current work
2. /project:session-failure-analysis [failed-task]
```

### Framework Health Indicators

#### ✅ Healthy Project State
- Active sprint with clear objectives
- Performance standards consistently met
- No three-strike situations
- Regular session documentation
- Quality gates passing

#### ⚠️ Warning Signs
- Sessions not updated for > 4 hours
- Performance metrics declining
- Multiple task failures (approaching three-strike)
- Sprint objectives unclear or behind schedule

#### 🚨 Critical Issues
- Three-strike rule triggered (STOP and analyze)
- Performance standards consistently missed
- No active sprint or session management
- Framework compliance failing

### Automated Health Check Sequence
```bash
# Run this sequence when unsure about project health:

# 1. Framework compliance
/project:session-rules check

# 2. Performance status (if performance session available)
# Check if any performance standards are being missed

# 3. Sprint alignment
/project:session-sprint status

# 4. Session status
/project:session-current

# 5. Recent activity review
/project:session-list

# Based on results, choose appropriate next action from decision matrix above
```

---

## 🚨 Common Mistakes to Avoid

### ❌ Don't Do This (SDLC v1.0)
- Starting work without checking project state and performance baseline
- Skipping session initialization or framework compliance check
- Not using appropriate session types (missing sprint-planning, performance, failure-analysis)
- Forgetting to update sessions regularly or track performance
- Not following 5-phase debugging protocol during issues
- Ignoring three-strike rule when tasks fail repeatedly
- Ending sessions without proper documentation and performance validation
- Missing performance standards (API > 500ms, Page > 2s, DB > 100ms)

### ✅ Do This Instead (SDLC v1.0)
- Always assess project state and framework compliance first
- Initialize sessions system with SDLC v1.0 framework if missing
- Use descriptive, sprint-aligned session names with performance goals
- Update sessions at logical checkpoints with performance metrics
- Follow systematic 5-phase debugging when issues arise
- Trigger mandatory failure analysis after three strikes
- End sessions with comprehensive delivery docs and performance validation
- Maintain performance-first development throughout all work

---

## 🔄 Workflow Examples by Project Phase

### Week 1: New Project
```bash
Day 1: /project:session-rules init → /project:session-sprint create 1.1-foundation → /project:session-start feature-project-setup
Day 2: /project:session-start infrastructure-build-pipeline
Day 3: /project:session-start feature-core-architecture
```

### Week 2-4: Active Development
```bash
/project:session-sprint status → /project:session-start feature-[component] → regular updates → /project:session-end
```

### Ongoing: Maintenance
```bash
Monthly: /project:session-start maintenance-dependencies
As needed: /project:session-start bug-[issue] or emergency-[critical-issue]
```

---

## 📊 Success Metrics (SDLC v1.0)

You're using the framework effectively when:
- ✅ Every development session is documented with performance tracking
- ✅ Sprint goals are clear, tracked, and aligned with business value
- ✅ Issues are debugged systematically using 5-phase protocol
- ✅ Performance standards consistently met (API < 500ms, Page < 2s, DB < 100ms)
- ✅ Quality gates are consistently passed before completion
- ✅ Three-strike rule prevents repeated failures through systematic analysis
- ✅ Knowledge transfer is comprehensive with failure prevention insights
- ✅ Future developers can understand your work and avoid past failures
- ✅ Framework compliance maintained across all development activities
- ✅ Performance-first development culture established and maintained

---

*This guide should be your first reference when starting any development work. When in doubt, assess project state first, then choose the appropriate command sequence.*