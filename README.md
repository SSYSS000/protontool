# protontool
A script that facilitates running executables and doing other stuff in a proton wineprefix.
It takes care of selecting the correct Proton version, compatdata and WINEPREFIX.

This script shouldn't require you to install any dependencies on GNU/Linux systems.

## Usage
       
       protontool [-ht] appid <proton args>
       
       options:
         -h   show this help text
         -t   treat appid as app name

       
Arguments are passed to `proton`, so run an executable as demonstrated:
       
       # Fallout 4's appid is "377160"
       $ ./protontool 377160 run ModOrganizer.exe
       
       # Use -t to look up appid automatically
       $ ./protontool -t "Fallout 4" waitforexitandrun ModOrganizer.exe
