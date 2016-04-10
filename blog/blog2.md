vagrant box update
vagrant up
vagrant ssh
bench init frappe-bench
cd frappe-bench
bench get-app erpnext https://github.com/frappe/erpnext         # Add ERPNext to your bench apps
bench new-site site1.local                      # Create a new site
password root - https://github.com/varying-vagrant-vagrants/vvv/wiki/Connecting-to-MySQL
will use password later
bench install-app erpnext             
