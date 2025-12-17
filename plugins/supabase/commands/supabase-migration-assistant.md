---
name: supabase-migration-assistant
description: Comprehensive database migration management for Supabase projects
allowed_tools:
  - Read
  - Write
  - Edit
  - Bash
---

# Supabase Migration Assistant

Manage database migrations for Supabase: **$ARGUMENTS**

## Supported Arguments

- `--create` - Generate new migration files
- `--alter` - Modify existing schema
- `--seed` - Populate database with test data
- `--rollback` - Revert migrations safely

## Workflow

### Phase 1: Planning
- Analyze current schema state
- Identify required changes
- Plan migration sequence
- Consider dependencies

### Phase 2: Code Generation
- Generate SQL migration files
- Create up and down scripts
- Add appropriate comments
- Version migration files

### Phase 3: Validation Testing
- Run dry-run validation
- Test on local/staging environment
- Verify data integrity
- Check for breaking changes

### Phase 4: Supabase Integration
- Apply migrations via Supabase CLI
- Monitor execution progress
- Validate successful application

### Phase 5: Type Generation
- Auto-generate TypeScript types
- Update type definitions
- Sync with application code

### Phase 6: Rollback Strategy
- Create rollback procedures
- Test rollback execution
- Document recovery steps

## Safety Features

- [ ] Pre-migration backups created
- [ ] Dry-run validation passed
- [ ] Rollback tested
- [ ] Data integrity verified
- [ ] Performance impact assessed

## Output

```
migrations/
├── 20240101000000_create_users_table.sql
├── 20240101000001_add_user_roles.sql
└── 20240101000002_create_posts_table.sql
```
