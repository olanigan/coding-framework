Start a performance optimization session following SDLC v1.0 performance-first development standards.

## Performance Optimization Session Creation Process:

1. **Generate Session Filename**: Create session file in `sessions/` using format:
   - `YYYY-MM-DD-HHMM-performance-[optimization-target].md`
   - Example: `2025-07-01-1400-performance-api-response-optimization`

2. **Use Performance Template**: Initialize with `templates/performance-optimization-session.md`

3. **Performance Categories** (SDLC v1.0 Standards):
   - **API Performance**: Response time, throughput, database optimization
   - **Frontend Performance**: Page load, bundle size, rendering optimization
   - **Database Performance**: Query optimization, indexing, connection pooling
   - **Infrastructure Performance**: Scaling, caching, CDN optimization
   - **Build Performance**: CI/CD optimization, development workflow

4. **Session Initialization**: Populate template with current performance baseline:

```markdown
# Development Session - [Date Time] - performance - [optimization-target]

## Session Overview
- **Start Time**: [Current timestamp]
- **Session Type**: Performance Optimization
- **Estimated Duration**: 2-6 hours
- **Performance Category**: [Category from above]
- **Related Sprint**: [Sprint 5.x if maintenance sprint]

## SDLC v1.0 Performance Standards Compliance
Reference: performance-standards.md

### Mandatory Targets:
- **API Response Time**: < 500ms end-to-end
- **Page Load Time**: < 2 seconds initial load
- **Database Query Time**: < 100ms execution
- **Component Render**: < 100ms for interactive elements
- **Core Web Vitals**: LCP < 2.5s, FID < 100ms, CLS < 0.1

## Current Performance Baseline
[Document current metrics before optimization]

[Continue with full performance-optimization-session.md template...]
```

5. **Pre-Optimization Checklist**:
   - [ ] **Performance Baseline**: Document current metrics
   - [ ] **Monitoring Setup**: Ensure performance monitoring active
   - [ ] **Test Environment**: Performance testing environment ready
   - [ ] **Standards Review**: Review performance-standards.md requirements
   - [ ] **Load Testing**: Baseline load test completed

6. **Performance Testing Integration**:
   - Use tools from performance-standards.md
   - Include synthetic and real user monitoring
   - Test across all target environments
   - Validate mobile and slow connection performance

7. **Optimization Strategy Framework**:
   - **Phase 1**: Quick wins (1-2 hours)
   - **Phase 2**: Structural improvements (2-4 hours)  
   - **Phase 3**: Advanced optimization (4+ hours)
   - Follow performance-standards.md optimization strategies

8. **Quality Gates Integration**:
   - All performance standards must be met
   - No performance regressions introduced
   - Load testing validates improvements
   - Real user monitoring shows positive impact

After creating the session file, update `sessions/.current-session` to track the active session filename.

## Confirmation Message:
Confirm performance session started with:
- Optimization target and expected improvements
- Current performance baseline metrics
- Performance standards compliance requirements
- Testing and validation approach

## Available Commands During Performance Work:
- `/project:session-update` - Log optimization progress and metrics
- `/project:session-debug` - If performance issues arise during optimization
- `/project:session-end` - Complete with performance results summary

## SDLC v1.0 Performance Requirements:
- **Performance Budgets**: Must be defined before optimization
- **Measurement-Driven**: All improvements must be measured
- **User-Centric Metrics**: Focus on user experience impact
- **Continuous Monitoring**: Real-time performance tracking required
- **No Regressions**: Performance cannot degrade in other areas

## Performance Monitoring Integration:
- Set up alerts for performance degradation
- Configure real user monitoring (RUM)
- Include performance metrics in deployment pipeline
- Plan quarterly performance reviews