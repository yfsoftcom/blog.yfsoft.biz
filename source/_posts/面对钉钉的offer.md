---
title: 面对钉钉的offer
date: 2016-10-18 09:46:26
tags: About Me
---

> 写这些只为总结总结自己，希望能从过去能回忆起来的一切来更好的发现自己。

昨天（10-17）去了杭州钉钉面试，来回路上花了近8个小时，到那儿聊了不到2个小时；算是非常昂贵的一次面试经历了。

---
前端不是我的强项，但是我的偏好和目标，所以面了前端的岗位，面试官是阿里的P8工程师，前端技术很厉害，而且人很好，很不错，聊到了很多细节，深入的话题，考验了我很多解决问题的想法，思路，没有很空洞的聊概念，先进的名词；算是很棒的一次体验。

---
面试之前需要通过他们内部的钉钉进行面试申请的审批提交，通过后会发送一条短信，告知专用的wifi帐户和密码。

开始面试没有太多废话，也是因为之前通过电话沟通过几次，基本情况都有了一个了解；直接打开mac链接上专用的wifi，登录github，打开自己的代码（这时的心情有点像脱得只剩裤衩），因为在身边的是一个经验丰富的老司机，看代码是了解一个开发者最正确的方式了，头一次这么紧张，不过也很高兴，展示自己最自信的一面不就是一直该做的嘛。接下来就是一顿问答:
>你是如何监控性能的？

- 首先用到了一些工具，来监控资源的消耗情况，比如阿里提供的：alinode
- 其次对每一次的请求都做了详细的日志记录，通过sql可以对执行结果做一个多维度的分析来预测问题。
- 做一些测试脚本进行自动化的测试来分析问题。

>有没有监控到性能问题？

- 有，请求涌入的时候会导致服务假死
- 服务端日志存储会消耗很多资源

>你是怎么解决的？

- 还没有彻底的解决，但是有了一些思路。
- 通过内存缓存，将日志延迟批量写入到mysql。
- 通过pm2守护node进程，捕获更多的error异常。

>关于前端，你有哪些经验或作品？

我当时掏出手机，将上一家公司的微信商城打开给他看了，然后他就针对这个商城问了很多细节的问题。

---

整个面试的过程很流畅，聊得也很开心，中途来了另一个面试官（看起来是钉钉后端的某个负责人），问了一些关于后端的内容，比如如何更安全和高效的交换前后端的数据等等。最后还聊了一些关于我为什么从java转到javascript的的问题，我没有正面回答只是说，javascript是一个发展的越来越像java的语言，而我更喜欢这个发展过程。

---

面试官当即表示，更愿意第二天就来报道；对我的整体评价是：前后端都有涉及，经验较为丰富，但细节不够深入。

继续加油～
