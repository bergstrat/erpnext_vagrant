==> default: Traceback (most recent call last):

==> default:   File "/usr/local/bin/virtualenv", line 11, in <module>

==> default:

==> default: sys.exit(main())

==> default:   File "/usr/local/lib/python2.7/dist-packages/virtualenv.py", line 708, in main

==> default:

==> default: symlink=options.symlink)

==> default:   File "/usr/local/lib/python2.7/dist-packages/virtualenv.py", line 921, in create_environment

==> default:

==> default: site_packages=site_packages, clear=clear, symlink=symlink))

==> default:   File "/usr/local/lib/python2.7/dist-packages/virtualenv.py", line 1353, in install_python

==> default:

==> default: os.symlink(py_executable_base, full_pth)

==> default: OSError

==> default: : [Errno 71] Protocol error

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

==> default:     return ctx.invoke(self.callback, **ctx.params)

==> default:   File "/usr/local/lib/python2.7/dist-packages/click/core.py", line 534, in invoke

==> default:     return callback(*args, **kwargs)

==> default:   File "/vagrant/bench-repo/bench/commands/make.py", line 17, in init

==> default:

==> default: no_auto_update=no_auto_update, frappe_path=frappe_path, frappe_branch=frappe_branch, verbose=verbose)

==> default:   File "/vagrant/bench-repo/bench/utils.py", line 56, in init

==> default:

==> default: setup_env(bench=path)

==> default:   File "/vagrant/bench-repo/bench/utils.py", line 102, in setup_env

==> default:

==> default: exec_cmd('virtualenv -q {} -p {}'.format('env', sys.executable), cwd=bench)

==> default:   File "/vagrant/bench-repo/bench/utils.py", line 99, in exec_cmd

==> default:

==> default: raise CommandFailedError(cmd)

==> default: bench.utils

==> default: .

==> default: CommandFailedError
