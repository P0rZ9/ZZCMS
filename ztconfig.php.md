

user/ztconfig.php

Vulnerability：
[]

There is unlink($f) to delete any file by controlling the value of $f

Control $f：
$oldbannerbg=isset($_POST["oldimg"])?$_POST["oldimg"]:'';


Delete install/install.lock:
6.jpg


delete install/install.lock successfully
7.jpg

