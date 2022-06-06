# videotools
A set of tools for the advanced videoartist


We use a lot of different media servers, but we always encounter the same issues. Like disable windows update, autostart Resolume Arena, or not when you try to solve something. I bundled  a set of video tools in a node-red patch and some batch scripts to make life  as a visual artist or video tech easier. This is the first test version. I assume some basic knoledge of computers/windows and of node-red. There are plenty of tutorials online about the latter.,  If you do not know what a powershell is this is probably not (yet) for you.

**Instructions:**

For all users:
- Exctract the content of videotools.zip
- The folder videotools can be placed in the root folder (C:\) of the windows machine.
- To be able to use the scripts, run setupfirsttime as administrator.
- to restore settings run remove videotools and restore permissions as administrator

Only for node-red users, assumes you have nodered running (skip if you dont intend to use this)
- if you want to use the node-red patch
- open a browser and open 127.0.0.1:1880
- import node-red-videotools-patch_0.x.json- choose deploy, or install dependancies in manage palette

Non Node-Red:
- If you do not use node-red, or intent to, all scripts in te videotools folder can be run manually by dubbleclicking.


**Trouble shooting / verify instal:**

1.
The shortcut files in the videotools folder can be run without the node-red interface.To verify if the were copied properly with all the file attributes, right clik on a shortcut file, choose properties and check if the "run as administrator" attribute is enabled.

If not, do so for all shortcuts in the root folder.


2. 
To verify is a startup program is added, open  a file explorer window and navigate to:C:\ProgramData\Microsoft\Windows\Start Menu\Programs\StartUp

All shortcuts to startup programs will be placed here.

For example, after running arena7atboot.bat a shortcut link will appear here and after running arena7not.bat it should disapear.If you then run the script from the shortcut, a window message will pop up to ask for permission. As of writing, from this window it is easy to set security levels to the lowest to avoid this message. Be aware that there is a security risk when you do so. Dont do this on workstations!

These are those files:

setupfirsttimewindowsupdatestart.lnk
windowsupdatestop.lnk
vncserverstop.lnk
vncserverstart.lnk
recoverydisable.lnk
recoveryenable.lnk
remove videotools and restore permissions.lnk

the other files can just run without administrator privelidges


3.
To verify if the windows services stop/enable:

press windows-key + r (run)services.msc

find:

Windows Update Service
vncserver


4. 
verify recovery disable

To verify if the crash boot recovery is enabled or disabled:run powershell as an administratorbcdedit

findrecoveryenabled         NO (or yes if you reenable it)



**About the software and where to get it:**

This all asumes the folowing software is properly installed and setup, of course adjust to your own preferences!

**Resolume arena 6 & 7:**
https://resolume.com

Yes, the software to manage videos over multiple projectors and map the hell out of it!



**Qlight:**
https://www.qlcplus.org

We use Qlight to translate art-net to analog dmx. And of course for some basic light control.


**Real VNC Server:**
https://www.realvnc.com

To manage a remote computer over vnc, encrypted. Local and with a paid account also remotely.  


**Node-Red:**
https://nodered.org

Node-red is a great tool to create interactive installations without a lot of programming knoledge.  It is able to send and receive osc, artnet, mqtt and even pj-link to control projectors.Like the name, it is node-based. There are great tutorials online and a lot of example patches te work with.

**Windows 10:**
https://www.microsoft.com/en-gb/windows/

We use Windows 10 Home and all this is tested at Windows 10 pro as well. The day Resolume Arena will run on linux, we will move on. Until then, thank you Bill.

If you have questions or comments or tips, pleas only use the comments at github
