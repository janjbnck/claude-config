---
paths:
  - "**/*.tsx"
  - "**/*.svelte"
  - "**/*.ts"
---

# TypeScript

- Strict typing, no `any`
- String literal unions instead of enums: `"sm" | "md"`, `"internal" | "external"`, `1 | 2 | 3 | 4 | 5 | 6`
- `as const` for fixed lists of keys
- `type` for data shapes, `interface Props` for component props
- `import type` for imports that are only types
- Use object property shorthand: `{ locale, namespace: "HomePage" }`
