Update the current development session with comprehensive checkpoint documentation and debugging protocol integration.

## Session Update Process:

1. **Verify Active Session**: Check if `sessions/.current-session` exists to find the active session
2. **No Active Session**: If none exists, inform user to start one with `/project:session-start`
3. **Active Session Found**: Append structured update to the session file

## Update Structure:

### Standard Update Format:
```markdown
### Checkpoint Update - [Timestamp] - [Checkpoint Type]

#### Summary
[User provided summary or auto-generated from recent activities]

#### Git Status & Changes
- **Branch**: [current branch] (commit: [latest commit hash])
- **Modified Files**: [list of modified files]
- **Added Files**: [list of new files]
- **Deleted Files**: [list of deleted files]
- **Staged Changes**: [files ready for commit]
- **Untracked Files**: [new untracked files]

#### Todo Progress Tracking
- **Completed**: [count] tasks
- **In Progress**: [count] tasks  
- **Pending**: [count] tasks
- **Recently Completed**:
  - ✓ [Task description]
  - ✓ [Task description]
- **Currently Working On**:
  - 🔄 [Task description]
- **Next Up**:
  - ⏳ [Task description]

#### Environment & Configuration Status
- **Development Environment**: [Status: OK/Issues]
- **Test Suite Status**: [Passing/Failing - count]
- **CORS Configuration**: [Verified/Needs Update]
- **Dependencies**: [Up to date/Updates needed]
- **Build Status**: [Success/Failure]

#### Code Quality Metrics
- **Linting**: [Status and any issues]
- **Type Checking**: [Status and any issues]
- **Test Coverage**: [Current percentage if available]
- **Performance**: [Any performance observations]

#### Issues Encountered & Solutions
[Document any problems and their resolutions]
- **Issue**: [Description]
  - **Impact**: [Severity and scope]
  - **Solution**: [How it was resolved]
  - **Prevention**: [How to avoid in future]

#### Debugging Protocol Checkpoints (if applicable)
- **Symptoms Analysis**: [Issues documented and categorized]
- **Browser DevTools**: [Network tab findings, console errors]
- **API Testing**: [CURL test results, endpoint validation]
- **Configuration Review**: [CORS, environment parity checks]

#### Architecture & Design Decisions
[Document any architectural decisions made during this checkpoint]
- **Decision**: [What was decided]
- **Rationale**: [Why this approach was chosen]
- **Alternatives Considered**: [Other options evaluated]
- **Trade-offs**: [Benefits and drawbacks]

#### Knowledge Transfer Notes
[Important insights for future developers]
- **Key Learnings**: [What was learned]
- **Gotchas**: [Things to watch out for]
- **Best Practices**: [Recommendations for similar work]

#### Delivery Progress
[Track progress toward delivery goals]
- **Acceptance Criteria Status**: [Which criteria are met]
- **Demo Readiness**: [What can be demonstrated]
- **Documentation Status**: [Current documentation state]
- **Deployment Readiness**: [Ready/Blockers]

#### Next Steps
[Clear action items for continuation]
- [ ] [Immediate next task]
- [ ] [Follow-up task]
- [ ] [Future consideration]
```

## Checkpoint Types:
- **milestone** - Major feature completion or significant progress
- **daily** - End of day summary and status
- **debug** - Debugging session results and findings
- **blocker** - Issues that prevent progress
- **integration** - System integration and testing updates
- **review** - Code review and quality assurance
- **deployment** - Deployment and production updates

## Automated Context Gathering:
When no specific update is provided, automatically gather:
1. **Recent Git Activity**: Analyze commits, branches, and file changes
2. **Todo List Changes**: Identify completed, updated, or new tasks
3. **Test Results**: Latest test run results and coverage
4. **Build Status**: Recent build logs and status
5. **Environment Health**: Check for configuration issues

## Integration with Other Commands:
- Reference `/project:session-debug` for systematic debugging
- Link to `/project:session-sprint` for sprint-level updates
- Prepare data for `/project:session-delivery` documentation

## Best Practices Integration:
- **TDD Compliance**: Verify test-first development approach
- **CORS Validation**: Check cross-origin configurations
- **Environment Parity**: Ensure development matches production
- **Documentation**: Maintain knowledge transfer quality
- **Security**: Flag any security considerations

## Emergency Response Integration:
If issues are encountered, automatically trigger debugging protocol:
1. **Symptoms Documentation** (5min)
2. **Browser DevTools Analysis** (10min)
3. **API Testing** (10min)
4. **Configuration Review** (15min)
5. **Solution Documentation**