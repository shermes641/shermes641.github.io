After changing the model, migrate the database:

###SMH ERROR: Unknown command: 'schemamigration'

    # python manage.py schemamigration webui --auto     # generate the migration files
    # python manage.py migrate                          # actually update the database tables
