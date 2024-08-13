ALTER TABLE me
ADD COLUMN role VARCHAR(50);
: adding a column to already table

UPDATE me
SET role = 'friend'
WHERE role IS NULL;
: updating a column

ALTER TABLE me
ADD CONSTRAINT role_check
CHECK (role IN ('owner', 'admin', 'friend'));
: adding a constraint like a check constraint


