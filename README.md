# BuildScript3
Build Script 3 for Kura Labs

#!/bin/bash

while true; do 

    echo "1. System Info Menu"

    echo "2. Your shell directory"

    echo "3. Home Directory"

    echo "4. Operating System name & Version"

    echo "5. Print Current Working Directory"

    echo "6. Number # of users logged in"

    echo "7. Hard disk information"

    echo "8. CPU Information"

    echo "9. Memory Information"

    echo "10. File System Information"

    echo "11. Currently running processes"

    echo "0. Exit Bash Script"

    read -p "Select a number to enter your choice: " choice

case $choice in
        0) echo "Exiting shell script"
                break;;
1) USER=$(whoami)
                echo "The user currently logged in is: $USER"
                ;;
        2) SHELL_DIRECTORY="$SHELL"
                echo "This shell directory is: $SHELL_DIRECTORY"
                ;;
        3) HOME="$HOME"
                echo "Home directory of this device is: $home"
                ;;
        4) Operating_System=$(uname)
           Operating_System_Version=$(uname -r)
                echo "The OS & OS Version is: $Operating_System, $Operating_System_Version"
                ;;
        5) current_work_dir=$(pwd)
                echo "The current work directory is: $current_work_dir"
                ;;
        6) user=$(w)
                echo "The users that are logged into this device are: $user"
                ;;
    7) Disk_Information=$(df -H)
                echo "HardDisk information is: $Disk_Information"
                ;;
        8) CPU_Information =$(cat /proc/cpuinfo)
                echo "CPU info is: $CPU_Information"
                ;;
        9) Memory_Used=$(free -m)
                echo "Memory used on this device is: $Memory_Used"
                ;;
        10) File_Sys_Info=$(df -T)
                echo "The file system information type on this directory is: #File_Sys_Info"
                ;;
        11) Processes_Running=$(ps aux)
                echo "The current proccess that are running on this device are: $Processes_Running"
                ;;
        *) echo "ERROR: Please input the appropriate number from 1-10, or press 0 to exit"
                ;;
        esac
done


#issues with bash script: #s 3, 8, and 10 do not work properly.
