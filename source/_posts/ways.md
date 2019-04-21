
title: 同步方法
---
```
npm install hexo-cli -g  # 先安装hexo的脚手架
git clone git@github.com:lanpangzhi/lanpangzhi.github.io.git  # 下载项目，因为hexo 是默认分支，所以这里直接会下载hexo分支
npm i # 安装依赖
hexo s # 启动服务器

git add . 			# 所有变化提交到暂存区
git commit -m "新增xxx文章"  	# 提交文件
git push origin hexo   		# 推送hexo分支
```