# 5. MinMax Explorer (Intermediate)

| Expected file |
| ------------- |
| `minmax-explorer.sql` |

Use the `MIN` and `MAX` functions along with subqueries to find extreme values and related product information.

## Instructions:

Using the `products` table, write a query to find:

- The lowest price among all products as `min_price`.
- The highest price among all products as `max_price`.
- The names of the product(s) with the lowest price as `min_price_products`.
- The names of the product(s) with the highest price as `max_price_products`.

**Note:** Ensure that the query handles cases where multiple products share the same minimum or maximum values by listing all relevant product names separated by commas.

## Resources:

- [SQLite MIN() and MAX() Functions](https://www.sqlite.org/lang_aggfunc.html#min)
- [SQLite Subqueries](https://www.sqlite.org/lang_select.html#subqueries)
- [SQLite GROUP_CONCAT Function](https://www.sqlite.org/lang_aggfunc.html#group_concat)
