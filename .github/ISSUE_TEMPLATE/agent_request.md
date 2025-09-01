---
name: New Agent Request
about: Request a new specialized agent for the workflow system
title: '[AGENT] '
labels: ['agent-request', 'enhancement', 'triage']
assignees: ''
---

## Agent Overview
**Proposed Agent Name**: [e.g., security-specialist, compliance-auditor, performance-optimizer]

**Agent Category**:
- [ ] Core Workflow Agent
- [ ] Domain Specialist
- [ ] Technology Specialist  
- [ ] Quality Specialist
- [ ] Manufacturing Specialist

## Agent Purpose
A clear description of what this agent would do and why it's needed.

## Domain Expertise
Describe the specific knowledge and capabilities this agent would provide:

### Primary Skills
- [Skill 1]
- [Skill 2]
- [Skill 3]

### Manufacturing Focus (if applicable)
- **Industry Sectors**: [e.g., food processing, pharmaceuticals, automotive]
- **Compliance Standards**: [e.g., FDA 21 CFR Part 11, HACCP, ISO 22000]
- **System Types**: [e.g., MES, SCADA, ERP, Historian]
- **Process Types**: [e.g., batch processing, continuous manufacturing, discrete manufacturing]

### .NET 9 Specialization (if applicable)
- **Architecture Patterns**: [e.g., Clean Architecture, CQRS, Event Sourcing]
- **Technology Stack**: [e.g., ASP.NET Core, Entity Framework, SignalR]
- **Azure Services**: [e.g., App Service, AKS, Key Vault, Application Insights]
- **Security Patterns**: [e.g., Azure AD B2C, JWT, OAuth 2.0]

## Use Cases

### Use Case 1: [Scenario Title]
**Context**: [Project type and situation where this agent would be valuable]
**Current Gap**: [What's missing without this agent]
**Agent Value**: [How this agent would help]
**Expected Output**: [What the agent would produce]

### Use Case 2: [Scenario Title] (if applicable)
**Context**: [Project type and situation where this agent would be valuable]
**Current Gap**: [What's missing without this agent]
**Agent Value**: [How this agent would help]
**Expected Output**: [What the agent would produce]

### Use Case 3: [Scenario Title] (if applicable)
**Context**: [Project type and situation where this agent would be valuable]
**Current Gap**: [What's missing without this agent]
**Agent Value**: [How this agent would help]
**Expected Output**: [What the agent would produce]

## Agent Integration

### When to Include Agent
Describe the conditions that would trigger including this agent in a workflow:
- **Request Types**: [NEW_PROJECT, BUG_FIX, ENHANCEMENT, REFACTOR]
- **Keywords**: [What terms in user requests would trigger this agent]
- **Project Context**: [What existing project state would indicate need for this agent]
- **Other Agents**: [What other agents this would commonly work with]

### Agent Chain Position
Where would this agent fit in the workflow?
- [ ] Early Phase (Analysis/Planning)
- [ ] Middle Phase (Architecture/Development)
- [ ] Late Phase (Validation/Testing)
- [ ] Cross-Cutting (Multiple phases)
- [ ] Conditional (Only when specific conditions met)

### Agent Dependencies
- **Requires Input From**: [Which agents should run before this one]
- **Provides Input To**: [Which agents would benefit from this agent's output]
- **Optional Collaboration**: [Which agents could enhance this agent's work]

## Context Awareness

### Reads Existing Documentation
What existing project documentation would this agent analyze?
- [ ] `docs/project/requirements.md`
- [ ] `docs/architecture/system-architecture.md`
- [ ] `docs/architecture/security-design.md`
- [ ] `docs/current/known-issues.md`
- [ ] Source code files
- [ ] Test files
- [ ] Configuration files
- [ ] Other: [specify]

### Creates/Updates Documentation
What documentation would this agent create or update?
- **New Documents**: [List new files the agent would create]
- **Updated Documents**: [List existing files the agent would enhance]
- **Iteration Documentation**: [What would be documented in iteration folders]

## Quality Contributions

### Quality Gates
How would this agent contribute to quality validation?
- **Quality Metrics**: [What specific quality criteria would this agent validate]
- **Scoring Weight**: [How important is this agent's validation to overall quality]
- **Pass/Fail Criteria**: [What constitutes passing validation from this agent]

### Quality Improvements
What quality improvements would this agent provide?
- [Quality improvement 1]
- [Quality improvement 2]
- [Quality improvement 3]

## Technical Specification

### Input Requirements
```yaml
required_context:
  - existing_project_state: boolean
  - request_classification: string
  - previous_agent_outputs: array

optional_context:
  - domain_requirements: object
  - compliance_standards: array
  - integration_systems: array
```

### Output Specification
```yaml
primary_outputs:
  documentation:
    - file_path: string
    - content_type: string
    - update_strategy: "create|update|append"
  
  recommendations:
    - category: string
    - priority: string
    - description: string
  
  quality_assessment:
    - criteria: string
    - score: number
    - feedback: string
```

### Agent Configuration
```yaml
agent_config:
  name: "proposed-agent-name"
  category: "specialist-type"
  triggers:
    - keywords: []
    - request_types: []
    - context_conditions: []
  
  capabilities:
    - primary_skills: []
    - domain_expertise: []
    - technology_focus: []
  
  integration:
    - depends_on: []
    - provides_to: []
    - quality_weight: number
```

## Manufacturing Considerations (if applicable)

### Compliance Requirements
- **Regulatory Standards**: [FDA, HACCP, ISO, etc.]
- **Audit Trail**: [What audit information would this agent generate]
- **Documentation Standards**: [What documentation standards would be enforced]
- **Validation Requirements**: [What validation would be performed]

### System Integration
- **MES Integration**: [How would this agent handle MES system patterns]
- **SCADA Patterns**: [What SCADA integration patterns would be supported]
- **ERP Connectivity**: [How would ERP integration be addressed]
- **Data Historian**: [What historian integration would be provided]

### Multi-Facility Support
- **Configuration Management**: [How would multi-facility configurations be handled]
- **Data Synchronization**: [What data sync patterns would be supported]
- **Compliance Variations**: [How would facility-specific compliance be managed]

## Success Metrics
How will we measure the success of this agent?

- **Usage Frequency**: [How often the agent is selected by orchestrator]
- **Quality Improvement**: [Measurable quality improvements provided]
- **User Satisfaction**: [Developer feedback on agent value]
- **Token Efficiency**: [Token usage optimization achieved]
- **Manufacturing Value**: [Industry-specific value delivered]

## Implementation Priority
- **Business Value**: [Critical/High/Medium/Low]
- **Implementation Effort**: [High/Medium/Low] 
- **Manufacturing Demand**: [High/Medium/Low]
- **Integration Complexity**: [High/Medium/Low]

## Additional Context
Any other context, examples, or requirements for this agent.

## Related Agents
List any existing agents that are similar or that this agent would complement.

---

**For Maintainers:**
- [ ] Agent requirements validated
- [ ] Domain expertise verified
- [ ] Integration points defined
- [ ] Quality contribution specified
- [ ] Implementation approach approved