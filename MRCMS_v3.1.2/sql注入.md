The /admin/article/delete interface of MRCMS version 3.1.2 has an sql injection vulnerability. Attackers can obtain sensitive database information or take over database or even server permissions through this sql injection vulnerability

## Vulnerability Analysis 

class file path：src/main/java/org/marker/mushroom/dao/DaoEngine.java

The sql statement found here has not undergone precompilation operations

![image-20250924005342380](https://github.com/xkalami-Tta0/picx-images-hosting/raw/master/MRCMS/image-20250924005342380.6pnvljzjhv.webp)

Follow up and call the function delete(), passing parameters through the rid parameter

![image-20250924005511601](https://github.com/xkalami-Tta0/picx-images-hosting/raw/master/MRCMS/image-20250924005511601.7snkwfvddg.webp)

Find the calling route and concatenate it to obtain the route /admin/article/delete

class file path：src/main/java/org/marker/mushroom/controller/ArticleController.java

![image-20250924005723348](https://github.com/xkalami-Tta0/picx-images-hosting/raw/master/MRCMS/image-20250924005723348.4jogzs7vqt.webp)

## Vulnerability reproduction

Construct poc![image.png](https://github.com/xkalami-Tta0/picx-images-hosting/raw/master/MRCMS/1756657489510-8e7c34ef-0573-47c5-b724-d0f3250b1369.461uiwygx.webp)

![image.png](https://github.com/xkalami-Tta0/picx-images-hosting/raw/master/MRCMS/1756657522144-1cf30a1e-8bc5-4a71-8aba-9a19542686ce.7lkd10aow2.webp)
