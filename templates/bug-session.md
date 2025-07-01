# Development Session - [Date Time] - bug - [issue-description]

## Session Overview
- **Start Time**: [Timestamp]
- **Sprint Type**: Bug Fix
- **Estimated Duration**: [1-4 hours]
- **Priority Level**: [Critical/High/Medium/Low]
- **Bug Severity**: [Production-blocking/Major/Minor/Cosmetic]
- **Issue Reference**: [Ticket/Issue number if applicable]
- **Related Sprint**: [Sprint 3.x if part of bug fix sprint]

## Bug Details & Reproduction
### Issue Description
- **Reported By**: [User/System/Monitoring]
- **Environment**: [Dev/Staging/Production]
- **Frequency**: [Always/Sometimes/Rarely]
- **User Impact**: [How this affects users]
- **Business Impact**: [Revenue/operations impact]
- **First Observed**: [When first noticed]
- **Regression**: [Is this a new issue or regression?]

### Reproduction Steps
1. [Step 1 to reproduce]
2. [Step 2 to reproduce]
3. [Expected result]
4. [Actual result]

### Browser/Device Information
- **Browser**: [Chrome/Firefox/Safari/Edge version]
- **Device**: [Desktop/Mobile/Tablet]
- **OS**: [Operating system and version]
- **Screen Size**: [If relevant to the bug]

### Error Information
- **Error Message**: [Exact error message if available]
- **Stack Trace**: [Relevant stack trace]
- **Browser Console**: [Console errors]
- **Server Logs**: [Backend errors]

## Pre-Investigation Checklist
- [ ] **Reproduction Verified**: Can reproduce the issue locally
- [ ] **Recent Changes**: Check recent deployments/commits
- [ ] **Similar Issues**: Search for related past issues
- [ ] **Environment Check**: Verify environment-specific issue
- [ ] **Test Coverage**: Check if area has test coverage
- [ ] **Performance Baseline**: Current performance metrics noted
- [ ] **Error Logs Gathered**: Collected all relevant logs

## Root Cause Analysis
### Initial Hypothesis
[Initial thoughts on what might be causing the issue]

### Investigation Approach
1. [First area to investigate]
2. [Second area to investigate]
3. [Third area to investigate]

## Systematic Debugging Protocol (CLAUDE.md)
Follow the proven 5-phase systematic debugging approach:

### Phase 1: Symptoms Analysis (5 minutes)
- [ ] **User Impact Assessment**
  - Number of affected users: [count/percentage]
  - Severity of impact: [description]
  - User workflow disruption: [details]
- [ ] **Error Frequency Analysis**
  - How often does it occur: [frequency]
  - Consistent reproduction: [yes/no/conditional]
  - Error patterns: [trends or patterns observed]
- [ ] **Recent Deployment Correlation**
  - Recent deployments: [list recent changes]
  - Timeline correlation: [when issue started vs deployments]
  - Configuration changes: [any environment changes]
- [ ] **Issue Categorization**
  - Type: [Frontend/Backend/Database/Configuration/Integration]
  - Scope: [Single user/Multiple users/System-wide]
  - Complexity: [Simple fix/Complex investigation required]

### Phase 2: Browser DevTools Analysis (10 minutes)
- [ ] **Network Tab Investigation**
  - Failed HTTP requests: [list failed requests]
  - Response codes: [4xx, 5xx errors]
  - Request timing: [slow requests identified]
  - CORS issues: [cross-origin problems]
- [ ] **Console Error Analysis**
  - JavaScript errors: [exact error messages]
  - Stack traces: [complete error stack traces]
  - Warning messages: [potential related warnings]
  - Component errors: [React/framework-specific errors]

### Phase 3: API Testing (10 minutes)
- [ ] **Direct CURL Testing**
  ```bash
  # Test API endpoint directly
  curl -X GET "api-endpoint" \
    -H "Content-Type: application/json" \
    -H "Origin: expected-domain"
  ```
- [ ] **Backend Log Verification**
  - Server error logs: [backend error messages]
  - Database query logs: [SQL errors or slow queries]
  - Authentication logs: [auth-related issues]
  - Rate limiting logs: [throttling issues]

### Phase 4: Configuration Review (15 minutes)
- [ ] **Environment Configuration**
  - Development vs Production: [config differences]
  - Environment variables: [missing or incorrect values]
  - Database configuration: [connection strings, timeouts]
  - Third-party services: [API keys, service availability]
- [ ] **CORS and Security Settings**
  - Allowed origins: [verify CORS configuration]
  - Headers configuration: [check allowed headers]
  - Methods configuration: [verify allowed methods]
  - Credentials handling: [cookie/auth configuration]

### Phase 5: Solution & Documentation
- [ ] **Root Cause Identification**
  - Primary cause: [main issue identified]
  - Contributing factors: [additional factors]
  - Why it wasn't caught: [testing or process gaps]
- [ ] **Fix Implementation**
  - Solution approach: [method chosen to fix]
  - Code changes: [specific changes made]
  - Configuration updates: [any config changes]
  - Testing performed: [how fix was validated]

