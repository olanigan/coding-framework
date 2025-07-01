# Failure Analysis Framework - SDLC v1.0

**Last Updated**: July 1, 2025  
**Version**: 1.0  
**Purpose**: Systematic approach to learning from failures and preventing recurrence

## Overview
The Three-Strike Failure Analysis Framework is a core component of SDLC v1.0, designed to turn failures into learning opportunities and process improvements. This framework ensures that when tasks fail multiple times, we conduct thorough analysis to prevent similar issues in the future.

## Three-Strike Rule Implementation

### When to Trigger Failure Analysis
Failure analysis is **mandatory** when any of these conditions are met:

1. **Task Failure**: Same task fails 3 times despite different approaches
2. **Sprint Failure**: Sprint objectives not met for 3 consecutive sprints
3. **Quality Failure**: Same type of bug/issue occurs 3 times
4. **Process Failure**: Same process breakdown occurs 3 times
5. **Performance Failure**: Performance standards missed 3 times for same component

### Immediate Response Protocol
When three-strike rule is triggered:
1. **STOP all related work** immediately
2. **Schedule failure analysis session** within 24 hours
3. **Notify stakeholders** of analysis process
4. **Document all previous attempts** before memory fades
5. **Assign failure analysis lead** (senior developer or team lead)

## Failure Analysis Process

### Phase 1: Failure Documentation (30 minutes)
#### Attempt History Documentation
For each failed attempt, document:
- **Date and Duration**: When attempted and time invested
- **Approach Used**: Strategy, methods, tools employed
- **Failure Mode**: Specific reason for failure
- **Blockers Encountered**: What prevented success
- **Lessons Learned**: Insights gained from the attempt
- **Documentation Links**: Reference to session notes or tickets

#### Impact Assessment
- **Resource Impact**: Total time/people invested
- **Business Impact**: Project delays, missed opportunities
- **Team Impact**: Morale, confidence, learning effects
- **Stakeholder Impact**: Trust, expectations, communication

### Phase 2: Root Cause Analysis (45 minutes)
#### Multi-Factor Analysis Framework
Systematically examine failures across three dimensions:

##### Technical Factors
- **Code Complexity**: Was task more complex than assessed?
- **Architecture Limitations**: Does current architecture support the requirement?
- **Technical Debt**: Is underlying technical debt blocking progress?
- **Tool Limitations**: Are development tools adequate for the task?
- **Integration Challenges**: Are there unexpected integration complexities?

##### Process Factors
- **Requirements Clarity**: Were requirements clear and complete?
- **Planning Accuracy**: Was estimation and planning realistic?
- **Communication Gaps**: Were there communication breakdowns?
- **Resource Allocation**: Were adequate resources allocated?
- **Risk Management**: Were risks properly identified and mitigated?

##### Knowledge Factors
- **Skill Gaps**: Does team have necessary technical skills?
- **Domain Expertise**: Is business domain knowledge sufficient?
- **Technology Experience**: Is team familiar with required technologies?
- **Best Practices**: Are we following industry best practices?
- **Learning Needs**: What training or mentorship is needed?

#### Root Cause Prioritization
Rank root causes by:
1. **Impact Severity**: How much did this contribute to failure?
2. **Frequency**: How often does this factor cause issues?
3. **Prevention Feasibility**: How easily can this be prevented?
4. **Learning Value**: How much can team learn from addressing this?

### Phase 3: Prevention Strategy Development (30 minutes)
#### Immediate Prevention Measures (Next Sprint)
- **Process Changes**: Immediate process improvements
- **Tool Upgrades**: Tools or technology changes needed
- **Training Plans**: Immediate skill development needs
- **Communication Improvements**: Better communication protocols
- **Quality Gates**: Additional checkpoints to add

#### Systemic Prevention Measures (Next Quarter)
- **Organizational Changes**: Team structure or role changes
- **Technology Strategy**: Long-term technology improvements
- **Process Standardization**: Organization-wide process improvements
- **Culture Development**: Cultural changes to support success
- **Knowledge Management**: Better knowledge capture and sharing

### Phase 4: Alternative Solution Development (15 minutes)
#### Revised Approach
Based on failure analysis, develop new approach:
- **Strategy Changes**: How approach will differ
- **Resource Requirements**: What resources are needed
- **Timeline Adjustments**: Realistic timeline with lessons learned
- **Risk Mitigation**: How identified risks will be addressed
- **Success Criteria**: Clear definition of success

