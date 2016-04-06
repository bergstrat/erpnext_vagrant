`02:02:26 system               | workerbeat.1 started (pid=12178)`
`02:02:26 system               | redis_async_broker.1 started (pid=12182)`
`02:02:26 redis_async_broker.1 | [12193] 16 Mar 02:02:26.652 # Fatal error, can't open config file 'config/redis_async_broker.conf'`
`02:02:26 system               | redis_async_broker.1 stopped (rc=1)`
`02:02:26 system               | web.1 started (pid=12179)`
`02:02:26 system               | async_worker.1 started (pid=12181)`
`02:02:26 system               | watch.1 started (pid=12180)`
`02:02:26 system               | redis_cache.1 started (pid=12183)`
`02:02:26 redis_cache.1        | [12195] 16 Mar 02:02:26.662 # Fatal error, can't open config file 'config/redis_cache.conf'`
`02:02:26 system               | redis_cache.1 stopped (rc=1)`
`02:02:26 system               | socketio.1 started (pid=12187)`
`02:02:26 system               | redis_celery.1 started (pid=12189)`
`02:02:26 system               | worker.1 started (pid=12184)`
`02:02:26 redis_celery.1       | [12201] 16 Mar 02:02:26.708 # Warning: no config file specified, using the default config. In order to specify a config file use redis-server /path/to/redis.conf`
`02:02:26 redis_celery.1       | [12201] 16 Mar 02:02:26.709 # Unable to set the max number of files limit to 10032 (Operation not permitted), setting the max clients configuration to 3984.`
`02:02:26 redis_celery.1       | [12201] 16 Mar 02:02:26.709 # Warning: 32 bit instance detected but no memory limit set. Setting 3 GB maxmemory limit with 'noeviction' policy now.`
`02:02:26 redis_celery.1       |                 _._`
`02:02:26 redis_celery.1       |            _.-``__ ''-._`
`02:02:26 redis_celery.1       |       _.-``    `.  `_.  ''-._           Redis 2.8.4 (00000000/0) 32 bit`
`02:02:26 redis_celery.1       |   .-`` .-```.  ```\/    _.,_ ''-._`
`02:02:26 redis_celery.1       |  (    '      ,       .-`  | `,    )     Running in stand alone mode`
`02:02:26 redis_celery.1       |  |`-._`-...-` __...-.``-._|'` _.-'|     Port: 6379``
`02:02:26 redis_celery.1       |  |    `-._   `._    /     _.-'    |     PID: 12201`
`02:02:26 redis_celery.1       |   `-._    `-._  `-./  _.-'    _.-'`
`02:02:26 redis_celery.1       |  |`-._`-._    `-.__.-'    _.-'_.-'|`
`02:02:26 redis_celery.1       |  |    `-._`-._        _.-'_.-'    |`           http://redis.io`
`02:02:26 redis_celery.1       |   `-._    `-._`-.__.-'_.-'    _.-'`
`02:02:26 redis_celery.1       |  |`-._`-._    `-.__.-'    _.-'_.-'|`
`02:02:26 redis_celery.1       |  |    `-._`-._        _.-'_.-'    |`
`02:02:26 redis_celery.1       |   `-._    `-._`-.__.-'_.-'    _.-'`
`02:02:26 redis_celery.1       |       `-._    `-.__.-'    _.-'`
`02:02:26 redis_celery.1       |           `-._        _.-'`
`02:02:26 redis_celery.1       |               `-.__.-'`
`02:02:26 redis_celery.1       |`
`02:02:26 redis_celery.1       | [12201] 16 Mar 02:02:26.709 # Server started, Redis version 2.8.4`
`02:02:26 redis_celery.1       | [12201] 16 Mar 02:02:26.709 # WARNING overcommit_memory is set to 0! Background save may fail under low memory condition. To fix this issue add 'vm.overcommit_memory = 1' to /etc/sysctl.conf and then reboot or run the command 'sysctl vm.overcommit_memory=1' for this to take effect.`
`02:02:26 redis_celery.1       | [12201] 16 Mar 02:02:26.737 * The server is now ready to accept connections on port 6379`
`02:02:26 system               | longjob_worker.1 started (pid=12200)`
`02:02:26 system               | sending SIGTERM to workerbeat.1 (pid 12178)`
`02:02:26 system               | sending SIGTERM to watch.1 (pid 12180)`
`02:02:26 system               | sending SIGTERM to redis_celery.1 (pid 12189)`
`02:02:26 system               | sending SIGTERM to web.1 (pid 12179)`
`02:02:26 system               | sending SIGTERM to async_worker.1 (pid 12181)`
`02:02:26 system               | sending SIGTERM to socketio.1 (pid 12187)`
`02:02:26 system               | sending SIGTERM to worker.1 (pid 12184)`
`02:02:26 system               | sending SIGTERM to longjob_worker.1 (pid 12200)`
`02:02:26 redis_celery.1       | [12201 | signal handler] (1458093746) Received SIGTERM, scheduling shutdown...`
`02:02:26 redis_celery.1       | [12201] 16 Mar 02:02:26.856 # User requested shutdown...`
`02:02:26 redis_celery.1       | [12201] 16 Mar 02:02:26.856 * Saving the final RDB snapshot before exiting.`
`02:02:26 system               | workerbeat.1 stopped (rc=-15)`
`02:02:26 system               | watch.1 stopped (rc=-15)`
`02:02:26 system               | web.1 stopped (rc=-15)`
`02:02:26 redis_celery.1       | [12201] 16 Mar 02:02:26.862 * DB saved on disk`
`02:02:26 redis_celery.1       | [12201] 16 Mar 02:02:26.862 # Redis is now ready to exit, bye bye...`
`02:02:26 system               | redis_celery.1 stopped (rc=-15)`
`02:02:26 system               | async_worker.1 stopped (rc=-15)`
`02:02:26 system               | longjob_worker.1 stopped (rc=-15)`
`02:02:26 system               | socketio.1 stopped (rc=-15)`
`02:02:26 system               | worker.1 stopped (rc=-15)`
