# Claude Sub-Agent Workflow Examples

This directory contains practical examples demonstrating the Claude Sub-Agent Spec Workflow System in various scenarios. Each example shows how the context-aware workflow system adapts to different project types and manufacturing requirements.

## Example Categories

### 🏭 Manufacturing Industry Examples
- **[Manufacturing Inventory System](manufacturing-inventory-system/)** - Complete new .NET 9 project for multi-facility inventory management
- **[Quality Management System](quality-management-system/)** - FDA-compliant quality system with audit trails
- **[Production Monitoring Dashboard](production-monitoring/)** - Real-time manufacturing dashboard with historian integration

### 🐛 Bug Fix Examples
- **[Authentication Bug Fix](bugfix-authentication/)** - Targeted bug fix workflow for login issues
- **[Performance Issue Fix](bugfix-performance/)** - Database optimization bug fix with minimal changes

### ✨ Enhancement Examples
- **[SignalR Real-Time Notifications](enhancement-signalr/)** - Adding real-time features to existing application
- **[Reporting Module Addition](enhancement-reporting/)** - Adding comprehensive reporting to manufacturing system

### 🔧 Refactoring Examples
- **[Clean Architecture Migration](refactor-clean-architecture/)** - Migrating legacy code to Clean Architecture
- **[Entity Framework Optimization](refactor-ef-performance/)** - Database layer performance improvements

## How to Use These Examples

### 1. Study the Context
Each example includes:
- **Initial project state** (what exists before the workflow)
- **Request classification** (how the orchestrator categorizes the work)
- **Agent selection** (which agents are chosen and why)
- **Workflow execution** (step-by-step agent chain)
- **Final output** (what gets produced)

### 2. Follow the Workflow
```bash
# Navigate to any example
cd examples/manufacturing-inventory-system/

# Review the context
cat docs/current/project-state.md

# See the workflow request
cat workflow-request.md

# Study the agent execution
cat agent-execution-log.md

# Examine the results
ls -la docs/iterations/
```

### 3. Adapt for Your Project
- Copy the relevant example structure
- Modify the context for your specific needs
- Run the workflow with your requirements
- Compare results with the example

## Example Structure

Each example follows this consistent structure:

```
example-name/
├── README.md                    # Example overview and instructions
├── workflow-request.md          # The original user request
├── agent-execution-log.md       # Complete workflow execution log
├── .claude/                     # Claude Code configuration
│   ├── agents/                  # Agents used in this example
│   └── commands/                # Workflow commands
├── docs/                        # Organized documentation (before/after)
│   ├── project/                 # Core project documentation
│   ├── architecture/            # System design
│   ├── iterations/              # Version-controlled changes
│   │   └── v1-example-work/     # The work done in this example
│   └── current/                 # Active project state
├── src/                         # Source code (if applicable)
├── tests/                       # Test code (if applicable)
└── before-after-comparison.md   # What changed during the workflow
```

## Getting Started with Examples

### Prerequisites
- Claude Code with Sub-Agents support
- .NET 9 SDK (for .NET examples)
- Basic understanding of manufacturing software (for industry examples)

### Quick Start
1. **Choose an example** that matches your scenario
2. **Read the README** in the example directory
3. **Study the workflow execution** to understand the process
4. **Run the example** in your own project context
5. **Compare results** with the provided outputs

### Example Usage Patterns

#### For New Projects
```bash
# Study the manufacturing inventory example
cd examples/manufacturing-inventory-system/
/agent-workflow "$(cat workflow-request.md)"
```

#### For Bug Fixes
```bash
# Learn from the authentication bug fix
cd examples/bugfix-authentication/
/agent-workflow "$(cat workflow-request.md)"
```

#### For Enhancements
```bash
# See how SignalR is added to existing systems
cd examples/enhancement-signalr/
/agent-workflow "$(cat workflow-request.md)"
```

## Manufacturing Domain Examples

### Industry-Specific Scenarios
- **Food Processing**: HACCP compliance, allergen management
- **Pharmaceuticals**: FDA validation, batch genealogy
- **Automotive**: ISO/TS 16949, supplier quality
- **Chemical**: Process safety, environmental compliance

### System Integration Examples
- **MES Integration**: Production data synchronization
- **SCADA Connectivity**: Real-time process monitoring
- **ERP Integration**: Master data and transaction sync
- **Historian Access**: Time-series data visualization

### Compliance Examples
- **FDA 21 CFR Part 11**: Electronic records and signatures
- **HACCP Implementation**: Critical control point monitoring
- **ISO 22000**: Food safety management system
- **SOX Compliance**: Financial controls and audit trails

## .NET 9 Technical Examples

### Clean Architecture
- Domain-driven design patterns
- Dependency injection configuration
- Layer separation and communication
- CQRS and event sourcing

### Entity Framework Core
- Code-first migrations
- Performance optimization
- Complex query patterns
- Multi-tenant data models

### Azure Integration
- App Service deployment
- Application Insights monitoring
- Key Vault secrets management
- Multi-environment configuration

## Contributing New Examples

We welcome new examples that demonstrate:

### High-Value Scenarios
- Real manufacturing use cases
- Complex system integrations
- Compliance implementations
- Performance optimizations
- Multi-facility deployments

### Example Requirements
- **Complete Context**: Before/after project state
- **Realistic Scope**: Achievable in single workflow execution
- **Clear Documentation**: Easy to understand and follow
- **Practical Value**: Applicable to real-world scenarios
- **Quality Output**: Demonstrates best practices

### Submission Guidelines
1. Follow the standard example structure
2. Include comprehensive documentation
3. Provide clear workflow execution logs
4. Demonstrate context-aware behavior
5. Show token usage efficiency
6. Include manufacturing relevance (if applicable)

## Example Index

| Example | Type | Industry | Complexity | .NET 9 | Azure |
|---------|------|----------|------------|--------|-------|
| Manufacturing Inventory | NEW_PROJECT | Manufacturing | High | ✅ | ✅ |
| Authentication Bug Fix | BUG_FIX | General | Low | ✅ | ❌ |
| SignalR Enhancement | ENHANCEMENT | Manufacturing | Medium | ✅ | ✅ |
| Clean Architecture Refactor | REFACTOR | General | High | ✅ | ❌ |
| Quality Management System | NEW_PROJECT | Food/Pharma | High | ✅ | ✅ |
| Performance Bug Fix | BUG_FIX | General | Medium | ✅ | ❌ |

## Support

If you need help with any example:
1. Check the example's README.md first
2. Review the agent execution logs
3. Compare with similar examples
4. Create a GitHub discussion
5. Open an issue for bugs or improvements

---

**Next Steps**: Choose an example that matches your scenario and dive in! The examples are designed to be practical learning tools that you can adapt for your own manufacturing software development needs.