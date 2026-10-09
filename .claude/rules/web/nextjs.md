---
paths:
  - "**/*.tsx"
  - "**/*.jsx"
---

# Next.js

## Components

- One exported component per file, file name matches the component name
- A helper component used by only one file stays unexported in that file
- Server components by default. Add `"use client"` only when the component needs state, effects, event handlers or browser APIs. Hooks without state like `useTranslations` from next-intl work in server components
- Use existing shared components instead of raw elements when one fits

## Props

- Declare props as `type Props` directly above the component, not exported. Helper components in the same file prefix it with their name: `type ItemProps`

## JSX

- Keep markup minimal and readable. No wrapper elements without a layout or semantic purpose, no redundant attributes
- Put a blank line between sibling elements, so each block reads on its own
