# Pull Request

## Description
Brief description of the changes and motivation for this PR.

## Type of Change
- [ ] Bug fix (non-breaking change that fixes an issue)
- [ ] New feature (non-breaking change that adds functionality)
- [ ] Breaking change (fix or feature that would cause existing functionality to not work as expected)
- [ ] Documentation update
- [ ] Performance improvement
- [ ] Refactoring (no functional changes)
- [ ] New agent development
- [ ] Agent enhancement
- [ ] Workflow system improvement

## Agent-Related Changes (if applicable)
- [ ] New agent added
- [ ] Existing agent enhanced
- [ ] Agent integration modified
- [ ] Workflow orchestration updated
- [ ] Context awareness improved
- [ ] Quality gate enhanced

### New/Modified Agents
List any agents that were created or modified:
- `agent-name.md` - [Description of changes]
- `another-agent.md` - [Description of changes]

## Manufacturing Domain (if applicable)
- [ ] General workflow improvement
- [ ] Manufacturing-specific feature
- [ ] Compliance enhancement (FDA, HACCP, ISO, etc.)
- [ ] System integration pattern (MES, SCADA, ERP)
- [ ] Multi-facility deployment feature
- [ ] Real-time data processing
- [ ] Audit trail and traceability

### Compliance Standards Addressed
- [ ] FDA 21 CFR Part 11
- [ ] HACCP
- [ ] ISO 22000/9001
- [ ] SOX Compliance
- [ ] GMP/cGMP
- [ ] Other: [specify]

## .NET 9 Enhancements (if applicable)
- [ ] Clean Architecture compliance
- [ ] Entity Framework Core optimization
- [ ] ASP.NET Core enhancement
- [ ] Azure integration improvement
- [ ] Security implementation
- [ ] Performance optimization
- [ ] Modern C# 13 features

## Context Awareness (if applicable)
- [ ] Improved project state analysis
- [ ] Enhanced document organization
- [ ] Better incremental updates
- [ ] Optimized agent selection
- [ ] Iteration management enhancement
- [ ] Token usage optimization

## Testing
- [ ] Unit tests added/updated
- [ ] Integration tests added/updated
- [ ] Agent workflow tests added/updated
- [ ] Manufacturing scenario tests added/updated
- [ ] Context awareness tests added/updated
- [ ] Quality gate validation tests added/updated
- [ ] Manual testing completed

### Test Coverage
- **New Code Coverage**: [X]%
- **Overall Project Coverage**: [X]%
- **Critical Path Coverage**: [X]%

## Documentation
- [ ] Code documentation updated (inline comments, XML docs)
- [ ] README.md updated
- [ ] CLAUDE.md updated
- [ ] Agent documentation created/updated
- [ ] Usage examples added
- [ ] Migration guide updated (if breaking changes)
- [ ] CHANGELOG.md updated

### Documentation Files Modified
- [ ] `README.md`
- [ ] `CLAUDE.md` 
- [ ] `agents/[agent-name].md`
- [ ] `examples/[example-name]/`
- [ ] `CHANGELOG.md`
- [ ] Other: [specify]

## Quality Assurance

### Code Quality
- [ ] Code follows established coding standards
- [ ] Code passes all linting rules
- [ ] Code follows Clean Architecture principles (if applicable)
- [ ] No hardcoded secrets or credentials
- [ ] Error handling is comprehensive
- [ ] Performance considerations addressed

### Agent Quality (if applicable)
- [ ] Agent follows established agent structure
- [ ] Agent includes context awareness features
- [ ] Agent provides clear input/output specifications
- [ ] Agent integrates properly with workflow
- [ ] Agent includes quality gate contributions
- [ ] Agent documentation is complete

### Manufacturing Quality (if applicable)
- [ ] Compliance requirements addressed
- [ ] Integration patterns follow industry standards
- [ ] Multi-facility considerations included
- [ ] Audit trail requirements met
- [ ] Real-time performance validated
- [ ] Security requirements satisfied

## Breaking Changes
If this introduces breaking changes, describe:

### What Breaks
- [Description of what will no longer work]

### Migration Path  
- [Steps users need to take to migrate]

### Deprecation Timeline
- [Timeline for deprecating old functionality]

## Performance Impact
- [ ] No performance impact
- [ ] Performance improved
- [ ] Performance impact analyzed and acceptable
- [ ] Performance benchmarks included

### Performance Details (if applicable)
- **Token Usage**: [Reduced by X% / Increased by X% / No change]
- **Agent Selection**: [Optimized / No change]
- **Quality Gate Speed**: [Improved by X% / No change]
- **Memory Usage**: [Improved / No change / Analyzed]

## Security Considerations
- [ ] No security implications
- [ ] Security review completed
- [ ] Security enhancements included
- [ ] Authentication/authorization addressed
- [ ] Input validation implemented
- [ ] Audit logging included

## Deployment Notes
Any special deployment considerations or requirements:

- [ ] No special deployment requirements
- [ ] Database migrations required
- [ ] Configuration changes required
- [ ] Environment variable updates needed
- [ ] Third-party service updates required
- [ ] Multi-facility deployment considerations

## Reviewer Guidelines

### For Maintainers
Please verify:
- [ ] All automated checks pass
- [ ] Code follows project standards
- [ ] Documentation is comprehensive
- [ ] Tests provide adequate coverage
- [ ] Breaking changes are properly handled
- [ ] Manufacturing domain requirements considered

### For Domain Experts
Please verify (if applicable):
- [ ] Manufacturing requirements properly addressed
- [ ] Compliance standards correctly implemented
- [ ] Integration patterns follow industry practices
- [ ] Multi-facility scenarios considered
- [ ] Real-time performance requirements met

### For Technical Reviewers
Please verify:
- [ ] .NET 9 best practices followed
- [ ] Clean Architecture principles maintained
- [ ] Security considerations addressed
- [ ] Performance implications assessed
- [ ] Error handling is robust

## Related Issues
Link related issues, discussions, or other PRs:

- Closes #[issue-number]
- Related to #[issue-number]
- Depends on #[pr-number]

## Screenshots (if applicable)
Add screenshots for UI changes or workflow demonstrations.

## Additional Context
Any additional information that reviewers should know:

---

## Pre-Submission Checklist
Before submitting this PR, confirm:

- [ ] Code compiles without errors
- [ ] All tests pass locally
- [ ] Documentation is updated and accurate
- [ ] Breaking changes are documented
- [ ] Performance impact is assessed
- [ ] Security implications are considered
- [ ] Manufacturing domain requirements are met (if applicable)

---

**Note for Reviewers**: This PR follows the [Contributing Guidelines](CONTRIBUTING.md). Please refer to those guidelines for detailed review criteria and standards.