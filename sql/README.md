## О проекте

В этом репозитории собраны:
- Базовые SELECT, WHERE, ORDER BY, GROUP BY, агрегация.
- Проверки качества данных.
- Запросы с JOIN по нескольким таблицам (users, products, orders).


## Используемые инструменты
- MySQL Workbench


## Примеры запросов

### Базовый SELECT

```sql
-- Пользователи с фамилией "Иванов"
SELECT *
FROM users
WHERE last_name = 'Иванов';
```

### Проверка дубликатов email

```sql
SELECT
    email,
    COUNT(*) AS cnt
FROM users
WHERE email IS NOT NULL
GROUP BY email
HAVING COUNT(*) > 1;
```

### JOIN: полная информация по заказу

```sql
SELECT
    u.first_name,
    u.last_name,
    u.email,
    p.product_name,
    p.category,
    o.quantity,
    o.total_price,
    o.order_date
FROM orders o
JOIN users u ON o.user_id = u.user_id
JOIN products p ON o.product_id = p.product_id;
```