# Contributing to Claude Sub-Agent Spec Workflow System

Thank you for your interest in contributing to the Claude Sub-Agent Spec Workflow System! This project aims to create a comprehensive, context-aware AI-driven development workflow system optimized for manufacturing industry applications.

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [How Can I Contribute?](#how-can-i-contribute)
- [Getting Started](#getting-started)
- [Development Guidelines](#development-guidelines)
- [Agent Development](#agent-development)
- [Documentation Standards](#documentation-standards)
- [Testing Guidelines](#testing-guidelines)
- [Submission Process](#submission-process)

## Code of Conduct

This project adheres to a code of conduct adapted for AI-assisted development:

- **Be Respectful**: Treat all contributors with respect and professionalism
- **Be Collaborative**: Work together to improve the workflow system
- **Be Constructive**: Provide helpful feedback and suggestions
- **Be Patient**: Remember that AI-assisted development is still evolving
- **Be Inclusive**: Welcome contributors of all skill levels and backgrounds

## How Can I Contribute?

### 🐛 Reporting Bugs

Before creating bug reports, please check existing issues. When creating a bug report, include:

- **Clear description** of the issue
- **Steps to reproduce** the problem
- **Expected vs actual behavior**
- **Environment details** (Claude Code version, .NET version, OS)
- **Agent logs** if applicable
- **Project context** (new project, enhancement, bug fix, refactor)

### 💡 Suggesting Enhancements

Enhancement suggestions are welcome! Please provide:

- **Clear description** of the enhancement
- **Use case scenarios** where it would be helpful
- **Manufacturing domain relevance** if applicable
- **Potential implementation approach**
- **Impact on existing workflows**

### 🔧 Code Contributions

We welcome code contributions in these areas:

- **New Specialized Agents**: Domain-specific agents for manufacturing, compliance, etc.
- **Workflow Improvements**: Better context awareness, agent selection logic
- **Quality Gates**: Enhanced validation criteria for .NET 9 projects
- **Documentation**: Examples, tutorials, best practices
- **Integration**: CI/CD, Azure DevOps, manufacturing systems

## Getting Started

### Prerequisites

- Claude Code (latest version with Sub-Agents support)
- .NET 9 SDK (for .NET projects)
- Git for version control
- Understanding of Clean Architecture principles
- Basic knowledge of manufacturing software requirements (for domain-specific contributions)

### Local Development Setup

1. **Fork and clone the repository**
   ```bash
   git clone https://github.com/YOUR_USERNAME/claude-sub-agent.git
   cd claude-sub-agent
   ```

2. **Set up the development environment**
   ```bash
   # Create test project structure
   mkdir -p test-project/.claude/{agents,commands,docs}
   cp -r agents/*/*.md test-project/.claude/agents/
   cp commands/*.md test-project/.claude/commands/
   ```

3. **Initialize documentation structure**
   ```bash
   cd test-project
   mkdir -p docs/{project,architecture,iterations,current,archive}
   touch docs/current/{active-tasks.md,known-issues.md,recent-changes.md}
   ```

4. **Test the workflow**
   ```bash
   # Test basic workflow functionality
   /agent-workflow "Create a simple test application"
   ```

## Development Guidelines

### .NET 9 Standards

All .NET-related contributions must follow:

- **Clean Architecture** principles with proper layer separation
- **Modern C# 13** features and patterns
- **Entity Framework Core** best practices for data access
- **ASP.NET Core** patterns for web APIs
- **xUnit** testing framework for all test code
- **Azure-ready** deployment configurations

### Code Quality Requirements

- **Code Analysis**: All C# code must pass StyleCop and Roslyn analyzers
- **Test Coverage**: Minimum 85% coverage for new features
- **Security**: Follow OWASP guidelines and secure coding practices
- **Performance**: Consider manufacturing environment performance requirements
- **Documentation**: All public APIs must have XML documentation

### Manufacturing Domain Guidelines

When contributing domain-specific features:

- **Compliance Awareness**: Consider FDA, HACCP, ISO standards
- **Integration Patterns**: Design for MES, SCADA, ERP system integration
- **Multi-Facility Support**: Account for distributed manufacturing operations
- **Audit Requirements**: Include appropriate logging and traceability
- **Real-Time Considerations**: Handle time-sensitive manufacturing data

## Agent Development

### Agent Structure

All agents must follow this structure:

```markdown
# Agent Name

## Role
Brief description of the agent's purpose and expertise

## Context Awareness
- How the agent reads existing project state
- What documentation it updates
- How it avoids regenerating existing work

## Capabilities
- Primary skills and knowledge areas
- .NET 9 specific optimizations
- Manufacturing domain expertise (if applicable)

## Input Requirements
- What information the agent needs
- Dependencies on other agents
- Context requirements

## Output Specifications
- Documentation files created/updated
- Code patterns generated
- Quality criteria applied

## Integration Points
- How it works with other agents
- Handoff protocols
- Quality gate contributions
```

### Agent Categories

Agents fall into these categories:

1. **Core Workflow Agents**: Essential for all projects (orchestrator, analyst, architect, developer, validator, tester)
2. **Domain Specialists**: Manufacturing, compliance, integration experts
3. **Technology Specialists**: Frontend, backend, database, security experts
4. **Quality Specialists**: Testing, performance, security validation experts

### Agent Testing

All agents must include:

- **Unit Tests**: Test individual agent logic
- **Integration Tests**: Test agent chains and handoffs
- **Context Tests**: Verify context awareness functionality
- **Quality Tests**: Validate quality gate contributions
- **Example Projects**: Demonstrate agent capabilities

## Documentation Standards

### Structured Documentation

Follow the established documentation hierarchy:

```
docs/
├── project/         # Stable core documentation
├── architecture/    # System design documentation
├── iterations/      # Version-controlled changes
├── current/         # Active working state
└── archive/         # Historical documentation
```

### Documentation Guidelines

- **Markdown Format**: Use GitHub-flavored markdown
- **Clear Headings**: Use descriptive section headers
- **Code Examples**: Include practical examples
- **Manufacturing Context**: Provide industry-specific examples
- **Version Control**: Document what changed and why
- **Incremental Updates**: Enhance rather than replace existing docs

### Agent Documentation

Each agent must have:

- **Agent specification** in markdown format
- **Usage examples** with before/after scenarios  
- **Integration examples** showing agent chains
- **Quality criteria** the agent validates
- **Manufacturing use cases** (if domain-specific)

## Testing Guidelines

### Test Categories

1. **Agent Unit Tests**: Test individual agent logic and outputs
2. **Workflow Integration Tests**: Test complete agent chains
3. **Context Awareness Tests**: Verify incremental documentation updates
4. **Quality Gate Tests**: Validate .NET 9 quality criteria
5. **Manufacturing Domain Tests**: Test industry-specific scenarios

### Test Requirements

- **Comprehensive Coverage**: Test all agent capabilities
- **Context Scenarios**: Test with existing vs new projects
- **Error Handling**: Test failure scenarios and recovery
- **Performance**: Test with realistic project sizes
- **Manufacturing Scenarios**: Test compliance and integration requirements

### Example Test Structure

```csharp
[Fact]
public async Task SpecDeveloper_WithExistingProject_UpdatesCodeIncrementally()
{
    // Arrange: Set up existing project context
    var existingProject = CreateManufacturingProjectContext();
    var enhancementRequest = "Add real-time inventory tracking";
    
    // Act: Run spec-developer agent
    var result = await specDeveloper.ProcessRequest(enhancementRequest, existingProject);
    
    // Assert: Verify incremental updates
    Assert.True(result.PreservedExistingCode);
    Assert.Contains("SignalR", result.AddedFeatures);
    Assert.Equal(95, result.QualityScore);
}
```

## Submission Process

### Pull Request Guidelines

1. **Fork the repository** and create a feature branch
2. **Follow naming conventions**: `feature/agent-name` or `fix/issue-description`
3. **Make focused changes**: One feature or fix per PR
4. **Write clear commit messages**: Follow conventional commit format
5. **Update documentation**: Include relevant documentation updates
6. **Add tests**: Ensure comprehensive test coverage
7. **Test thoroughly**: Verify all existing tests pass

### PR Description Template

```markdown
## Description
Brief description of changes and motivation

## Type of Change
- [ ] Bug fix
- [ ] New agent
- [ ] Enhancement to existing agent
- [ ] Documentation update
- [ ] Performance improvement
- [ ] Manufacturing domain feature

## Manufacturing Relevance
- [ ] General workflow improvement
- [ ] Manufacturing-specific feature
- [ ] Compliance-related enhancement
- [ ] Integration pattern

## Testing
- [ ] Unit tests added/updated
- [ ] Integration tests added/updated
- [ ] Manual testing completed
- [ ] Quality gates validated

## Context Awareness
- [ ] Agent reads existing project state
- [ ] Updates documentation incrementally
- [ ] Preserves existing work
- [ ] Follows iteration structure

## Checklist
- [ ] Code follows .NET coding standards
- [ ] Documentation is updated
- [ ] Tests are comprehensive
- [ ] Manufacturing context is considered
- [ ] Quality gates are met
```

### Review Process

1. **Automated Checks**: CI/CD pipeline validates basic requirements
2. **Peer Review**: Other contributors review the changes
3. **Maintainer Review**: Project maintainers provide final approval
4. **Testing**: Changes are tested in realistic scenarios
5. **Documentation**: Verify documentation is complete and accurate

### Merge Requirements

- ✅ All automated checks pass
- ✅ At least one peer review approval
- ✅ Maintainer approval
- ✅ No merge conflicts
- ✅ Documentation is updated
- ✅ Tests are comprehensive

## Community

### Getting Help

- **GitHub Discussions**: For questions and general discussion
- **GitHub Issues**: For bug reports and feature requests
- **Claude Code Documentation**: For Claude Code specific questions

### Recognition

Contributors are recognized through:

- **Contributor list** in README.md
- **Release notes** crediting significant contributions
- **Community spotlights** for exceptional contributions
- **Maintainer status** for long-term contributors

## Manufacturing Industry Focus

### Domain Expertise

We especially welcome contributors with expertise in:

- **Manufacturing Execution Systems (MES)**
- **Supervisory Control and Data Acquisition (SCADA)**
- **Enterprise Resource Planning (ERP) integration**
- **Quality Management Systems (QMS)**
- **Regulatory compliance** (FDA, HACCP, ISO)
- **Industrial IoT and data historian systems**
- **Production planning and scheduling**
- **Supply chain management**

### Compliance Considerations

When contributing manufacturing-related features, consider:

- **FDA 21 CFR Part 11** for electronic records and signatures
- **HACCP** requirements for food safety
- **ISO standards** for quality management
- **SOX compliance** for financial controls
- **GMP guidelines** for manufacturing practices

## Questions?

If you have questions about contributing, please:

1. Check existing documentation and issues
2. Search GitHub Discussions
3. Create a new discussion or issue
4. Contact maintainers directly if needed

Thank you for contributing to the Claude Sub-Agent Spec Workflow System! Together, we can create powerful tools for AI-assisted manufacturing software development.