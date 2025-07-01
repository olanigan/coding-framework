Start a failure analysis session following SDLC v1.0 three-strike rule framework.

## Failure Analysis Session Creation Process:

**TRIGGER**: This session type is **mandatory** when the three-strike rule is activated:
- Same task fails 3 times despite different approaches
- Sprint objectives not met for 3 consecutive sprints  
- Same type of bug/issue occurs 3 times
- Same process breakdown occurs 3 times
- Performance standards missed 3 times for same component

1. **Immediate Response Protocol**:
   - **STOP** all related work immediately
   - Schedule failure analysis session within 24 hours
   - Notify stakeholders of analysis process
   - Assign failure analysis lead (senior developer or team lead)

2. **Generate Session Filename**: Create session file in `sessions/` using format:
   - `YYYY-MM-DD-HHMM-failure-analysis-[failed-task-description].md`
   - Example: `2025-07-01-1400-failure-analysis-oauth-integration-attempts`

3. **Use Failure Analysis Template**: Initialize with `templates/failure-analysis-session.md`

4. **Session Initialization**: Populate template with failure context:

```markdown
# Development Session - [Date Time] - failure-analysis - [failed-task-description]

## Session Overview
- **Start Time**: [Current timestamp]
- **Session Type**: Failure Analysis (Three-Strike Rule Triggered)
- **Estimated Duration**: 1-2 hours
- **Priority Level**: High - Process Improvement
- **Failed Task**: [Description of task that failed 3 times]
- **Original Sprint**: [Sprint where failures occurred]

## SDLC v1.0 Three-Strike Rule Compliance
Reference: failure-analysis-framework.md

## Immediate Actions Taken:
- [ ] All related work stopped
- [ ] Stakeholders notified
- [ ] Failure analysis lead assigned: [Name]
- [ ] Previous attempt documentation gathered

[Continue with full failure-analysis-session.md template...]
```

5. **Pre-Analysis Documentation Requirements**:
   - [ ] **Attempt History**: Document all 3 failed attempts
   - [ ] **Resource Impact**: Total time and people invested
   - [ ] **Business Impact**: Project delays and missed opportunities
   - [ ] **Team Impact**: Morale and confidence effects
   - [ ] **Timeline**: When attempts were made and failed

6. **Root Cause Analysis Framework** (failure-analysis-framework.md):
   - **Technical Factors**: Code complexity, architecture limitations, tool issues
   - **Process Factors**: Requirements clarity, planning accuracy, communication gaps
   - **Knowledge Factors**: Skill gaps, domain expertise, technology experience

7. **Analysis Session Structure**:
   - **Opening (5 min)**: Review purpose and process
   - **Attempt Documentation (30 min)**: Document all failed attempts
   - **Root Cause Analysis (45 min)**: Systematic cause identification
   - **Prevention Strategy (30 min)**: Develop prevention measures
   - **Alternative Solution (15 min)**: Create new approach

8. **Prevention Strategy Development**:
   - **Immediate**: Next sprint prevention measures
   - **Systemic**: Long-term organizational improvements
   - **Knowledge**: Training and skill development needs
   - **Process**: Workflow and communication improvements

After creating the session file, update `sessions/.current-session` to track the active session filename.

## Confirmation Message:
Confirm failure analysis session started with:
- Failed task description and attempt count
- Analysis lead and session participants
- Expected session duration and outcome
- Stakeholder notification status

## Available Commands During Analysis:
- `/project:session-update` - Log analysis findings and decisions
- `/project:session-end` - Complete with prevention strategy and alternative approach

## SDLC v1.0 Failure Analysis Requirements:
- **Systematic Analysis**: Follow failure-analysis-framework.md process
- **Multi-Factor Examination**: Technical, process, and knowledge factors
- **Prevention Focus**: Must produce prevention strategy
- **Alternative Solution**: Must develop new approach with success criteria
- **Knowledge Transfer**: Document insights for team learning

## Cultural Integration:
- **Psychological Safety**: Treat as learning opportunity, not blame
- **Process Improvement**: Focus on system enhancement
- **Team Learning**: Share insights across organization
- **Continuous Improvement**: Update processes based on findings

## Success Metrics:
- **Root Cause Identified**: Clear understanding of failure factors
- **Prevention Strategy**: Actionable prevention measures defined
- **Alternative Approach**: Viable new solution developed
- **Team Learning**: Knowledge captured and shared