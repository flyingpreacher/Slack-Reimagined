##Configuring Fonts
###*Install webcore-fonts from sbopkg*

This add Windows core fonts and helps the fonts inside Firefox look much better!

1. It took me a long time to install these fonts because I could not figure out how to make sbopkg.conf file accept my designation for SBo-git -current.
2. I realized that I had to put it into the /etc/sbopkg/sbopkg.conf because it was not working in the ~/.sbopkg.conf. ~~I cannot run sbopkg from my user account, so I have to login as root to do it. Even though I have added myself to the sudo group.~~ 

###*How to use sudo on Slackware*
Ok, here is an example of how you run sudo on Slackware. Enter your user's password after this command, NOT the ROOT PASSWORD:

```$ sudo su -c pkgtool```


