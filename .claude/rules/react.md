---
paths:
  - "src/**/*.tsx"
---

# React components and pages

## Components

- One component per file, file name matches the component name
- Write components as `export default function Name({ ... }: Props)`. No arrow function components, no `React.FC`
- Generic building blocks go in `src/components/ui/`, page-level pieces in `src/components/layout/`
- A helper component used by only one file stays unexported in that file
- Server components by default. Add `"use client"` as the first line, followed by a blank line, only when the component needs hooks or browser APIs
- A component that calls `useSearchParams` goes into its own small subcomponent wrapped in `<Suspense>` so the page can still render statically
- When the same markup shows up in several places, extract it into a component in `src/components/ui/`
- Use existing shared components instead of raw elements when one fits

## Props

- Declare props as `interface Props` directly above the component, not exported
- Tiny helper components can type props inline: `{ previousPage }: { previousPage?: string }`
- Destructure props in the signature and set defaults there: `size = "md"`, `important = true`, `gapSize = "md"`
- `children: React.ReactNode` and `className?: string` are the standard props. Use `React.ReactNode` from the global namespace without importing React
- Variants are string literal unions (`size?: "xs" | "sm" | "md" | "lg"`), mapped to Tailwind classes with a `switch` inside an IIFE or a ternary into a `...Class` const
- Polymorphic elements use a `Tag` variable: `` const Tag = `h${level}` as keyof JSX.IntrinsicElements; `` with `JSX` imported from `react/jsx-runtime`

## Pages

- Every page exports `generateMetadata` that returns `title` and `description`. The title joins the page title and the site name with an en dash. The homepage leads with the site name, subpages lead with their own title
- Static images are imported from `@/assets/` and rendered with `next/image`
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

- Render lists inline with `.map((item) => <li key={item.key}>...)`. Keys come from the data's `key` field
- When one item maps to several siblings, wrap them in `<React.Fragment key={...}>`
- Render optional parts with `value && (...)`
- Use semantic elements: `main`, `header`, `footer`, `nav`, `section`, `article`, `time`, `ul`/`li`
- Use `<b>` for labels and `<strong>` for important text
- Use HTML entities for typographic characters in JSX text: `&nbsp;`, `&ndash;`
