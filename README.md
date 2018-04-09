<h1 align="center">hexo-theme-art</h1>
<p align="center">一款基于 bootstrap 4.0 的 hexo 主题</p>

### 概览

**hexo-theme-art** 主题的主要特点是简单易用  [>>>>>>在线演示](https://www.niuhp.com)。  


主题使用了以下第三方库（详情可查看 [head.ejs](layout/_partial/head.ejs) ）：  
1. [bootstrap 4.0.0](https://getbootstrap.com/docs/4.0/getting-started/introduction/)
2. [jquery 3.3.1](http://api.jquery.com/)
3. [Font Awesome 4.7.0](https://fontawesome.com/)

布局使用到的 css、js 有：  
1. [分页工具 bs_paginator.js](scripts/bs_paginator.js)
2. [归档页样式 archive.css](source/css/archive.css)
3. [文章页样式 article.css](source/css/article.css)
4. [公共样式 common.styl](source/css/common.styl)
5. [代码及 Font Awesome 图标高亮样式 highlight.styl](source/css/highlight.styl)
6. [主题布局样式 layout.css](source/css/layout.css)
    
**注意：** 目前主题主要在 PC 上使用，手机、Pad 上尚未测试。

### 安装

1. 切换博客根目录 `cd root_dir_of_your_site`
2. 下载主题源码 `git clone https://github.com/niuhp/hexo-theme-art.git themes/art`
3. 使用 art 主题，替换博客根目录下 `_config.yml` 中 `theme` 的值为 `art`
4. 执行 `hexo g` 重新生成博客页面

### 主要特性

1. 支持畅言评论及赞赏功能,修改 [_config.yml](_config.yml) 中 `changyan` 属性的 `appid` 及 `appkey`，如下：
    ```yaml
    # 畅言评论
    changyan:
      appid: # 你的 appid
      appkey: # 你的 appkey
      show_comment: true # 文章末显示评论框
      show_reward: true  # 文章末显示打赏
      #评论数显示设置：archive 归档页显示，detail 详情页显示
      show_count:
        archive: true
        detail: true
    ``` 
2. 支持百度统计及百度分享功能,修改 [_config.yml](_config.yml) 中 `baidu` 属性的 `tongji` 及 `share`，如下： 
   ```yaml
   baidu:
     tongji:   # 你的百度统计帐号
     share: true  # 百度分享
   ```
   你也可以修改 [baidu_share.ejs](layout/_plugin/baidu_share.ejs) 的内容自定义分享插件
3. 支持网站图标，修改 [_config.yml](_config.yml) 中 `favicon` 属性   
4. 自定义顶部导航栏，修改 [_config.yml](_config.yml) 中 `menu` 属性，新增加导航需要在 [languages](languages) 下各文件增加语言文件
5. 优雅的文件摘要，你可以在文章中添加 `excerptImg` 属性为每篇文章指定一个摘要图片：  
    ```yaml
    title: hexo-theme-art 使用说明
    categories: Hexo
    excerptImg: https://s.niuhp.com/blog/springcloud/helloworld/head.png
    tags: 
         - Hexo
    ```
    另外还可以修改 [_config.yml](_config.yml) 中 `max_excerpt_len` 属性的值指定文章摘要最大长度（添加摘要需要在文章中加入<!-- more -->标记，标记之前内容为摘要）
6. 定制 *关于我* 插件内容，修改 [_config.yml](_config.yml) 中 `widget_about` 相关属性
    ```yaml
    # 关于我挂件
    widget_about:
      headImg: https://s.niuhp.com/blog/329620302.gif  # 头像
      name: 牛海朋 # 名字
      motto: hello,world  # 格言，显示在名字下面
      github: https://github.com/niuhp  # github 帐号
      weibo: https://weibo.com/u/2273910663  # 微博帐号
      zhihu: https://www.zhihu.com/people/xyzabchi  # 知乎帐号
      weixin: https://s.niuhp.com/blog/weixin.png # 微信二维码图片
      qq: 329620302  # QQ 号
      twitter: https://twitter.com/niuhp # 推特帐号
      linkedin: http://www.linkedin.com/in/%E6%B5%B7%E6%9C%8B-%E7%89%9B-8627b9108/ # 领英帐号
      facebook: https://www.facebook.com/niu.haipeng # 脸书帐号
    ```

### 贡献

欢迎有兴趣的同学共同开发优化这个主题，有意者联系 [QQ 329620302](http://wpa.qq.com/msgrd?v=3&uin=329620302&site=qq&menu=yes) 