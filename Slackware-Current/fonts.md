##Configuring Fonts
###*Install webcore-fonts from sbopkg*

This add Windows core fonts and helps the fonts inside Firefox look much better!

1. It took me a long time to install these fonts because I could not figure out how to make sbopkg.conf file accept my designation for SBo-git -current.
2. I realized that I had to put it into the /etc/sbopkg/sbopkg.conf because it was not working in the ~/.sbopkg.conf. ~~I cannot run sbopkg from my user account, so I have to login as root to do it. Even though I have added myself to the sudo group.~~ 
3. 
Here is exactly what I had to do:

edit the file /etc/sbopkg/repos.d/40-sbo.repo adding, on top of the other entries, another one like this
Code:

SBo 14.1 "SBo repository for Slackware 14.1" _SBo rsync slackbuilds.org::slackbuilds/14.1 GPG

then edit /etc/sbopkg/sbopkg.conf setting the variables REPO_BRANCH and REPO_NAME like this
Code:

REPO_BRANCH=${REPO_BRANCH:-14.1}
REPO_NAME=${REPO_NAME:-SBo}

sync
Code:

sbopkg -r

and you should be ready to go.

(notice that a /root/.sbopkg.conf file, if exists, will override the options in /etc/sbopkg/sbopkg.conf)



###*Create mkinitrd for generic kernel*
As root, run this command:

        # /usr/share/mkinitrd/mkinitrd_command_generator.sh
      
Enter the results in the terminal to create your new mkinitrd for your updated kernel, etc.<br>
Done!
