# Git

## Commits

- Conventional Commits without a scope: `type: description`
- Short description, either the name of the feature or an imperative: `feat: dark mode`, `feat: privacy policy content`, `fix: crop image`, `refactor: organize project structure`
- Subject line only, no body. Attribution trailers like `Co-Authored-By` are fine
- Small commits that each do one thing

## Branches and pull requests

- Never push to the default branch directly. Create a branch before committing and open a PR
- Branch names are kebab-case and describe the feature: `initialize-i18n`, `locale-based-routing`
- In collaborative repositories, branch names start with the user's GitHub username: `<username>/locale-based-routing`
- PR titles use the same format as commit messages: `feat: locale-based routing`
- PR descriptions start with `**TL;DR:**` and an easy to understand summary of at most two short sentences, followed by a short bullet list where each bullet describes one logical change, not every line that changed. Closing keywords like `Closes #12` are fine
- If a PR needs something that isn't clear from the code, like database changes, another PR merged first or special testing steps, put a fitting GitHub alert above the TL;DR
- Assign PRs to the user with `--assignee @me`
