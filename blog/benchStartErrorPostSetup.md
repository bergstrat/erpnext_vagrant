`ty-32:/vagrant/frappe-bench$ bench setup redis-async-broker`

`vagrant@vagrant-ubuntu-trusty-32:/vagrant/frappe-bench$ bench setup redis-cache`

`vagrant@vagrant-ubuntu-trusty-32:/vagrant/frappe-bench$ bench start`

`02:03:36 system               | watch.1 started (pid=12264)`

`02:03:36 system               | redis_celery.1 started (pid=12263)`

`02:03:36 redis_celery.1       | [12271] 16 Mar 02:03:36.656 # Warning: no config file specified, using the default config. In order to specify a config file use redis-server /path/to/redis.conf`

`02:03:36 redis_celery.1       | [12271] 16 Mar 02:03:36.657 # Unable to set the max number of files limit to 10032 (Operation not permitted), setting the max clients configuration to 3984.`

`02:03:36 redis_celery.1       | [12271] 16 Mar 02:03:36.657 # Warning: 32 bit instance detected but no memory limit set. Setting 3 GB maxmemory limit with 'noeviction' policy now.`

`02:03:36 redis_celery.1       |                 _._`

`02:03:36 redis_celery.1       |            _.-``__ ''-._`

`02:03:36 redis_celery.1       |       _.-``    `.  `_.  ''-._           Redis 2.8.4 (00000000/0) 32 bit`

`02:03:36 redis_celery.1       |   .-`` .-```.  ```\/    _.,_ ''-._`

`02:03:36 redis_celery.1       |  (    '      ,       .-`  | `,    )     Running in stand alone mode`

`02:03:36 redis_celery.1       |  |`-._`-...-` __...-.``-._|'` _.-'|`     Port: 6379`

`02:03:36 redis_celery.1       |  |    `-._   `._    /     _.-'    |     PID: 12271`

`02:03:36 redis_celery.1       |   `-._    `-._  `-./  _.-'    _.-'`

`02:03:36 redis_celery.1       |  |`-._`-._    `-.__.-'    _.-'_.-'|`

`02:03:36 redis_celery.1       |  |    `-._`-._        _.-'_.-'    |           http://redis.io`

`02:03:36 redis_celery.1       |   `-._    `-._`-.__.-'_.-'    _.-'`

`02:03:36 redis_celery.1       |  |`-._`-._    `-.__.-'    _.-'_.-'|`

`02:03:36 redis_celery.1       |  |    `-._`-._        _.-'_.-'    |`

`02:03:36 redis_celery.1       |   `-._    `-._`-.__.-'_.-'    _.-'`

`02:03:36 redis_celery.1       |       `-._    `-.__.-'    _.-'`

`02:03:36 redis_celery.1       |           `-._        _.-'`

`02:03:36 redis_celery.1       |               `-.__.-'`

`02:03:36 redis_celery.1       |`

`02:03:36 redis_celery.1       | [12271] 16 Mar 02:03:36.658 # Server started, Redis version 2.8.4`

`02:03:36 redis_celery.1       | [12271] 16 Mar 02:03:36.658 # WARNING overcommit_memory is set to 0! Background save may fail under low memory condition. To fix this issue add 'vm.overcommit_memory = 1' to /etc/sysctl.conf and then reboot or run the command 'sysctl vm.overcommit_memory=1' for this to take effect.`

`02:03:36 redis_celery.1       | [12271] 16 Mar 02:03:36.671 * DB loaded from disk: 0.014 seconds`

`02:03:36 redis_celery.1       | [12271] 16 Mar 02:03:36.671 * The server is now ready to accept connections on port 6379`

`02:03:36 system               | web.1 started (pid=12265)`

`02:03:36 system               | workerbeat.1 started (pid=12266)`

`02:03:36 system               | redis_async_broker.1 started (pid=12275)`

`02:03:36 redis_async_broker.1 | [12287] 16 Mar 02:03:36.701 # Unable to set the max number of files limit to 10032 (Operation not permitted), setting the max clients configuration to 3984.`

`02:03:36 redis_async_broker.1 | [12287] 16 Mar 02:03:36.701 # Warning: 32 bit instance detected but no memory limit set. Setting 3 GB maxmemory limit with 'noeviction' policy now.`

`02:03:36 redis_async_broker.1 |                 _._`

`02:03:36 redis_async_broker.1 |            _.-``__ ''-._`

