Structured Query Language, ou Linguagem de Consulta Estruturada é a linguagem padrão para [[Banco de Dados Relacional]].
## Comandos DDL - Data Definition Language
- CREATE
- DROP
- ALTER
```SQL
CREATE TABLE users (
  id INTEGER PRIMARY KEY AUTOINCREMENT,
  name VARCHAR,
  email VARCHAR,
  password VARCHAR,
  avatar VARCHAR NULL,
  created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
  updated_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
)

ALTER TABLE clients RENAME TO users
ALTER TABLE users ADD status VARCHAR
ALTER TABLE users RENAME COLUMN status TO active
ALTER TABLE users DROP COLUMN active
```

## Comandos DML - Data Manipulation Language
- CREATE - INSERT
- READ - SELECT
- UPDATE - UPDATE
- DELETE - DELETE

```SQL
INSERT INTO users (name, email, password) VALUES ('Gabriel', 'gabirel@gmail.com', '123')
SELECT * FROM users
UPDATE users SET avatar = 'gabriel.png' WHERE id = 1
DELETE FROM users WHERE id = 1
```