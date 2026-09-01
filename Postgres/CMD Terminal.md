
### 📁 Connection & Session

|Command|Description|
|---|---|
|`\c dbname`|Connect to a new database|
|`\conninfo`|Show current connection info|
|`\q`|Quit `psql`|
|`\password`|Change your password|

---

### 📊 Database Info

| Command         | Description                                |
| --------------- | ------------------------------------------ |
| `\l` or `\list` | List all databases                         |
| `\dt`           | List all tables                            |
| `\d`            | Describe a table, view, sequence, or index |
| `\d tablename`  | Describe a specific table                  |
| `\dv`           | List all views                             |
| `\di`           | List all indexes                           |
| `\df`           | List all functions                         |
| `\dn`           | List schemas                               |
| `\db`           | List tablespaces                           |
| `\encoding`     | Show current client encoding               |

---

### 👤 User & Roles

|Command|Description|
|---|---|
|`\du` or `\dg`|List all roles/users|

---

### 📦 Schema/Object Management

|Command|Description|
|---|---|
|`\d+ tablename`|Describe table with more detail|
|`\x`|Toggle expanded display|

---

### 📂 File I/O

|Command|Description|
|---|---|
|`\i filename.sql`|Execute commands from a file|
|`\o filename`|Output results to a file|
|`\qecho text`|Write text to output|
|`\copy`|Use `COPY` from client side|

---

### ⚙️ Variables and Settings

|Command|Description|
|---|---|
|`\set`|Set a variable|
|`\unset`|Unset a variable|
|`\timing`|Toggle timing of SQL commands|
|`\prompt`|Prompt user for input|

---

### 🧪 Running SQL

|Command|Description|
|---|---|
|`;`|End SQL command|
|`SELECT * FROM table;`|Standard SQL query|
|`BEGIN;`, `COMMIT;`, `ROLLBACK;`|Transaction control|

---

### 📜 History & Help

|Command|Description|
|---|---|
|`\s`|Show command history|
|`\h` or `\help`|Help on SQL commands, e.g. `\h SELECT`|

---

### 📋 Examples

`\l                     -- List all databases \c mydb                -- Connect to "mydb" \dt                    -- List all tables \d users               -- Describe table "users" \du                    -- List all roles \q                     -- Quit`