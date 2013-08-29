heroku-django-template
======================

This repository provides a good starting point for a Django application running on Heroku with 
sessions via Redis (via Redis To Go) and caching from MemCachier.  The database is automatically 
set up and defaults to a _dev.db_ SQLite database when you're running things locally.  The Redis
sessions and memcache caching is also disabled automagically when you're doing things locally.


Running your app in debug
-------------------------

By default, the Heroku app will run in production mode so you won't see any of those pretty 
errors.  The same is true for running things locally (either via `foreman start` or `python 
manage.py runserver`).  To enable debug, either create a file called _.debug_ in the root or 
set your DEBUG environment variable to 1.  It's easy to just `touch .debug` locally and forget 
about it - it's already in _.gitignore_ so you don't have to worry about committing it.

To toggle debug on and off on Heroku, you can do the following:

*ON:* `heroku config:set DEBUG=1`

*OFF:* `heroku config:set DEBUG=0`



License
-------

This was written by Jonathan Enzinna.  Do whatever you want with this.  If you like it, I only (nicely) ask that you tell me you liked it.  You don't have to, I would appreciate it.  Other than that, do whatever you want with it.  A copy of the actual license is in the _LICENSE_ file.
