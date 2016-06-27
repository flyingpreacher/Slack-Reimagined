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

