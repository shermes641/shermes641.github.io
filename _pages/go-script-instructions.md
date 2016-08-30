go script is a task runner. It is currently setup to do things like starting and stopping python servers. The following is our initial list of tasks.

**Note: Be sure to set the virtualenv manually as these commands are not setting it.**

###SMH  ERROR:  Unknown command: 'runfcgi'

- `./go startprod` start prod server
- `./go stopprod` stop prod server
- `./go startstg` start staging server
- `./go stopstg` stop staging server