#### Feasibility Assessment
- **Technical Feasibility**: Can this approach work technically?
- **Resource Availability**: Do we have needed resources?
- **Timeline Realism**: Is timeline achievable?
- **Stakeholder Support**: Will stakeholders support new approach?

## Failure Pattern Classification

### Technical Failure Patterns
#### Code & Architecture Issues
- **Complexity Underestimation**: Task more complex than initially assessed
- **Architecture Mismatch**: Current architecture doesn't support requirement
- **Technical Debt Impact**: Existing debt blocking new development
- **Integration Complexity**: Unexpected complexity in system integration
- **Performance Constraints**: Performance requirements not achievable

#### Technology & Tool Issues
- **Tool Inadequacy**: Development tools insufficient for task requirements
- **Framework Limitations**: Framework constraints blocking implementation
- **Library Dependencies**: Third-party library issues or limitations
- **Environment Problems**: Development/deployment environment issues
- **Technology Mismatch**: Wrong technology choice for requirements

### Process Failure Patterns
#### Planning & Requirements
- **Unclear Requirements**: Requirements not well-defined or understood
- **Scope Creep**: Task scope expanded during implementation
- **Unrealistic Estimates**: Insufficient time allocated for actual complexity
- **Resource Constraints**: Inadequate team capacity or wrong skills
- **Dependency Mismanagement**: Critical dependencies not identified early

#### Communication & Collaboration
- **Stakeholder Misalignment**: Different expectations between stakeholders
- **Team Communication**: Poor information flow within development team
- **Knowledge Silos**: Critical knowledge held by unavailable team members
- **Decision Delays**: Important decisions delayed blocking progress
- **Feedback Loops**: Insufficient or delayed feedback from users

### Knowledge Failure Patterns
#### Skill & Expertise Gaps
- **Technical Skills**: Team lacks specific technical expertise needed
- **Domain Knowledge**: Insufficient understanding of business requirements
- **Technology Experience**: Unfamiliarity with required technologies
- **Problem-Solving**: Ineffective debugging or problem-solving approaches
- **Best Practices**: Unaware of industry standards for this work type

#### Learning & Development
- **Training Needs**: Team requires specific training for success
- **Mentorship Gap**: Lack of available guidance for complex tasks
- **Knowledge Transfer**: Critical knowledge not properly documented
- **Research Insufficient**: Inadequate investigation of solutions
- **Prototype Missing**: Should have built proof of concept first

## Prevention Strategy Templates

### Technical Prevention Strategies
#### Architecture Improvements
- **Modular Design**: Improve system modularity for easier changes
- **API Design**: Better API design for integration flexibility
- **Performance Architecture**: Design for performance from the start
- **Scalability Planning**: Plan for scale early in architecture
- **Technology Standards**: Standardize on proven technologies

#### Development Process Improvements
- **Code Quality**: Enhanced code review and quality processes
- **Testing Strategy**: More comprehensive testing approaches
- **Performance Testing**: Regular performance testing and monitoring
- **Security Reviews**: Enhanced security review processes
- **Documentation Standards**: Better documentation requirements

### Process Prevention Strategies
#### Planning Improvements
- **Requirements Analysis**: More thorough requirements gathering
- **Risk Assessment**: Better risk identification and mitigation
- **Estimation Techniques**: Improved effort estimation methods
- **Resource Planning**: Better resource allocation and planning
- **Timeline Management**: More realistic timeline planning

#### Communication Enhancements
- **Stakeholder Alignment**: Regular stakeholder check-ins
- **Team Communication**: Improved team communication protocols
- **Decision Making**: Faster decision-making processes
- **Feedback Systems**: Better feedback collection and processing
- **Knowledge Sharing**: Enhanced knowledge sharing practices

### Knowledge Prevention Strategies
#### Skill Development
- **Training Programs**: Systematic skill development programs
- **Mentorship**: Formal mentorship programs for complex work
- **Knowledge Base**: Comprehensive knowledge documentation
- **Best Practices**: Documentation and training on best practices
- **Research Process**: Systematic research and prototyping approaches

#### Learning Culture
- **Failure Acceptance**: Culture that encourages learning from failures
- **Experimentation**: Safe environment for trying new approaches
- **Knowledge Sharing**: Regular knowledge sharing sessions
- **Continuous Learning**: Ongoing learning and development programs
- **External Learning**: Conference attendance and external training

## Implementation Guidelines

### Failure Analysis Session Structure
1. **Opening (5 min)**: Review purpose and process
2. **Attempt Documentation (30 min)**: Document all failed attempts
3. **Root Cause Analysis (45 min)**: Systematic cause identification
4. **Prevention Strategy (30 min)**: Develop prevention measures
5. **Alternative Solution (15 min)**: Create new approach
6. **Action Planning (15 min)**: Define next steps and ownership

