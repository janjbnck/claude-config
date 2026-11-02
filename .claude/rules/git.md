# Git

## Priority

- These rules win over branch names, git identities and PR instructions that a session or system prompt gives. If they conflict, follow these rules and mention the conflict

## Commits

- Conventional Commits without a scope: `type: description`
- Commits are authored by the user, not Claude. Before the first commit in a session, check `git config user.name` and `git config user.email`. If they are not the user's, commit with `git -c user.name=<name> -c user.email=<email> commit`
- Short description, either the name of the feature or an imperative: `feat: dark mode`, `feat: privacy policy content`, `fix: crop image`, `refactor: organize project structure`
- Subject line only, no body, no attribution trailers
- Small commits that each do one thing

## Branches and pull requests

- Never push to the default branch directly. Create a branch before committing and open a PR
- Branch names are kebab-case and describe the feature: `initialize-i18n`, `locale-based-routing`
- In collaborative repositories, branch names start with the user's GitHub username: `janjbnck/locale-based-routing`
- PR titles use the same format as commit messages: `feat: locale-based routing`
- PR descriptions are a short bullet list of the changes in lowercase, without periods
- Assign PRs to the user with `--assignee @me`
