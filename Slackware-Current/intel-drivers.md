To enable Intel Graphics when removing NVIDIA drivers, create a file named <b>10-intel.conf</b> and include the following:

	Section "Device"
   		Identifier  "Intel Graphics"
   		Driver      "intel"
	EndSection
	
Put this file in <b>/usr/share/X11/xorg.conf.d/</b>

Reboot and Enjoy!

:sunglasses:
