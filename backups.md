Dump the schema of the database
```postgres
pg_dump --schema-only --no-owner --no-privileges -h localhost -U postgres -d school_journey_db -f school_journey_db_schema.sql
```
