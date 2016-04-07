Getting Started with ERPNext Using Vagrant

--------------------------------------------

```<a href="https://erpnext.com/">ERPNEXT</a> is a web based software that helps businesses with processes related to accounts payable, inventory management, human resources etc. With my experince working in accounting, I felt this was the perfect project to contribute to. The project was suggested to me through the reddit community in r/opensource. ERPNExt had an active community and straight forward install instructions. I introduced myself <a href="https://discuss.erpnext.com/t/getting-erpnext-installed-for-developing/10877/3">here</a> and was ready to get started. As recommended, I decided to install the program for developement using a vagrant environment. The instructions to do so can be found <a href="https://github.com/frappe/erpnext_vagrant/blob/master/README.md">here</a>. For my first attempt at installation, I followed the instructions exactly as stated. This failed because I did not run vagrant up inside the erpnext_vagrant directory. I found out the cause of the problem after making a forum <a href="https://discuss.erpnext.com/t/trouble-installing-erpnext-w-vagrant-solved/11086/3">post</a>. Trying again, this time running the command `cd erpnext_vagrant` after cloning the repo, `vagrant up` ran sccessfully. I used `vagrant ssh` to connect and the vagrant environment was started. As per step 5 in the instructions, I ran `vim /vagrant/frappe-bench/sites/site1.local/site_config.json` and set my developer mode to 1. This gave me an error 'E212: Cannot open file for writing' when trying to exit using :wq . My solution to this was to go to the sites folder with `cd /vagrant/frappe-bench/sites` and create a directory called site1.local. I then ran `cd site1.local` and created the file site_confrig.json using vim. I editted the README.md adding an install step, instructions on dealing with the E212 error and fixed a spelling mistake.```
I commited my editted README.md file <a href="https://github.com/bergstrat/erpnext_vagrant/commit/0b1fc9e167e78e96d827dfb952d3ae4bcf7d9eab">here</a>

Going back to the /vagrant/frappe-bench directory, I ran `bench start` which... ran with errors.

redis_async_broker.1 started (pid=12182)

02:02:26 redis_async_broker.1 | [12193] 16 Mar 02:02:26.652 # Fatal error, can't open config file 'config/redis_async_broker.conf'

02:02:26 system               | redis_async_broker.1 stopped (rc=1)

02:02:26 system               | web.1 started (pid=12179)

02:02:26 system               | async_worker.1 started (pid=12181)

02:02:26 system               | watch.1 started (pid=12180)

02:02:26 system               | redis_cache.1 started (pid=12183)

02:02:26 redis_cache.1        | [12195] 16 Mar 02:02:26.662 # Fatal error, can't open config file 'config/redis_cache.conf'

02:02:26 system               | redis_cache.1 stopped (rc=1)

The solution was to run two commands:
1. `bench setup redis_async_broker`
2. `bench setup redis_cache`

Running `bench start` once more, I got a new error.

connections on port 11311

02:03:36 system               | socketio.1 started (pid=12268)

02:03:36 system               | worker.1 started (pid=12288)

02:03:36 system               | longjob_worker.1 started (pid=12298)

02:03:37 socketio.1           | module.js:341

02:03:37 socketio.1           |     throw err;

02:03:37 socketio.1           |     ^

02:03:37 socketio.1           |

02:03:37 socketio.1           | Error: Cannot find module '/vagrant/frappe-bench/apps/frappe/socketio.js'

02:03:37 socketio.1           |     at Function.Module._resolveFilename (module.js:339:15)

02:03:37 socketio.1           |     at Function.Module._load (module.js:290:25)

02:03:37 socketio.1           |     at Function.Module.runMain (module.js:447:10)

02:03:37 socketio.1           |     at startup (node.js:141:18)

02:03:37 socketio.1           |     at node.js:933:3

02:03:37 system               | socketio.1 stopped (rc=1)


I tried running `bench setup socketio`, hoping to get similiar results to the errors mentioned previously but received the following error:

/bin/sh: 1: npm: not found

Traceback (most recent call last):

  File "/usr/local/bin/bench", line 9, in <module>

      load_entry_point('bench==0.0.0', 'console_scripts', 'bench')()

        File "/vagrant/bench-repo/bench/cli.py", line 60, in cli

	    bench()

	      File "/usr/local/lib/python2.7/dist-packages/click/core.py", line 716, in __call__

	          return self.main(*args, **kwargs)

		    File "/usr/local/lib/python2.7/dist-packages/click/core.py", line 696, in main

		        rv = self.invoke(ctx)

			  File "/usr/local/lib/python2.7/dist-packages/click/core.py", line 1060, in invoke

			      return _process_result(sub_ctx.command.invoke(sub_ctx))

			        File "/usr/local/lib/python2.7/dist-packages/click/core.py", line 1060, in invoke

				    return _process_result(sub_ctx.command.invoke(sub_ctx))

				      File "/usr/local/lib/python2.7/dist-packages/click/core.py", line 889, in invoke

				          return ctx.invoke(self.callback, **ctx.params)

					    File "/usr/local/lib/python2.7/dist-packages/click/core.py", line 534, in invoke

					        return callback(*args, **kwargs)

						  File "/vagrant/bench-repo/bench/cli.py", line 487, in _setup_socketio

						      setup_socketio()

						        File "/vagrant/bench-repo/bench/utils.py", line 115, in setup_socketio

							    exec_cmd("npm install socket.io redis express superagent cookie", 
							    cwd=bench)
							      File "/vagrant/bench-repo/bench/utils.py", line 105, in exec_cmd
							    
							          raise CommandFailedError(cmd)
							
								  bench.utils.CommandFailedError: npm install socket.io redis express superagent cookie

The complete logs containing the above errors can be found in the blog directory of my forked repo of erpnext_vagrant.

The above solutions were suggested to me in response to a third forum <a href="https://discuss.erpnext.com/t/error-cant-open-config-file-when-i-run-bench-start/11088/12">post</a>.
The issues seems to be with the process ran by `vagrant up`. It is suppose to install a frappe app in the /vagrant/freppe-bench/apps directory. Over the next two weeks, I intended on looking for errors that occur when running `vagrant up` and look for the root g directory in my forked repo of erpnext_vagrant.

The Steps I took to install and run erpnext are below.

1. `git clone https://github.com/bergstrat/erpnext_vagrant`
2. `cd erpnext_vagrant`
3. `vagrant up`
4. `vagrant ssh`
5. `cd /vagrant/frappe-bench/sites`
6. `mkdir site1.local`
7. `cd site1.local`
8. `vim site_config.json`
9. Insert` "developer_mode" :1 ` and exit vim
10. `cd /vagrant/frappe-bench`
11. `bench setup redis_async_broker`
12. `bench setup redis_cache`
13. `bench start`
