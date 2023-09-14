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
