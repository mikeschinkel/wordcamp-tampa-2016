#No More Cowboy Coding!

**_AKA Easy Local WordPress Development_**

_Presented by Mike Schinkel_

##Agenda
### SURVEY
####Skill Set
- Designers? 
- Backend Developers
- Frontend Developers
- Full stack Developers?
- Site Builders _(not a programmer?)_
- End Users of WordPress?
- None of the Above?

####Organization Type
- Individual Freelancer?
- Work for an Agency?
- Work for a Company Building Own Sites?
- Commercial Theme Developers?
- Commercial Plugin Developers?
- Work for a Web Host?
- None of the Above?


### BACKGROUND
- What Defines a Web Server?
- What Defines WordPress on a Web Server?
- Web Servers vs Local Computers
- Benefits of Local Development
- Options for Local Development
- Options for Local WordPress Development

### WORKSHOP
1. Install VirtualBox
2. Install Vagrant
3. Install Vagrant Plugins
4. Pick your "Sites" Directory
5. Get WPLib Box
6. Now: Vagrant Up!
7. Open wplib.box
8. Login to the Admin Console
9. Change the Domain Name
10. Exploring the Database
11. Debugging with PhpStorm
12. Fixing IP Conflicts
13. Importing Your Own Project
14. Multi-tenancy

	

#WORKSHOP

##Software Required
- VirtualBox _([_Download Here_](virtualbox.org/wiki/Downloads))_
- Vagrant _([_Download Here_](https://www.vagrantup.com/downloads.html))_

OR

- Use a Thumb Drive _(One of four Lexar 8Gb drives)_ 
- Instructions Here for Unzipping `vagrant.d.zip`

##WorkShop Instructions For:

- [Mac OS X Users](mac-os-x-bash.md)
- [Windows Users with Powershell](windows-powershell.md)
- [Windows Users w/o Powershell](windows-cmd.md)








#BACKGROUND
##What Defines a Web Server?
- A computer running software
- Web Server software aka a "Listener" on port 80
- Maybe a database server like MySQL
- Maybe a programming language like PHP		

##What Defines WordPress on a Web Server?
- Apache or Nginx web server
- MySQL or MariaDB database server
- PHP programming language 
- Source code _(PHP + CSS + JS + HTML + Images + etc.)_	
	- WordPress Core 
	- One Theme
	- Zero or More Plugins
- A Database containing Content _(and some configuration)_
- Uploaded Files: _(Images, PDFs, etc.)_

##Web Servers vs Local Computers
- Both are just computers
- IP addresses:
	- Laptop/Desktop: Dynamically assigned _(usually)_
	- Hosted Website: Statically assigned
- Both can host websites
- All you need to host locally in to install the software

##Benefits of Local Development
- No more Cowboy Coding!
- Local Changes do not affect the Live Website
- Ability to use a Debugger
- No Latency when editing theme and plugin files.
- Try "with if" scenarios
	- If no good, throw away and start over
- Easier to use Version Control
- Easier to use Composer
- Easier to level up to Best Practices over time

##Options for Local Development
1. Install on your computer
	- Free, open source and standard
	- Commercial and proprietary
2. Install a Virtual Machine from on a Hypervisor _(VirtualBox or VMware)_
	- Free
3. Install Docker Container in a Virtual Machine with a Hypervisor
	- Free and Commercial

##Options for Local WordPress Development
- WAMP/MAMP/XXAMP (Commercial)
- Laravel Homestead (free, optimized for Laravel)
- Laravel Valet (free, installs directly on your computer)
- ScotchBox (free, generic PHP, no XDEBUG)
- VVV (Free, Complicated)
- VIP Quickstart (Free, Ironically named)
- Trellis (Free, Complicated)
- DesktopServer (Commercial)
- Pressmatic (Commercial)
- Many other lesser known solutions _(most are free)_
- WPLib Box (Free, Simple)
	- Full Disclosure - I designed it, and our team built it.

##Questions?
- Anything except future plans

##WPLib Future Plans

- We Pledge:

	- To keep WPLib Box software **_always free to use_**
	- To solve the harder problems WordPress site builders experience
	- To have a fanatical focus on _"Developer Experience"_
	- To make it easier for WordPress Pros to follow best practices vs. not.

- **Multi-project Support** in the very near future _(~1 month?)_, including:

	- An **Admin Console** 
	- An **API**
	- An **In-Box Command Line Tool**

- A Windows and Mac Command Line Tool to Manage the Box
- Commercial Support to include Installers for Mac & Windows
- Build Tools
- Deployment Tools
- Installable Packages
- Hardware versions of WPLib Box 
	- Would you be interested in one?
- Questions?