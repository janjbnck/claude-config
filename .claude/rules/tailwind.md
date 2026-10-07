---
paths:
  - "**/*.tsx"
  - "**/*.svelte"
  - "**/*.html"
  - "**/*.css"
---

# Tailwind

## General

- Tailwind utility classes directly in the class attribute. No CSS modules, no `clsx` or `cn`
- Keep class lists minimal. Only add classes that visibly change something
- Stick to default utilities and the default scale. Use arbitrary values like `w-[37px]` only when no default fits
- Style descendants from the container with arbitrary variants instead of repeating classes on every child: `[&_a]:underline`, `[&_b]:font-medium`, `[&_li]:pl-2`
- Use `size-*` when width and height are equal

## Responsive design

Desktop-first. Base classes target desktop, and `max-sm:` overrides them for small screens:

- `px-8 max-sm:px-6`, `py-32 max-sm:py-24`
- `gap-32 max-sm:gap-24`
- `text-4xl max-sm:text-3xl`
- `max-sm:flex-col-reverse`, `max-sm:text-center`, `max-sm:justify-center`
