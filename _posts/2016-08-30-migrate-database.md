---
layout: post
title:  "Migrate DB"
date:   2016-08-30 11:09:34 -0600
categories: jekyll update
---
After changing the model, migrate the database:

###SMH ERROR: Unknown command: 'schemamigration'

    # python manage.py schemamigration webui --auto     # generate the migration files
    # python manage.py migrate                          # actually update the database tables
