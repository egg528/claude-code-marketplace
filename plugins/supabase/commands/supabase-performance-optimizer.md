---
name: supabase-performance-optimizer
description: Optimize Supabase database performance with intelligent analysis and recommendations
allowed_tools:
  - Read
  - Write
  - Edit
  - Bash
---

# Supabase Performance Optimizer

Optimize database performance: **$ARGUMENTS**

## Supported Arguments

- `--queries` - Analyze and optimize queries
- `--indexes` - Review and recommend indexes
- `--storage` - Optimize storage efficiency
- `--rls` - Streamline RLS policies
- `--functions` - Optimize database functions
- `--full` - Complete optimization analysis

## Optimization Areas

### 1. Query Optimization
- Analyze execution times
- Identify slow queries
- Suggest query rewrites
- Optimize JOIN operations

### 2. Index Management
- Recommend new indexes
- Identify unused indexes
- Remove redundant indexes
- Analyze index effectiveness

### 3. Storage Efficiency
- Data type optimization
- Archive old data
- Implement partitioning
- Compress large columns

### 4. RLS Policy Optimization
- Streamline policy logic
- Reduce policy overhead
- Combine redundant policies
- Cache policy results

### 5. Function Performance
- Optimize function execution
- Review execution plans
- Reduce function overhead
- Implement caching

## Analysis Sources

- Application SQL queries
- TypeScript/JavaScript files
- Current schema structure
- Recent execution patterns

## Output Report

```markdown
# Performance Optimization Report

## Summary
- Queries analyzed: 50
- Improvements found: 12
- Estimated performance gain: 40%

## Recommendations
1. [High] Add index on users.email
2. [Medium] Rewrite query in posts.ts:45
3. [Low] Archive old audit logs

## Implementation Plan
[Step-by-step optimization guide]
```

## Quality Checklist

- [ ] Slow queries identified
- [ ] Index recommendations reviewed
- [ ] RLS policies optimized
- [ ] Storage efficiency improved
