# scanning.net

/bin/bash
Tested on Kali Linux / Parrot Os / Ubuntu/ Arco Linux / Archman 
Simple script for Install https://github.com/waild0/scanning.net
Colors
cyan='\e[0;36m'
green='\e[0;32m'
lightgreen='\e[1;32m'
white='\e[1;37m'
red='\e[1;31m'
yellow='\e[1;33m'
blue='\e[1;34m'
Options
path=`pwd` # Path
VeR="V3.6" # Version
Check root exist
[[ `id -u` -eq 0 ]] > /dev/null 2>&1 || { echo  $red "You must be root to run the script"; exit 1; }
echo -e $cyan ""
echo " ☠️
echo " ☠️
echo "  ☠️.                 ALID
echo ".  ☠️.             ☠️
echo ".   ☠️            ☠️
echo ".     ☠️.  ☠️.  ☠️
echo "         ☠️.  ☠️ 
echo -e $white "------------------------------"
echo -e $red "[ ✔ ] Installer The Tool [ ✔ ] "; 
echo -e $white "------------------------------"
echo -e $green "[ ! ] Moving scanning folder "
mkdir /usr/share/scanning
cp -r Dev /usr/share/scanning
cp install /usr/share/scanning 
cp update.py /usr/share/Scanning
cp -r modules /usr/share/Scanning
cp ScAnNiNg.py /usr/share/ScAnNiNg
echo -e $blue "[ ✔ ]Done"
echo -e $red "[*] Creating Icons Dirctory"
cp -r $path/sca/Scanning.desktop /usr/share/applications/scanning.desktop
cp -r $path/sca/Scanning.png /usr/share/icons/Scanning.png
echo -e $yellow "[*] Creating shortcut command $red scanning"
echo "#!/bin/sh" >> /usr/bin/Scanning  
echo "cd /usr/share/Scanning" >> /usr/bin/Scanning 
echo "exec python2 Scanning.py \"\$@\"" >> /usr/bin/Scanning  
chmod +x /usr/bin/scanning 
echo -e $white "------------------------------------------------------------------------"
echo -e $red "[ ✔ ] scanning Is Installed In Application (information gathering) [ ✔ ]"
echo -e $white "------------------------------------------------------------------------"
echo -e $green"╔────────────────────────────╗ "
echo -e $blue "|Run in Terminal<(SCANNING)> |  "
echo -e $green"╚────────────────────────────╝ "
exit
