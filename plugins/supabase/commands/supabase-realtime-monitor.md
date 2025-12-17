---
name: supabase-realtime-monitor
description: Monitor and optimize Supabase realtime connections with comprehensive performance analysis
allowed_tools:
  - Read
  - Write
  - Edit
  - Bash
---

# Supabase Realtime Monitor

Monitor Supabase realtime connections: **$ARGUMENTS**

## Supported Arguments

- `--connections` - Track active connections
- `--subscriptions` - Monitor subscriptions
- `--performance` - Analyze throughput
- `--debug` - Enable debug mode
- `--analytics` - Generate usage reports

## Monitoring Areas

### 1. Connection Analysis
- Track active connections
- Monitor connection stability
- Analyze connection lifecycle
- Troubleshoot connection issues

### 2. Subscription Management
- Monitor active subscriptions
- Optimize subscription patterns
- Detect subscription leaks
- Analyze channel usage

### 3. Performance Optimization
- Analyze message throughput
- Reduce connection overhead
- Optimize broadcast patterns
- Monitor latency

### 4. Error Monitoring
- Track connection failures
- Monitor reconnection attempts
- Implement recovery strategies
- Alert on anomalies

### 5. Analytics Dashboard
- Generate usage reports
- Track trends over time
- Identify peak usage
- Capacity planning

### 6. Developer Tools
- Debug utilities
- Testing capabilities
- Log analysis
- Connection simulation

## Context Detection

Automatically identifies subscriptions by searching for:
- `subscribe` patterns
- `realtime` references
- `channel` definitions
- WebSocket connections

## Output Report

```markdown
# Realtime Monitor Report

## Active Connections
- Total: 150
- Stable: 145
- Reconnecting: 5

## Subscriptions
- Channels: 12
- Listeners: 45

## Performance
- Avg latency: 50ms
- Messages/sec: 1000
- Errors: 0.1%

## Recommendations
[Optimization suggestions]
```

## Quality Checklist

- [ ] Connection stability verified
- [ ] No subscription leaks
- [ ] Latency within targets
- [ ] Error rate acceptable
