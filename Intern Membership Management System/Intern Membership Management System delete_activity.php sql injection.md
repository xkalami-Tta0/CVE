#  Intern Membership Management System delete_activity.php sql injection

## NAME OF AFFECTED PRODUCT(S)

Intern Membership Management System

## Vendor Homepage

https://code-projects.org/intern-membership-management-system-in-php-with-source-code/

## Vulnerable File

delete_activity.php

## VERSION(S)

v1.0

## Vulnerability Type

SQL injection

## DESCRIPTION

There is a SQL injection vulnerability in the delete_activity.php file of the Intern Membership Management System project, which can be exploited by attackers to obtain sensitive data information

## Vulnerability details and POC

![image-20260107010530152](https://github.com/xkalami-Tta0/picx-images-hosting/raw/master/Intern-Membership-Management-System/image-20260107010530152.6ikrw6jam2.webp)

![image-20260107010544541](https://github.com/xkalami-Tta0/picx-images-hosting/raw/master/Intern-Membership-Management-System/image-20260107010544541.41yjh9cepp.webp)

Data packet：

```
GET /intern/admin/delete_activity.php?activity_id=50 HTTP/1.1
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

![image-20260107012808462](https://github.com/xkalami-Tta0/picx-images-hosting/raw/master/Intern-Membership-Management-System/image-20260107012808462.45i5ez5zrx.webp)
