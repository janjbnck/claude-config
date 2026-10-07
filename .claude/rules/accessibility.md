---
paths:
  - "src/**/*.tsx"
---

# Accessibility

## Headings and landmarks

- Every `section` and `nav` has a heading. If it shouldn't be visible, render it anyway with `className="sr-only"`
- A `nav` points to its heading with `aria-labelledby`. Heading ids are kebab-case and end in `-title`. Inside lists, prefix them with the item key: `` `${item.key}-technologies-title` ``
- Heading levels follow the document outline: one `h1` per page, `h2` for sections, `h3` for items, `h4` below that. Change the look with styling, never by skipping levels

## Hidden and decorative content

- Decorative elements get `aria-hidden`: icons, blinking cursors, connector lines
- Icon-only links need a `<span className="sr-only">` with the translated label
- Animated or partial text renders the visible version with `aria-hidden` and the full text in an `sr-only` span

## Links

- External links open in a new tab with `target="_blank" rel="noopener noreferrer"`
- Text links to external sites end with an external link icon after the text, like `box-arrow-up-right` from Bootstrap Icons

## Other

- Dates are wrapped in `<time dateTime={isoString}>` with the locale-formatted text inside
- Image `alt` texts come from the translations
- `<html lang>` is set to the current locale
