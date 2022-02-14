# protontool
A script that facilitates running executables in a Proton wineprefix.
It takes care of selecting the correct Proton version, compatdata and WINEPREFIX.

This script shouldn't require you to install any dependencies on GNU/Linux systems.

ATTENTION: Use at your own risk. I am not responsible for broken Proton prefixes, games or apps ceasing to work properly, etc.

## Usage
       
       protontool [-ht] appid <proton args>
       
       options:
         -h   show this help text
         -t   treat appid as the name of the app's install directory

       
Arguments are passed to `proton`, so run an executable as demonstrated:
       
       # Fallout 4's appid is "377160"
       $ ./protontool 377160 run ModOrganizer.exe
       
       # Use -t to look up appid automatically. Here "Fallout 4" is the name of the game's install directory under steamapps/common/.
       $ ./protontool -t "Fallout 4" waitforexitandrun ModOrganizer.exe
