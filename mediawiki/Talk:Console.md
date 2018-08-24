I have a different keyboard layout, is there a way to find out which key number is the tilde? (Using MS 1.9)
:I don't think the key numbers change.  The raw key codes are abstracted away by SDL and the kernel. --[[User:Tuxdev|Tuxdev]] 02:11, 11 Nov 2006 (CET)
:In the MS 1.9 preview builds, the Console is deactivated by default. Once it is activated, you can change simply change the console key in the "Options > Setup Keyboard" menu. --[[User:Sommer|Sommer]] 10:29, 11 Nov 2006 (CET)

Where Is The SuperTux configuration file
--[[User:66.230.114.105|66.230.114.105]] 19:40, 16 August 2007 (UTC)
:That depends on what operating system you use, on Linux it would be /home/yourusername/.supertux2/config, on Windows somewhere like c:\Documents and Settings\yourusername\.supertux2\config (if I recall correctly, I'm a Linux user :) ) --[[User:AnMaster|AnMaster]] 14:01, 17 August 2007 (UTC)

When scrolling up commands, should it not skip through repeated commands?
: Probably, come to think of it, but why bother changing it when you can just use the autocomplete? Although it would  probably be best to add it in anyway. --[[User:Mathnerd314|Mathnerd314]] 19:19, 20 May 2008 (UTC)

== where is the supertux config ==

hi i am a mac user and i have no idea where the config file is
im trying to access the console and there is no description of how to access it on a mac

:I suspect it may be in your home directory, under a hidden directory in it called .supertux2 or like on windows in some directory called something like "Application Data". However as I'm a Linux user I don't know exactly. --[[User:AnMaster|AnMaster]] 00:03, 23 December 2007 (UTC)

---Thanks. i looked in the home directory with Finder showing hidden files and folders, and for some reason, the directory called .supertux2 suddenly appeared. i edited the config file to (console #t) and then opened supertux. i navigated to the keyboard setup and didnt see the console option. what should i do? i am trying to access the console from Mac OS X.

::The safest way to enable the in-game console is to start SuperTux with the --console switch, e.g. on Linux you would run something along the lines of "/usr/games/supertux2 --console", on Windows "C:\Program Files\SuperTux 0.3.1\supertux2.exe --console", on Mac OS X "/Applications/SuperTux.app/Contents/MacOS/supertux2 --console" (all the time substituting the path you installed SuperTux in, of course). SuperTux will then display a new menu entry in the Keyboard Setup that will let you assign a key to toggling the console. --[[User:Sommer|Sommer]] 01:03, 24 December 2007 (UTC)