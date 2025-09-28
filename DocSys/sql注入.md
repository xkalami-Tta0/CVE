# Vulnerability Introduction

The /Manage/getUserList.do interface of DocSystem has a SQL injection vulnerability.，Attackers can obtain sensitive database information or take over database or even server permissions through this sql injection vulnerability

# Vulnerability analysis

Vulnerable class file：src/com/DocSystem/mapping/UserMapper.xml

![image-20250929001437676](https://github.com/xkalami-Tta0/picx-images-hosting/raw/master/DocSys/image-20250929001437676.6bhg1solcj.webp)

follow up queryUserWithParamLike

![image-20250929001542555](https://github.com/xkalami-Tta0/picx-images-hosting/raw/master/DocSys/image-20250929001542555.9kgjygc2z6.webp)

follow up getUserListWithParamLike

![image-20250929001553249](https://github.com/xkalami-Tta0/picx-images-hosting/raw/master/DocSys/image-20250929001553249.8z6wc5hmoh.webp)

follow up getUserListOnPage

![image-20250929001620374](https://github.com/xkalami-Tta0/picx-images-hosting/raw/master/DocSys/image-20250929001620374.3k8dtq2hao.webp)

follow up getUserList，The corresponding route for the access is /Manage/getUserList.do, and the corresponding parameters are userName, pageIndex, and pageSize.

![image-20250929001640013](https://github.com/xkalami-Tta0/picx-images-hosting/raw/master/DocSys/image-20250929001640013.1zimu959u7.webp)

# Vulnerability reproduction

Constructing a data packet, userName has SQL injection

![image-20250929001953081](https://github.com/xkalami-Tta0/picx-images-hosting/raw/master/DocSys/image-20250929001953081.6bhg1solcd.webp)

python sqlmap.py -r 1.txt -p userName --batch

![image.png](https://github.com/xkalami-Tta0/picx-images-hosting/raw/master/DocSys/1759053751956-422b5931-f973-4425-a971-b6840c609db7.54y4t71v9l.webp)
