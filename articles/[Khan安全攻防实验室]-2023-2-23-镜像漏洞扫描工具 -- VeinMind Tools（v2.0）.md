#  镜像漏洞扫描工具 -- VeinMind Tools（v2.0）

[ Khan安全攻防实验室 ](javascript:void\(0\);)

**Khan安全攻防实验室** ![]()

微信号 KhanCJSH

功能介绍 安全不是一个人，我们来自五湖四海。研究方向Web内网渗透，免杀技术，红蓝攻防对抗，CTF。

____

___发表于_

收录于合集

以下文章来源于CT Stack 安全社区 ，作者问脉团队

![](http://wx.qlogo.cn/mmhead/Q3auHgzwzM6YjufPtB0QfHxZNtuaLtInJJrnYvxaTEeP9b99RYx6icA/0)
**CT Stack 安全社区** .

“守护安全工具成长” 秉持探索与共享的理念，收录更多优质工具。规范安全工具标准，与之共生共赢。

##

## ❗❗ **问脉团队结合 v2.0 核心亮点功能为大家准备了   **5 篇技术性文章  **以供大家理解学习，涉及: **「报告器
」、「命令行」、「漏洞扫描」、「逃逸风险检测」、「容器扫描」**
五大板块，文章会在本周内陆续与大家见面，文末扫码添加小助手加入用户交流群，不错过每一次干货分享噢 ❗❗**

## 1问脉 Tools v2.0

VeinMind Tools 是基于 VeinMind SDK 打造的一个容器安全工具集，目前已支持镜像恶意文件、后门、敏感信息、弱口令等扫描功能。此次
**更新的 v2.0  版本**，优化、增添了以下 **核心亮点功能** ：

  * 🔥 veinmind-asset 升级为 veinmind-vuln， **支持镜像/容器漏洞扫描**

  * 🎯 新增 veinmind-escalate 逃逸检测插件， **扫描容器/镜像中的逃逸风险**

  * 🧶 IaC 支持扫描  **kubernetes**  集群

  * 🏅 插件报告输出优化： **支持 cli/json/htm**

  * 🍄 runner cmd 优化：协议化扫描对象

  * 💫 runner 支持插件参数自定义

  * 🥳 runner 支持扫描 tar 类型镜像

  * 📑 script.sh => makefile

  * ...

  

🌟 GitHub 地址：https://github.com/chaitin/veinmind-tools 🌟  

## 2veinmind-vuln

veinmind-vuln 插件是由 veinmind-asset 插件升级而来，在资产信息扫描的基础上，对所有的资产信息进行了 cve
漏洞匹配。最大程度上发现并检测镜像应用漏洞信息。

  * 扫描镜像/容器的 OS 信息

  * 扫描镜像/容器内系统安装的 packages

  * 扫描镜像/容器内应用安装的 libraries

  * 扫描镜像/容器是否存在已知 cve (beta)

  * 支持 JSON/CLI/HTML 等多种报告格式输出

![](http://hk-proxy.gitwarp.com/https://raw.githubusercontent.com/tuchuang9/tc1/refs/heads/main/public/20230223091124.png)

![](http://hk-proxy.gitwarp.com/https://raw.githubusercontent.com/tuchuang9/tc1/refs/heads/main/public/20230223091125.png)

## 3veinmind-escalate

veinmind-escalate 插件支持对指定容器或镜像进行逃逸风险检测。

  * 快速扫描容器/镜像中的逃逸风险

  * 支持 docker/containerd 容器运行时

  * 支持 JSON/CLI/HTML 等多种报告格式输出

![](http://hk-proxy.gitwarp.com/https://raw.githubusercontent.com/tuchuang9/tc1/refs/heads/main/public/20230223091127.png)

![](http://hk-proxy.gitwarp.com/https://raw.githubusercontent.com/tuchuang9/tc1/refs/heads/main/public/20230223091128.png)

## 4IaC 支持扫描 Kubernetes 集群

veinmind-iac 用于扫描 IaC(Infrastructure as Code) 文件内的风险问题。

  * 支持 dockerfile/kubernetes IaC 类型文件

  * 支持指定目录自动递归扫描

  * 支持 JSON/CLI/HTML 等多种报告格式输出

  

![](http://hk-proxy.gitwarp.com/https://raw.githubusercontent.com/tuchuang9/tc1/refs/heads/main/public/20230223091129.png)

![](http://hk-proxy.gitwarp.com/https://raw.githubusercontent.com/tuchuang9/tc1/refs/heads/main/public/20230223091130.png)

## 5插件报告输出优化

  * 支持 JSON/CLI/HTML 等多种报告格式输出

## 6runner 优化

  * 自动扫描并注册当前目录下(含子目录)的插件

  * 统一运行基于不同语言实现的问脉插件

  * 插件可以和 runner 进行通信，如上报事件进行告警等

  

* * *

## VeinMind Tools

![](http://hk-proxy.gitwarp.com/https://raw.githubusercontent.com/tuchuang9/tc1/refs/heads/main/public/20230223091131.png)

  

##  **😎 扫码添加小助手加入用户交流群，不错过每一次干货分享噢  ❗❗**

![](http://hk-proxy.gitwarp.com/https://raw.githubusercontent.com/tuchuang9/tc1/refs/heads/main/public/20230223091134.png)

##  **👇 点击阅读原文使用 VeinMind  Tools**

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

