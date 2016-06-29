####*Create mkinitrd for generic kernel*
As root, run this command:

        # /usr/share/mkinitrd/mkinitrd_command_generator.sh
      
Enter the results in the terminal to create your new mkinitrd for your updated kernel, etc.<br>
Done!

####Create a User Account

The first thing you will need to do is create your own non-root user account. There are two ways you can do this, both from the console. The recommended way is to use Slackware's own interactive adduser script, thus:

    # adduser

and follow the prompts. Read the user management page for more detail on the adduser script. You can use the non-interactive standard Linux program useradd too:

    # useradd -m -g users -G wheel,floppy,audio,video,cdrom,plugdev,power,netdev,lp,scanner -s /bin/bash <your user name>
    
<b>Change slackpkg mirror to http://dfw.mirror.rackspace.com/slackware/</b>

