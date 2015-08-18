# NXOS_Reloadin
reload in command for NXOS.  Used to schedule reloads 

# Written by Ryan Tischer @ Cisco -  @ryantischer
# Designed to run on Nexus 9000 swtich
# script replicates IOS "reload in" command to schedule reloads
# leverages scheduler feature in NXOS

#Usage - 

#copy/save script in bootflash/scripts folder on swtich
#from NXOS CLI type "source reloadin.py [options]
#options...
#	- number of minutes until reload
#	- "save" to save configuration before reload.  Must be used as second option behine minutes
#	- "cancel" cancel reload
#Examples
# source reloadin.py 20 - schedules a reload in 20 minutes
# source reloadin.py 20 save - schedules a reload in 20 minutes and saves the config
# source reloadin.py cancel - cancels current reloadin command.  

# Possiable issue - 
# I have no idea what will happen with a day change...for example if the current time is 11:55 and 
# the reloadin.py 20 is issued.  It could work, it could break, it could form a blackhole.
