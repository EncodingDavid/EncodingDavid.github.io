---
categories: 
   - [Termux]
   - [Hexo]
cover: /img/termux.webp
---

> 在看之前，确保你有一个github或者gitee账户，申请一个账号十分简单，如果你的网络环境不好，建议使用gitee。
>
> 以及一个安装了termux的安卓手机。
>
> 本文需要具备一定的linux命令、vim基本操作和Markdown语法，如果对此不熟悉可以百度一下教程。

## 准备

- 1. 在GitHub或者gitee上创建一个空的仓库

![image-20200724045235778](https://tva1.sinaimg.cn/large/007S8ZIlgy1gh1l2a0fqmj30sq08wjsp.jpg)

- 2. 记住要添加REAME.md，不然不能形成网址。

![image-20200724044709066](https://tva1.sinaimg.cn/large/007S8ZIlgy1gh1lnyk367j326y0c8jxg.jpg)

- 3. 服务->gitee pages

![image-20200724045553710](https://tva1.sinaimg.cn/large/007S8ZIlgy1gh1l5xzwsbj315q0j2dhn.jpg)

因为我已经部署了，所以这里只需要更新即可，未部署会显示部署。

## 配置termux（粘贴到termux）

1. ```pkg update && pkg install vim curl wget git unzip  nodejs-lts openssh -y && npm install hexo-cli -g && hexo init blog && cd blog && npm install hexo-deployer-git --save && npm audit fix && hexo g && hexo s```

   如果提示y输入y并回车

2. 打开http://localhost:4000即可看到生成的blog，此时的blog就像毛坯房，非常简陋，不过没关系，hexo提供了各种丰富的主题。

## 部署在gitee上

在termux输入

1. `git config --global user.name "你的gitee用户名"`

2. `git config --global user.email "你的邮箱"`

3. `ssh-keygen -t rsa -C "你的邮箱（所有的邮箱都是同一个，否则会大麻烦）"`

   一直回车就行

4. 查看你的密钥 `cat ~/.ssh/id_rsa.pub`

   Mac用户: `cat /Users/david/.ssh/id_rsa.pub `把david替换成你的用户名

5. 完整复制到gitee。

   ![image-20200724053150002](https://tva1.sinaimg.cn/large/007S8ZIlgy1gh1m77cts3j30vo0kmad2.jpg)

6. 粘贴到gitee（**「个人设置」->「安全设置」->「SSH公钥」->「[添加公钥](https://gitee.com/profile/sshkeys)」**

   ![image-20200724053331025](https://tva1.sinaimg.cn/large/007S8ZIlgy1gh1m8uzc7oj31ma0n6wi0.jpg)

## 配置博客

1. vim _config.yml

2. ```yaml
   # Site
   title: 输入你的标题 
   subtitle: 输入你的副标题,
   description: 输入你的描述，也可以是联系方式，gitee或者GitHub地址
   keywords:关键词，可不填
   author: 输入你的昵称
   language: 默认英文，中文填zh-Cn
   timezone: 时区，中国的填Asia/shanghai
   
   # URL
   ## If your site is put in a subdirectory, set url as 'http://yoursite.com/child' and root as '/child/'
   url: 填你的网站的地址，即你在gitee部署的网址
   ```

3. 修改部署的地址

4. 1. 获取git的地址，也就是git clone的地址

      ![image-20200724050410519](https://tva1.sinaimg.cn/large/007S8ZIlgy1gh1lebqdm2j30qg0jiju7.jpg)

   2. 依旧是进入到_config.yml

      ![image-20200724050203949](https://tva1.sinaimg.cn/large/007S8ZIlgy1gh1lc64wboj310a08w0tt.jpg)

   3. 保存，退出。

   4. 博客内容存在source/_posts，可以建立一个md文件随便写点什么。

   

   
