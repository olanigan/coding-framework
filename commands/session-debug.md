Execute systematic debugging protocol based on CLAUDE.md emergency response checklist and TDD best practices.

## Debugging Command Usage:
- `/project:session-debug start [issue-description]` - Begin systematic debugging session
- `/project:session-debug symptoms` - Document and analyze symptoms (5min)
- `/project:session-debug browser` - Browser DevTools analysis (10min)
- `/project:session-debug api` - Direct API testing with CURL (10min)
- `/project:session-debug config` - Configuration review (15min)
- `/project:session-debug complete [solution]` - Document solution and close

## Systematic Debugging Protocol:

### Phase 1: Symptoms Analysis (5 minutes)

When starting debug session (`/project:session-debug start [issue-description]`):

1. **Create Debug Session File**: `debug/[YYYY-MM-DD-HHMM]-[issue-type].md`

```markdown
# Debug Session - [Timestamp] - [Issue Description]

## Issue Overview
- **Issue Type**: [Frontend/Backend/Infrastructure/CORS/Performance/Security]
- **Severity**: [Critical/High/Medium/Low]
- **User Impact**: [Description of user impact]
- **Environment**: [Development/Staging/Production]
- **Reported By**: [Source of issue report]

## Symptoms Documentation
### User-Reported Symptoms
- **What**: [What the user was trying to do]
- **Expected**: [What should have happened]
- **Actual**: [What actually happened]
- **Frequency**: [Always/Sometimes/Rarely]
- **Reproducible**: [Yes/No/Partially]

### Error Messages
- **Console Errors**: [Browser console output]
- **Server Logs**: [Backend error logs]
- **Network Errors**: [HTTP status codes and messages]
- **Database Errors**: [DB error messages if applicable]

### Environmental Context
- **Browser**: [Chrome/Firefox/Safari/Edge + version]
- **Device**: [Desktop/Mobile/Tablet]
- **Operating System**: [OS version]
- **Network**: [WiFi/Cellular/Corporate]
- **Time of Occurrence**: [When did it start happening]

### Recent Changes
- **Deployments**: [Recent deployments in last 24h]
- **Configuration Changes**: [Any config updates]
- **Dependency Updates**: [Package/library updates]
- **Database Changes**: [Schema or data changes]

## Investigation Timeline
[Track investigation progress with timestamps]
```

2. **Initial Assessment**:
   - Categorize issue type (CORS, API, UI, Configuration, Performance)
   - Assess severity and user impact
   - Identify recent changes that might be related
   - Document reproduction steps

### Phase 2: Browser DevTools Analysis (10 minutes)

When analyzing browser issues (`/project:session-debug browser`):

1. **Network Tab Investigation**:
   - Failed requests and HTTP status codes
   - CORS errors and preflight requests
   - Request/response headers
   - Timing analysis for performance issues

2. **Console Analysis**:
   - JavaScript errors and stack traces
   - Warning messages
   - Failed resource loading
   - Network connectivity issues

3. **Application State**:
   - Local storage and session storage
   - Cookies and authentication tokens
   - Service worker status
   - Cache status

**Documentation Format**:
```markdown
### Browser DevTools Analysis - [Timestamp]

#### Network Tab Findings
- **Failed Requests**: [List with status codes]
- **CORS Errors**: [Origin/destination analysis]
- **Headers**: [Relevant request/response headers]
- **Timing**: [Performance bottlenecks identified]

#### Console Errors
- **JavaScript Errors**: [Error messages and stack traces]
- **Resource Loading**: [Failed CSS/JS/image loads]
- **API Responses**: [Unexpected API responses]

#### Application State
- **Authentication**: [Token status and validity]
- **Local Storage**: [Relevant stored data]
- **Cookies**: [Session and tracking cookies]
- **Cache**: [Service worker and browser cache]

#### Screenshots
- [Reference to screenshots if taken]
```

### Phase 3: API Testing with CURL (10 minutes)

When testing APIs directly (`/project:session-debug api`):

1. **Direct API Validation**:
   - Test endpoints independently of browser
   - Verify CORS headers with origin headers
   - Check authentication and authorization
   - Validate request/response formats

2. **CORS Specific Testing**:
```bash
# Test CORS preflight
curl -H "Origin: https://app.domain.com" \
     -H "Access-Control-Request-Method: POST" \
     -H "Access-Control-Request-Headers: Content-Type,Authorization" \
     -X OPTIONS \
     https://api.domain.com/endpoint

# Test actual request with origin
curl -H "Origin: https://app.domain.com" \
     -H "Content-Type: application/json" \
     -H "Authorization: Bearer token" \
     -X POST \
     -d '{"data": "test"}' \
     https://api.domain.com/endpoint
```

