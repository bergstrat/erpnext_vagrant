# Installing prerequisites under Windows: #

1. Download and install **Virtual Box**. Attention! There are known problems with VirtualBox 5.0.2 on Windows 10 hosts and with Windows 10 guests. Some of the problems are fixed in the most recent test build which can be found at https://www.virtualbox.org/wiki/Testbuilds.
2. Download and install **Vagrant** for Windows https://www.vagrantup.com/downloads.html
3. Download and install **GitHub Desktop** for Windows at https://desktop.github.com/
4. From now on use **Git Shell** (on your Desktop) to run all commands since it supports some Linux commands natively, most importantly SSH. This means you won't have to install and set up Putty.
5. (Optional) Install a good text editor such as **Atom** at https://atom.io/

# Set up an ERPNext dev environment using Vagrant: # 

1. Clone this repo into a local folder with `git clone https://github.com/frappe/erpnext_vagrant.git erpnext_vagrant`
2. Make erpnext_vagrant your working directory with `cd erpnext_vagrant`
3. Start your virtual machine by running `vagrant up`
4. Connect to your guest system via SSH with `vagrant ssh`
5. run `bench init frappe-bench`
6. make frappe-bench your working directory with `cd frappe-bench`
7. run `bench new-site site1.local`. You will be prompted for a SQL password which is "root". You will then be asked to enter and reenter a password which you will use to log into ERPNext.
8. Set `"developer_mode": 1` in `/vagrant/frappe-bench/sites/site1.local/site_config.json`, for example by running `vim /vagrant/frappe-bench/sites/site1.local/site_config.json`. When in vim press `i` to insert text. After inserting press `ESC` and write `:wq` to write and quit the file. More on vim here https://www.linux.com/learn/tutorials/228600-vim-101-a-beginners-guide-to-vim.
9. Go to your frappe-bench folder with `cd /vagrant/frappe-bench/` and run `bench install-app erpnext`
10. start bench with `bench start`
11. Open your browser on your host system and work on your ERPNExt by browsing to `http://localhost:8080/` or `http://127.0.0.1:8080`
