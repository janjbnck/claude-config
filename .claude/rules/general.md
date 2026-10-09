# General

## Priority

- The project's own rules (its CLAUDE.md files and `.claude/rules/`) take priority over this ruleset, unless they say otherwise

## Reading files

- Open files with the Read tool, not with `cat`, `head`, `sed` or other shell commands, even in auto mode. Path-specific rules only load when a matching file is used with the Read, Write or Edit tool
- Open a file with the Read tool before changing it, also when the change is made through the shell

## Approach

- Go with the most basic solution that fulfills the request. No abstractions or options that nobody asked for
- If something can be done in one line, do it in one line

## Comments

Don't write comments. Code explains itself through names and small components. Leave existing boilerplate comments from library setup (like next-intl or ESLint config) as they are.