**Documentation Format**:
```markdown
### API Testing Analysis - [Timestamp]

#### CURL Test Results
- **Endpoint**: [API endpoint tested]
- **Method**: [HTTP method]
- **Headers Sent**: [Request headers]
- **Response Status**: [HTTP status code]
- **Response Headers**: [CORS and other relevant headers]
- **Response Body**: [Response content]

#### CORS Configuration Test
- **Preflight Response**: [OPTIONS request result]
- **Access-Control-Allow-Origin**: [Value received]
- **Access-Control-Allow-Methods**: [Allowed methods]
- **Access-Control-Allow-Headers**: [Allowed headers]

#### Authentication Test
- **Token Validity**: [Valid/Invalid/Expired]
- **Authorization Headers**: [Correct format and content]
- **Permission Level**: [Adequate permissions for operation]

#### Data Validation
- **Request Format**: [JSON schema validation]
- **Response Format**: [Expected vs actual structure]
- **Error Handling**: [Proper error responses]
```

### Phase 4: Configuration Review (15 minutes)

When reviewing configuration (`/project:session-debug config`):

1. **Environment Configuration**:
   - Compare development vs staging vs production settings
   - Verify environment variables
   - Check CORS domain configurations
   - Validate API endpoints and base URLs

2. **Infrastructure Configuration**:
   - DNS resolution and routing
   - SSL/TLS certificate status
   - Load balancer configuration
   - CDN settings and cache behavior

3. **Application Configuration**:
   - Framework-specific settings
   - Database connection strings
   - Third-party service configurations
   - Feature flags and toggles

**Documentation Format**:
```markdown
### Configuration Review - [Timestamp]

#### Environment Parity Check
- **Development**: [Config status and issues]
- **Staging**: [Config status and issues]
- **Production**: [Config status and issues]
- **Differences Found**: [Critical configuration differences]

#### CORS Configuration
- **Allowed Origins**: [List of configured origins]
- **Allowed Methods**: [Configured HTTP methods]
- **Allowed Headers**: [Configured headers]
- **Credentials Support**: [Enabled/Disabled]

#### DNS and Infrastructure
- **DNS Resolution**: [Domain resolution status]
- **SSL Certificates**: [Certificate validity and chain]
- **Load Balancer**: [Health check and routing]
- **CDN**: [Cache status and purge needed]

#### Application Settings
- **API Base URLs**: [Correct endpoints configured]
- **Database**: [Connection and query status]
- **External Services**: [Third-party integrations]
- **Feature Flags**: [Relevant feature status]
```

### Phase 5: Solution Documentation

When completing debug session (`/project:session-debug complete [solution]`):

1. **Root Cause Analysis**:
```markdown
### Solution Documentation - [Timestamp]

#### Root Cause
- **Primary Cause**: [What caused the issue]
- **Contributing Factors**: [Additional factors]
- **Why It Happened**: [Process or system failure]

#### Solution Implemented
- **Fix Applied**: [Detailed description of fix]
- **Files Changed**: [List of modified files]
- **Configuration Updates**: [Config changes made]
- **Deployment Steps**: [How fix was deployed]

#### Verification
- **Testing Performed**: [How fix was verified]
- **User Acceptance**: [User validation if applicable]
- **Monitoring**: [Ongoing monitoring put in place]

#### Prevention Measures
- **Process Improvements**: [Changes to prevent recurrence]
- **Monitoring Enhancements**: [New alerts or checks]
- **Documentation Updates**: [Knowledge base updates]
- **Training Needs**: [Team education required]

#### Time Investment
- **Total Debug Time**: [Time spent debugging]
- **Time to Resolution**: [Time from start to fix]
- **Future Prevention**: [Estimated time saved by prevention]
```

## Emergency Response Checklist:

### Critical Issues (Production Down):
1. **Immediate Response** (2 minutes):
   - [ ] Alert team and stakeholders
   - [ ] Check service status pages
   - [ ] Verify infrastructure health
   - [ ] Start incident log

2. **Quick Assessment** (5 minutes):
   - [ ] Recent deployment rollback if needed
   - [ ] Check error rate spikes
   - [ ] Verify external service status
   - [ ] Document user impact

3. **Systematic Investigation** (Follow standard protocol)

### Development Issues:
1. **Environment Verification**:
   - [ ] Local development server running
   - [ ] Correct branch and latest code
   - [ ] Environment variables loaded
   - [ ] Dependencies up to date

2. **Common Issue Checks**:
   - [ ] CORS configuration for current domain
   - [ ] API endpoint accessibility
   - [ ] Authentication token validity
   - [ ] Network connectivity

## Integration with Session Management:

- **Auto-link to Active Session**: Connect debug session to current development session
- **Sprint Impact Assessment**: Evaluate impact on sprint goals
- **Knowledge Transfer**: Document lessons learned for future sessions
- **Delivery Impact**: Assess effect on delivery timeline

## Best Practices Enforcement:

- **Progressive Debugging**: Symptoms → Browser → API → Config → Solution
- **Documentation First**: Document before investigating
- **Time-boxed Phases**: Stick to time limits for systematic approach
- **Verification Required**: Always verify fix works as expected
- **Prevention Focus**: Always include prevention measures