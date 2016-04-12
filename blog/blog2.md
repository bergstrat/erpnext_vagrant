On with the Journey to Properly Install ERPNext with Vagrant
---------------------------------------------------------------

As of the end of my last blog post, I had a broken version of ERPNext installed within a vagrant environment. In order to find and 
fix the issues causing the program to not install correctly, I deleted my local repo so I could reinstall ERPNext and document any
errors that occur during installation.

I recloned my git repo and I was on my way. I ran `vagrant up` and monitored the console as it installed.

I found multiple errors that occured during the installation process which I documented and uploaded to the blog directory of my git repo. 

Once the install process was complete, I ran `vagrant ssh` and I was back up and running in the vagrant environment. 

But... things were different this time. 

I did not have a `frappe-bench` folder in /vagrant and some of the `bench` commands no longer 
existed; specifically `bench setup redis_async_broker`. 

Because of the change of existing commands, I can only assume changes have been made to the `frappe-bench` software since my last blog post.

At this point, I was quite confused as to how to proceed. The few things I had working during my last blog post no longer existed. 

SO, I figured I would try installing `frappe-bench` and `erpnext` manually in my vagrant environment following the instructions found <a 
href="https://github.com/frappe/bench#setting-up-erpnext">here</a>.

I ran `bench init frappe-bench` which seemed to work without error. Progress!

I then ran `cd frappe-bench` to make `frappe-bench` my working directory 

followed by `bench get-app https://github.com/frappe/erpnext`which also seemed to do what it is suppose to do.

The next command I ran was `bench new-site site1.local`. 

In the last blog post, I simply created a directory in sites called `site1.local` to store my `site_config.json` file in. Though this doesn't account for the frappe app that should have been installed with `vagrant up` missing,
I imagine this was a source of some of the errors that occured when I ran `bench start`. 
In summary, a bench site and a directory are not the same thing! 

When running `bench new-site1.local`, I was prompted for a "MYSQL Password" which, after some googling, I found out was "root". I was then prompted to enter and reenter a password which would later be used to log in to ERPNext.

Once the site was created, I ran `cd sites/site1.local` then `vim site_config.json` which, unlike before, already existed. 

Within, I added the line `developer_mode":1`, saved and quit.

I made `vagrant/frappe-bench` my working directory and ran the last install command `bench install-app erpnext`.

Now for the moment of truth... I ran `bench start` which seemed to put giberish on the screen different than the giberish I saw weeks 
earlier. I crossed my fingers and went to localhost:8080. To my suprise, I saw a login screen! 

I logged in under with the username `Administrator` and the password I had entered previously when I ran `bench new-site site1.local`. I finished creating my profile and I was done. I was ready to start helping with the development of ERPNext. I shut down vagrant and called it a day. 

Originally when I first went to localhost:8080, I was landed on a log in page. When I later went back into vagrant  after shutting down and ran `bench start`, I landed on a different "test" screen made for developers. I am not sure if completing the profile creation process or if rerunning vagrant was what made the changes to the landing screen, but that is neither here nor there. I uploaded a screenshot landingScreen.jpg to the blog directory of my forked repo to be viewed. I updated my README file to include the new install instructions which I will submit a pull request for once I figure out how to submit a pull request containing only certain commits.

The final, complete and seemingly correct installation instructions are:

1. `vagrant up`

2. `vagrant ssh`

3. `bench init frappe-bench`

4. `cd frappe-bench`

5. `bench get-app erpnext https://github.com/frappe/erpnext`

6. `bench new-site site1.local` using password "root"

7. `cd sites/site1.local`

8. `vim site_config.json` adding in the line `"developer_mode:1"`

9. `cd ..`

10. `cd ..`

11. `bench install-app erpnext`

12. `bench start`       
