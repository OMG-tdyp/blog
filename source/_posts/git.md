---
title: git的一些常用操作
date: 2018-05-08 16:14:20
tags: [git]
categories: git
---

## 1、克隆远程仓库到本地
首先你要知道一个远程仓库的地址，然后
```javascript
git clone git@github.com:OMG-tdyp/vue-koa2.git
```


## 2、添加本地仓库远程
在GitHub上创建一个新的仓库后，可以把本地仓库的内容推送到GitHub仓库
要关联一个远程库，使用命令（例如）
```javascript 
git remote add origin git@github.com:OMG-tdyp/vue-koa2.git
```
关联后，使用命令
```javascript 
git push -u origin master
```
第一次推送master分支的所有内容


## 3、把文件添加到版本库
```javascript
git add .(这个是添加所有，也可以添加单个文件)
git commit -m "此次操作所做的事情"
```
add 命令把文件提交到缓存区
commit 把缓存区文件提交到版本库，-m 参数是指定comments
可以add多次，一次commit


## 4、查看版本库状态
```javascript
git status
```
该命令查看到的结果分为两部分：
一，add到缓存区内等待被commit到版本库的更改。
二，工作区内的还未add到缓存区的更改


## 5、拉取最新代码
```javascript
git pull
```


## 6、提交最新代码
```javascript
git push
```


## 7、废弃工作区修改
单个文件废弃
```javascript
git checkout -- index.txt
```
整个工程废弃
```javascript
git checkout -f
```
这个命令会把你工作区中的修改回退到最后一次add命令之前的状态
即如果缓存区有内容，则回退到和缓存区一直
如果缓存区为空，则回退到和版本库一致