---
layout: post
title:  "Rails with PostgreSQL"
published: true
---

Ruby on Rails uses sqlite3 as default database. But sometimes you need to use other database such as PostgreSQL.

## Install PostgreSQL

### On Linux

First, update apt-get:

{% highlight bash %}
sudo apt-get update
{% endhighlight %}

Then install PostgreSQL and its development libraries:

`sudo apt-get install postgresql postgresql-contrib libpq-dev`

PostgreSQL is now installed but you should create a new database user, that your Rails application will use.

#### Create Database User

Create a PostgreSQL superuser user with this command

{% highlight bash %}
sudo -u postgres createuser -s pguser
{% endhighlight %}

If you want to set a password for the database user, enter the PostgreSQL console with this command:

{% highlight bash %}
sudo -u postgres psql
{% endhighlight %}

The PostgreSQL console is indicated by the postgres=# prompt. At the PostgreSQL prompt, enter this command to set the password for the database user that you created:

{% highlight bash %}
postgres=# \password pguser
{% endhighlight %}

Enter your desired password at the prompt, and confirm it.

Now you may exit the PostgreSQL console by entering this command:

{% highlight bash %}
postgres=# \q
{% endhighlight %}

#### Configure Database Connection

{% highlight bash %}
vi config/database.yml
{% endhighlight %}

Under the default section, find the line that says "pool: 5" and add the following lines under it.

{% highlight bash %}
host: localhost
username: pguser
password: pguser_password
{% endhighlight %}

Save and exit.

#### Create Application Databases

{% highlight bash %}
rake db:create
{% endhighlight %}

#### Run Server

{% highlight bash %}
rails server
{% endhighlight %}
