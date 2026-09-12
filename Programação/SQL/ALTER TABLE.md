
# Add Column 

```postgresql
ALTER TABLE ALUNOS
ADD COLUMN notas FLOAT;
```

# Drop Column

```postgresql
ALTER TABLE ALUNOS
DROP COLUMN notas;
```


# Alter Column

```postgreSQL
ALTER TABLE ALUNOS
ALTER COLUMN notas TYPE DECIMAL;
```

# Change Column Name

```postgreSQL
ALTER TABLE ALUNOS
RENAME COLUMN notas TO notes;
```

# Add Constraint 

```postgreSQL
ALTER TABLE ALUNOS
ADD CONSTRAINT not_null_idade_alunos NOT NULL idade;
```