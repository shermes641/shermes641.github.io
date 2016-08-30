---
layout: post
title:  "Heroku Server Setup"
date:   2016-08-30 11:09:34 -0600
categories: jekyll update
---
    # wget -qO- https://toolbelt.heroku.com/install-ubuntu.sh | sh
    https://devcenter.heroku.com/articles/getting-started-with-django#prerequisites

Download Heroku toolbelt:

    https://toolbelt.heroku.com/
This Wiki is a summed up and archived version mostly of this page:

    https://devcenter.heroku.com/articles/getting-started-with-django#prerequisites
Install toolbelt using:

    # wget -qO- https://toolbelt.heroku.com/install-ubuntu.sh | sh
Login to Heroku

    # heroku login
    ...
Create a django subdirectory, the root for all Django projects:

    # mkdir django
    # cd django
Create a virtual environment:

    # virtualenv env
Install all of the Heroku required stuff:

    # pip install django-toolbelt
Install required libraries for app

    # pip install django-mptt
    # pip install django-smart-selects
    # pip install django-bower
    # pip install django-nvd3
    # pip install django-extensions
    # pip install django-suit
    # pip install pytz
    # pip install dj_static
    # pip install dj_database_url
    # pip install South
    # pip install psycopg2
    # pip install parse
Test the application locally

    # foreman start
    => run web browser to make sure server is running
Generate the requirements.txt file that Heroku uses to know what the application is

    # pip freeze > requirements.txt
Update settings.py as mentioned in the Heroku "Getting Started with Django on Heroku"

    => This will fail when attempting to run database stuff on the local machine.
    => Change this line:
    =>    DATABASES['default'] =  dj_database_url.config()
    => To this:
    =>    DATABASES['default'] =  dj_database_url.config(default='postgres://postgres:asdf626X@127.0.0.1/testdb')
Similarly, update wsgi.py as mentioned in "GSwDoH"
Push local repository to Git origin

    # git commit -a
    # git add {whatever needs to be added}
    # git push origin master
Add SSH keys for Heroku:

    # heroku keys:add
Make sure local files for application are commited to Github, including requirements.txt
Push files to Heroku:

    # git push heroku master
Start the execution piece on Heroku and verify it is running

    # heroku ps:scale web=1
    # heroku ps
    ... prints status
Get the database setup on Heroku

    # heroku run python manage.py syncdb
    # heroku run python manage.py migrate
Now populate the initial data on the Heroku server... you must be in the project root directory!

    # heroku run python manage.py shell_plus
    ....
    (InteractiveConsole)
    >>> import fixtures.webui.fix as fix
    >>> fix.initSystems()
Attempt to run the server on Heroku:

    # heroku open
