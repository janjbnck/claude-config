---
paths:
  - "**/*.tsx"
---

# Next.js

## Components

- One exported component per file, file name matches the component name
- Write components as `export default function Name({ ... }: Props)`. No arrow function components, no `React.FC`
- A helper component used by only one file stays unexported in that file
- Server components by default. Add `"use client"` as the first line, followed by a blank line, only when the component needs state, effects, event handlers or browser APIs. Hooks without state like `useTranslations` from next-intl work in server components
- A component that calls `useSearchParams` goes into its own small subcomponent wrapped in `<Suspense>` so the page can still render statically
- Use existing shared components instead of raw elements when one fits

## Props

- Declare props as `interface Props` directly above the component, not exported. Helper components in the same file prefix it with their name: `interface ItemProps`
- Tiny helper components can type props inline: `{ previousPage }: { previousPage?: string }`
- Polymorphic elements use a `Tag` variable: ``const Tag = `h${level}` as keyof JSX.IntrinsicElements;`` with `JSX` imported from `react/jsx-runtime`

## Pages

- Static images are imported and rendered with `next/image`
- Third-party scripts load with `next/script`

## JSX

- Keep markup minimal and readable. No wrapper elements without a layout or semantic purpose, no redundant attributes
- Put a blank line between sibling elements, so each block reads on its own:

  ```tsx
  <header>
    <h1>...</h1>

    <nav aria-labelledby="social-media-profile-title">...</nav>
  </header>
  ```

- Render lists inline with `.map((item) => <li key={item.key}>...)`. Keys come from a stable field in the data, not the array index
- When one item maps to several siblings, wrap them in `<React.Fragment key={...}>`
- Render optional parts with `value && (...)`. Compare numbers explicitly so `0` doesn't render: `items.length > 0 && (...)`
