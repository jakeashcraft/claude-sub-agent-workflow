# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Claude Sub-Agent Spec Workflow System - A context-aware AI-driven development workflow system optimized for .NET 9 development. This system transforms project ideas into production-ready applications through specialized AI agents that understand existing project state and work in intelligent, coordinated phases with organized documentation structure.

## Project Documentation Conventions (Important)

**Structured Documentation Organization:** All documentation must be organized in the hierarchical `docs/` structure. This prevents document chaos and enables context-aware workflow management.

### Core Documentation Structure

```
docs/
├── project/                    # Core project docs (stable, rarely change)
│   ├── requirements.md         # Master requirements
│   ├── project-charter.md      # Project overview and goals  
│   ├── stakeholders.md         # Key stakeholders and contacts
│   └── success-criteria.md     # Definition of done
├── architecture/               # System design (update when structural changes needed)
│   ├── system-architecture.md  # Clean Architecture design
│   ├── api-specifications.md   # OpenAPI/Swagger specifications
│   ├── data-models.md          # Entity Framework Core models
│   ├── security-design.md      # Authentication & authorization
│   └── deployment-strategy.md  # Azure deployment configuration
├── iterations/                 # Version-controlled changes
│   ├── v1-initial-setup/       # Initial project creation
│   │   ├── iteration-overview.md
│   │   ├── implementation-plan.md
│   │   ├── validation-report.md
│   │   └── retrospective.md
│   ├── v2-auth-bugfix/         # Bug fix iteration
│   ├── v3-reporting-feature/   # New feature iteration
│   └── v4-performance-opts/    # Performance optimization iteration
├── current/                    # Active working state
│   ├── request-analysis.md     # Current request classification
│   ├── active-tasks.md         # Work in progress
│   ├── known-issues.md         # Identified problems
│   ├── next-priorities.md      # Upcoming work queue
│   └── recent-changes.md       # Change log
└── archive/                    # Completed/obsolete docs
    └── old-requirements-v1.md
```

### Documentation Rules

- **Never create documentation in project root** except README.md
- **Use iteration folders** for all new work to maintain version control
- **Update current/ folder** to track active state and recent changes
- **Read existing documentation** before creating new files to understand context
- **Append to change logs** rather than overwrite existing information
- **Archive obsolete documents** instead of deleting them

> **Critical:** The context-aware workflow depends on this organized structure. Scattered documentation breaks the intelligent agent selection system.

## Enhanced Development Commands

### Context-Aware Workflow Execution

```bash
# New Project (Full workflow)
/agent-workflow "Create a .NET 9 Web API for manufacturing inventory with Clean Architecture and Azure deployment"

# Bug Fix (Targeted workflow)  
/agent-workflow "The user authentication is failing after Azure AD B2C integration"

# Enhancement (Selective workflow)
/agent-workflow "Add real-time notifications using SignalR to the existing application"

# Refactoring (Optimization workflow)
/agent-workflow "Optimize Entity Framework queries and implement caching patterns"

# Database-Intensive Enhancement (Includes database-specialist)
/agent-workflow "Add Wonderware Historian integration for real-time batch tracking with FDA audit trail"

# Manual orchestration with context awareness
Use spec-orchestrator: Analyze existing project state and fix the login validation issue

# Phase-specific execution with context
Use spec-analyst: Update requirements for the new reporting feature based on existing project
Use spec-architect: Review and enhance existing architecture for performance improvements
Use database-specialist: Design manufacturing database patterns with historian integration and FDA compliance
Use spec-developer: Implement targeted bug fixes following existing code patterns
```

### Quality Gates and Testing (.NET 9 Enhanced)

```bash
# The system includes three automated quality gates optimized for .NET 9:
# Gate 1: Planning Quality (95% threshold) - Clean Architecture feasibility, EF Core models
# Gate 2: Development Quality (90% threshold) - Code quality, xUnit coverage, security
# Gate 3: Production Readiness (85% threshold) - Azure deployment, monitoring, documentation

# Manual validation with .NET focus
Use spec-validator: Evaluate .NET 9 code quality with Clean Architecture compliance scoring
Use spec-tester: Generate xUnit test suite with integration tests and proper mocking patterns
```

### Project Structure Operations (.NET 9)

