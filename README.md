https://blog.logrocket.com/crud-rest-api-node-js-express-postgresql/

mkdir pg-lesson-one
cd pg-lesson-one
createdb -U travis pg-lesson-two
npm init -y
npm install pg
touch index.js
psql -U travis pg-lesson-two

PostgreSQL command prompt
psql is the PostgreSQL interactive terminal. Running psql will connect you to a PostgreSQL host. Running psql --help will give you more information about the available options for connecting with psql:

-h: --host=HOSTNAME: The database server host or socket directory; the default is local socket
-p: --port=PORT: The database server port; the default is 5432
-U: --username=USERNAME: The database username; the default is your_username
-w: --no-password: Never prompt for password
-W: --password: Force password prompt, which should happen automatically


\q: Exit psql connection
\c: Connect to a new database
\dt: List all tables
\du: List all roles
\list: List databases




>>psql -U travis pg-lesson-two
>>CREATE TABLE users (ID SERIAL PRIMARY KEY, name VARCHAR(30), email VARCHAR(30));
>>INSERT INTO users (name, email) VALUES ('Jerry', 'jerry@example.com'), ('George', 'george@example.com'), ('Travis', 'joshua@example.com'), ('Debbie', 'debbie@example.com');
>>SELECT * FROM users;