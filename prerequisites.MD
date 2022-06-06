#prerequisites

**Before you begin!**

You will need a properly configured computer running Microsoft Windows 10 home or pro.
Our Server was configured with just login and password, not a microsoft account. 
(this can be done by install windows without network connections)

It can be handy to have windows autologin enabled.

HKEY_LOCAL_MACHINE \ SOFTWARE \ Microsoft \ Windows NT \ CurrentVersion
Windows+R key, regedit

set (or add values)
DefaultUserName
to Yourusername

DefaultPassword
to your password

AutoAdminLogon
to 1

Also node-red running at boot is recomended.
See https://nodered.org/docs/getting-started/windows for instructions.

In node-red make sure at least the following flows installed through manage my palette:

node-red-dashboard
https://flows.nodered.org/node/node-red-dashboard


Later on I will also use:

node-red-contrib-osc
https://flows.nodered.org/node/node-red-contrib-osc

node-red-contrib-pjlink
https://flows.nodered.org/node/node-red-contrib-pjlink

node-red-contrib-artnet-node
https://flows.nodered.org/node/node-red-contrib-artnet-node
