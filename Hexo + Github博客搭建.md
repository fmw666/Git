# 🌞Hexo + Github博客搭建
## 发布博客
+ 在本地`hexo\blog\source\_posts`文件夹下,创建一个[markdown]()文件
+ 内容格式仿照当前文件夹下 `hello-workd.md` 文件
+ 回到`hexo\blog`文件夹下，打开[git bash]()
 ```bash
 hexo g  //生成网页
 hexo d  //部署到远端(github)
 ```
## 更换主题
+ 在本地`hexo\blog\themes`文件夹下，创建一个名为`next`的文件夹（用于存放将下载的next主题）
+ 回到`hexo\blog`文件夹下，打开[git bash]()
 ```bash
 git clone https://github.com/iissnan/hexo-theme-next themes/next
 ```
+ 在当前`blog`文件夹下打开`_config.yml`文件，搜索[theme]()字段，将其值修改为`next`
+ 打开[git bash]()
 ```bash
 hexo clean  //清理缓存
 hexo g    //重新生成博客代码
 hexo d   //部署到本地
 ```
 
 *[更多相关](https://www.jianshu.com/p/33bc0a0a6e90)*
## 博客网站美化
> 在Hexo中有两份主要的配置文件，其名称都是 `_config.yml`。 其中，一份位于站点根目录下，主要包含 Hexo本身的配置；另一份位于主题目录下，这份配置由主题作者提供，主要用于配置主题相关的选项。

+ 站点配置：
  在本地的blog文件夹下打开`_config.yml`文件，如下可以修改博客网站的标题、描述，语言等属性
  ![site.png](https://i.loli.net/2018/11/02/5bdbc51db2332.png)
+ 主题设置：
  - Next文档地址：[http://theme-next.iissnan.com/getting-started.html](http://theme-next.iissnan.com/getting-started.html) 
  - 其他参考：
  
     [hexo的next主题个性化教程](https://www.jianshu.com/p/f054333ac9e6) 
     
     [打造个性超赞博客Hexo+Next+githubPages的超深度优化](https://reuixiy.github.io/technology/computer/computer-aided-art/2017/06/09/hexo-next-optimization.html#)