`02:03:36 redis_async_broker.1 |       _.-``    `.  `_.  ''-._           Redis 2.8.4 (00000000/0) 32 bit`

`02:03:36 redis_async_broker.1 |   .-`` .-```.  ```\/    _.,_ ''-._`

`02:03:36 redis_async_broker.1 |  (    '      ,       .-`  | `,    )     Running in stand alone mode`

`02:03:36 redis_async_broker.1 |  |`-._`-...-` __...-.``-._|'` _.-'|     Port: 12311`

`02:03:36 redis_async_broker.1 |  |    `-._   `._    /     _.-'    |     PID: 12287`

`02:03:36 redis_async_broker.1 |   `-._    `-._  `-./  _.-'    _.-'`

`02:03:36 redis_async_broker.1 |  |`-._`-._    `-.__.-'    _.-'_.-'|`

`02:03:36 redis_async_broker.1 |  |    `-._`-._        _.-'_.-'    |           http://redis.io`

`02:03:36 redis_async_broker.1 |   `-._    `-._`-.__.-'_.-'    _.-'`

`02:03:36 redis_async_broker.1 |  |`-._`-._    `-.__.-'    _.-'_.-'|`

`02:03:36 redis_async_broker.1 |  |    `-._`-._        _.-'_.-'    |`

`02:03:36 redis_async_broker.1 |   `-._    `-._`-.__.-'_.-'    _.-'`

`02:03:36 redis_async_broker.1 |       `-._    `-.__.-'    _.-'`

`02:03:36 redis_async_broker.1 |           `-._        _.-'`

`02:03:36 redis_async_broker.1 |               `-.__.-'`

`02:03:36 redis_async_broker.1 |`

`02:03:36 redis_async_broker.1 | [12287] 16 Mar 02:03:36.701 # Server started, Redis version 2.8.4`

`02:03:36 redis_async_broker.1 | [12287] 16 Mar 02:03:36.701 # WARNING overcommit_memory is set to 0! Background save may fail under low memory condition. To fix this issue add 'vm.overcommit_memory = 1' to /etc/sysctl.conf and then reboot or run the command 'sysctl vm.overcommit_memory=1' for this to take effect.`

`02:03:36 redis_async_broker.1 | [12287] 16 Mar 02:03:36.703 * The server is now ready to accept connections on port 12311`

`02:03:36 system               | async_worker.1 started (pid=12267)`

`02:03:36 system               | redis_cache.1 started (pid=12269)`

`02:03:36 redis_cache.1        | [12294] 16 Mar 02:03:36.729 # Unable to set the max number of files limit to 10032 (Operation not permitted), setting the max clients configuration to 3984.`

`02:03:36 redis_cache.1        |                 _._`

`02:03:36 redis_cache.1        |            _.-``__ ''-._`

`02:03:36 redis_cache.1        |       _.-``    `.  `_.  ''-._           Redis 2.8.4 (00000000/0) 32 bit`

`02:03:36 redis_cache.1        |   .-`` .-```.  ```\/    _.,_ ''-._`

`02:03:36 redis_cache.1        |  (    '      ,       .-`  | `,    )     Running in stand alone mode`

`02:03:36 redis_cache.1        |  |`-._`-...-` __...-.``-._|'` _.-'|     Port: 11311`

`02:03:36 redis_cache.1        |  |    `-._   `._    /     _.-'    |     PID: 12294`

`02:03:36 redis_cache.1        |   `-._    `-._  `-./  _.-'    _.-'`

`02:03:36 redis_cache.1        |  |`-._`-._    `-.__.-'    _.-'_.-'|`

`02:03:36 redis_cache.1        |  |    `-._`-._        _.-'_.-'    |           http://redis.io`

`02:03:36 redis_cache.1        |   `-._    `-._`-.__.-'_.-'    _.-'`

`02:03:36 redis_cache.1        |  |`-._`-._    `-.__.-'    _.-'_.-'|`

`02:03:36 redis_cache.1        |  |    `-._`-._        _.-'_.-'    |`

`02:03:36 redis_cache.1        |   `-._    `-._`-.__.-'_.-'    _.-'`

`02:03:36 redis_cache.1        |       `-._    `-.__.-'    _.-'`

`02:03:36 redis_cache.1        |           `-._        _.-'`

`02:03:36 redis_cache.1        |               `-.__.-'`

`02:03:36 redis_cache.1        |`

