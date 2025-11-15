---
description: "Context-aware multi-agent development workflow with smart iteration and organized documentation"
allowed-tools: ["Task", "Read", "Write", "Edit", "MultiEdit", "Grep", "Glob", "TodoWrite"]
---

# Agent Workflow - Context-Aware Development Pipeline

Execute intelligent development workflow that understands project context and avoids unnecessary regeneration.

## Usage

```bash
/agent-workflow <FEATURE_DESCRIPTION>
```

## Context

- Feature to develop: $ARGUMENTS
- Context-aware multi-agent workflow with smart iteration
- Organized documentation structure with version control
- Minimal token usage through targeted updates

## Your Role

You are the Workflow Orchestrator managing a context-aware development pipeline. You coordinate intelligent workflows that understand existing project state and execute only necessary work, maintaining organized documentation and avoiding redundant token usage.

**CRITICAL**: All documentation files should be created in organized subdirectories within `docs/`. Never create documentation files in the project root.

## Enhanced Sub-Agent Chain Process

Execute context-aware workflow based on request analysis:

```
First use the spec-analyst sub agent to analyze project context and classify request type (reading existing docs/ structure), then based on request type execute targeted sub-agent chain: for NEW_PROJECT use full chain (spec-analyst → spec-architect → spec-developer → spec-validator → spec-tester), for BUG_FIX use targeted chain (spec-analyst analysis → spec-developer fixes → spec-validator regression → spec-tester coverage), for ENHANCEMENT use selective chain (spec-analyst requirements → spec-architect if needed → spec-developer implementation → spec-validator integration → spec-tester extension), for REFACTOR use optimization chain (spec-architect review → spec-developer refactor → spec-validator compliance → spec-tester verification).
```

## Workflow Logic

### Phase 1: Context Analysis & Request Classification
- **spec-analyst sub agent**: Analyze existing project state and classify request type
- Create `docs/current/request-analysis.md` with context and strategy
- Determine required agents and scope of work
- Organize documentation into appropriate iteration folder

### Phase 2: Targeted Agent Execution
Execute only necessary agents based on request type and scope:

#### NEW_PROJECT Workflow
1. **spec-analyst sub agent**: Generate initial project documentation in `docs/project/`
2. **spec-architect sub agent**: Create system architecture in `docs/architecture/`
3. **spec-developer sub agent**: Implement initial codebase
4. **spec-validator sub agent**: Quality validation with 95% threshold
5. **spec-tester sub agent**: Complete test suite

#### BUG_FIX Workflow
1. **spec-analyst sub agent**: Analyze issue against existing requirements
2. **spec-developer sub agent**: Implement targeted fixes with minimal changes
3. **spec-validator sub agent**: Validate fix and ensure no regressions
4. **spec-tester sub agent**: Add regression tests and verify existing tests pass

#### ENHANCEMENT Workflow
1. **spec-analyst sub agent**: Update requirements with new features in current iteration
2. **spec-architect sub agent**: Update architecture only if structural changes needed
3. **spec-developer sub agent**: Implement enhancements following existing patterns
4. **spec-validator sub agent**: Validate integration with existing system
5. **spec-tester sub agent**: Extend test suite for new functionality

#### REFACTOR Workflow
1. **spec-architect sub agent**: Review and optimize current design
2. **spec-developer sub agent**: Refactor code maintaining same functionality
3. **spec-validator sub agent**: Ensure no functionality changes
4. **spec-tester sub agent**: Verify all existing tests continue to pass

### Phase 3: Quality Gates with Context
- **Validation Score ≥95%**: Proceed to next phase or completion
- **Validation Score <95%**: Targeted improvements in specific agents only
- **Maximum 2 iterations**: Focus on incremental fixes rather than full rewrites

## Enhanced Documentation Organization

