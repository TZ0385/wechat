#  打破技术壁垒！数据安全运营与ChatGPT联动的初探

[ NOVASEC ](javascript:void\(0\);)

**NOVASEC** ![]()

微信号 NOVA_SEC

功能介绍 NOVA SEC 新星安全 萌新启蒙之路 愿大家都能成为最闪耀的星。

____

___发表于_

收录于合集

以下文章来源于A9 Team ，作者Zer0n1

![](http://wx.qlogo.cn/mmhead/Q3auHgzwzM4SFGux5JpJuWNMAeDzm5rGZ9W56glZ9VMlmeA9Hnea9Q/0)
**A9 Team** .

A9 Team
是一个虚拟安全团队，成员来自安信、青藤、观星、梆梆、微步、安全狗等公司。成员能力涉及安全建设、安全运营、安全攻防等领域，致力于持续分享信息安全工作中的思考和实践，期望和朋友们共同进步，守望相助，合作共赢。

  

  

  

  

**点击蓝字 关注我们**

 **”**

 **免责声明**  

 **本文章只用于技术交流，若使用本文章提供的技术信息进行非法操作，后果均由使用者本人负责。**

![](http://hk-proxy.gitwarp.com/https://raw.githubusercontent.com/tuchuang9/tc1/refs/heads/main/public/20230225215640.png)

 **前言**  

    近期国内互联网圈好热闹呀，原因是因为漂亮国OpenAI在2022年11月30日研发了一款聊天机器人程序—ChatGpt，这款机器人知无不言言无不尽，上线2个月活跃用户破亿，直接引爆互联网圈，在全球创下来互联网历史上用户增长最快的应用程序。

  

    ChatGPT的最大亮点在于模拟人类思维方式和对话逻辑的一个应用程序，并不像传统的“人工智障”，遇到不懂的问题来个不知道或者答非所答。ChatGPT在对话的过程中会关联使用者的对话，既上下文理解，实现连续对话，产生的相应的智能回答。

  

    互联网圈们在狂欢ChatGpt的到来，狂呼着人工智能成为新的转折点时，此时有一大波“信息泄露”也在悄然无声地向我们袭来，通讯软件Telegram多频道大面积转发某隐私查询机器人链接，网传该机器人泄露了国内数十亿条个人信息，以快递信息为主。这一消息在迅速在微博等平台引发热议，成为这几日里的两大焦点。



![](http://hk-proxy.gitwarp.com/https://raw.githubusercontent.com/tuchuang9/tc1/refs/heads/main/public/20230225215642.png)

  

    数据的安全成为人们的担忧，口中热议的对象，而作为一个数据数据安全运营人员，在担心自己数据泄露的同时，也在思考运营的过程中关于数据安全的问题。如何保障公司的数据安全，如何通过技术方面检测在数据泄露的场景中是否还有未知场景我们没有发现的？数据常泄露的点有哪些？数据泄露是被动的，还是主动的？能否检测数据泄露在发生前，运营人员及时将风险扼杀摇篮中，降低数据安全泄露的风险隐患。

  

    因在ChatGPT上体验了一段时间，感受到ChatGPT的“博学多才”，想象ChatGPT是否可以在我运营工作中做一个“安全顾问”，将数据安全运营时所需的技术与ChatGPT进行联动，看看是否能擦出一丝火花，填补一下我的专业知识领域中的一些空白技术

  

![](http://hk-proxy.gitwarp.com/https://raw.githubusercontent.com/tuchuang9/tc1/refs/heads/main/public/20230225215643.png)

    本文仅讨论数据安全运营的技术问题，作者仅是一个数据安全的运营人员，所学的知识仅仅是运营知识和技术，关于数据安全的体系框架还是一个新手村的菜鸟，难登大雅之堂，就不班门弄斧了，只分享一下作者在日常运营上技术方面跟ChatGPT联动，再畅想一下未来的人工智能，各位看官乐呵乐呵，如有错误，欢迎各位看官指正。

  

    使用过数据安全设备的同学都应该知道，数据安全常见设备主要由邮件防泄漏、终端数据防泄漏、数据库审计、应用数据防泄漏等热门产品，都是为了防止数据泄露而产生的，原理基本都是通过正则表达式去识别数据，进而对数据进行分级分类，梳理内部资产。

  

![](http://hk-proxy.gitwarp.com/https://raw.githubusercontent.com/tuchuang9/tc1/refs/heads/main/public/20230225215645.png)

    对于各种信息的正则表达式，每家的安全设备都有各自的默认规则，在应对公司不一样的场景中，有的规则无法识别或者是识别精确率有待提高，运营人员在运营的过程中需要优化规则，在修改的过程中又可能因缺乏技术、不了解具体正则表达原理，出现优化完后还存在需要提高精确率的问题，在网上寻找修改大同小异，很难去进一步优化。

  

    例如在运营过程中优化个人信息类的手机号码，要清楚了解移动、联通、电信三大运营商的开头前3位有多少个组合，内容里的手机号码前面或后面存在逗号等其他干扰字符串能否识别，是否精准识别手机号码，出现长度12位以上无序数字是否也会识别成手机号码的误报，是否存在虚拟手机号码等场景。

  

    在优化的过程中不断测试不同场景，提高识别率，精确数据的资产，这个过程非常漫长，除了需要对正则表达式很熟悉之外，还要对场景可能会出现的问题要非常熟悉。在ChatGPT还未出现时，这些问题存在不少困扰，但ChatGPT的出现降低了我们的难题。

![](http://hk-proxy.gitwarp.com/https://raw.githubusercontent.com/tuchuang9/tc1/refs/heads/main/public/20230225215647.png)

  

    正如上述所说，ChatGPT可以通过上下文理解实现连续对话，与ChatGP不断对话，不断测试需求，不断去识别场景，还是以优化手机号为例：  

  

![](http://hk-proxy.gitwarp.com/https://raw.githubusercontent.com/tuchuang9/tc1/refs/heads/main/public/20230225215648.png)

ChatGPT提供的正则表达：

^1(3\d|4[5-9]|5[0-35-9]|6[56]|7[0135-8]|8\d|9[89])\d{8}$

  

![](http://hk-proxy.gitwarp.com/https://raw.githubusercontent.com/tuchuang9/tc1/refs/heads/main/public/20230225215649.png)

第一次优化的正则表达：

 (?<!\d)(1(3\d|4[5-9]|5[0-35-9]|6[56]|7[0135-8]|8\d|9[89])\d{8})(?!\d)

  

![](http://hk-proxy.gitwarp.com/https://raw.githubusercontent.com/tuchuang9/tc1/refs/heads/main/public/20230225215650.png)

![](http://hk-proxy.gitwarp.com/https://raw.githubusercontent.com/tuchuang9/tc1/refs/heads/main/public/20230225215651.png)

第二次优化来的正则表达：

(?<!\d)(1[3-9]\d{9})(?!\d)

  

![](http://hk-proxy.gitwarp.com/https://raw.githubusercontent.com/tuchuang9/tc1/refs/heads/main/public/20230225215654.png)

第三次优化的正则表达跟第二次是一样的：

(?<!\d)(1[3-9]\d{9})(?!\d)

  

![](http://hk-proxy.gitwarp.com/https://raw.githubusercontent.com/tuchuang9/tc1/refs/heads/main/public/20230225215655.png)

第四次优化时与ChatGPT交流可以看到像跟人类一样交流，当发现自己错误时会承认错误，然后纠正自己的错误，第四次正则表达：

(?<!\d)(1(3[0-9]|4[5-9]|5[0-35-9]|6[56]|7[0135-8]|8\d|9[89])\d{8})(?!\d)

  

![](http://hk-proxy.gitwarp.com/https://raw.githubusercontent.com/tuchuang9/tc1/refs/heads/main/public/20230225215657.png)

第五次优化正则表达：

(?<!\d)(1(3[0-9]|4[5-9]|5[0-35-9]|6[56]|7[013-9]|8\d|9[0-35-9])\d{8})(?!\d)

  

![](http://hk-proxy.gitwarp.com/https://raw.githubusercontent.com/tuchuang9/tc1/refs/heads/main/public/20230225215659.png)

![](http://hk-proxy.gitwarp.com/https://raw.githubusercontent.com/tuchuang9/tc1/refs/heads/main/public/20230225215700.png)

    可以看到与ChatGPT沟通交流时，我们不断在问问题，ChatGPT会根据上下文不断去完善我们所要的答案，真正做到了像人类一样来聊天交流，有来有回的回答，只要你问，它就不断修正自己给你的答案。这个过程比起去网上找答案的时间还短，也更精确。

![](http://hk-proxy.gitwarp.com/https://raw.githubusercontent.com/tuchuang9/tc1/refs/heads/main/public/20230225215647.png)

 ****
这也是为什么ChatGPT会引爆互联网圈，有人认为是人工智能的转折点，真正的AI时代来临，国内大厂纷纷争着做出另一款ChatGPT，确实，它是真的香。

  

    当然，以上例子只是为了拿来抛砖引玉，实际上的ChatGPT能做的事情比这个还多的多，缺陷也比较明显，目前所学的知识截止2021年9月。在2022年的技术知识查不到，但不影响它成为自己的“百度”。

  

![](http://hk-proxy.gitwarp.com/https://raw.githubusercontent.com/tuchuang9/tc1/refs/heads/main/public/20230225215703.png)

    除了可以拿来实现技术手段外，也能指导如何开展数据安全工作，成为工作中的百科小能手，无所不知的“安全小顾问”。但是在使用时请注意数据的泄露，切记不要将公司内部文件及个人敏感信息放到ChatGPT上提问，毕竟不属于公司内部产品，把公司内部数据放到ChatGPT上因为数据脱离公司内部可控范围内导致存在风险隐患。

  

    ChatGPT能够通过学习和理解人类的语言来进行对话，模拟人类一样正常交流。通过ChatGPT可以畅想一下未来的人工智能场景，假设在未来ChatGPT普及时，ChatGPT被各种安全公司细分领域定制化训练，通过不断训练单独一个专业领域上的知识，让安全设备可以变得和人类一样“思考”，除了文本聊天之外，还支持上传文件、图片、软件等多样化，在安全领域是否可以向专业技术人员一样思考，就像下面场景：

  

    1、数据安全：在对数据泄露溯源时，将日志上传到ChatGPT自动分析数据的链路流程，用户在什么时间段、访问了什么数据、做了什么操作等；

  

    2、代码审计：将源代码文件上传到ChatGPT进行自动化源代码审计，将审计出来的结果通过复现出来证明存在漏洞等；

  

    3、应急响应：将病毒样本上传到ChatGPT分析病毒是如何运行、什么特征等情况；将主机或安全设备上的日志上传到ChatGPT分析日志中是否存在入侵痕迹，通过时间维度画出攻击链路图等；

  

    4、红蓝对抗自动化：模拟红蓝对抗攻击，自动识别指纹、指定payload，24小时自动化寻找公司内部薄弱点等；

  

    5、提高安全设备防御能力：通过不断学习训练拦截更多绕过免杀的技术....等等各种安全所需场景。

  

★

    最后，引用网上一句话，取代你的不是AI，而是更会使用AI的人，希望你我共勉。

  

![](http://hk-proxy.gitwarp.com/https://raw.githubusercontent.com/tuchuang9/tc1/refs/heads/main/public/20230225215704.png)

  

![]()

  

文章中的一些问题希望各位大佬不吝赐教，对于一些错误之处希望各位师傅多多指正！

  

  

  

  

![](http://hk-proxy.gitwarp.com/https://raw.githubusercontent.com/tuchuang9/tc1/refs/heads/main/public/20230225215705.png)

✦

✦  ✦

![](http://hk-proxy.gitwarp.com/https://raw.githubusercontent.com/tuchuang9/tc1/refs/heads/main/public/20230225215706.png)

 **公众号｜A9 Team  
**

 **  
**

 **作者｜Zer0n1**

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

