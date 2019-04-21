title: hexo 指北
---
> Theresa发现，最近几篇Luogu日报都是关于hexo的内容，决定将自己当初搭建博客时写下的记录也发上来

>~~万一过审了呢QvQ~~

---正文---

---
首先，$ hexo+github $搭建博客的精髓在于$Free$，也就是使用的是$github$提供的空间而不是购买服务器，也就是Luogu的同学们不必花格外的$Money$了~~毕竟还有₵₵₤在~~。

#### STEP1

拥有属于自己的github账号的同学请看STEP2

打开[github官网](https://github.com/)，已有账号点击[登录](https://github.com/login)，或者新人点击[注册](https://github.com/join?source=header-home)。

注册$github$账号只需要用邮箱，所以手机不在~~的机房里~~也可以轻松完成。

(外国网站在天朝可能会有卡顿或加载不出来的情况，多试几次就好啦

#### STEP2

已经建立好$Repository$ 的同学请看STEP3

登录账号并打开[github官网](https://github.com/)，在首页点击的$Start$ $a$ $project$ 按钮，也就是[这里](https://github.com/new)

在 $Repository$ $name$ 一栏里输入名称，格式为 " 你的github用户名+.github.io "

>举个栗子：SSS-Theresa 是Theresa的用户名，那么Theresa所要键入的就是" SSS-Theresa.github.io " 

也就是这样

![Pic1](https://cdn.luogu.org/upload/pic/53620.png )

由于Theresa已经建立了相同名称的$repository$，所以会提示重复，同学们就不会这样啦！

![Pic2](https://cdn.luogu.org/upload/pic/53624.png )

下面的内容大致就是这样，通常情况下，选择$Public$即可。

#### STEP3

已经安装好$Git$与$Node.js$的同学请看STEP4

$github$部分的配置暂告一段落，接下来是环境的配置(重要QvQ)

需要用到的软件是 [Git](https://git-scm.com/)和[Node.js](https://nodejs.org/zh-cn/)这二者，如果是普通的$OIER$应该是没有的，所以直接点击上面的链接即可。

(Theresa:如果官网比较卡顿，可以选择$Google$一下，在其他应用商店中下载

安装部分...官网上会自动选择合适的版本，在其他地方下载则要先在 控制面板\系统和安全\系统 中查看是32位还是64位，注意了喽，不对应的版本是无法安装的

安装时可能有较多选项，一直按"Next"即可，最终按下"Finish"完成安装。

(Theresa:$Node.js$在完成安装时窗口有一定概率~~对Theresa来说是100%~~ 到桌面最左侧，多数时候无法拖出，直接关闭即可

#### STEP4

>建立文件夹，文件夹名称最好是英文...如" hexo "

![Pic3](https://cdn.luogu.org/upload/pic/53628.png )

接下来在文件夹中右击，再点击 $Git$ $Bash$ $Here$

![Pic4](https://cdn.luogu.org/upload/pic/53629.png )

打开的是类似这样的窗口

![Pic5](https://cdn.luogu.org/upload/pic/53631.png  )

#### 接下来是重头戏，请同学们务必按步骤进行QvQ

有些步骤可以在其他位置进行，但为了方便在这里一并进行

```
cd D:/hexo
//定位到该位置，是为了以防万一，cd后面的路径改为自己建立文件夹的路径
npm  install  hexo-cli -g
//全局安装hexo需要的内容
hexo init
//在当前文件夹安装hexo所需文件
npm install
//在当前文件夹安装hexo所需文件
git config  --global  user.name  "SSS-Theresa"  
git config  --global  user.email  SSS-Theresa@qq.com
//这两条是配置本电脑中的个人信息
//这两条不要直接复制哇QAQ，要将后面的东西改为自己的呢...
ssh-keygen -t rsa -C SSS-Theresa@qq.com
//生成本地的SSH码
//同样要将后面的东西改为自己的呢...
//这一项会出现需要键入其他东西(似乎)，直接按回车即可，若出现(yes/no)则键入yes
cat ~/.ssh/id_rsa.pub、
//键入后会出现一大串字符——开始下一步

```

完成上面的步骤后再次打开[github官网](https://github.com/)，点击
右侧头像，再点击下拉菜单栏的[Settings](https://github.com/settings/profile)

![Pic6](https://cdn.luogu.org/upload/pic/53636.png )

//Theresa只截一部分图是在给大家省流量哇QAQ

点击打开页面中的[SSH and GPG keys](https://github.com/settings/keys)

![Pic7](https://cdn.luogu.org/upload/pic/53640.png )

点击[New SSH key](https://github.com/settings/ssh/new)

![Pic8](https://cdn.luogu.org/upload/pic/53641.png )

将复制过来的大串字符粘贴到$Key$下方的本文框中

![Pic9](https://cdn.luogu.org/upload/pic/53645.png )

再点击$Add$ $SSH$ $key$

完成！

最后打开之前建立的文件夹，打开文件 _config.yml

![Pic10](https://cdn.luogu.org/upload/pic/53647.png )

将文档打开到最末，将
```
deploy:
  type:


```
替换为
```
deploy:
  type: git
  repository: git@github.com:SSS-Theresa/SSS-Theresa.github.io.git
  branch: master
```
//当然要将信息改为自己的啦

#### STEP5
关于hexo的基础配置已经正式结束，但若是按照Theresa的步骤，同学们至今应当未曾见过自己的博客(QAQ

再次在建立的文件夹根目录下右击，再点击 $Git$ $Bash$ $Here$，输入
```
hexo g
hexo s
```
此时(先不要按Ctrl+C哇)打开[预览网页](http://localhost:4000/)

即可看到自己的blog啦！

这时(请放心地按下Ctrl+C吧)使用

```
hexo d
```
就可以上传自己的博客了

>Bug警告：

>如果出现上传失败的情况下，可以尝试键入
```
npm  install  hexo-deployer-git  --save
```
>如果想知道常用hexo命令语句，请翻到本页面最末

#### STEP6

毫无疑问，初生的博客十分简陋，我们要对其进行修改

首先是外观。

点击

[hexo官方主题网页 - Themes | Hexo](https://hexo.io/themes/)

[有哪些好看的 Hexo 主题? - 知乎](https://www.zhihu.com/question/24422335/answer/115800792)

选择心仪的主题，或者直接在Google上搜索亦可

我们以最常用的主题之一——next 为例

进入主题的github源代码页面

![Pic](https://cdn.luogu.org/upload/pic/53649.png )

点击$Clone$ $or$ $download$

![Pic12](https://cdn.luogu.org/upload/pic/53650.png )

点击$Download$ $ZIP$

下载后得到的是一个压缩包，解压后将整个文件夹放到```D:\hexo\themes```中

打开_config.yml

搜索"theme:"(不连双引号)

将默认的 "landscape" 改为文件夹名称

注意，粘贴后要确认名称与英文冒号之间有一个英文空格，否则会报错！

保存后再使用```hexo s``` 查看效果吧

再具体的美化就不多说了，以后可能会写吧

#### STEP7

但此时但博客依旧不够完善：
>1.这还不是自己的
>2.没有博文

STEP7就来解决这样的问题嘞。

打开文件夹根目录下的_config.yml

```
# Site
title: Hexo
#网站的标题名称
subtitle:
#副标题
description:
#一句话介绍
keywords:
#？
author: John Doe
#作者名称
language:
#语言
timezone:
#？
```
将各项内容更改，变成自己的博客吧！

(打问号的反正用不到QAQ...如果有同学问我再补吧...

但是——如果就这样将标题改为带有中文的，如$Theresa的小站$

会惊讶地发现，标题是一串奇怪的符号

事实上，默认地文件格式是ANSI，而中文在这种格式的文件中无法正常预览

点击文件——>另存为

![Pic13](https://cdn.luogu.org/upload/pic/53657.png )

将编码改为 UTF-8，再保存

![Pic14](https://cdn.luogu.org/upload/pic/53659.png )

再打开预览就可以啦！(重新打开)

开始第二项议程——博文

有2种方法~~(手动和自动)~~，但既然楼上的dalao们好像讲的都是自动化~~生产~~博文，Theresa就直接手动吧...

打开建立的文件夹根目录\source\_posts

新建本文文档，并将名称改为"名称+.md"的形式(后缀txt不要留啊)，用上面的方法将编码改为UTF-8

```
---
title: 
#标题
tags: 
#标签
date: 
#日期
updated: 
#更新日期
categories: 
#分类
---
```
将这样的内容粘贴进去，填好内容，即可开始写博文啦！

#### STEP final

至此，一个全新的博客已经出现在你的眼前了，下面给出的则是常用的命令

```
hexo g
//在本地建立hexo配置
hexo s
//在本地预览本地建立的配置
hexo clean
//清除本地建立的配置
hexo d
//上传本地建立的配置
```

就说这些，虽然其他的命令，但日常所需但就是这么4条，Theresa也不想复制粘贴什么东西给大家看，毕竟实用性第一嘛QwQ

如果还有疑问，在下面留言或是私信我吧