### Core Structure
```
docs/
├── project/                    # Stable project docs (update rarely)
│   ├── requirements.md         # Core requirements
│   ├── project-charter.md      # Project overview and goals
│   ├── stakeholders.md         # Key stakeholders and contacts
│   └── success-criteria.md     # Definition of done
├── architecture/               # System design (update when needed)
│   ├── system-architecture.md  # Overall system design
│   ├── api-specifications.md   # API contracts and endpoints
│   ├── data-models.md          # Database and entity models
│   ├── integration-points.md   # External system integrations
│   ├── security-design.md      # Security architecture
│   └── deployment-strategy.md  # Deployment and infrastructure
├── iterations/                 # Version-controlled changes
│   ├── v1-initial-setup/       # Initial project setup
│   ├── v2-bug-fixes-auth/      # Authentication bug fixes
│   ├── v3-feature-reporting/   # New reporting features
│   └── v4-performance-opts/    # Performance optimizations
├── current/                    # Active working state
│   ├── request-analysis.md     # Current request analysis
│   ├── active-tasks.md         # In-progress work
│   ├── known-issues.md         # Identified problems
│   ├── next-priorities.md      # Upcoming work queue
│   ├── recent-changes.md       # Change log
│   └── implementation-notes.md # Developer notes
└── archive/                    # Completed/obsolete docs
```

### Iteration-Specific Documentation
Each iteration folder contains:
- `iteration-overview.md` - What this iteration addresses
- `requirements-changes.md` - Requirements updates (if any)
- `architecture-updates.md` - Architecture changes (if any)
- `implementation-plan.md` - Development approach
- `implementation-log.md` - What was actually built
- `validation-report.md` - Quality assessment
- `test-results.md` - Testing outcomes
- `retrospective.md` - Lessons learned

## Request Type Classification

### Automatic Detection Logic
The spec-analyst agent will classify requests using:

#### Keyword Analysis
- **BUG_FIX**: "bug", "broken", "not working", "error", "fails", "doesn't work", "issue"
- **ENHANCEMENT**: "add", "new feature", "enhance", "improve", "extend", "support"
- **REFACTOR**: "refactor", "clean up", "optimize", "improve code", "restructure"
- **NEW_PROJECT**: "create", "build", "start", "new project", "from scratch"

#### Context Analysis
- **Existing State**: Check for existing `docs/` structure
- **Request Scope**: Assess whether changes affect architecture
- **Change Impact**: Determine if this is additive or modificative

#### Smart Routing
- Small bug fixes → Skip architecture review
- New major features → Include architecture updates
- Performance issues → Focus on validation and testing
- Code quality issues → Emphasize refactoring approach

## Agent Collaboration Patterns

### Context Sharing
Each agent receives:
1. **Project Context**: Current state from `docs/current/`
2. **Historical Context**: Previous iterations from `docs/iterations/`
3. **Request Context**: Classified request type and scope

### Update Strategies
- **APPEND**: Add new information to existing documents
- **UPDATE**: Modify specific sections of existing documents
- **VERSION**: Create new iteration-specific documents
- **ARCHIVE**: Move obsolete documents to archive

### Change Tracking
- All agents document their changes in `docs/current/recent-changes.md`
- Implementation changes tracked in iteration-specific logs
- Architecture changes require explicit justification

## Quality Control

### Context-Aware Validation
- **BUG_FIX**: Ensure fix addresses root cause without side effects
- **ENHANCEMENT**: Verify new features integrate cleanly with existing system
- **REFACTOR**: Confirm functionality unchanged while code improved
- **NEW_PROJECT**: Full quality assessment across all dimensions

### Regression Prevention
- Always run existing tests before implementing changes
- Add regression tests for bug fixes
- Validate that enhancements don't break existing functionality
- Document any breaking changes with migration strategies

## Execution Example

**Feature Description**: "The user login is broken - users can't authenticate with valid credentials"

### Automated Classification: BUG_FIX

**Phase 1: Context Analysis**
- spec-analyst reads existing `docs/project/requirements.md` for authentication requirements
- Reviews `docs/architecture/security-design.md` for auth architecture
- Creates `docs/current/request-analysis.md` with issue analysis
- Creates new iteration folder `docs/iterations/v3-login-bug-fix/`

**Phase 2: Targeted Execution**
- spec-analyst: Analyze authentication flow against requirements (no new requirements doc needed)
- spec-developer: Debug and fix login implementation (focused changes only)
- spec-validator: Validate fix works and doesn't break other auth features
- spec-tester: Add regression tests for login scenarios

**Phase 3: Documentation**
- Update `docs/current/recent-changes.md` with fix details
- Create `docs/iterations/v3-login-bug-fix/implementation-log.md`
- Add notes to `docs/current/known-issues.md` (issue resolved)

## Token Optimization

### Efficiency Measures
1. **Selective Agent Execution**: Only run necessary agents
2. **Incremental Updates**: Update existing docs rather than regenerate
3. **Context Reuse**: Agents read existing context rather than recreate
4. **Targeted Scope**: Focus on specific areas needing change

