End the current development session with comprehensive delivery documentation and retrospective analysis.

## Session Completion Process:

1. **Verify Active Session**: Check `sessions/.current-session` for the active session
2. **No Active Session**: If none exists, inform user there's nothing to end
3. **Session Exists**: Generate comprehensive session completion documentation

## Final Session Summary Structure:

### Session Completion Documentation
```markdown
## 🎯 Session Completion Summary - [Sprint Type] - [Session Name]

### Session Overview
- **Duration**: [Start time] → [End time] ([Total duration])
- **Sprint Type**: [Category and classification]
- **Priority Level**: [Final priority assessment]
- **Session Status**: [Completed/Partially Completed/Blocked]

### 📊 Delivery Metrics & Status

#### Goals Achievement
- **Total Goals**: [count]
- **Completed**: [count] ✅
- **Partially Completed**: [count] ⚠️
- **Not Completed**: [count] ❌

**Detailed Goal Status**:
- ✅ [Goal 1]: [Completion details and acceptance criteria met]
- ⚠️ [Goal 2]: [Partial completion details and remaining work]
- ❌ [Goal 3]: [Reason for non-completion and next steps]

#### Acceptance Criteria Status
[Detailed assessment of all acceptance criteria]
- **Functional Requirements**: [Met/Partially Met/Not Met]
- **Technical Requirements**: [Met/Partially Met/Not Met]
- **Quality Requirements**: [Met/Partially Met/Not Met]

### 🔄 Development Activity Summary

#### Git Repository Changes
- **Total Commits**: [count]
- **Files Changed**: [count] (Added: [count], Modified: [count], Deleted: [count])
- **Lines of Code**: +[additions] -[deletions]
- **Branches**: [list of branches worked on]
- **Final Branch**: [current branch] (commit: [hash])

**Detailed File Changes**:
- **Added Files**:
  - [file1] - [description of purpose]
  - [file2] - [description of purpose]
- **Modified Files**:
  - [file1] - [what was changed and why]
  - [file2] - [what was changed and why]
- **Deleted Files**:
  - [file1] - [reason for deletion]

#### Todo List Completion
- **Total Tasks**: [count]
- **Completed**: [count] ([percentage]%)
- **In Progress**: [count] (carried forward)
- **Pending**: [count] (carried forward)

**Completed Tasks**:
- ✅ [Task description] - [completion notes]
- ✅ [Task description] - [completion notes]

**Incomplete Tasks & Status**:
- 🔄 [Task in progress] - [current status and next steps]
- ⏳ [Pending task] - [reason for delay and timeline]

### 🏗️ Architecture & Technical Decisions

#### Key Architectural Decisions
- **Decision 1**: [What was decided]
  - **Rationale**: [Why this approach]
  - **Alternatives**: [What was considered]
  - **Impact**: [Long-term implications]

#### Technology Stack Changes
- **Dependencies Added**: [list with versions and purposes]
- **Dependencies Removed**: [list with reasons]
- **Configuration Changes**: [environment, build, deployment]
- **Database Changes**: [schema, migrations, data]

### 🧪 Testing & Quality Assurance

#### Test Coverage & Results
- **Test Suite Status**: [Passing/Failing]
- **New Tests Added**: [count and coverage areas]
- **Test Coverage**: [percentage if available]
- **Performance Tests**: [results and benchmarks]

#### Code Quality Metrics
- **Linting Status**: [clean/issues resolved]
- **Type Checking**: [clean/issues resolved]
- **Security Scan**: [results and actions taken]
- **Code Review**: [status and feedback addressed]

### 🚀 Deployment & Environment

#### Deployment Readiness
- **Production Ready**: [Yes/No/Partially]
- **Staging Deployed**: [Yes/No]
- **Environment Parity**: [Verified/Issues]
- **CORS Configuration**: [Tested/Updated]

#### Environment Configuration
- **Development Environment**: [status and any issues]
- **Test Environment**: [status and any issues]
- **Production Environment**: [status and any issues]

### 🐛 Issues & Problem Resolution

#### Issues Encountered
- **Issue 1**: [Description]
  - **Severity**: [High/Medium/Low]
  - **Impact**: [Scope and consequences]
  - **Solution**: [How it was resolved]
  - **Time Spent**: [effort investment]
  - **Prevention**: [future mitigation strategies]

#### Debugging Protocol Usage
- **Systematic Debugging Applied**: [Yes/No]
- **Browser DevTools**: [findings and actions]
- **API Testing**: [CURL results and validations]
- **Configuration Review**: [issues found and resolved]

### 📚 Knowledge Transfer & Documentation

#### Key Learnings
- **Technical Insights**: [Important discoveries]
- **Best Practices**: [What worked well]
- **Gotchas**: [Things future developers should know]
- **Anti-patterns**: [What to avoid]

#### Documentation Updates
- **API Documentation**: [updated/created]
- **README Updates**: [changes made]
- **Architecture Docs**: [new/updated diagrams or explanations]
- **Deployment Guides**: [procedures documented]

### 🔮 Future Considerations

#### Immediate Next Steps
- **Priority 1**: [Immediate action needed]
- **Priority 2**: [Important follow-up]
- **Priority 3**: [Future consideration]

#### Technical Debt & Improvements
- **Refactoring Opportunities**: [areas for improvement]
- **Performance Optimization**: [potential optimizations]
- **Security Enhancements**: [security considerations]
- **Scalability Considerations**: [future scaling needs]

#### Recommendations for Future Development
- **Development Approach**: [what worked and what didn't]
- **Tool Recommendations**: [helpful tools or libraries]
- **Process Improvements**: [workflow optimizations]

### 📈 Sprint & Project Impact

#### Sprint Contribution
- **Sprint Goals Met**: [contribution to overall sprint]
- **Blockers Removed**: [dependencies unblocked for team]
- **Velocity Impact**: [effect on team velocity]

#### Project Milestones
- **Milestones Achieved**: [significant project milestones]
- **Risk Mitigation**: [risks addressed or introduced]
- **Stakeholder Value**: [business value delivered]

### 🎓 Retrospective Analysis

#### What Went Well
- [Successful approaches and practices]
- [Effective tools and techniques]
- [Positive outcomes and achievements]

#### What Could Be Improved
- [Areas for improvement identified]
- [Process inefficiencies encountered]
- [Knowledge gaps revealed]

#### Action Items for Future Sessions
- **Process Improvements**: [specific changes to make]
- **Tool Enhancements**: [tools to adopt or improve]
- **Skill Development**: [areas for learning and growth]

### 🔗 References & Links
- **Related Sessions**: [links to related session files]
- **External Documentation**: [relevant external resources]
- **Code References**: [important code locations]
- **Issue Tracking**: [links to tickets or issues]

---

**Session Completion Time**: [timestamp]
**Next Session Recommendations**: [suggestions for continuation]
**Knowledge Transfer Complete**: ✅
```

4. **Post-Completion Actions**:
   - Clear `sessions/.current-session` file (don't remove, just empty)
   - Generate any required delivery documentation
   - Update project documentation if needed
   - Create follow-up tasks if session was incomplete

5. **Integration with Delivery Pipeline**:
   - Reference `/project:session-delivery` for formal delivery docs
   - Prepare retrospective data for sprint reviews
   - Update project backlog with lessons learned

6. **Quality Assurance Check**:
   - Verify all acceptance criteria are documented
   - Ensure knowledge transfer completeness
   - Confirm future developer can continue work

The documentation should be comprehensive enough that another developer or AI can:
- Understand what was accomplished
- Continue the work where it left off
- Learn from the problems encountered
- Apply the lessons learned to future work
- Assess the impact on the larger project

## Final Confirmation:
Inform user that the session has been comprehensively documented and remind them:
- Session is now closed and documented
- Documentation is available for future reference
- Use `/project:session-list` to view all sessions
- Use `/project:session-start` to begin new work