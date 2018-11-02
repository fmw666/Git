# 📕Git基本教程

*⚡[Git]()是目前世界上最先进的分布式版本控制系统（没有之一）。*

- **在[Windows]()上安装[Git]()**

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
  
  ![git.png](https://i.loli.net/2018/11/01/5bdb01c742769.png)
  
   > `id_rsa.pub` 就是我们待会需要的公钥文件，使用命令 `$ cat id_rsa.pub` 再将内容复制到剪切板，然后进入github账号设置里面添加SSH key
   
   然后输入 `$ ssh -T git@github.com` 测试连通状态
   
- **创建本地仓库**

  + 选择一个本地文件夹，用作保存本地仓库文件，尽量是空文件夹。
  + 然后使用命令 `$ git init` 初始化文件夹。
    > 其实是在当前文件夹下生成一个叫 `.git` 的隐藏文件夹，里面是一些配置文件，不要随意更改。
   
  + 使用 `$ git clone https://github.com/name/repository.git` 将远程仓库克隆到本地此文件夹下。
    > [name]() 是自己的昵称，[repository]() 是自己的仓库名，不要忘记末尾的 `.git` 后缀。
   
  + 然后此文件夹下会多一个和你仓储名一样的文件夹，内部文件与远程仓库一样。
  
- **常用命令**

  ```git
  $ git add . //添加文件
  $ git commit -m "commit-messages" //提交本地仓库
  $ git push origin master //提交远程仓库
  $ git pull //拉取远程文件，与以下命令类似
  $ git branch temp //创建本地分支
  $ git fetch origin master:temp
  $ git merge master
  ```
- **图床介绍**

  *写博客就无法避免上传图片，图床就是这么一个地方，就是一个网站，你发自己的图片上传到它的网站，然后它给你一个这个图片的链接，插入博客中就能显示图片了。*
  + 推荐一个知名的，七牛云[https://portal.qiniu.com/](https://portal.qiniu.com/)，注册完实名认证后有一些优惠。 
  + 还有一个神奇的网站：[https://sm.ms/](https://sm.ms/)，也能用
  
- **Hexo+github博客搭建**  

  + 推荐一个CSDN博主的文章，[点击这里](https://blog.csdn.net/Mr_yu_java/article/details/81077064)
  + 一个git用户很详细的分享，[点击这里](https://hans2936.github.io/2018/06/06/HexoLog/)
  + 当然，官方教程更全面，[点击这里](https://hexo.io/zh-cn/docs/deployment.html)
  
  *这里分享一篇我的总结，[点击这里](Hexo + Github博客搭建.md) *
  
