- setup python (2.X) and postgres (9.5.X?)
- clone Server-Python git repo
- pip install -r ./requirements.txt
- pip install git+git://github.com/arskom/spyne.git
- create 'testdb' database
- pg_dump ph -U poweruser -W -h ph.cpaipntc9bpw.us-west-2.rds.amazonaws.com > ph.sql

###SMH the command above 'pg_dump: [archiver (db)] connection to database "ph" failed: could not connect to server: Connection refused
' using the PW from prod_settings.py

- psql -U postgres -d testdb < ph.sql
