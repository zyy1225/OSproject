# StudyGit

## 基本操作

![git](https://raw.githubusercontent.com/zyy1225/OSproject-miniprogram2020/master/Notes/Mei%20Zuhao/pictures/git.jpg)

- workspace：工作区
- staging area：暂存区/缓存区
- local repository：或本地仓库
- remote repository：远程仓库

```
$ git init #初始化仓库

$ git clone <url> #拷贝一份远程仓库，即下载一个项目

$ git status #查看仓库的状态

$ git pull origin master:feature-A #将远程主机origin的master分支拉取过来，与本地的feature-A分支合并
$ git pull origin master #如果远程分支是与当前分支合并，则冒号后面的部分可省略

$ git diff #比较工作区中的该文件与暂存区或版本库最后一次提交中的区别

$ git add [file1] [file2] ... #添加一个或多个文件到暂存区
$ git add [dir] #添加指定目录到暂存区，包括子目录
$ git add . #添加当前目录下的所有文件到暂存区

$ git commit -m 'message' #提交暂存区到本地仓库中，message是备注信息
$ git commit [file1] [file2] ... -m 'message' #提交暂存区的指定文件到本地仓库中
$ git commit -a #-a参数设置修改文件后不需要执行git add命令，直接提交

$ git branch #显示分支一览表
$ git branch feature-A #创建feature-A分支
$ git checkout feature-A #将当前分支切换为feature-A 分支
$ git checkout -b feature-A #创建新分支feature-A并立即切换到该分支下

$ git push origin feature-A -f #本地强制上传到远程feature-A，把远程的覆盖

$ git merge feature-B #把当前所在分支与feature-B分支合并
$ git rebase feature-B #把当前所在分支与feature-B分支合并（与merge有区别）
```



## 文件操作

```
$ mkdir dirName #创建一个名为dirName的文件夹
$ mkdir -p dirName/dirSub #在dirName目录下创建dirSub目录，-p代表如果dirName不存在，则新建一个

$ cd dirName #进入dirName目录

$ pwd #当前所在位置
```

