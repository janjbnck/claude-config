---
paths:
  - "src/data/**"
---

# Content data

- Structured content (links, lists, resume entries) lives in `src/data/data.ts` as named, camelCase `export const` arrays: `bannerLinks`, `footerLinks`, `resumeItems`
- Types for the content live in `src/data/types.ts` as `export type`, PascalCase and singular: `BannerLink`, `ResumeItem`
- Annotate arrays with their type: `export const bannerLinks: BannerLink[] = [...]`
- Every object has a `key` that serves as both the React key and the translation key
- Data holds what doesn't get translated: URLs, icon names, dates, discriminators. Visible text goes into the translations under the item's key
- Lists that only contain keys use `as const`:

  ```ts
  export const privacyRights = [
    "information",
    "deletion",
    "restriction",
  ] as const;
  ```

- Dates are ISO strings: `"2025-08"` for months, `"2026-08-27"` for days
- Discriminators are string literal unions (`type: "internal" | "external"`), optional fields use `?`
- One property per line, with trailing commas
