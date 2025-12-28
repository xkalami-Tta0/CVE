# Vulnerability Introduction（漏洞简介）

The /Manage/getGroupAllUsers.do interface of DocSystemV2.02.36 has a SQL injection vulnerability.，Attackers can obtain sensitive database information or take over database or even server permissions through this sql injection vulnerability（DocSystemV2.02.36的/Manage/getGroupAllUsers.do接口存在SQL注入漏洞。攻击者可以通过此SQL注入漏洞获取敏感的数据库信息，或接管数据库甚至服务器权限）

supplier:https://github.com/RainyGao-GitHub/DocSys/releases/tag/DocSys_V2.02.36

Vulnerability file:src/com/DocSystem/mapping/GroupMemberMapper.xml

# Vulnerability analysis and reproduction（漏洞分析复现）

code analysis

![image-20251228165007155](https://github.com/xkalami-Tta0/picx-images-hosting/raw/master/DocSys/image-20251228165007155.2vf7va607y.webp)

![image-20251228165025889](https://github.com/xkalami-Tta0/picx-images-hosting/raw/master/DocSys/image-20251228165025889.3d59jv7dss.webp)

poc

![image-20251228165050023](https://github.com/xkalami-Tta0/picx-images-hosting/raw/master/DocSys/image-20251228165050023.5trhyse9p6.webp)

![image-20251228165110785](https://github.com/xkalami-Tta0/picx-images-hosting/raw/master/DocSys/image-20251228165110785.13m90dmnbt.webp)

python sqlmap.py -r 1.txt -p searchWord --batch --level 3 --risk 3

![image-20251228165121141](https://github.com/xkalami-Tta0/picx-images-hosting/raw/master/DocSys/image-20251228165121141.5q7w12l6zc.webp)
