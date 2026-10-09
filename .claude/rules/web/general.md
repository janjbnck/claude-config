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

Follow the project's formatter config. Without one, use Prettier defaults.

## Imports and exports

Sort imports by the project's formatter config. Without one, use the Biome order:

1. URLs: `https://example.org`
2. Protocol sources: `node:path`, `bun:test`, `jsr:@my/lib`, `npm:lib`
3. Packages: `lib`, `@scope/lib`
4. Aliases starting with `@/`, `#`, `~`, `$` or `%`
5. Absolute and relative paths: `/abs`, `../parent`, `./sibling`

- Use the project's path alias (like `@/`) for imports from other folders: `@/components/ui/Heading`, `@/data/data`
- Use relative paths only inside the same folder: `./routing`, `./types`
- Default exports for components and config files
- Named exports for data, types and i18n helpers

## Naming

- camelCase for variables, functions and data arrays: `bannerLinks`, `previousPageUrl`, `lastUpdatedDate`
- Descriptive full words, no abbreviations except established ones like `Props`, `params`, `id`, `url` and `i18n`

## Website text

- Use Title Case for English headings, other languages keep their normal capitalization
- Write paragraphs in a natural style. Use plain words and leave out filler
- No em dashes or semicolons. Use commas, periods or parentheses instead
- No unusual characters like `…` or curly quotes unless the text needs them
- Write typographic characters as HTML entities in markup text: `&nbsp;`, `&ndash;`. In JS strings and JSON, use the character itself and write non-breaking spaces as `\u00a0`
