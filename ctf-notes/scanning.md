# Recon and Scanning

## STEALTH

tor - proxychains firefox www.whatismyip.com

## RECONNAISSANCE AND ROUTE MAPPING

whois - \#whois example.com  
 dmitry - \#dmitry -winsepo output.txt example.com  
 recon-ng - follow up with a tutorial

 {many dns specific tools}

 traceroute  
 hping3 - hping3 -S www.google.com -p 80 -c 3  
 intrace  
 trace6

## ENUMERATION 

scanme.nmap.org

initial scan -- nmap -sC -sV -oA nmap &lt;ip&gt;

 alive6  
 detect-new-ip6  
 dnmap  
 xprobe2 www.example.com  
 nmap - nmap -sS -O target.com  
 fping  
 hping2  
 hping3  
 nping

###  internal network

 snmpwalk  
 metasploit snmpenum  
 -SMB sessions  
 nmap --script smb-enum-users.nse -p445 &lt; host &gt;  
 msf - auxiliary/scanner/smb/smb\_enumusers

 smbclient -I TargetIP -L administrator -N -U ""  
 enum4linux \[options\] target-ip  
 rpcclient -U "Vagrant" 192.168.0.129

 sparta

 hydra -l {usrname} -P /usr/share/wordlists/rockyou.txt ssh://10.13.37.244:22

## VULNERABILITY SCANNING

nmap --script-updatedb  
 openvas

 wpscan - wordpress

