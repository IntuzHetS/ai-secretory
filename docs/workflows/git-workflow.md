# Git Workflow Guidelines

## Branch Strategy

### Main Branches
- `master`: Production-ready code
- `development`: Integration branch for features

### Supporting Branches
- `feature/*`: New features
- `bugfix/*`: Bug fixes
- `hotfix/*`: Urgent production fixes
- `release/*`: Release preparation

## Workflow Patterns

### Feature Development
1. Create feature branch from development
```bash
git checkout development
git pull origin development
git checkout -b feature/your-feature
```

2. Make changes and commit
```bash
git add .
git commit -m "feat(scope): your changes"
```

3. Push changes
```bash
git push -u origin feature/your-feature
```

4. Create Pull Request to development

### Hotfix Process
1. Create hotfix branch from master
2. Fix the issue
3. Merge to both master and development
4. Create release tag

### Release Process
1. Create release branch
2. Prepare release
3. Merge to master and development
4. Tag the release

## Commit Conventions

We follow conventional commits:
```
<type>(<scope>): <description>

[optional body]

[optional footer]
```

Types:
- feat: New feature
- fix: Bug fix
- docs: Documentation
- style: Code style
- refactor: Code refactoring
- test: Testing
- chore: Maintenance 

## Documentation Updates
1. Make documentation changes
2. Commit with proper message format:
   ```bash
   git commit -m "docs(scope): your changes"
   ```
3. Push changes
4. Create Pull Request if needed

## Expert Interactions
Quick commands for expert interactions:
- `doc`: Trigger Documentation Manager
- `sec`: Trigger Security Expert
- `git`: Trigger Git Expert

## Daily Workflow
1. Morning checklist:
   - Check documentation updates
   - Review security logs
   - Sync documentation

2. Documentation helpers:
   - Auto-formatting
   - Link validation
   - TOC generation
   - Improvement suggestions 