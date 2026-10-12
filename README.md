# nodejs-todo-demo-app

A simple ToDo app in Node.js and Express.

## Database

The application uses MySQL. SQLite is not used.

Copy `.env.example` to `.env`, then replace the placeholder values with your
local MySQL values. The application loads `.env` automatically:

```text
MYSQL_HOST=localhost
MYSQL_USER=your_mysql_username
MYSQL_PASSWORD=your_mysql_password
MYSQL_DB=todo_db
```

The application creates the `todo_items` table automatically when it starts.
It does not create or delete the MySQL database itself.

## Run

Install dependencies and start the application:

```bash
npm install
npm start
```

Open <http://localhost:3000>.

For development with automatic restart:

```bash
npm run dev
```

## Run with Docker Compose

Make sure `.env` contains `MYSQL_PASSWORD` and `MYSQL_DB`, then run:

```bash
docker compose up --build
```

Open <http://localhost:3000>. Stop the services with `Ctrl+C`.
