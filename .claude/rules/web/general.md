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
- Use default exports for components

## Naming

- Name component files in PascalCase: `PageHeader.tsx`
- Use descriptive full words and no abbreviations except established ones like `Props`, `params`, `id`, `url` and `i18n`

## Website text

- Use Title Case for English headings and keep the normal capitalization of other languages
- Write paragraphs in a natural style. Use plain words and leave out filler
- Don't use em dashes or semicolons. Use commas, periods or parentheses instead
- Don't use unusual characters unless the text needs them. Use en dashes and non-breaking spaces where they belong
- Write typographic characters as HTML entities in markup text: `&nbsp;`, `&ndash;`. In JS strings and JSON, use the character itself and write non-breaking spaces as `\u00a0`
