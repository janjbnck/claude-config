# General

## Approach

- Go with the most basic solution that fulfills the request. No abstractions or options that nobody asked for
- Handle common and plausible edge cases, skip far-fetched ones
- If something can be done in one line, do it in one line
- Skip anything that adds complexity for little benefit

## Formatting

Use project defaults, then Prettier defaults:

- 2-space indentation
- Double quotes
- Semicolons
- Trailing commas in multi-line literals and argument lists
- Lines wrap at about 80 characters
- Arrow function parameters always in parentheses: `(link) => ...`

## Imports and exports

- Order: external packages first (`next`, `next-intl`, `react`), then `@/` imports, then relative imports
- Use the `@/` alias for imports from other folders: `@/components/ui/Heading`, `@/data/data`
- Use relative paths only inside the same folder: `./routing`, `./types`
- Default exports for components, pages, layouts and config files
- Named exports for data, types and i18n helpers

## Naming

- PascalCase for components, component files and types: `PageHeader.tsx`, `ResumeItem`
- camelCase for variables, functions and data arrays: `bannerLinks`, `previousPageUrl`, `lastUpdatedDate`
- Descriptive full words, no abbreviations.
- kebab-case for DOM ids: `social-media-profile-title`

## Comments

Don't write comments. Code explains itself through names and small components. Leave existing boilerplate comments from library setup (like next-intl or ESLint config) as they are.
