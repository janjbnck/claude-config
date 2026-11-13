---
paths:
  - "**/*.tsx"
  - "**/*.jsx"
---

# Next.js

## Components

- Export one component per file and name the file after the component
- Keep a helper component that only one file uses unexported in that file
- Use server components by default. Add `"use client"` only when the component needs state, effects, event handlers or browser APIs. Hooks without state like `useTranslations` from next-intl work in server components
- Use existing shared components instead of raw elements when one fits

## Props

- Declare props as `type Props` directly above the component, not exported. For helper components in the same file, prefix it with their name: `type ItemProps`
- Feel free to type props inline in tiny helper components: `{ previousPage }: { previousPage?: string }`

## JSX

- Keep markup minimal and readable. No wrapper elements without a layout or semantic purpose, no redundant attributes
- Put a blank line between sibling elements, so each block reads on its own:

  ```tsx
  <header>
    <h1>...</h1>

    <nav aria-labelledby="social-media-profile-title">...</nav>
  </header>
  ```
