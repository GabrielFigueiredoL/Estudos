## Criação de [[Banco de Dados]] pelo [[Node.js]]
```js
const sqlite3 = require("sqlite3")

const sqlite = require("sqlite")

const path = require("path")

async function sqliteConnection() {
  const database = await sqlite.open({
    filename: path.resolve(__dirname, "..", "database.db"),
    driver: sqlite3.Database
  })
  return database
}

module.exports = sqliteConnection
```

## Criação de Banco de Dados com [[Migrations]]

Utilizando o knex, após fazer as configurações iniciais:
```js
exports.up = knex => knex.schema.createTable("notes", table => {
  table.increments('id')
  table.text('title')
  table.text('description')
  table.integer('user_id').references('id').inTable("users"
  table.timestamp("created_at").default(knex.fn.now())
  table.timestamp("updated_at").default(knex.fn.now())
})

exports.down = knex => knex.schema.dropTable("notes")
```

