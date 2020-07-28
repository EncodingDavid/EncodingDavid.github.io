---
title:
date:
tags:
categories: macOS
keywords:
description:
top_img: 
cover: /img/Homebrew-for-macOS.jpg
comments: True
toc:  True
toc_number: True
copyright: True
mathjax:
katex:
---

# Brew遇到的坑

当我尝试更新big sur的时候，发现brew install用不了了，系统一直提示下图。

![image-20200727024818135](https://tva1.sinaimg.cn/large/007S8ZIlgy1gh4yc1m6gtj30wy07awfu.jpg)

接着我找了很多资料，发现要将command line tool卸了重装，于是我一股脑卸了但是发现重装不了，一直提示正在查找软件，这让我十分懊悔，为啥手贱要把clt卸了。



于是我继续找资料，发现big sur要安装最新的xcode才行，也就是beta版，加上我租房的地方网速贼慢，所以导致我一晚上的时间都在下载，经过不断努力，终于成功安装上了新版的clt。



这次让我得出一个结论：不要轻易尝试新版本，除非你有两台。之前也犯过类似的错误，Mojave的时候Catalina出来了，我激动了一个晚上，结果第二天更新的时候发现xcode用不了，终端也是用不了，而beta版的xcode和clt还没那么快上架，在学习的时候非常不方便，不过新版本的改动令人跃跃欲试，即便知道有这个风险，我还是会去冒这个险，车到山前必有路。



我下好了Xcode-beta之后，发现依然存在上述问题，于是我又搜索了一次，原来是需要进到xcode里面操作，具体操作如下图。

![image-20200727025730155](https://tva1.sinaimg.cn/large/007S8ZIlgy1gh4ylksl7ij30nk0kqmz8.jpg)

然后进去网页，确保你下了beta版的clt和beta版的xcode，记住版本一定要对应。

![image-20200727025855404](https://tva1.sinaimg.cn/large/007S8ZIlgy1gh4ynrcvg0j31b60u0wju.jpg)

下载好了之后，我们需要选择clt版本，不然brew一直报错。

![image-20200727030026085](https://tva1.sinaimg.cn/large/007S8ZIlgy1gh4yojoprmj30eg0jmacs.jpg)

![image-20200727030114954](https://tva1.sinaimg.cn/large/007S8ZIlgy1gh4ypfhvg7j315u0u07ff.jpg)

这样子再使用brew的时候就不会出现上述问题，解决完之后，我觉得有必要写博客记录一下，下次出现还可以再回来。

![image-20200727031251160](https://tva1.sinaimg.cn/large/007S8ZIlgy1gh4z1islzpj30xo08s75c.jpg)