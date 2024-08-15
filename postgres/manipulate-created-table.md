# Postgres queries

Add the column to the ready present table,

```postgres
ALTER TABLE me
ADD COLUMN role VARCHAR(50);
```

UPDATE me
SET role = 'friend'
WHERE role IS NULL;
: updating a column

Adding a constraint to the database like a check constraint

```postgres
ALTER TABLE me
ADD CONSTRAINT role_check
CHECK (role IN ('owner', 'admin', 'friend'));
```

When you alter the columns in postgres then don't forget to fix the sequence

```postgres
SELECT setval('users_user_id_seq', (SELECT MAX(user_id) FROM users) + 1);
```