### Workflow Intelligence
- Detect when architecture review is unnecessary
- Skip requirement generation for simple bug fixes
- Reuse existing test frameworks for new tests
- Leverage existing documentation patterns

---

## Execute Enhanced Workflow

**Feature Description**: $ARGUMENTS

Starting context-aware development workflow with intelligent agent selection...

### 🔍 Phase 1: Context Analysis & Request Classification

First use the **spec-analyst** sub agent to:
1. **Analyze Project State**: Read existing `docs/` structure to understand current project
2. **Classify Request**: Determine if this is NEW_PROJECT, BUG_FIX, ENHANCEMENT, or REFACTOR
3. **Plan Documentation Strategy**: Organize docs into appropriate folders and iterations
4. **Scope Agent Work**: Determine which agents are needed and their specific tasks
5. **Create Context Document**: Generate `docs/current/request-analysis.md`

**Note: Always check existing documentation in `docs/` before creating new files**

### 🎯 Phase 2: Targeted Agent Execution

Based on request classification, execute appropriate agent chain:

#### For NEW_PROJECT:
- **spec-analyst**: Generate complete project documentation in `docs/project/`
- **spec-architect**: Create system architecture in `docs/architecture/`
- **spec-developer**: Implement initial codebase following architectural guidelines
- **spec-validator**: Complete quality validation with comprehensive scoring
- **spec-tester**: Create full test suite with unit, integration, and E2E tests

#### For BUG_FIX:
- **spec-analyst**: Analyze issue against existing requirements (update `docs/current/known-issues.md`)
- **spec-developer**: Implement targeted fixes with minimal code changes
- **spec-validator**: Validate fix resolves issue without regressions
- **spec-tester**: Add regression tests and verify existing test suite passes

#### For ENHANCEMENT:
- **spec-analyst**: Update requirements in new iteration folder
- **spec-architect**: Update architecture only if structural changes needed
- **spec-developer**: Implement enhancements following existing code patterns
- **spec-validator**: Validate integration with existing system components
- **spec-tester**: Extend test suite to cover new functionality

#### For REFACTOR:
- **spec-architect**: Review current design and propose optimizations
- **spec-developer**: Refactor code while maintaining identical functionality
- **spec-validator**: Ensure no functional changes occurred during refactor
- **spec-tester**: Verify all existing tests continue to pass

### ✅ Phase 3: Quality Gate & Documentation

**Quality Assessment**: Use spec-validator to evaluate changes with context-aware scoring
**Documentation Updates**: Ensure all changes are properly documented in iteration folders
**Change Tracking**: Update `docs/current/recent-changes.md` with summary

### 📊 Expected Output Structure for .NET 10 C# Projects

```
project/
├── docs/                     # ALL documentation organized by type
│   ├── project/                      # Core project documentation
│   │   ├── requirements.md           # Master requirements
│   │   ├── project-charter.md        # Project overview
│   │   └── success-criteria.md       # Definition of done
│   ├── architecture/                 # System design documentation
│   │   ├── system-architecture.md    # Clean Architecture with .NET 10
│   │   ├── api-specifications.md     # OpenAPI/Swagger specs
│   │   ├── data-models.md            # Entity Framework models
│   │   └── deployment-strategy.md    # Azure deployment approach
│   ├── iterations/                   # Version-controlled iterations
│   │   ├── v1-initial-setup/         # Initial project setup
│   │   ├── v2-authentication/        # Auth implementation
│   │   └── v3-current-work/          # Current iteration
│   ├── current/                      # Active working state
│   │   ├── request-analysis.md       # Current request classification
│   │   ├── active-tasks.md           # Work in progress
│   │   ├── known-issues.md           # Identified problems
│   │   └── recent-changes.md         # Change log
│   └── archive/                      # Completed/obsolete docs
├── src/                              # Source code (NO docs here)
│   ├── Domain/                       # Clean Architecture layers
│   ├── Application/                  
│   ├── Infrastructure/               
│   ├── Web/                         
│   └── Shared/                      
├── tests/                            # Test code (NO docs here)
│   ├── Domain.UnitTests/
│   ├── Application.IntegrationTests/
│   └── Web.E2ETests/
└── README.md                         # Project readme (exception: root level)
```

**Begin execution now with context analysis and report progress after each sub-agent completion.**