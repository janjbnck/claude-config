---
paths:
  - "**/*.tsx"
  - "**/*.svelte"
  - "**/*.html"
  - "**/*.css"
  - "**/*.js"
  - "**/*.ts"
---

# General

## Formatting

Follow the project's formatter config. Without one, use Prettier defaults:

- 2-space indentation
- Double quotes
- Semicolons
- Trailing commas in multi-line literals and argument lists
- Lines wrap at about 80 characters
- Arrow function parameters always in parentheses: `(link) => ...`

## Imports and exports

- Order: follow the project's formatter config. Without one, use Biome defaults:

1. URLs (`https://example.org`)
2. Protocol sources (`node:path`, `bun:test`, `jsr:@my/lib`, `npm:lib`)
3. Packages (`lib`, `@scope/lib`)
4. Aliases starting with `@/`, `#`, `~`, `$` or `%`
5. Absolute and relative paths (`/abs`, `../parent`, `./sibling`)

- Use the project's path alias (like `@/`) for imports from other folders: `@/components/ui/Heading`, `@/data/data`
- Use relative paths only inside the same folder: `./routing`, `./types`
- Default exports for components, pages, layouts and config files
- Named exports for data, types and i18n helpers

## Naming

- PascalCase for components, component files and types: `PageHeader.tsx`, `ResumeItem`
- camelCase for variables, functions and data arrays: `bannerLinks`, `previousPageUrl`, `lastUpdatedDate`
- Descriptive full words, no abbreviations
- kebab-case for DOM ids: `social-media-profile-title`
