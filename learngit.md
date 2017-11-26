# learn git

[TOC]

## 安装后设置

> git config --global user.name "name"
>
> git config --global user.email "email@example.com"

## 创建库与添加文件

> 初始化一个git仓库：git init
>
> 添加文件到git仓库，分两步：
>
> 1. git add
> 2. git commit

## 查看工作区的状态

> 查看工作区状态：git status
>
> 查看修改内容：git diff

## 文件版本

> HEAD指向的就是当前版本
>
> 版本回退或前进：git reset --hard commit_id
>
> git log查看提交历史，以确定回退到哪个版本
>
> git reflog可以查看所用历史命令（包括commit_id）

## 工作区和版本库

1. 工作区即工作目录
2. 版本库（repository）包括暂存区（stage，index）和分支，指向分支的指针HEAD

## 丢弃修改

1. 丢弃工作区的修改：git checkout -- file（实质为用版本库替换工作区）
2. 丢弃暂存区的修改，分两步
   1. 将暂存区修改送回工作区：git reset HEAD file
   2. git checkout -- file

## 删除文件

1. 将文件在工作区删除
2. git rm
3. git commit

## 添加远程库

1. 添加远程库：git remote add origin git@github.com:xxx/xxx
2. 本地库推送到远程库：git push -u origin master（第一次推送需要参数“-u”）
3. 推送：git push origin master

## 克隆远程库

git clone git@github.com:xxx/xxx

## 分支

查看分支：git branch

创建分支：git branch name

切换分支：git checkout name

创建+切换分支：git checkout -b name

合并某分支到当前分支：git merge name

删除分支：git branch -d name