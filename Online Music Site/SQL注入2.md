# Online Music Site In PHP login.php SQL injection

## NAME OF AFFECTED PRODUCT(S)

Online Music Site

## Vendor Homepage

https://code-projects.org/online-music-site-in-php-with-source-code/

## Vulnerable File

login.php

## VERSION(S)

v1.0

## Vulnerability Type

SQL injection

## DESCRIPTION

The Online Music Site project has a SQL injection vulnerability in the login.php file when the user is not logged in on the frontend. An attacker can exploit this vulnerability to obtain sensitive information

## Vulnerability details and POC

There are no restrictions or filters on the parameters username and password

![image-20260105201223139](https://github.com/xkalami-Tta0/picx-images-hosting/raw/master/Online-Music-Site/image-20260105201223139.3ns3oohdum.webp)

![image-20260105201405101](https://github.com/xkalami-Tta0/picx-images-hosting/raw/master/Online-Music-Site/image-20260105201405101.9kgnvoxwt9.webp)

data packet：

POST /mis/login.php HTTP/1.1
Host: localhost
Content-Length: 28
Cache-Control: max-age=0
sec-ch-ua: "Not_A Brand";v="99", "Chromium";v="142"
sec-ch-ua-mobile: ?0
sec-ch-ua-platform: "Windows"
Accept-Language: zh-CN,zh;q=0.9
Origin: http://localhost
Content-Type: application/x-www-form-urlencoded
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/142.0.0.0 Safari/537.36
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.7
Sec-Fetch-Site: same-origin
Sec-Fetch-Mode: navigate
Sec-Fetch-User: ?1
Sec-Fetch-Dest: document
Referer: http://localhost/mis/loginpage.php
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

username=harry&password=pass

![image-20260105201434073](https://github.com/xkalami-Tta0/picx-images-hosting/raw/master/Online-Music-Site/image-20260105201434073.3yexhtwlzw.webp)

![image-20260105201535235](https://github.com/xkalami-Tta0/picx-images-hosting/raw/master/Online-Music-Site/image-20260105201535235.4ubexa6afv.webp)
