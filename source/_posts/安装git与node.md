---
title: 安装git与nodejs
date: 2016-09-01 09:37:48
tags:
---

# 安装git
1. [下载git](http://rj.baidu.com/soft/detail/30195.html?ald)

2. 安装git,我们选择命令行形式，这样无论在window下还是在linux下 都可以,其他步骤一路next.
![git安装](http://ocvxdeagu.bkt.clouddn.com/git%E5%AE%89%E8%A3%85.png)

3. $ git --version 查看git版本 


# 安装node
1. 先安装nodejs的多版本管理器[下载gnvm](https://github.com/Kenshin/gnvm)

2. 选个文件夹保存后，在此文件夹目录里 ，按shift＋鼠标右键，点击‘在此处打开命令窗口’
		
		$ gnvm install latest 安装最新版node 	
		$ gnvm npm laltest 安装最新版npm
		$ node －v 查看node版本
		
		其他命令：
		$ gnvm install 5.0.0  安装指定版本的node
		$ gnvm ls 查看所有安装了的node
		$ gnvm search 5.*.* 查看所有5开头的版本号
		$ gnvm use 5.0.0 切换到指定版本
		$ gnvm update latest 更新最新版本的node
		$ gnvm config registry TAOBAO 配置镜像源为淘宝源
		
*  也可不安装gnvm，直接安装一个版本的node [node中文网](http://nodejs.cn/download/releases/)，node自带了npm.
*  配置淘宝镜像源：
		
		$ npm config set registry https://registry.npm.taobao.org 		

	ps:如果在命令窗输入查看node版本提示错误的话，
	
	需要配置下环境变量：右键我的电脑－>高级系统设置－>环境变量->编辑Path，
	
	在末尾添加 ;你的node的路径; 如 ;D:/node/6.5.0/;
		

# 生成ssh
1. 设置git的用户名和邮箱


		$ git config —global user.name “你的名字”

		$ git config —global user.email “你的邮箱”
	

2. 生成ssh

		$ ssh-keygen -t rsa -C "你的邮箱"
	
		接下来按三个回车
3. 	复制ssh：

	C:\Users\Administrator\.ssh)找到id_rsa.pub,用记事本即可打开。

	mac用户复制ssh
	
		mac用户：
		$ cd /
		$ cd ~/.ssh
		$ vi id_rsa.pub 

		
# 把ssh添加到github上

1. 注册github账号
2. 点击右上角弹出的列表选择setting
3. 点击左侧列表的SSH and GPG keys
4. 点击右侧上方的New SSH key
5. 输入标题和刚生成的ssh
	

