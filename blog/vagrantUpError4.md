==> default: npm

==> default:

==> default: WARN

==> default:

==> default: enoent

==> default:  ENOENT: no such file or directory, open '/vagrant/frappe-bench/package.json'

==> default: npm

==> default:

==> default: WARN

==> default:  frappe-bench No description

==> default: npm

==> default:

==> default: WARN

==> default:  frappe-bench No repository field.

==> default: npm

==> default:

==> default: WARN

==> default:  frappe-bench No README data

==> default: npm

==> default:

==> default: WARN

==> default:  frappe-bench No license field.

==> default: npm

==> default:

==> default: ERR!

==> default:  Linux 3.13.0-85-generic

==> default: npm

==> default:

==> default: ERR!

==> default:

==> default: argv

==> default:  "/usr/bin/nodejs" "/usr/bin/npm" "install" "socket.io" "redis" "express" "superagent" "cookie"

==> default: npm

==> default:

==> default: ERR!

==> default:

==> default: node

==> default:  v5.10.1

==> default: npm

==> default:

==> default: ERR!

==> default:  npm  v3.8.3

==> default: npm ERR! path ../mime/cli.js

==> default: npm ERR! code EPROTO

==> default: npm ERR! errno -71

==> default: npm ERR! syscall symlink

==> default: npm

==> default:

==> default: ERR!

==> default:  EPROTO: protocol error, symlink '../mime/cli.js' -> '/vagrant/frappe-bench/node_modules/.bin/mime'

==> default: npm

==> default:

==> default: ERR!

==> default:

==> default: npm ERR! If you need help, you may report this error at:

==> default: npm ERR!     <https://github.com/npm/npm/issues>

==> default: npm

==> default:

==> default: ERR!

==> default:  Please include the following file with any support request:

==> default: npm

==> default:

==> default: ERR!

==> default:      /vagrant/frappe-bench/npm-debug.log

==> default: Traceback (most recent call last):

==> default:   File "/usr/local/bin/bench", line 9, in <module>

==> default:

==> default: load_entry_point('bench==2.0.0', 'console_scripts', 'bench')()

==> default:   File "/vagrant/bench-repo/bench/cli.py", line 40, in cli

==> default:

==> default: bench_command()

==> default:   File "/usr/local/lib/python2.7/dist-packages/click/core.py", line 716, in __call__

==> default:

==> default: return self.main(*args, **kwargs)

==> default:   File "/usr/local/lib/python2.7/dist-packages/click/core.py", line 696, in main

==> default:

==> default: rv = self.invoke(ctx)

==> default:   File "/usr/local/lib/python2.7/dist-packages/click/core.py", line 1060, in invoke

==> default:

==> default: return _process_result(sub_ctx.command.invoke(sub_ctx))

==> default:   File "/usr/local/lib/python2.7/dist-packages/click/core.py", line 1060, in invoke

==> default:

==> default: return _process_result(sub_ctx.command.invoke(sub_ctx))

==> default:   File "/usr/local/lib/python2.7/dist-packages/click/core.py", line 889, in invoke

==> default:     return ctx.invoke(self.callback, **ctx.params)

==> default:   File "/usr/local/lib/python2.7/dist-packages/click/core.py", line 534, in invoke

==> default:     return callback(*args, **kwargs)

==> default:   File "/vagrant/bench-repo/bench/commands/setup.py", line 77, in setup_socketio

==> default:

==> default: setup_socketio()

==> default:   File "/vagrant/bench-repo/bench/utils.py", line 109, in setup_socketio

==> default:

==> default: exec_cmd("npm install socket.io redis express superagent cookie", cwd=bench)

==> default:   File "/vagrant/bench-repo/bench/utils.py", line 99, in exec_cmd

==> default:

==> default: raise CommandFailedError(cmd)

==> default: bench.utils

==> default: .

==> default: CommandFailedError
