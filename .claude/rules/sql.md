---
paths:
  - "**/*.sql"
---

# SQL

## Aliases

- Use the initials of each word in the table name as the table alias: `very_long_table_name vltn`, `order_items oi`, `customers c`
- Don't use single-letter aliases for multi-word tables or meaningless aliases like `a`, `b`, `t1`
- When two aliases would collide, add letters until they are unique: `orders ord`, `organizations org`
- In self-joins, give each table an alias that describes its role: `employees emp`, `employees mgr`
