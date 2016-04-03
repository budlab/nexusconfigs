#HOWTO add configuration files to the repository

####clone the repository to your pc (only have to do once)
     
     git clone https://github.com/budlab/configs.git

####make the configuration changes you want on the Nexus switches
####copy the new running configuration to your pc

     copy running-config scp://username@yourpc/home/username/configs/N5548_A-running-config vrf default
     copy running-config scp://username@yourpc/home/username/configs/N5548_B-running-config vrf default

####check the status

     git status

####if the configutartion was modified then add the files

     git add N5548_A-running-config
     git add N5548_B-running-config

####commit the changes

     git commit -m "description of the changes you made"

####copy the configuration files to github

     git push https://username:password@github.com/budlab/configs.git

####if making changes but someone else made changes before
####pull the leatest files from github
####go to the configs directory (it is in the home directory in my case)

     cd configs
     git pull

####do the things described above
