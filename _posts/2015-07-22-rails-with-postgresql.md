---
layout: post
title:  "Rails with PostgreSQL"
date:   2015-07-22 10:39
published: true
---

Ruby on Rails uses sqlite3 as default database. But sometimes you need to use other database such as PostgreSQL.

## Install PostgreSQL

### On Linux

First, update apt-get:

`sudo apt-get update`

Then install PostgreSQL and its development libraries:

`sudo apt-get install postgresql postgresql-contrib libpq-dev`

PostgreSQL is now installed but you should create a new database user, that your Rails application will use.

#### Create Database User

Create a PostgreSQL superuser user with this command

`sudo -u postgres createuser -s pguser`

If you want to set a password for the database user, enter the PostgreSQL console with this command:

`sudo -u postgres psql`

The PostgreSQL console is indicated by the postgres=# prompt. At the PostgreSQL prompt, enter this command to set the password for the database user that you created:

`postgres=# \password pguser`

Enter your desired password at the prompt, and confirm it.

Now you may exit the PostgreSQL console by entering this command:

`postgres=# \q`

#### Configure Database Connection

`vi config/database.yml`


Under the default section, find the line that says "pool: 5" and add the following lines under it.

`host: localhost`
`username: pguser`
`password: pguser_password`

Save and exit.

#### Create Application Databases

`rake db:create`

#### Run Server

`rails server` or `rails s`
