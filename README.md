# pg_dump_and_restore

## dumping and restoring. Mac

Step 1 - In the terminal, navigate to the folder where you want to dump the data.

## pg_dump 
To dump data:<br>
In the Terminal, navigate to where you want to dump the database, then enter:<br>
`/Library/PostgreSQL/15/bin/pg_dump -U postgres -p 5433 pet_info > petstuff.sql`

## psql restore
To restore data from a pg_dump, enter:<br>
`/Library/PostgreSQL/15/bin/psql -U postgres -p 5433 pet_info < petstuff.sql`

## Restoring from pgAdmin backup databse
IF ERROR: <br>
“The input is a PostgreSQL custom-format dump.<br>
Use the pg_restore command-line client to restore this dump to a database.”<br>
This database was backed up from pgAdmin, not from a pg_dump.<br>
To restore data that was backed up from pgAdmin (via the same ol’ terminal), enter:<br>
`/Library/PostgreSQL/15/bin/pg_restore -U postgres -p 5433 -d pet_info lugares.sql`
