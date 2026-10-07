# Git

## Commits

- Conventional Commits without a scope: `type: description`
- Types:
  - `feat` for new or changed functionality
  - `fix` for corrections
  - `refactor` for restructuring without behavior changes
  - `perf` for performance improvements
  - `style` for formatting without behavior changes
  - `test` for adding or changing tests
  - `docs` for documentation
  - `build` for dependencies and build configuration
  - `ci` for CI configuration
  - `chore` for maintenance that fits no other type, like the Claude rules
  - `revert` for reverting an earlier commit
- Description in lowercase and short, without a trailing period. Either the name of the feature or an imperative: `feat: dark mode`, `feat: privacy policy content`, `fix: crop image`, `refactor: organize project structure`
- Subject line only, no body
- Small commits that each do one thing

## Branches and pull requests

- Branch names are kebab-case and describe the feature: `initialize-i18n`, `locale-based-routing`
- For collaborative repositories branch names start with the user's GitHub username: `janjbnck/locale-based-routing`
- PR titles use the same format as commit messages: `feat: locale-based routing`
- PR descriptions are a short bullet list of the changes in lowercase, without periods. Planned follow-ups go in parentheses:

  ```md
  - configure next-intl with static locale for now (will be changed in a follow-up PR)
  - add first i18n strings
  - show strings on home page
  ```
