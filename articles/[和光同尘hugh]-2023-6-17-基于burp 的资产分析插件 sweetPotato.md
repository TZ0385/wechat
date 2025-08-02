#  基于burp 的资产分析插件 sweetPotato

原创 Hugh  [ 和光同尘hugh ](javascript:void\(0\);)

**和光同尘hugh** ![]()

微信号 hughone1

功能介绍 分享技术，分享生活

____

___发表于_

收录于合集 #网络安全 3个

  * 好久没有更新了，分享一个好用的burp插件吧

  * 在使用HAE插件时经常会因为数据包过大而导致Burp suite 卡死，因此找到了一款

  * Hae 的平替版本 sweetPotato----插件地址：https://github.com/z2p/sweetPotato

 **免责声明**

该工具仅用于安全自查检测  
由于传播、利用此工具所提供的信息而造成的任何直接或者间接的后果及损失，均由使用者本人负责，作者不为此承担任何责任。  
本人拥有对此工具的修改和解释权。未经网络安全部门及相关部门允许，不得善自使用本工具进行任何攻击活动，不得以任何方式将其用于商业目的。

  

#  **插件简介**

平时积累的一些攻防经验想做成自动化去提升在公司项目以及外部SRC效果，故闲暇时间开发了这款基于burpsuite的工具。  
过去在内部使用效果也还可以，现在工作原因不再参与红队类的业务了，将其开源供大家学习分享，过程中大家有发现任何问题和需求，欢迎提交，我会在空余时间进行优化。  
主要集合了以下几个类别的功能：

  * 资产收集管理的概念，用户可设置域名，插件会随着被动流量进行分析，提取属于目标的域名资产，并会对资产递归访问，快速发现更多业务

  * 被动检测能力：基于代理过去的流量进行分析，尝试提取可疑脆弱点（插件不会发包）

  * 主动检测能力：基于代理过去的流量，然后进行二次加工（插件会额外发包）

  * 提供全局配置管理的界面，可选择对流量以及上述（2）（3）的功能进行配置

  * 当然还提供一些蛮多细小功能，就供大家琢磨了

#  **功能演示**

核心只演示资产收集管理的功能，其他功能大家可以慢慢体验

https://github.com/z2p/sweetPotato/blob/main/picture/show.gif

![](http://hk-proxy.gitwarp.com/https://raw.githubusercontent.com/tuchuang9/tc1/refs/heads/main/public/20230617223234.png)

  

 **使用心得**  

该插件的核心是它的json规则，对于使用用户而言，具有充分的可自定义空间  

https://github.com/z2p/sweetPotato/blob/main/resources/finger.json

![](http://hk-proxy.gitwarp.com/https://raw.githubusercontent.com/tuchuang9/tc1/refs/heads/main/public/20230617223249.png)

  

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

