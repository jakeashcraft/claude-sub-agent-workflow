---
name: Bug Report
about: Create a report to help us improve the workflow system
title: '[BUG] '
labels: ['bug', 'triage']
assignees: ''
---

## Bug Description
A clear and concise description of what the bug is.

## Environment
- **Claude Code Version**: [e.g., latest, v1.2.3]
- **Operating System**: [e.g., Windows 11, macOS Monterey, Ubuntu 22.04]
- **Project Type**: [e.g., NEW_PROJECT, BUG_FIX, ENHANCEMENT, REFACTOR]
- **.NET Version**: [e.g., .NET 9.0, .NET 8.0, N/A]
- **Agent Used**: [e.g., spec-orchestrator, spec-developer, database-specialist]

## Steps to Reproduce
1. Go to '...'
2. Run command '...'
3. Use agent '...'
4. See error

## Expected Behavior
A clear and concise description of what you expected to happen.

## Actual Behavior
A clear and concise description of what actually happened.

## Agent Workflow Context
- **Request Classification**: [e.g., correctly identified as BUG_FIX, misclassified as ENHANCEMENT]
- **Agent Chain**: [e.g., orchestrator → analyst → developer, full chain executed unnecessarily]
- **Documentation State**: [e.g., existing docs/ structure, no previous context]
- **Quality Gate Results**: [e.g., passed 85%, failed at development gate]

## Error Messages/Logs
```
Paste any error messages or relevant log output here
```

## Screenshots
If applicable, add screenshots to help explain your problem.

## Manufacturing Context (if applicable)
- **Industry Domain**: [e.g., food processing, pharmaceuticals, automotive]
- **Compliance Requirements**: [e.g., FDA 21 CFR Part 11, HACCP, ISO 22000]
- **Integration Systems**: [e.g., MES, SCADA, ERP systems]
- **Multi-Facility**: [e.g., single facility, multi-facility deployment]

## Project Structure
```
your-project/
├── .claude/
│   ├── agents/
│   └── docs/
├── docs/
│   ├── project/
│   ├── architecture/
│   ├── iterations/
│   └── current/
└── [relevant files]
```

## Context Awareness Issues (if applicable)
- [ ] Agent didn't read existing documentation
- [ ] Agent regenerated existing content unnecessarily
- [ ] Agent didn't follow iteration structure
- [ ] Agent missed existing project state
- [ ] Wrong request classification by orchestrator

## Workaround
If you found a workaround, please describe it here.

## Additional Context
Add any other context about the problem here.

## Impact Assessment
- **Severity**: [Critical/High/Medium/Low]
- **Frequency**: [Always/Often/Sometimes/Rare]
- **Workaround Available**: [Yes/No]
- **Blocks Development**: [Yes/No]

## Suggested Solution (optional)
If you have ideas on how to fix this issue, please describe them here.

---

**For Maintainers:**
- [ ] Bug reproduced
- [ ] Root cause identified
- [ ] Fix implemented
- [ ] Test cases added
- [ ] Documentation updated