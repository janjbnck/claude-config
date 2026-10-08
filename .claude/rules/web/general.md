---
paths:
  - "**/*.tsx"
  - "**/*.jsx"
  - "**/*.ts"
  - "**/*.js"
  - "**/*.svelte"
  - "**/*.html"
  - "**/*.css"
  - "**/*.json"
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

Sort imports by the project's formatter config. Without one, use the Biome order:

1. URLs: `https://example.org`
2. Protocol sources: `node:path`, `bun:test`, `jsr:@my/lib`, `npm:lib`
3. Packages: `lib`, `@scope/lib`
4. Aliases starting with `@/`, `#`, `~`, `$` or `%`
5. Absolute and relative paths: `/abs`, `../parent`, `./sibling`

- Use the project's path alias (like `@/`) for imports from other folders: `@/components/ui/Heading`, `@/data/data`
- Use relative paths only inside the same folder: `./routing`, `./types`
- Default exports for components, pages, layouts and config files
- Named exports for data, types and i18n helpers

## Naming

- PascalCase for components, component files and types: `PageHeader.tsx`, `ResumeItem`
- camelCase for variables, functions and data arrays: `bannerLinks`, `previousPageUrl`, `lastUpdatedDate`
- Descriptive full words, no abbreviations
- kebab-case for DOM ids: `social-media-profile-title`

## Website text

- Use Title Case for headings
- Write paragraphs in a natural style. Use plain words and leave out filler
- No em dashes or semicolons. Use commas, periods or parentheses instead
- No invisible Unicode characters like zero-width spaces and no unusual characters unless the text needs them. En dashes and non-breaking spaces are fine where they belong
