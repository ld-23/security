# Password Cracking



Create Hash without hyphen

* echo -n "Mask101" \| md5sum \| tr -d " -" &gt; hash

  
 Hashcat Mask Brute Force:

* hashcat -m 0 -a 3 hash SKY-QQTY-?d?d?d?d --force
* Try Hashlist against Wordlist:
* hashcat -a 0 -m 500 -o cracked.txt hash /root/wordlists/metasploit/password.lst --force

  
 John the Ripper:

* john --wordlist=/root/wordlists/rockyou.txt 1.txt

