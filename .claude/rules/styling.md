---
paths:
  - "src/**/*.tsx"
  - "src/**/*.css"
---

# Styling

## Tailwind

- Tailwind utility classes directly in `className`. No CSS modules, no `clsx` or `cn`
- Keep class lists minimal. Only add classes that visibly change something
- Stick to default utilities and the default scale. Use arbitrary values like `w-[37px]` only when no default fits
- Custom CSS only goes in `src/app/globals.css`: design tokens, `@theme inline`, keyframes and animation classes
- Combine classes with template literals. An optional `className` prop goes in as `${className ?? ""}`
- Conditional classes use a ternary with both branches: `${important ? "text-foreground-highlight" : "text-foreground"}`
- Split long class lists into named consts and join them in the template literal:

  ```tsx
  const baseClasses = "rounded-full border px-2 py-0.5 text-xs ...";
  const hoverClasses = "hover:bg-green-600/10 hover:border-green-700 ...";
  const darkModeClasses = "dark:border-green-500 dark:bg-green-500/10 ...";
  ```

- Style descendants from the container with arbitrary variants instead of repeating classes on every child: `[&_a]:underline`, `[&_b]:font-medium`, `[&_li]:pl-2`

## Colors and dark mode

- Use semantic color tokens like `background`, `foreground` and `border`, not raw palette colors
- Tokens are CSS variables on `:root`, overridden in `@media (prefers-color-scheme: dark)` and exposed through `@theme inline`. A new token gets added in all three places
- Dark mode follows the system and mostly comes from the tokens. Use `dark:` variants only where tokens can't help, like `dark:brightness-85 dark:shadow-none` on images

## Responsive design

Desktop-first. Base classes target desktop, and `max-sm:` overrides them for small screens:

- `px-8 max-sm:px-6`, `py-32 max-sm:py-24`
- `gap-32 max-sm:gap-24`
- `text-4xl max-sm:text-3xl`
- `max-sm:flex-col-reverse`, `max-sm:text-center`, `max-sm:justify-center`

## Layout and spacing

- Stack sections with `flex flex-col` and `gap-*` instead of margins
- Margins only for spacing around headings
- Use `size-*` when width and height are equal

## Recurring patterns

- Hover effects always get `transition-colors` (or `transition`)
- Decorative images and symbols: `select-none pointer-events-none`
