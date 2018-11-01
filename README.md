# 📕Git基本教程

*⚡[Git]()是目前世界上最先进的分布式版本控制系统（没有之一）。*

- 在[Windows]()上安装[Git]()

  > [Git官网](https://git-scm.com/downloads)直接下载安装程序，（网速慢的同学请移步[国内镜像](https://pan.baidu.com/s/1kU5OCOB#list/path=%2Fpub%2Fgit)）
  
  + 安装完成后，在开始菜单里找到`"Git"->"Git Bash"`,进行如下配置：
  
  ```git
  $ git config --global user.name "Your Name"  
  $ git config --global user.email "email@example.com"
  ```
  + 生成相应的令牌，本地一份，Github 一份，这样 Github 可以在你使用仓库的时候，进行校验确定你的身份。
  
  ```git
  $ cd ~/.ssh
  $ mkdir key_backup
  $ ssh-keygen -t rsa -C "email@example.com"
  ```
  + 生成如下两个文件：
  
  <img src="https://img-blog.csdn.net/20180331221012285?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0tOSUdIX1lVTg==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70">
  
   > `id_rsa.pub` 就是我们待会需要的公钥文件，使用命令 `$ cat id_rsa.pub` 再将内容复制到剪切板，然后进入github账号设置里面添加SSH key
   
   然后输入 `$ ssh -T git@github.com` 测试连通状态
   
- 创建本地仓库

  + 选择一个本地文件夹，用作保存本地仓库文件，尽量是空文件夹。
  + 然后使用命令 `$ git init` 初始化文件夹。
    > 其实是在当前文件夹下生成一个叫 `.git` 的隐藏文件夹，里面是一些配置文件，不要随意更改。
   
  + 使用 `$ git clone https://github.com/name/repository.git` 将远程仓库克隆到本地此文件夹下。
    > [name]() 是自己的昵称，[repository]() 是自己的仓库名，不要忘记末尾的 `.git` 后缀。
   
  + 然后此文件夹下会多一个和你仓储名一样的文件夹，内部文件与远程仓库一样。
  
- 常用命令

  ```git
  $ git add . //添加文件
  $ git commit -m "commit-messages" //提交本地仓库
  $ git push origin master //提交远程仓库
  $ git pull //拉取远程文件，与以下命令类似
  $ git branch temp //创建本地分支
  $ git fetch origin master:temp
  $ git merge master
  ```