`02:03:36 redis_cache.1        | [12294] 16 Mar 02:03:36.729 # Server started, Redis version 2.8.4`

`02:03:36 redis_cache.1        | [12294] 16 Mar 02:03:36.729 # WARNING overcommit_memory is set to 0! Background save may fail under low memory condition. To fix this issue add 'vm.overcommit_memory = 1' to /etc/sysctl.conf and then reboot or run the command 'sysctl vm.overcommit_memory=1' for this to take effect.`

`02:03:36 redis_cache.1        | [12294] 16 Mar 02:03:36.736 * The server is now ready to accept connections on port 11311`

`02:03:36 system               | socketio.1 started (pid=12268)`

`02:03:36 system               | worker.1 started (pid=12288)`

`02:03:36 system               | longjob_worker.1 started (pid=12298)`

`02:03:37 socketio.1           | module.js:341`

`02:03:37 socketio.1           |     throw err;`

`02:03:37 socketio.1           |     ^`

`02:03:37 socketio.1           |`

`02:03:37 socketio.1           | Error: Cannot find module '/vagrant/frappe-bench/apps/frappe/socketio.js'`

`02:03:37 socketio.1           |     at Function.Module._resolveFilename (module.js:339:15)`

`02:03:37 socketio.1           |     at Function.Module._load (module.js:290:25)`

`02:03:37 socketio.1           |     at Function.Module.runMain (module.js:447:10)`

`02:03:37 socketio.1           |     at startup (node.js:141:18)`

`02:03:37 socketio.1           |     at node.js:933:3`

`02:03:37 system               | socketio.1 stopped (rc=1)`

`02:03:37 system               | sending SIGTERM to workerbeat.1 (pid 12266)`

`02:03:37 system               | sending SIGTERM to watch.1 (pid 12264)`

`02:03:37 system               | sending SIGTERM to redis_celery.1 (pid 12263)`

`02:03:37 system               | sending SIGTERM to web.1 (pid 12265)`

`02:03:37 system               | sending SIGTERM to async_worker.1 (pid 12267)`

`02:03:37 system               | sending SIGTERM to redis_async_broker.1 (pid 12275)`

`02:03:37 system               | sending SIGTERM to redis_cache.1 (pid 12269)`

`02:03:37 system               | sending SIGTERM to worker.1 (pid 12288)`

`02:03:37 system               | sending SIGTERM to longjob_worker.1 (pid 12298)`

`02:03:37 system               | workerbeat.1 stopped (rc=-15)`

`02:03:37 redis_celery.1       | [12271 | signal handler] (1458093817) Received SIGTERM, scheduling shutdown...`

`02:03:37 redis_celery.1       | [12271] 16 Mar 02:03:37.254 # User requested shutdown...`

`02:03:37 redis_celery.1       | [12271] 16 Mar 02:03:37.254 * Saving the final RDB snapshot before exiting.`

`02:03:37 system               | watch.1 stopped (rc=-15)`

`02:03:37 redis_celery.1       | [12271] 16 Mar 02:03:37.260 * DB saved on disk`

`02:03:37 redis_celery.1       | [12271] 16 Mar 02:03:37.260 # Redis is now ready to exit, bye bye...`

`02:03:37 system               | redis_celery.1 stopped (rc=-15)`

`02:03:37 system               | web.1 stopped (rc=-15)`

`02:03:37 redis_async_broker.1 | [12287 | signal handler] (1458093817) Received SIGTERM, scheduling shutdown...`

`02:03:37 redis_async_broker.1 | [12287] 16 Mar 02:03:37.285 # User requested shutdown...`

`02:03:37 redis_async_broker.1 | [12287] 16 Mar 02:03:37.285 # Redis is now ready to exit, bye bye...`

`02:03:37 system               | redis_async_broker.1 stopped (rc=-15)`

`02:03:37 redis_cache.1        | [12294 | signal handler] (1458093817) Received SIGTERM, scheduling shutdown...`

`02:03:37 redis_cache.1        | [12294] 16 Mar 02:03:37.288 # User requested shutdown...`

`02:03:37 redis_cache.1        | [12294] 16 Mar 02:03:37.288 # Redis is now ready to exit, bye bye...`

`02:03:37 system               | redis_cache.1 stopped (rc=-15)`

`02:03:37 system               | worker.1 stopped (rc=-15)`

`02:03:37 system               | longjob_worker.1 stopped (rc=-15)`

`02:03:37 system               | async_worker.1 stopped (rc=-15)`

