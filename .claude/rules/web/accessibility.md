---
paths:
  - "**/*.tsx"
  - "**/*.jsx"
  - "**/*.svelte"
  - "**/*.html"
---

# Accessibility

## Headings and landmarks

- Give every `section` and `nav` a heading. If it shouldn't be visible, render it anyway with the `sr-only` class

## Hidden and decorative content

- Add `aria-hidden` to decorative elements: icons, blinking cursors, connector lines
- Give icon-only links an `sr-only` span with the label
- For animated or partial text, render the visible version with `aria-hidden` and the full text in an `sr-only` span

## Links

- Open external links in a new tab with `target="_blank" rel="noopener noreferrer"`
- End text links to external sites with an external link icon after the text, like `box-arrow-up-right` from Bootstrap Icons

## Other

- Use `<b>` for labels and visual highlighting, `<strong>` for important text
- Wrap dates in `<time>` with the ISO string in the `datetime` or `dateTime` attribute and the locale-formatted text inside
- Translate image `alt` texts if the project uses i18n
