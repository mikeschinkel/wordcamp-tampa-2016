#No More Cowboy Coding!

**_AKA Easy Local WordPress Development_**

_Presented by Mike Schinkel_

##Debugging with PhpStorm and XDEBUG

###Run/Debug Configuration
1. `Run > Edit Configurations`

	![](images/run-debug-configurations-1.png)
2. `[+]`
3. `PHP Web Application`
	![](images/run-debug-configurations-2-3.png)
4. Name: `example.box`
5. `[...]`
	![](images/run-debug-configurations-4-5,13.png)
6. `[+]`
7. Name: `wplib.box`
8. Host: `wplib.box`
9. Use Path Mappings: `[x]`
10. Expand Directory Tree
11. Map `www` => `/var/www`
12. `[Ok]`
	![](images/run-debug-configurations-6-12.png)
13. `[Ok]`
	![](images/run-debug-configurations-4-5,13.png)

###Preferences/Deployment
1. `PhpStorm > Preferences` (Mac OS X) OR `File > Settings` (Windows - _I THINK_ - Ask if not)
	![](images/preferences-deployment-1.png)

2. `Build, Execution, Deployment > Deployment`
3. `[+]`
4. Name: `example.box`
5. Type: `local or mounted folder`
6. `[Ok]`
	![](images/preferences-deployment-2-6.png)
7. Folder: `[...]` 
	![](images/preferences-deployment-7,10-11.png)
8. Select your `example.box` site folder/directory
9. `[Ok]`
	![](images/preferences-deployment-8-9.png)
10. Web Server Root URL: `http://example.box`
11. `[Mappings]` tab
	![](images/preferences-deployment-7,10-11.png)
12. Local Path: Add `/www` or `\www` to what is already there
13. Deployment Path on Server: `/`
14. `[Ok]`
	![](images/preferences-deployment-12-14.png)

###Add the Debugging Bookmarklets to your Browser
1. Visit [PhpStorm Bookmarklets](https://www.jetbrains.com/phpstorm/marklets/) page
2. Click `[GENERATE]` under *Xdebug*
3. Drag _"Start Debugger_" and _"Debug this Page"_ 
4. To your Browser Toolbar
	![](images/debugging-bookmarklets-1-4.png)

###Enable Debugging in PhpStorm
1. `Run > Break at First Line in PHP Scripts`
2. `Run > Start Listening for PHP Debug Connections`
	![](images/enable-debugging-1-2.png)

###Start Debugging
- Visit http://example.box
- Click _"Debug this Page"_
- Enjoy!
