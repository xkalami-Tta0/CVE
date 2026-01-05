# Online Music Site In PHP  Administrator/PHP/AdminViewSongs.php SQL injection

## NAME OF AFFECTED PRODUCT(S)

Online Music Site

## Vendor Homepage

https://code-projects.org/online-music-site-in-php-with-source-code/

## Vulnerable File

Administrator/PHP/AdminViewSongs.php

## VERSION(S)

v1.0

## Vulnerability Type

SQL injection

## DESCRIPTION

The Online Music Site project has a SQL injection vulnerability in the Administrator/PHP/AdminViewSongs.php file when the user is not logged in on the frontend. An attacker can exploit this vulnerability to obtain sensitive information

## Vulnerability details and POC

There are no restrictions or filters for the parameter id

![image-20260105202749961](https://github.com/xkalami-Tta0/picx-images-hosting/raw/master/Online-Music-Site/image-20260105202749961.32ig2doouy.webp)

![image-20260105202901133](https://github.com/xkalami-Tta0/picx-images-hosting/raw/master/Online-Music-Site/image-20260105202901133.465yvgfdk.webp)

data packet：

GET /mis/Administrator/PHP/AdminViewSongs.php?id=95 HTTP/1.1
Host: localhost
sec-ch-ua: "Not_A Brand";v="99", "Chromium";v="142"
sec-ch-ua-mobile: ?0
sec-ch-ua-platform: "Windows"
Accept-Language: zh-CN,zh;q=0.9
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/142.0.0.0 Safari/537.36
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.7
Sec-Fetch-Site: same-origin
Sec-Fetch-Mode: navigate
Sec-Fetch-User: ?1
Sec-Fetch-Dest: document
Referer: http://localhost/mis/Administrator/PHP/AdminViewAlbums.php
Accept-Encoding: gzip, deflate, br
Cookie: PHPSESSID=131ljj8el3r53ldv370bbg1rk7
Connection: keep-alive

![image-20260105202959864](https://github.com/xkalami-Tta0/picx-images-hosting/raw/master/Online-Music-Site/image-20260105202959864.4ubexa81qu.webp)
