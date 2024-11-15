## Math Master

| Expected file |
| ------------- |
| `math-master.sql` |

Apply advanced mathematical functions in SELECT statements.

### Instructions:

Using the `products` table, create a query showing:
1. `name`
2. Square root of `quantity` as `sqrt_quantity`
3. `price` rounded up to nearest integer as `ceiling_price`
4. `price` rounded down to nearest integer as `floor_price`
5. `rating` multiplied by 20 as `rating_percent`
6. `price` multiplied by `quantity` as `total_value`

### Expected Result:

| name      | sqrt_quantity | ceiling_price | floor_price | rating_percent | total_value |
|-----------|---------------|---------------|-------------|----------------|-------------|
| Product A | 5.48          | 25            | 24          | 90.0           | 749.70      |
| Product B | 4.24          | 33            | 32          | 96.0           | 585.00      |
[... rest of products ...]
