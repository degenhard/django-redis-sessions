django-redis-sessions (with Django 1.3 & domain socket connection)
==================================================================
Redis database backend for your sessions


------------
Installation
------------

1. Run ``pip install git+git://github.com/degenhard/django-redis-sessions.git#egg=django-redis-sessions`` or alternatively  download the tarball and run ``python setup.py install``,

**For Django > 1.3 use origin package** (https://github.com/martinrusev/django-redis-sessions)

2. Set ``redis_sessions.session`` as your session engine, like so::

       SESSION_ENGINE = 'redis_sessions.session'

3. Optional settings::

       SESSION_REDIS_HOST = 'localhost'
       SESSION_REDIS_PORT = 6379
       SESSION_REDIS_DB = 0
       SESSION_REDIS_PASSWORD = 'password'
       SESSION_REDIS_PREFIX = 'session'

       If you prefer domain socket connection, you can just add this line instead of SESSION_REDIS_HOST and SESSION_REDIS_PORT.

       SESSION_REDIS_UNIX_DOMAIN_SOCKET_PATH = '/var/run/redis/redis.sock'

4. That's it
