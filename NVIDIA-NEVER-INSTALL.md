##Never Install NVIDIA drivers on Slackware. Why?

They are TOO HARD TO REMOVE and properly RESTORE your Intel/Other drivers.

Here is what I had to do to remove NVIDIA <b>installed via sbopkg</b>:

    # nvidia-switch --remove
    # sbopkg 
    
This opens the ncurses dialog menu where you can remove "nvidia-kernel" and "nvidia-driver". 

You can remove vdpau if you like, but I just kept it. 

Finally, I had to remove and reinstall mesa:

    # slackpkg remove mesa
    # slackpkg install mesa
    
NOTE: When you remove NVIDIA drivers <i>/usr/lib64/libEGL.so.1</i> is removed. You cannot 'startx' to get into your desktop environment without it, so you have to reinstall mesa to get it back.


