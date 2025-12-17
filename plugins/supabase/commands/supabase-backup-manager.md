---
name: supabase-backup-manager
description: Comprehensive database backup management for Supabase projects
allowed_tools:
  - Read
  - Write
  - Edit
  - Bash
---

# Supabase Backup Manager

Manage database backups for Supabase: **$ARGUMENTS**

## Supported Arguments

- `--create` - Generate database snapshot
- `--restore` - Recover from backup
- `--schedule` - Configure automated backups
- `--validate` - Verify backup integrity
- `--cleanup` - Remove obsolete backups

## Core Functions

### Backup Creation
- Generate database snapshots
- Export data in multiple formats
- Support incremental backups
- Compress and encrypt backups

### Data Restoration
- Recover from backups
- Point-in-time recovery
- Validate data integrity
- Selective table restoration

### Schedule Management
- Configure automated routines
- Set retention policies
- Define backup frequency
- Setup failure notifications

### Validation
- Verify backup integrity
- Test recovery procedures
- Check completeness
- Validate checksums

### Storage Management
- Compress archives
- Manage storage capacity
- Implement archival strategies
- Cross-region replication

## Disaster Recovery

- [ ] Recovery procedures documented
- [ ] Backup restoration tested
- [ ] RTO/RPO targets defined
- [ ] Failover process validated

## Output

```
backups/
├── daily/
│   └── backup_20240101_daily.sql.gz
├── weekly/
│   └── backup_20240101_weekly.sql.gz
└── monthly/
    └── backup_20240101_monthly.sql.gz
```