```bash
# Initialize context-aware project structure
mkdir -p .claude/{agents,commands,docs/{project,architecture,iterations,current,archive}}
cp agents/*/*.md .claude/agents/
cp commands/agent-workflow.md .claude/commands/

# .NET 9 project structure (follows Clean Architecture)
src/
├── Domain/                           # Entities, Value Objects, Domain Services
├── Application/                      # Use Cases, DTOs, Application Services  
├── Infrastructure/                   # EF Core, External APIs, Azure services
├── Web/                              # ASP.NET Core Web API, Controllers
└── Shared/                           # Cross-cutting concerns, contracts

tests/
├── Domain.UnitTests/                 # xUnit domain logic tests
├── Application.IntegrationTests/     # Application service tests
├── Infrastructure.IntegrationTests/  # EF Core, external service tests  
└── Web.IntegrationTests/             # API integration tests with TestServer
```

## System Architecture

### Context-Aware Multi-Phase Workflow Design

The system follows an intelligent, context-aware approach that analyzes existing project state:

1. **Context Analysis Phase (5-10% of project time)**
   - spec-orchestrator: Project state analysis and request classification
   - Determines optimal agent chain based on request type
   - Creates appropriate iteration folder structure

2. **Targeted Agent Execution (60-80% of project time)**
   - **NEW_PROJECT**: Full chain (analyst → architect → developer → validator → tester)
   - **BUG_FIX**: Targeted chain (analyst analysis → developer fixes → validator regression)  
   - **ENHANCEMENT**: Selective chain (analyst updates → architect if needed → developer → validator → tester)
   - **REFACTOR**: Optimization chain (architect review → developer refactor → validator compliance)

3. **Quality Validation Phase (10-15% of project time)**
   - Context-aware validation based on change type
   - .NET 9 specific quality criteria
   - Azure deployment readiness assessment
   - Limited retries (max 2) to prevent token waste

### Agent Categories (.NET 9 Specialized)

**Context-Aware Workflow Agents**

- spec-orchestrator: .NET 9 workflow coordination with request classification
- spec-analyst: Requirements analysis with C# domain modeling expertise
- spec-architect: Clean Architecture design for .NET 9 with EF Core and Azure
- **database-specialist: Manufacturing database expertise (auto-included for database-intensive requests)**
- spec-developer: Modern C# 13 implementation with ASP.NET Core patterns
- spec-validator: .NET quality validation with security and performance focus
- spec-tester: xUnit testing with integration and mocking best practices

**Domain Specialists (.NET 9)**

- senior-frontend-architect: Razor Pages/MVC/Blazor Server/WebAssembly expert
- senior-backend-architect: .NET 9 backend systems and microservices
- ui-ux-master: Blazor component design and accessibility

### Quality Framework (.NET 9)

Each phase includes .NET-specific automated quality gates:

#### Planning Gate (95% threshold)
- Requirements completeness with C# domain modeling
- Clean Architecture feasibility assessment
- Entity Framework Core model validation
- Azure deployment strategy verification
- Security design compliance (Azure AD, Key Vault)

#### Development Gate (90% threshold)  
- C# code quality (Roslyn analyzers, StyleCop)
- xUnit test coverage (minimum 85%)
- Clean Architecture layer compliance
- Entity Framework performance patterns
- Security implementation validation

#### Production Gate (85% threshold)
- Overall .NET quality score
- Azure deployment readiness
- Application Insights monitoring configuration
- Operational documentation completeness
- Performance benchmark validation

### Agent Communication Protocol

Agents now communicate through context-aware structured artifacts:

- Each agent reads existing project state from organized documentation
- Agents update existing documents incrementally rather than recreate
- New work is organized into iteration-specific folders
- Orchestrator manages context sharing between agents
- Quality gates provide .NET-specific feedback for improvements

## Expected Output Structure (.NET 9 Clean Architecture)

