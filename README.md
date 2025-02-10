# Laravel Migration Naming Conventions

This document outlines common naming conventions and **verb prefixes** used when creating migrations in Laravel using Artisan CLI. These conventions help to clearly describe the changes being made to the database schema and maintain consistency across the project.

## Common Prewords (Verb Prefixes) for Migrations

### 1. **add_**
- Used when adding something to the database (e.g., adding columns to a table).
- Example: `php artisan make:migration add_email_to_users_table`
- This means you're adding an `email` column to the `users` table.

### 2. **create_**
- Used when creating a new table.
- Example: `php artisan make:migration create_posts_table`
- This means you're creating a new `posts` table.

### 3. **rename_**
- Used when renaming something (e.g., a table or column).
- Example: `php artisan make:migration rename_users_to_customers_table`
- This means you're renaming the `users` table to `customers`.

### 4. **drop_**
- Used when removing something (e.g., a column or a table).
- Example: `php artisan make:migration drop_email_from_users_table`
- This means you're removing the `email` column from the `users` table.

### 5. **update_**
- Used when modifying an existing structure (e.g., changing column types).
- Example: `php artisan make:migration update_price_column_in_products_table`
- This means you're updating the `price` column in the `products` table.

### 6. **remove_**
- Used for dropping or removing a column or constraint.
- Example: `php artisan make:migration remove_old_column_from_users_table`
- This means you're removing a column from the `users` table.

### 7. **drop_if_exists_**
- Used when you want to drop a table or column only if it exists.
- Example: `php artisan make:migration drop_if_exists_old_table`
- This means you're dropping the `old_table` if it exists.

### 8. **alter_**
- Used when you are modifying an existing table or column but not necessarily dropping it.
- Example: `php artisan make:migration alter_users_table_add_status_column`
- This means you're altering the `users` table to add the `status` column.

### 9. **sync_**
- Often used for synchronizing a table or making mass changes.
- Example: `php artisan make:migration sync_users_and_orders`
- This could represent a migration for updating relationships or syncing data.

### 10. **truncate_**
- Used when truncating (emptying) a table.
- Example: `php artisan make:migration truncate_orders_table`
- This means you're truncating (removing all rows) from the `orders` table.

## Best Practices for Migration Naming

- **Be descriptive**: Name migrations clearly so that it’s easy to understand what they do without reading the code.
- **Follow conventions**: Stick to the common verb prefixes to maintain consistency across the project.
- **Use snake_case**: When naming migrations, use `snake_case` (lowercase letters and underscores) to separate words, as it’s the Laravel convention for file names.

## Examples of Migration Naming Conventions

1. **Creating a table**:
   - `php artisan make:migration create_users_table`
   - This means you're creating the `users` table.

2. **Adding a column**:
   - `php artisan make:migration add_is_active_to_users_table`
   - This means you're adding an `is_active` column to the `users` table.

3. **Renaming a column**:
   - `php artisan make:migration rename_name_to_full_name_in_users_table`
   - This means you're renaming the `name` column to `full_name` in the `users` table.

4. **Dropping a column**:
   - `php artisan make:migration drop_bio_from_users_table`
   - This means you're removing the `bio` column from the `users` table.

5. **Updating a column**:
   - `php artisan make:migration update_price_column_in_products_table`
   - This means you're updating the `price` column in the `products` table.

## Conclusion

By following these naming conventions for migrations, you can ensure clarity and maintain consistency across your project. These conventions help you and your team understand exactly what each migration is doing to the database schema and make it easier to collaborate on projects.

