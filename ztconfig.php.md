

user/ztconfig.php


Vulnerability：
![image](https://github.com/P0rZ9/ZZCMS/blob/master/5.jpg)

There is unlink($f) to delete any file by controlling the value of $f

Control $f：
$oldbannerbg=isset($_POST["oldimg"])?$_POST["oldimg"]:'';


Delete install/install.lock:
![image](https://github.com/P0rZ9/ZZCMS/blob/master/6.jpg)


delete install/install.lock successfully
![image](https://github.com/P0rZ9/ZZCMS/blob/master/7.jpg)

