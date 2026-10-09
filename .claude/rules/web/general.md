---
paths:
  - "**/*.tsx"
  - "**/*.jsx"
  - "**/*.ts"
  - "**/*.js"
  - "**/*.mjs"
  - "**/*.svelte"
  - "**/*.html"
  - "**/*.css"
  - "**/*.json"
---

# General

## Formatting

Without a formatter config in the project, format like Prettier's defaults and sort imports like Biome.

## Imports and exports

- Use the project's path alias (like `@/`) for imports from other folders: `@/components/ui/Heading`, `@/data/data`
- Use relative paths only inside the same folder: `./routing`, `./types`
- Default exports for components

## Naming

- PascalCase for component files: `PageHeader.tsx`
- Descriptive full words, no abbreviations except established ones like `Props`, `params`, `id`, `url` and `i18n`

## Website text

- Use Title Case for English headings, other languages keep their normal capitalization
- Write paragraphs in a natural style. Use plain words and leave out filler
- No em dashes or semicolons. Use commas, periods or parentheses instead
- No unusual characters unless the text needs them. En dashes and non-breaking spaces are fine where they belong
- Write typographic characters as HTML entities in markup text: `&nbsp;`, `&ndash;`. In JS strings and JSON, use the character itself and write non-breaking spaces as `\u00a0`
