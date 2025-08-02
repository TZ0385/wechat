#  风险提示｜泛微 OA e-cology 前台SQL注入漏洞

[ 长亭安全应急响应中心 ](javascript:void\(0\);)

**长亭安全应急响应中心** ![]()

微信号 chaitin_cert

功能介绍 长亭安全应急响应中心致力于发布最新的漏洞风险提示与威胁情报，专注于网络安全领域的研究和解决方案。

____

___发表于_

收录于合集 #2023漏洞风险提示 16个

![](https://raw.githubusercontent.com/tuchuang9/tc1/refs/heads/main/public/20230714180257.png)

  

泛微e-cology是一款由泛微网络科技开发的协同管理平台，支持人力资源、财务、行政等多功能管理和移动办公。

  

近期，长亭科技监测到泛微官方发布了新补丁修复了一处SQL注入漏洞。

  

长亭应急团队经过分析后发现该漏洞类型为SQL注入，仍有较多公网系统仍未修复漏洞。长亭应急响应实验室根据漏洞原理编写了X-
POC远程检测工具和牧云本地检测工具，目前已向公众开放下载使用。

  

#

  
 **漏洞描述**  Description  
  
 **0** **1**

该漏洞是由于泛微e-cology未对用户的输入进行有效的过滤，直接将其拼接进了SQL查询语句中，导致系统出现SQL注入漏洞。

  

  
 **检测工具**  Detection  
  
 **0** **2**

#

#  ****

##  **X-POC远程检测工具**

###  检测方法：

  * 

    
    
    xpoc -r 400 -t 目标URL

###

  

![](https://raw.githubusercontent.com/tuchuang9/tc1/refs/heads/main/public/20230714180258.png)

  

工具获取方式：  

https://github.com/chaitin/xpoc

https://stack.chaitin.com/tool/detail?id=1036

##  **牧云本地检测工具**

###  检测方法：

在本地主机上执行以下命令即可无害化扫描：

  * 

    
    
    weaver_ecology_sqli_scanner_windows_amd64.exe

![](https://raw.githubusercontent.com/tuchuang9/tc1/refs/heads/main/public/20230714180259.png)

工具获取方式：

https://stack.chaitin.com/tool/detail?id=1194

  

  
 **影响范围**  Affects  
  
 **0** **3**

e-cology 9 部分版本

    
    
      
    

  
 **解决方案**  Solution  
  
 **0** **4**

##  **临时缓解方案**

限制访问来源地址，如非必要，不要将系统开放在互联网上。

##  **升级修复方案**

官方已发布升级补丁包，支持在线升级和离线补丁安装，可在参考链接[1] 进行下载使用。

  

  
 **产品支持**  Support  
  
 **0** **5**

 **云图** ：默认支持该产品的指纹识别，同时支持该漏洞的PoC原理检测。

 **洞鉴** ：预计 7 月 11 日发布引擎升级包，支持该漏洞的扫描。

 **雷池** ：已发布虚拟补丁，支持该漏洞利用行为检测。

 **全悉** ：已发布规则升级包，支持该漏洞利用行为的检测。

 **牧云** ：使用管理平台 23.05.001
及以上版本的用户可通过升级平台下载应急漏洞情报库升级包（EMERVULN-23.07.010）“漏洞应急”功能支持该漏洞的检测；其它管理平台版本暂不支持该漏洞检测。

  

  
 **时间线**  Timeline  
  
 **0** **6**

7月7日 长亭科技获取漏洞情报

7月10日 长亭应急响应实验室漏洞分析与复现

7月11日 长亭安全应急响应中心发布通告

  

参考资料：

[1] https://www.weaver.com.cn/cs/securityDownload.html?src=cn

  
  
  
 **长亭应急响应服务**  
  
  

全力进行产品升级

及时将风险提示预案发送给客户

检测业务是否收到此次漏洞影响

请联系长亭应急团队

7*24小时，守护您的安全

  

第一时间找到我们：

邮箱：support@chaitin.com

应急响应热线：4000-327-707

预览时标签不可点

微信扫一扫  
关注该公众号

[知道了](javascript:;)

微信扫一扫  
使用小程序

****

[取消](javascript:void\(0\);) [允许](javascript:void\(0\);)

****

[取消](javascript:void\(0\);) [允许](javascript:void\(0\);)

： ， 。   视频 小程序 赞 ，轻点两下取消赞 在看 ，轻点两下取消在看

