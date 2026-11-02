---
paths:
  - "**/*.sql"
---

# SQL

## Aliases

- Table aliases are the initials of each word in the table name: `very_long_table_name vltn`, `order_items oi`, `customers c`
- No single-letter aliases for multi-word tables and no meaningless aliases like `a`, `b`, `t1`
- When two aliases would collide, add letters until they are unique: `orders ord`, `organizations org`
- Self-joins get an alias that describes the role: `employees emp`, `employees mgr`
