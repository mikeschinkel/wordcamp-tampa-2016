#No More Cowboy Coding!

**_AKA Easy Local WordPress Development_**

_Presented by Mike Schinkel_

#Instructions for Windows users NOT using Powershell

##1. Install VirtualBox
	https://www.virtualbox.org/wiki/Downloads
	
##2. Install Vagrant
    https://www.vagrantup.com/downloads.html
    
##3. Install Vagrant Plugins
- Vagrant Hosts Updater:

        vagrant plugin install vagrant-hostsupdater

- Vagrant Triggers:

	    vagrant plugin install vagrant-triggers

##4. Pick your _"Sites"_ Directory

	c:
	cd %userprofile%
	if not exist "Sites" mkdir Sites

##5. Get WPLib Box
### _Download_ if you DO NOT have Git installed:

- Using your Browser navigate to `https://github.com/wplib/wplib-box`
- Click the green _"Clone or Download"_ Button
- Click _"Download ZIP"_
- Save to the `%UserProfile%\Sites` directory
- Unzip `master.zip`
- Rename the `wplib-box-master` directory to `wplib.box`
- In your Command window type: 

		cd %UserProfile%\Sites\wplib.box


### _Clone_ if you have Git installed:

	c:
	cd %userprofile%
    git clone https://github.com/wplib/wplib-box.git wplib.box
    cd wplib.box

##6. Now: Vagrant Up!
Now just run: 

	vagrant up

This should only take 4-5 minutes, mostly to download the actual box image file itself.

##7. Open wplib.box
Next open http://wplib.box in your browser.
	
##8. Login to the Admin Console

Login to the `/wp-admin/` and look around

- Username: `admin`
- Password: `admin`

##9. Change the Domain Name

1. Change the domain name from `wplib.box` to `example.box`:

		c:
		cd %UserProfile%\Sites
		rename wplib.box example.box

2. Open `Vagrantfile` from `../Sites/example.box/` in your editor.

3. Find these lines:

    	config.vm.hostname = "wplib.box"
	    config.hostsupdater.aliases = [
    	    "adminer.wplib.box",
        	"mailhog.wplib.box"
	    ] 

4. Replace `wplib.box` with `example.box`.
5. Return back to Command line in `Sites/example.box/` directory
6. Run:

   		vagrant reload
   		
7. Open http://example.box in your browser.

##10. Exploring the Database

1. Open http://adminer.example.box in your browser
2. Enter credentials:

- Username: `wordpress`
- Password: `wordpress`
- Database: `wordpress`

3. Look around!

##11. Debugging with PhpStorm

- PhpStorm and XDEBUG

##12. Fixing IP Conflicts

- Open the file named `IP` in `Sites/example.box/`.
- Change it if you need to

##13. Importing Your Own Project

1. Edit `Vagrantfile` to use your own domain name i.e. `mysite.dev` instead of `example.box`
1. Export your own MySQL database to `Sites/example.box/sql/mysite.sql`
2. Delete the contents of the `www` directory
3. Copy your code into the `www` directory
4. Update `DB_USER`, `DB_PASSWORD` and `DB_NAME` in `wp-config.php` to be:
	- Username: `wordpress`
	- Password: `wordpress`
	- Database: `wordpress`
5. Run `vagrant ssh`
6. Run `box import-db mysite.sql`	
7. Type `exit`
8. Open `example.dev` in your browser






