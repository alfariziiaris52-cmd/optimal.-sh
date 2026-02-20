#!/bin/bash

while true
do
clear
echo "================================="
echo "        🔥 OPTIMAL GAMES 🔥"
echo "================================="
echo "1. Boost FPS (Kill Background Apps)"
echo "2. Lite Mode (Reduce System Load)"
echo "3. Exit"
echo "================================="
read -p "Select option: " pilih

if [ "$pilih" = "1" ]; then
    echo "Boosting performance..."
    
    pkill -f com.facebook.katana 2>/dev/null
    pkill -f com.instagram.android 2>/dev/null
    pkill -f com.zhiliaoapp.musically 2>/dev/null
    pkill -f com.android.chrome 2>/dev/null
    
    echo "Background apps closed."
    sleep 2

elif [ "$pilih" = "2" ]; then
    echo "Reducing system load..."
    
    termux-wake-lock
    sync
    
    echo "Tips:"
    echo "- Set game graphics to LOW"
    echo "- Set FPS to 30/45"
    echo "- Turn off shadows"
    sleep 3

elif [ "$pilih" = "3" ]; then
    echo "Exiting..."
    exit

else
    echo "Invalid option!"
    sleep 1
fi

done
