Here is the location of the most recent files for Dropline Gnome:<br>
http://www.droplinegnome.org/files/3.20/testing/x86-64/

~~Download the latest PackageKit-1.1.1-x86_64-1dl.txz (as of 4-22-16), and run these commands as ROOT:~~

The following commands DO NOT WORK FULLY!<br> 
<b>PackageKit does not download the files properly and you will not be able to login to your Slackware Installation.</b><br>
Download all the packages manually with WGET, and use the following commands instead:

    $ wget -r -np -nH --cut-dirs=3 -R index.html http://droplinegnome.org/files/3.20/testing/x86-64/
    
    
    DO NOT USE THESE COMMANDS************************
    # installpkg PackageKit-1.1.1-x86_64-1dl.txz 
    # pkcon refresh force
    # pkcon install dropline
    DO NOT USE THESE COMMANDS************************


####Gnome Terminal 
If it is not working correctly, and gives you this error:

    Error constructing proxy for org.gnome.Terminal:/org/gnome/Terminal/Factory0: Error calling StartServiceByName for org.gnome.Terminal: GDBus.Error:org.freedesktop.DBus.Error.Spawn.ChildExited: Process org.gnome.Terminal exited with status 8

go to /etc/profile.d/lang.sh<br>
UNCOMMENT the line in that file which says:

    export LANG=en_US.UTF-8

This enables Unicode text and allows gnome-terminal to operate properly.

REBOOT!

<b>Enabling Unicode is what made it work for me.</b><br>

Also, run stty with "-a" option:

    # stty -a

If you see “-iutf8” among the results, the current virtual console is not configured for UTF-8, <b>otherwise if you see “iutf8” (without minus sign), the vc is properly configured. </b> 