```
project/
├── .claude/
│   ├── docs/                             # Organized documentation (replaces scattered docs)
│   │   ├── project/                      # Stable project documentation
│   │   ├── architecture/                 # System design documentation
│   │   ├── iterations/                   # Version-controlled changes
│   │   │   ├── v1-initial-setup/
│   │   │   ├── v2-auth-fixes/
│   │   │   └── v3-reporting-feature/
│   │   ├── current/                      # Active working state
│   │   └── archive/                      # Historical documentation
│   ├── agents/                           # Context-aware specialized agents
│   └── commands/                         # Enhanced workflow commands
├── src/                                  # .NET 9 Clean Architecture
│   ├── Domain/                           # Business entities and rules
│   │   ├── Entities/
│   │   ├── ValueObjects/
│   │   ├── DomainServices/
│   │   └── Interfaces/
│   ├── Application/                      # Use cases and application logic
│   │   ├── Commands/
│   │   ├── Queries/
│   │   ├── DTOs/
│   │   └── Services/
│   ├── Infrastructure/                   # External concerns
│   │   ├── Data/                         # EF Core DbContext
│   │   ├── Services/                     # External service implementations
│   │   └── Configuration/                # Dependency injection setup
│   ├── Web/                              # ASP.NET Core Web API
│   │   ├── Controllers/                  # API controllers
│   │   ├── Middleware/                   # Custom middleware
│   │   └── Configuration/                # Web-specific setup
│   └── Shared/                           # Cross-cutting concerns
├── tests/                                # xUnit test projects
│   ├── Domain.UnitTests/                 # Domain logic unit tests
│   ├── Application.IntegrationTests/     # Application service tests
│   ├── Infrastructure.IntegrationTests/  # Data access tests
│   └── Web.IntegrationTests/             # API integration tests
├── docker/                               # Container configuration
├── scripts/                              # Build and deployment scripts
├── global.json                           # .NET SDK version
├── Directory.Build.props                 # MSBuild properties
└── README.md                             # Project documentation
```

## Key Integration Points

### Enhanced Slash Command Integration

The `/agent-workflow` command provides context-aware execution:

```bash
# Automatic request classification
/agent-workflow "Fix the authentication bug" 
# → Automatically classified as BUG_FIX, uses targeted agent chain

# Force specific workflow type  
/agent-workflow "Add new feature" --force-type=ENHANCEMENT
# → Forces enhancement workflow even if classification is uncertain

# Quality threshold adjustment
/agent-workflow "Quick prototype" --quality=75
# → Lower quality threshold for rapid prototyping

# Agent chain override
/agent-workflow "Performance optimization" --agents=spec-architect,spec-developer,spec-validator
# → Uses only specified agents
```

### Enhanced Sub-Agent Chain Process

The system uses intelligent sub-agent chaining based on context:

```
First use the spec-orchestrator sub agent to analyze existing docs/ structure and classify request type, 
then based on classification: for NEW_PROJECT execute full chain (spec-analyst → spec-architect → [database-specialist if database-intensive] → spec-developer → spec-validator → spec-tester), for BUG_FIX execute targeted chain (spec-analyst analysis → [database-specialist if performance/query issues] → spec-developer fixes → spec-validator regression), for 
ENHANCEMENT execute selective chain (spec-analyst updates → spec-architect if needed → [database-specialist if database changes] → spec-developer → spec-validator → spec-tester), for REFACTOR execute optimization chain (spec-architect review → [database-specialist if database optimization] → spec-developer refactor → spec-validator compliance), with quality gates using .NET 9 specific criteria and maximum 2 retry iterations.
```

### Enhanced Quality Gate Mechanism

- **Context-Aware Validation**: Different criteria based on request type
- **Validation Score ≥90%**: Proceed to next phase (raised from 85%)
- **Validation Score <90%**: Targeted feedback with maximum 2 iterations
- **.NET 9 Specific Metrics**: Clean Architecture, EF Core, security, performance
- **Token Efficiency**: Avoid full workflow restarts through targeted improvements

## Best Practices

### For Context-Aware Development

- **Trust Request Classification**: Let the orchestrator analyze and classify your request
- **Leverage Existing Context**: Agents will read existing documentation automatically
- **Use Iteration Folders**: Each significant change gets its own versioned iteration
- **Maintain Current State**: Keep `current/` folder updated with active work and issues
- **Review Recent Changes**: Check `recent-changes.md` to understand project evolution

### For .NET 9 Development

- **Follow Clean Architecture**: Use established layer separation and dependency flow
- **Entity Framework Best Practices**: Optimize queries, use proper change tracking
- **Modern C# Features**: Leverage records, pattern matching, nullable reference types
- **Azure-First Design**: Plan for cloud deployment from initial architecture
- **Security by Design**: Implement proper authentication, authorization, input validation

### For Documentation Management

- **Stable vs Dynamic Content**: Core docs in `project/`, changes in `iterations/`
- **Version Control Changes**: Each iteration has complete context and rationale
- **Incremental Updates**: Agents append/update rather than recreate documents
- **Change Tracking**: Always document what changed, why, and impact
- **Archive Management**: Move obsolete documents to `archive/` folder

### For Token Optimization  

- **Precise Requests**: Be specific about what needs to change
- **Context Reuse**: Let agents read existing state instead of re-explaining
- **Targeted Changes**: Make focused improvements rather than full rewrites
- **Trust Agent Selection**: Allow orchestrator to choose minimal necessary agents