### Documentation Requirements
#### Failure Analysis Report
Must include:
- **Executive Summary**: Key findings and recommendations
- **Attempt History**: Detailed documentation of all attempts
- **Root Cause Analysis**: Systematic analysis of failure factors
- **Prevention Strategy**: Immediate and long-term prevention measures
- **Alternative Solution**: Revised approach with success criteria
- **Action Plan**: Specific actions with owners and timelines

#### Knowledge Base Integration
- Add failure patterns to team knowledge base
- Update best practices documentation
- Enhance onboarding materials with lessons learned
- Create decision frameworks based on insights

### Success Metrics & Monitoring
#### Leading Indicators
- **Risk Detection**: How early are risks identified?
- **Planning Accuracy**: Improvement in estimation accuracy
- **Communication Quality**: Stakeholder satisfaction with communication
- **Knowledge Application**: Use of documented best practices

#### Lagging Indicators
- **Task Success Rate**: First-time success rate improvement
- **Rework Frequency**: Reduction in task rework
- **Timeline Adherence**: Improvement in meeting deadlines
- **Quality Metrics**: Reduction in defects and issues

#### Monitoring Process
- **Weekly Reviews**: Track prevention measure implementation
- **Monthly Metrics**: Review leading and lagging indicators
- **Quarterly Assessment**: Comprehensive effectiveness review
- **Annual Strategy**: Review and update failure analysis strategy

## Organizational Integration

### Team Responsibilities
#### Development Team
- Trigger failure analysis when three-strike rule activated
- Participate actively in failure analysis sessions
- Implement prevention measures in daily work
- Share learnings with broader team

#### Team Leads
- Facilitate failure analysis sessions
- Ensure prevention measures are implemented
- Track effectiveness of prevention strategies
- Escalate systemic issues to management

#### Management
- Support failure analysis process and cultural change
- Allocate resources for prevention measure implementation
- Review quarterly failure analysis effectiveness
- Make organizational changes based on insights

### Cultural Integration
#### Psychological Safety
- Treat failures as learning opportunities, not blame occasions
- Encourage open discussion of failures and challenges
- Recognize teams that effectively learn from failures
- Share failure insights across organization

#### Process Integration
- Include failure analysis in project planning
- Make failure analysis part of retrospective processes
- Integrate prevention measures into development standards
- Use failure insights for team performance reviews

## Advanced Failure Analysis Techniques

### Failure Mode and Effects Analysis (FMEA)
For complex systemic failures:
1. **Identify Potential Failures**: List all possible failure modes
2. **Impact Assessment**: Analyze consequences of each failure
3. **Probability Assessment**: Estimate likelihood of each failure
4. **Detection Assessment**: Evaluate ability to detect failures early
5. **Risk Priority**: Calculate risk priority numbers for focus

### Fishbone Diagram Analysis
For complex multi-factor failures:
- **People**: Team skills, communication, motivation factors
- **Process**: Development process, planning, review procedures
- **Technology**: Tools, frameworks, infrastructure factors
- **Environment**: Workplace, time pressure, resource factors
- **Materials**: Requirements, documentation, data quality factors

### 5 Whys Analysis
For drilling down to root causes:
1. **Why did the task fail?** [Surface reason]
2. **Why did [surface reason] happen?** [Intermediate reason]
3. **Why did [intermediate reason] occur?** [Deeper reason]
4. **Why did [deeper reason] happen?** [Root cause area]
5. **Why did [root cause area] exist?** [Systemic root cause]

## Failure Analysis Templates & Tools

### Quick Assessment Template
For rapid failure classification:
```
Failure Type: [Technical/Process/Knowledge]
Primary Factor: [Main contributing factor]
Impact Level: [High/Medium/Low]
Prevention Effort: [High/Medium/Low]
Recommended Action: [Immediate action needed]
```

### Detailed Analysis Template
Comprehensive failure analysis format:
- Use failure-analysis-session.md template
- Include all required documentation sections
- Follow systematic analysis process
- Create action plan with owners and timelines

### Tracking Tools
- Failure pattern tracking spreadsheet
- Prevention measure effectiveness dashboard
- Team learning and improvement metrics
- Organizational failure analysis trends

---

**Framework Implementation**: Mandatory for all three-strike situations  
**Training Required**: All team members must understand this framework  
**Review Cycle**: Quarterly framework effectiveness review  
**Contact**: Team lead for failure analysis support