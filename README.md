# LinuxSetup
Place for my Linux scripts and files

The names will generally give you a good clue as to where they go...
If you want to use these, awesome.

You should know what everything does before using any of these files.
These things may harm your systems.
USE AT YOUR OWN RISK! I take no responsibility if these things break anything.
Except if they break the entire universe. Because that's god level, and I'll claim that.


## Create 01-aesix
This file must be in "/etc/update-motd.d/" must be executable, and must be the only executable script running on ssh login for aesthetic purposes.  Additional work will be needed to make it work with multiple IPs.  I only have 1 WAN routable IP (1 each, v4 and v6) and as such, this script works perfectly fine for my needs.

This script requires an additional file to be located at "~/ssh-motd" for which the user can alter.  
Alternatively, the ssh-motd file can be hosted in a non-user area, the script re-directed to it.  
This file is used by me for the welcome section.  If using a global file, the $USERNAME variable and scripts can be commented out.

## ssh-motd
This is a simple text file, with no scripting support.  It is read by 01-aesix to fill the welcome section.  This has been added as a user file so the user can use it as a reminder section, or to leave a note for other persons with account access.  This can be hosted in a non-user global area, with minor changes to the 01-aesix script, to disallow user changes.  This goes against the spirit, however :)
