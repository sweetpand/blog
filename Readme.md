Blog
====

Blog is a simple blog web application.

## Required Software

* _Node.js (7.10.0)_
* _MySQL (5.7.18)_

## Usage

Create an `.env` file with secrets and parameters for all the components.

```bash
# Database
BLOG_DATABASE_HOST=the location of the database server (localhost by default)
BLOG_DATABASE_PORT=the database port (3306 by default)
BLOG_DATABASE_DIALECT=the dialect of the database management engine (mysql by default)
BLOG_DATABASE_NAME=the name of the database (blog by default)
BLOG_DATABASE_USER=the user of the database with write permissions (blog_user by default)
BLOG_DATABASE_PASSWORD=his pasword (empty by default)

# Server
BLOG_SERVER_PORT=the port to use by the server (8080 by default)

# Session
BLOG_SESSION_SECRET=session secret to use with cookies

# bcrypt
BLOG_BCRYPT_SALT_LENGTH=length of the random salt (8 by default)

# Default Users
BLOG_ADMIN_PASSWORD=administrator password
BLOG_USER_PASSWORD=test user password
```

Create the database and the database user with the password specified in the
previous step in `.env` file (you can use MySQL Workbench, other management
tools, or issue SQL queries manually from the `mysql` command).

Install dependencies, ensure the database system is running, and start the
server.

```bash
npm install # to install dependencies
npm start   # to start the server
```

You can also use a local testing database stored in the `development` directory.

Ensure that MySQL was installed, and the `mysqld` binary is in the `PATH`
environment variable.

```bash
cd development
./bootstrap # create the database, install dependencies; run it only once
./start     # start MySQL with the local database and the blog server
```

## Credits

Toksaitov Dmitrii Alexandrovich (<dmitrii@toksaitov.com>)

