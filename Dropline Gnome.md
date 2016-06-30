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
Look for the line in that file which says:

    # en_US is the Slackware default locale:
    export LANG=en_US

and change the value to your own language. 

And if I also wanted to make the computer support Unicode text, I would change it to

    # en_US is the Slackware default locale:
    export LANG=en_US.UTF-8
    
<b>Enabling Unicode is what made it work for me. I rebooted, installed gnome-terminal and it worked!!</b><br>

Run stty with "-a" option to make sure you are setup for Unicode properly:

    # stty -a

If you see “-iutf8” among the results, the current virtual console is not configured for UTF-8, otherwise if you see “iutf8” (without minus sign), the vc is properly configured. 

