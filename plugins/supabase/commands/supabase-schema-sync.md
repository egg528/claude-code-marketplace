---
name: supabase-schema-sync
description: Synchronize database schemas between local environments and Supabase
allowed_tools:
  - Read
  - Write
  - Edit
  - Bash
---

# Supabase Schema Sync

Synchronize database schemas: **$ARGUMENTS**

## Supported Arguments

- `--pull` - Pull schema from remote Supabase
- `--push` - Push local schema to remote
- `--diff` - Compare local and remote schemas
- `--validate` - Validate schema consistency

## Workflow

### Phase 1: Connection
- Connect to Supabase via MCP
- Authenticate with project credentials
- Verify connection status

### Phase 2: Comparison
- Fetch remote schema
- Load local schema files
- Generate diff report
- Identify conflicts

### Phase 3: Sync Execution
- Apply schema changes
- Handle conflicts
- Preserve data integrity
- Update local files

### Phase 4: Validation
- Verify schema consistency
- Check foreign key constraints
- Validate RLS policies
- Test data access

### Phase 5: Migration Generation
- Create migration scripts
- Version control changes
- Document modifications

### Phase 6: Safety Protocols
- Create backups before sync
- Verify permissions
- Test rollback procedures

## Safety Mechanisms

- [ ] Dry-run mode available
- [ ] Backup created before changes
- [ ] Rollback procedures tested
- [ ] Foreign key constraints validated
- [ ] Data integrity verified

## Output

```markdown
# Schema Sync Report

## Changes Detected
- Tables added: 2
- Columns modified: 5
- Indexes created: 3
- RLS policies updated: 4

## Conflicts
[List of conflicts requiring manual resolution]

## Migration Files Generated
- 20240101_sync_users_table.sql
- 20240101_sync_posts_table.sql
```

## Context Detection

Automatically identifies:
- Local schema files (*.sql)
- Configuration directories
- Database-related Git changes
- Migration history
