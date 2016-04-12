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

==> default:   File "/usr/local/lib/python2.7/dist-packages/click/core.py", line 889, in invoke

==> default:

==> default: return ctx.invoke(self.callback, **ctx.params)

==> default:   File "/usr/local/lib/python2.7/dist-packages/click/core.py", line 534, in invoke

==> default:

==> default: return callback(*args, **kwargs)

==> default:   File "/vagrant/bench-repo/bench/commands/make.py", line 28, in get_app

==> default:

==> default: get_app(name, git_url, branch=branch)

==> default:   File "/vagrant/bench-repo/bench/app.py", line 56, in get_app

==> default:

==> default: install_app(app, bench=bench, verbose=verbose)

==> default:   File "/vagrant/bench-repo/bench/app.py", line 82, in install_app

==> default:

==> default: find_links=find_links))

==> default:   File "/vagrant/bench-repo/bench/utils.py", line 99, in exec_cmd

==> default:

==> default: raise CommandFailedError(cmd)

==> default: bench.utils

==> default: .

==> default: CommandFailedError

==> default: :

==> default: ./env/bin/pip install -q  -e ./apps/erpnext

==> default: Error: no such option: --install-app

==> default: Usage: bench [OPTIONS] COMMAND [ARGS]...

==> default: Error: No such command "use".
