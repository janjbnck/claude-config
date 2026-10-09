# Git

## Commits

- Conventional Commits without a scope: `type: description`
- Short description, either the name of the feature or an imperative: `feat: dark mode`, `feat: privacy policy content`, `fix: crop image`, `refactor: organize project structure`
- Subject line only, no body. Attribution trailers like `Co-Authored-By` are fine
- Small commits that each do one thing

## Branches and pull requests

- Never push to the default branch directly. Create a branch before committing and open a PR
- Branch names are kebab-case and describe the feature: `initialize-i18n`, `locale-based-routing`
- In collaborative repositories, branch names start with the user's GitHub username: `janjbnck/locale-based-routing`
- PR titles use the same format as commit messages: `feat: locale-based routing`
- PR descriptions are a short bullet list of the changes in lowercase, without periods
- Assign PRs to the user with `--assignee @me`