## Progress Log
### [Time] - Investigation Start
[Investigation notes will be added here]

### [Time] - Root Cause Identified
[Root cause details will be documented here]

### [Time] - Fix Implementation
[Implementation details will be recorded here]

## Three-Strike Analysis (If Applicable)
If this is the 3rd attempt at fixing this issue, conduct formal failure analysis:

### Attempt History
1. **Attempt 1**: [Previous approach, failure mode, lessons]
2. **Attempt 2**: [Modified approach, failure mode, lessons]  
3. **Attempt 3**: [Current approach, outcomes]

### Root Cause Analysis
- **Technical Factors**: [Code issues, architecture problems, tool limitations]
- **Process Factors**: [Planning gaps, communication issues, resource constraints]
- **Knowledge Factors**: [Missing expertise, documentation gaps, learning needs]

## Solution Documentation
### Root Cause
[Detailed explanation of what caused the issue]

### Fix Applied
- **Code Changes**: [Files and changes made]
- **Configuration Changes**: [Any config updates]
- **Database Changes**: [Any data fixes]

### Code Changes Example
```diff
// Example of fix implementation
- old code that caused the issue
+ new code that fixes the issue
```

### Verification Steps
1. [How to verify the fix works]
2. [Test scenarios to run]
3. [Expected outcomes]

## Testing & Validation
- [ ] **Manual Testing**: Fix verified manually
- [ ] **Automated Tests**: New tests added to prevent regression
- [ ] **Edge Cases**: Related edge cases tested
- [ ] **Performance**: No performance degradation
- [ ] **Cross-browser**: Tested across target browsers
- [ ] **Mobile Testing**: Verified on mobile devices if applicable
- [ ] **User Acceptance**: Fix solves original user problem

## Quality Gates
- [ ] **Bug Resolution**: Original issue completely fixed
- [ ] **No Regressions**: No new issues introduced
- [ ] **Performance**: Metrics within acceptable range
- [ ] **Test Coverage**: New tests prevent recurrence
- [ ] **Code Quality**: Fix follows coding standards
- [ ] **Documentation**: All changes documented

## Regression Prevention
### Tests Added
- [Test 1 description and purpose]
- [Test 2 description and purpose]
- [Integration test for the specific scenario]
- [Performance test to catch degradation]

### Monitoring Added
- [Monitoring/alerting improvements]
- [Log improvements for better debugging]
- [Performance metrics tracking]
- [Error rate monitoring]

### Documentation Updates
- [Code comments added for clarity]
- [README updates if setup changed]
- [API documentation if behavior changed]
- [Troubleshooting guide enhanced]
- [Knowledge base article created]

## Deployment Plan
- [ ] **Fix Tested**: Thoroughly tested in development
- [ ] **Review Required**: Code review completed
- [ ] **Staging Deployment**: Deployed and verified in staging
- [ ] **Production Plan**: Deployment window identified
- [ ] **Rollback Plan**: Rollback procedure documented

## Performance Impact Analysis
### Before Fix
- **Response Time**: [ms]
- **Error Rate**: [%]
- **User Experience**: [description]

### After Fix
- **Response Time**: [ms]
- **Error Rate**: [%]
- **User Experience**: [description]
- **Performance Change**: [improved/unchanged/degraded by X%]

## Lessons Learned
### What Went Wrong
[Analysis of how this bug was introduced]

### What Worked Well
- [Effective debugging technique]
- [Tool that helped identify the issue]
- [Process that expedited resolution]

### Prevention Measures
- **Code Review**: [Enhanced review checklist items]
- **Testing**: [New test scenarios to add]
- **Monitoring**: [Alerts to implement]
- **Documentation**: [Guides to create or update]

### Process Improvements
- [Development process changes]
- [Testing strategy updates]
- [Deployment procedure enhancements]

## Knowledge Transfer
### Technical Insights
- **Bug Pattern**: [Type of issue and characteristics]
- **Detection Method**: [How to identify similar issues]
- **Solution Pattern**: [Reusable solution approach]
- **Prevention Strategy**: [How to avoid this in future]

### Team Learning
- [Key insight that team should know]
- [Tool or technique that proved valuable]
- [Process improvement to share]

## Follow-up Actions
### Immediate (Next 24 hours)
- [ ] Deploy fix to affected environments
- [ ] Monitor for issue recurrence
- [ ] Communicate resolution to stakeholders

### Short-term (Next Sprint)
- [ ] Add comprehensive test coverage
- [ ] Update monitoring and alerting
- [ ] Document in team knowledge base

### Long-term (Next Quarter)
- [ ] Architecture improvements to prevent class of issues
- [ ] Tool or process enhancements
- [ ] Team training on prevention techniques

## Session Completion Checklist
- [ ] **Bug Fixed**: Issue completely resolved
- [ ] **Tests Added**: Regression tests prevent recurrence
- [ ] **Performance Verified**: No negative impact
- [ ] **Documentation Complete**: All updates made
- [ ] **Knowledge Captured**: Learnings documented
- [ ] **Team Notified**: Resolution communicated