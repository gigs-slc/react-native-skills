# AI_CONSTRAINTS.md

> This file defines NON-NEGOTIABLE rules that ALL AI agents MUST follow.
> Copy this template to your project's `docs/` folder and customize for your needs.

## Purpose

This file serves as the source of truth for AI agent behavior in your codebase. All agents (Orchestrator, Architect, Implementation, Review, etc.) must read and follow these constraints before taking any action.

---

## How to Use This Template

1. Copy this file to your project: `docs/AI_CONSTRAINTS.md`
2. Customize each section for your project's needs
3. Remove sections that don't apply
4. Add project-specific constraints
5. Reference this file in your CLAUDE.md or project instructions

---

## MANDATORY RULES (Non-Negotiable)

### File Size Limits
<!-- Customize these limits for your project -->
- **Component files**: Maximum 300 lines
- **Hook files**: Maximum 200 lines
- **Utility files**: Maximum 150 lines
- **Test files**: Maximum 500 lines

**Enforcement**: If a file exceeds limits, it MUST be split before adding more code.

### Required Patterns
<!-- Define patterns that must always be used -->

Example patterns (customize for your project):
```typescript
// All text must use your Text component, not React Native's
import { Text } from '@/components/ui/Text';  // REQUIRED
import { Text } from 'react-native';          // FORBIDDEN

// All API calls must use your API client
import { api } from '@/services/api';         // REQUIRED
fetch('https://...');                         // FORBIDDEN
```

### Forbidden Patterns
<!-- List patterns that must never be used -->

| Pattern | Reason | Alternative |
|---------|--------|-------------|
| `console.log` in production | Security/performance | Use logging service |
| Inline styles | Performance | Use StyleSheet.create |
| `any` type | Type safety | Define proper types |
| Direct state mutation | React rules | Use setState/dispatch |

---

## LOCKED FILES

These files are stable and should NOT be modified without explicit approval:

<!-- List your locked files -->
```
src/stores/           # State management is locked
src/services/api.ts   # API client is locked
src/navigation/       # Navigation structure is locked
```

**To modify locked files**: Request explicit approval from project lead first.

---

## STATE MANAGEMENT CONSTRAINTS

<!-- Define your state management rules -->

### Zustand Stores (if using Zustand)
- Only create new stores with approval
- Never duplicate state between stores
- Use selectors for derived state

### Context (if using Context)
- Keep context values minimal
- Memoize context values
- Split contexts by update frequency

---

## NAVIGATION CONSTRAINTS

<!-- Define navigation rules -->

- Use file-based routing (Expo Router)
- Never use navigation.navigate with string literals
- Always type-check route params
- Modals must use proper modal routes

---

## TESTING REQUIREMENTS

<!-- Define what must be tested -->

Before marking work complete:
- [ ] No TypeScript errors (`bun run build`)
- [ ] No lint errors (`bun run format`)
- [ ] E2E tests pass (if applicable)
- [ ] Manual testing on iOS and Android

---

## DEPENDENCY RULES

<!-- Control what can be added -->

### Approved Dependencies
Dependencies that can be freely used:
- expo-* (official Expo packages)
- react-native-reanimated
- zustand
- tanstack/react-query

### Restricted Dependencies
Require approval before adding:
- Any new animation library
- Any new state management
- Any native module

### Forbidden Dependencies
Never add these:
- moment.js (use date-fns)
- lodash (use native methods)

---

## CODE STYLE CONSTRAINTS

### Naming Conventions
- Components: PascalCase (`UserProfile.tsx`)
- Hooks: camelCase with `use` prefix (`useAuth.ts`)
- Utils: camelCase (`formatDate.ts`)
- Constants: SCREAMING_SNAKE_CASE

### File Organization
```
components/
  UserProfile/
    index.tsx          # Main component
    UserProfile.tsx    # Implementation
    types.ts           # Types only
    hooks.ts           # Component-specific hooks
```

---

## SECURITY CONSTRAINTS

- Never log sensitive data (tokens, passwords, PII)
- Never commit .env files
- Always validate external input
- Use HTTPS for all API calls

---

## PERFORMANCE CONSTRAINTS

- Lists must use FlashList or virtualization
- Images must use expo-image with proper sizing
- Animations must use Reanimated (worklet thread)
- No synchronous storage operations

---

## CUSTOM CONSTRAINTS

<!-- Add your project-specific constraints here -->

### Example: Brand Guidelines
- Primary color: #007AFF
- Font family: Inter
- Border radius: 8px standard, 16px cards

### Example: Feature Flags
- New features behind feature flags
- A/B tests must have tracking

---

## Constraint Violation Protocol

If an agent encounters a situation that would violate constraints:

1. **STOP** - Do not proceed with the violation
2. **DOCUMENT** - Note the constraint and why it blocks progress
3. **REPORT** - Inform the Orchestrator/user immediately
4. **WAIT** - Do not attempt workarounds without approval

---

## Version History

| Date | Change | Author |
|------|--------|--------|
| YYYY-MM-DD | Initial constraints | Your Name |

---

*This file is the source of truth. When in doubt, constraints win.*
