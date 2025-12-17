---
name: supabase-security-audit
description: Comprehensive Supabase security audit with RLS policy analysis and vulnerability assessment
allowed_tools:
  - Read
  - Write
  - Edit
  - Bash
---

# Supabase Security Audit

Perform comprehensive Supabase security audit: **$ARGUMENTS**

## Supported Arguments

- `--rls` - Focus on Row Level Security policies
- `--permissions` - Analyze permissions and access controls
- `--auth` - Review authentication configuration
- `--api-keys` - Check API key management
- `--full` - Complete security audit (default)

## Audit Areas

### 1. Row Level Security (RLS) Analysis
- Review all RLS policies for completeness
- Identify tables without RLS enabled
- Check for overly permissive policies
- Validate policy logic and conditions
- Test policy effectiveness with sample queries

### 2. Permission & Access Control
- Review role definitions and grants
- Check schema-level permissions
- Validate function security (SECURITY DEFINER vs INVOKER)
- Audit trigger permissions

### 3. Authentication Configuration
- Review auth settings and providers
- Check password policies
- Validate JWT configuration
- Review session management

### 4. API Key Management
- Check for exposed keys in codebase
- Review key rotation practices
- Validate key permissions scope
- Check for unused or stale keys

### 5. Data Protection
- Verify encryption at rest
- Check sensitive data handling
- Review backup encryption
- Validate data masking policies

### 6. Vulnerability Scanning
- SQL injection vectors
- Privilege escalation paths
- Data exposure risks
- Configuration weaknesses

## Compliance Checks

- [ ] GDPR data protection requirements
- [ ] SOC2 access control standards
- [ ] OWASP security guidelines

## Output Report

```markdown
# Security Audit Report

## Summary
- Critical: X issues
- High: X issues
- Medium: X issues
- Low: X issues

## Findings
[Detailed findings with remediation steps]

## Recommendations
[Prioritized action items]
```

## Quality Checklist

- [ ] All tables reviewed for RLS
- [ ] No overly permissive policies
- [ ] API keys properly scoped
- [ ] Auth configuration secure
- [ ] No exposed credentials