## Troubleshooting

### Context-Aware Issues

- **Wrong Classification**: Use `--force-type=` to override automatic classification
- **Missing Context**: Initialize with `/agent-workflow "Setup project structure" --force-type=NEW_PROJECT`
- **Document Chaos**: Migrate existing docs using structured organization
- **Agent Confusion**: Check that `docs/` structure exists and has current state

### .NET 9 Specific Issues

- **Clean Architecture Violations**: Review architecture compliance in validation reports
- **Entity Framework Performance**: Check query analysis and implement proper patterns
- **Azure Deployment Problems**: Validate deployment configuration and monitoring setup
- **Security Concerns**: Ensure proper authentication/authorization implementation

### Debug Mode

Enable comprehensive debugging for complex issues:

```bash
/agent-workflow "Debug workflow classification and agent selection" --debug=true --verbose=true
```

## Integration with External Systems

The enhanced system integrates with:

- **GitHub Actions**: Context-aware CI/CD validation based on change type
- **Azure DevOps**: .NET 9 build pipelines with quality gate integration
- **Visual Studio**: Roslyn analyzer integration for code quality
- **Entity Framework**: Migration and performance optimization
- **Azure Services**: App Service, Key Vault, Application Insights integration

## Manufacturing Facility Deployment Considerations

For manufacturing facility deployments across US operations:

- **Multi-Facility Architecture**: Centralized services with facility-specific configurations
- **Compliance Requirements**: FDA, HACCP, and other regulatory compliance
- **Integration Points**: MES systems, SCADA, ERP integration patterns
- **Security**: Industrial network security, role-based access by facility/function
- **Reliability**: High availability patterns for manufacturing environments

> Remember: The context-aware workflow system eliminates document chaos while dramatically reducing token usage through intelligent agent selection. Focus on describing what needs to change rather than re-explaining existing system context.

## Git Discipline - MANDATORY FOR ALL AGENTS

### Core Git Safety Rules

**CRITICAL**: Every agent MUST follow these git practices to prevent work loss and maintain project integrity:

1. **Auto-Commit Every 30 Minutes**
   ```bash
   # Set a timer/reminder to commit regularly
   git add -A
   git commit -m "Progress: [specific description of what was done]"
   
   # Include iteration context in commit messages
   git commit -m "Progress: [v3-feature-name] Implement SignalR hub for real-time updates"
   ```

2. **Commit Before Context Switches**
   - ALWAYS commit before switching between agents or request types
   - Never leave uncommitted changes when changing workflow phases
   - Tag working versions before major architectural changes
   - Commit after completing each agent's work in the chain

3. **Context-Aware Branch Strategy**
   ```bash
   # Branch naming aligned with iteration folders
   git checkout -b feature/v3-enhancement-signalr
   git checkout -b bugfix/v4-auth-issue
   git checkout -b refactor/v5-ef-optimization
   
   # After completing iteration work
   git add -A
   git commit -m "Complete: [iteration-id] [feature description]"
   git tag iteration-v3-complete-$(date +%Y%m%d-%H%M%S)
   ```

4. **Meaningful Commit Messages (Aligned with Request Types)**
   - **NEW_PROJECT**: "Initial: Set up Clean Architecture with .NET 9 foundation"
   - **BUG_FIX**: "Fix: Resolve null reference in UserService authentication"
   - **ENHANCEMENT**: "Feature: Add SignalR real-time notifications to dashboard"
   - **REFACTOR**: "Refactor: Optimize EF Core queries for 40% performance gain"
   - **WIP**: "WIP: [iteration-v3] Implementing batch processing logic"

5. **Documentation-Code Synchronization**
   ```bash
   # Always commit docs/ changes with related code changes
   git add docs/iterations/v3-feature/
   git add src/
   git commit -m "Feature: [v3] Complete SignalR implementation with documentation"
   ```

6. **Never Work >1 Hour Without Committing**
   - Set hourly reminders to commit work
   - Even incomplete features should be committed as "WIP: [description]"
   - This ensures work survives crashes, errors, or context switches

### Git Emergency Recovery

If something goes wrong:
```bash
# Check recent commits with context
git log --oneline -20 --graph --decorate

# View specific iteration work
git log --oneline --grep="v3-" 

# Recover from last stable state
git stash save "Emergency stash: $(date +%Y%m%d-%H%M%S)"  # Save with timestamp
git reset --hard HEAD  # Return to last commit

# Check all stashed changes
git stash list
git stash show -p stash@{0}  # Preview stash contents
git stash pop  # Restore most recent stash

# Recover from accidental deletions
git reflog  # View all recent actions
git checkout HEAD~1 -- docs/  # Restore docs from previous commit

# Find lost iteration work
git log --all --grep="iteration-v" --oneline

# Create recovery branch if needed
git checkout -b recovery/$(date +%Y%m%d-%H%M%S)
git cherry-pick [commit-hash]  # Selectively recover commits
```

