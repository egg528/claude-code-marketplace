---
name: supabase-type-generator
description: Generate comprehensive TypeScript types from Supabase schema with automatic synchronization
allowed_tools:
  - Read
  - Write
  - Edit
  - Bash
---

# Supabase Type Generator

Generate comprehensive TypeScript types from Supabase database schema: **$ARGUMENTS**

## Supported Arguments

- `--all-tables` - Generate types for all tables
- `--specific-table <name>` - Generate types for a specific table
- `--functions` - Include database function types
- `--enums` - Include enum types
- `--views` - Include view types

## Workflow

### Phase 1: Schema Analysis
- Extract database structure via Supabase MCP
- Map PostgreSQL data types to TypeScript equivalents
- Identify relationships and foreign keys

### Phase 2: Type Generation
- Create table interfaces with proper typing
- Generate utility types (Insert, Update, Row)
- Create type guards for runtime validation

### Phase 3: Integration Setup
- Configure import paths
- Set up build process integration
- Create barrel exports

### Phase 4: Validation
- Test type compatibility with existing code
- Verify application integration
- Check for type conflicts

### Phase 5: Synchronization
- Monitor schema changes
- Auto-regenerate types on changes
- Detect breaking changes and warn

### Phase 6: Developer Experience
- Provide IDE integration hints
- Generate usage documentation
- Create example snippets

## Output Structure

```typescript
// types/database.ts
export interface Database {
  public: {
    Tables: {
      [tableName]: {
        Row: { ... }
        Insert: { ... }
        Update: { ... }
      }
    }
    Views: { ... }
    Functions: { ... }
    Enums: { ... }
  }
}
```

## Quality Checks

- [ ] All tables have corresponding types
- [ ] Nullable fields properly marked
- [ ] Foreign key relationships typed
- [ ] Enums converted to union types
- [ ] No TypeScript compilation errors
