---
name: supabase-data-explorer
description: Explore and analyze Supabase database with intelligent querying and data insights
allowed_tools:
  - Read
  - Write
  - Edit
  - Bash
---

# Supabase Data Explorer

Explore and analyze Supabase database: **$ARGUMENTS**

## Supported Arguments

- `--table <name>` - Analyze specific table
- `--query <sql>` - Execute read-only SQL query
- `--export <format>` - Export data (csv, json, xlsx)
- `--inspect` - Full database inspection
- `--stats` - Generate statistics

## Exploration Frameworks

### 1. Database Discovery
- Discover table structures
- Identify data patterns
- Map relationships
- Analyze data distribution

### 2. Intelligent Querying
- Read-only MCP access
- Query optimization suggestions
- Result pagination
- Query history tracking

### 3. Data Analysis
- Trend analysis
- Statistical summaries
- Anomaly detection
- Data quality assessment

### 4. Schema Inspection
- Examine relationships
- Review constraints
- Check indexes
- Validate foreign keys

### 5. Export & Visualization
- Multiple export formats
- Data sampling
- Filtered exports
- Report generation

### 6. Performance Analysis
- Query execution plans
- Slow query identification
- Optimization suggestions

## Safety Mechanisms

- [ ] Read-only operations only
- [ ] Query validation before execution
- [ ] Result limiting enabled
- [ ] Resource usage monitored

## Output

```markdown
# Data Exploration Report

## Table: users
- Total rows: 10,000
- Columns: 12
- Indexes: 3
- Foreign keys: 2

## Data Distribution
[Statistics and insights]

## Recommendations
[Optimization suggestions]
```
