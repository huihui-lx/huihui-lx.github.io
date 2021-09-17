---
title: Git和GitHub的使用
author: huihui-lx
avatar: https://cdn.jsdelivr.net/gh/huihui-lx/cdn/img/head_portrait/1.jpg
authorLink: huihui-lx.com
categories: 技术
date: 2021-9-16 20:00
comments: true
tags: 
    - 算法
keywords: Sakura
description: 使用git和github
photos: https://cdn.jsdelivr.net/gh/huihui-lx/cdn/img/article/1.jpg
---

## Git和GitHub的使用

### 常用的git命令

```
git init  初始化本地git仓库
git clone + ssh 克隆
git status  查看当前状态   
 - 1. 红褐色: 创建之后没有add，没提交，不在版本控制范围之内. 
 - 2. 绿色：add之后是文件绿色的，没有提交（commit）.
 - 3. 蓝色：原本有一个文件，改动过后没有提交（commit）是蓝色的，提交之后，变成正常颜色。
git add xxx  将xxx文件添加到暂存区
git add .  将当前子目录下所有更改过的文件提交到暂存区
git commit -m "提交说明"  提交

git remote  列出你指定的每一个远程服务器的简写。 如果你已经克隆了自己的仓库，那么至少应该能看到 origin ——这是 Git 给你克隆的仓库服务器的默认名字： 
git remote -v  你也可以指定选项 -v，会显示需要读写远程仓库使用的 Git 保存的简写与其对应的 URL。
git remote add <shortname> <url>  自行添加远程仓库  例如: git remote add origin git@github.com:huihui-lx/Plants-vs-Zombies.git
git push
 1. git push <远程主机名> <本地分支名>:<远程主机分支名>
 	git push origin master:main
 2. git push <远程主机名> <本地分支名>  省略了远程主机分支名, 则git会push与本地分支名相同的远程分支
 	git push origin master 等价于 git push origin master:master

```



### 常见错误

```
 ! [rejected]        master -> main (fetch first)
原因: github中的README.md文件不在本地代码目录中
解决方法: git pull --rebase origin <远程分支名>
```

