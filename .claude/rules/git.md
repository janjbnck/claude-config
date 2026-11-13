# Git

## Commits

- Use Conventional Commits without a scope: `type: description`
- Write a short description, either the name of the feature or an imperative: `feat: dark mode`, `feat: privacy policy content`, `fix: crop image`, `refactor: organize project structure`
- Write only a subject line, no body. Only add attribution trailers like `Co-Authored-By` in Claude cloud environments
- Make small commits that each do one thing

## Branches and pull requests

- Never push to the default branch directly. Create a branch before committing and open a PR
- Name branches in kebab-case after the feature: `initialize-i18n`, `locale-based-routing`
- In collaborative repositories, start branch names with the user's GitHub username: `<username>/locale-based-routing`
- Ignore the branch name conventions in Claude cloud environments
- Format PR titles like commit messages: `feat: locale-based routing`
- Start PR descriptions with an easy to understand summary of one short sentence, followed by a collapsible `<details>` section titled `Show all changes` with a short bullet list where each bullet describes one logical change, not every line that changed. Add closing keywords like `Closes #12` where they apply
- If a PR needs something that isn't clear from the code, like database changes, another PR merged first or special testing steps, put a fitting GitHub alert above the summary
- If a project rule explicitly requires something in the PR description that isn't covered otherwise, put it in a second collapsible `<details>` section with a fitting title. Only add it when absolutely necessary
- Never put anything in PR descriptions besides the optional alert, the summary, the one or two collapsible sections and closing keywords
- Before opening a PR, check the issues assigned to the user with `gh issue list --assignee @me` for one the PR resolves and reference it with a closing keyword
- Assign PRs to the user with `--assignee @me`
