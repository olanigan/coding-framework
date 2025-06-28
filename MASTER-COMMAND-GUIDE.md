# Master Command Usage Guide 🎯
*The Complete Reference for Agentic Coding Session Management*

> **Use this guide to determine which commands to use in any development scenario**

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

# 2. Begin systematic debugging
/project:session-debug start "[detailed issue description]"

# 3. Follow debugging protocol
/project:session-debug symptoms
/project:session-debug browser
/project:session-debug api
/project:session-debug config

# 4. Document solution
/project:session-debug complete "[solution description]"

# 5. End emergency session
/project:session-end

# 6. Create follow-up sprint if needed
/project:session-sprint create 9.x-emergency-follow-up
```

---

## 🎯 Task-Specific Command Selection

### Development Sessions

**Feature Development**:
```bash
# Check sprint alignment first
/project:session-sprint status

# Start feature session
/project:session-start feature-[component-name]

# Regular updates
/project:session-update milestone "[achievement]"
/project:session-update daily "[progress summary]"

# Before ending, check delivery readiness
/project:session-delivery status

# End with comprehensive docs
/project:session-end
```

**Bug Fixing Workflow**:
```bash
# Start bug session
/project:session-start bug-[issue-description]

# If debugging needed
/project:session-debug start "[issue details]"
# Follow debugging protocol...
/project:session-debug complete "[solution]"

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

# 3. Follow the 4-phase protocol
/project:session-debug symptoms    # 5 min
/project:session-debug browser     # 10 min  
/project:session-debug api         # 10 min
/project:session-debug config      # 15 min

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
You are an expert development agent using the Mega Agentic Coding Session Management System. 

BEFORE starting any coding work, ALWAYS:

1. ASSESS PROJECT STATE:
   - New project? → `/project:session-rules init` first
   - Existing project? → `/project:session-rules check` to assess compliance
   - Emergency? → `/project:session-start emergency-[issue]` immediately

2. CHECK CURRENT CONTEXT:
   - Active session? → `/project:session-current`
   - Active sprint? → `/project:session-sprint status`
   - Project rules? → `/project:session-rules check`

3. SELECT APPROPRIATE SESSION TYPE:
   - New feature → `feature-[component-name]`
   - Bug fix → `bug-[issue-description]`
   - Research → `research-[topic]`
   - Infrastructure → `infrastructure-[component]`
   - Maintenance → `maintenance-[area]`
   - Emergency → `emergency-[issue]`

4. FOLLOW SESSION WORKFLOW:
   - Start: `/project:session-start [type]-[descriptive-name]`
   - Update: `/project:session-update [checkpoint-type] "[description]"` every 2-4 hours
   - Debug if needed: `/project:session-debug` protocol (symptoms→browser→api→config)
   - End: `/project:session-end` with comprehensive documentation

5. USE DEBUGGING PROTOCOL FOR ANY ISSUES:
   - Start: `/project:session-debug start "[issue description]"`
   - Phase 1: `/project:session-debug symptoms` (5 min)
   - Phase 2: `/project:session-debug browser` (10 min)
   - Phase 3: `/project:session-debug api` (10 min)
   - Phase 4: `/project:session-debug config` (15 min)
   - Complete: `/project:session-debug complete "[solution]"`

6. MAINTAIN QUALITY:
   - Check compliance: `/project:session-rules check` regularly
   - Document decisions and rationale in updates
   - Use appropriate checkpoint types (milestone, daily, debug, blocker, etc.)
   - Ensure CORS validation and environment parity
   - Follow TDD practices when applicable

7. DELIVERY FOCUS:
   - Check readiness: `/project:session-delivery status`
   - Generate docs: `/project:session-delivery create [type]`
   - Publish when ready: `/project:session-delivery publish`

REMEMBER: Every significant development activity should be wrapped in a session. Sessions provide context, ensure quality, and preserve knowledge for future work.
```

---

## 🚨 Common Mistakes to Avoid

### ❌ Don't Do This
- Starting work without checking project state
- Skipping session initialization
- Not using appropriate session types
- Forgetting to update sessions regularly
- Not following debugging protocol during issues
- Ending sessions without proper documentation

### ✅ Do This Instead
- Always assess project state first
- Initialize sessions system if missing
- Use descriptive, sprint-aligned session names
- Update sessions at logical checkpoints
- Follow systematic debugging when issues arise
- End sessions with comprehensive delivery docs

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

## 📊 Success Metrics

You're using the system effectively when:
- ✅ Every development session is documented
- ✅ Sprint goals are clear and tracked
- ✅ Issues are debugged systematically
- ✅ Quality gates are consistently met
- ✅ Knowledge transfer is comprehensive
- ✅ Future developers can understand your work

---

*This guide should be your first reference when starting any development work. When in doubt, assess project state first, then choose the appropriate command sequence.*