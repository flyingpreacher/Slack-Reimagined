####Font too small when you first login to Slackware? 

Here is what you do:

    # nano /etc/default/grub
  
Look for the line that says GRUB_CMDLINE_LINUX=""

Change it to GRUB_CMDLINE_LINUX="800x600" or whatever resolution you need.

    # grub-mkconfig -o /boot/grub/grub.cfg
    # reboot

Enjoy!!