### Integration with Context-Aware Workflow

**Git practices support the organized documentation structure:**
- Commits align with iteration folders (v1, v2, v3...)
- Branch names reflect request classification (feature/, bugfix/, refactor/)
- Tags mark completed iterations for easy rollback
- Documentation and code changes are always synchronized

**Quality Gate Checkpoints:**
- Commit before each quality gate validation
- Tag successful quality gate passes
- Branch protection for production-ready code

## Advanced Git Practices for .NET Manufacturing Systems

### Context-Aware Commit Discipline

Building on the core Git Discipline rules, these practices optimize commits for the context-aware workflow:

#### 1. **Iteration-Aligned Commit Strategy**
```bash
# Link commits to iteration work
git commit -m "Enhancement: [v3-signalr] Add real-time production alerts to dashboard"
git commit -m "Fix: [v4-auth] Resolve Azure AD B2C token validation"
git commit -m "Refactor: [v5-perf] Optimize EF Core queries for 40% improvement"

# Progress tracking within iterations
git commit -m "WIP: [v3-signalr] Configure SignalR hub infrastructure"
git commit -m "Progress: [v3-signalr] Implement client-side connection handling"
git commit -m "Complete: [v3-signalr] SignalR real-time notifications ready for testing"
```

#### 2. **.NET 9 Quality Gate Commits**
```bash
# Before each quality gate
git commit -m "Pre-Gate: [v3] Code complete, ready for development quality validation"
git tag "quality-gate-dev-v3-$(date +%Y%m%d-%H%M%S)"

# After quality improvements
git commit -m "Quality: [v3] Address EF Core performance feedback from validator"
git commit -m "Security: [v3] Implement authentication improvements per audit"
```

#### 3. **Manufacturing Domain-Specific Commits**
```bash
# Compliance and regulation focused
git commit -m "Compliance: Add FDA 21 CFR Part 11 audit trail to batch records"
git commit -m "Security: Implement role-based access for facility operations"
git commit -m "Integration: Add MES system data synchronization for production metrics"

# Manufacturing-specific features
git commit -m "Feature: [v2-quality] Add SPC control charts for process monitoring"
git commit -m "Fix: [v3-inventory] Resolve lot traceability chain breaks"
git commit -m "Enhancement: [v4-maintenance] Add predictive maintenance alerts"
```

#### 4. **Architecture-Aware Commit Patterns**
```bash
# Clean Architecture layer commits
git commit -m "Domain: Add production batch value objects and business rules"
git commit -m "Application: Implement CQRS pattern for inventory commands"
git commit -m "Infrastructure: Configure EF Core migrations for facility data"
git commit -m "Web: Add manufacturing dashboard API endpoints"

# Cross-layer changes
git commit -m "Architecture: [v3] Add event sourcing for audit trail requirements"
```

### Smart Commit Splitting Guidelines

For manufacturing systems, split commits based on:

1. **Regulatory Boundaries**: Separate FDA, HACCP, and ISO compliance changes
2. **Facility Concerns**: Multi-facility features vs single-facility fixes  
3. **System Integration**: MES, SCADA, ERP integration points
4. **Security Domains**: Authentication, authorization, data protection
5. **Architecture Layers**: Domain, Application, Infrastructure, Web layers

### Quality Assurance Integration

```bash
# Pre-commit validation aligned with quality gates
git add -A
dotnet build --no-restore  # Verify .NET 9 compilation
dotnet test --no-build     # Run xUnit test suite
dotnet format --verify-no-changes  # Code formatting check

# Only commit if all checks pass
git commit -m "Quality: [v3-feature] All quality gates passed, ready for validation"
```

### Documentation Synchronization

```bash
# Always sync documentation with code changes
git add docs/iterations/v3-signalr/
git add src/Web/Hubs/
git commit -m "Complete: [v3-signalr] SignalR implementation with full documentation"

# Update current state tracking
git add docs/current/recent-changes.md
git add docs/current/active-tasks.md
git commit -m "Update: Current project state after v3 completion"
```

This approach ensures commits support the context-aware workflow while maintaining manufacturing system integrity and compliance requirements.