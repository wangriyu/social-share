# social-share

一款分享插件

### 字体

来源: icon-fonts http://www.iconfont.cn

在线:

```
  <link href="//at.alicdn.com/t/font_635087_ef20v4flda62yb9.css" rel="stylesheet">
```

本地(引入 fonts):

```
  <link href="src/css/iconfont.css" rel="stylesheet">
```

### 效果

[Demo](https://htmlpreview.github.io/?https://github.com/wangriyu/social-share/blob/08f4f6e2a8582a6138f8fd751887f7516f294d77/index.html)

[Blog](http://blog.wangriyu.wang/tags/)

![gif](share.gif)

### 使用

在 head 引入:

```html
  <!--<link href='//at.alicdn.com/t/font_635087_ef20v4flda62yb9.css' rel='stylesheet'>-->
  <link href='src/css/iconfont.css' rel='stylesheet'>
  <link rel='stylesheet' href='src/css/spongebob.min.css' type='text/css' media='all'/>
```

在 body 中插入:

```html
<div>
  <div class='social_share'>
    <ul id='social_list' class='social_icon_list'></ul>
  </div>
  <script>
    /*
    * title, url, author, img 必填
    * services 选填，false 关闭相应分享
    */
    var shareConfig = {
      title: 'Wang RiYu\'s Blog',
      url: window.location.href,
      author: '鱼乐',
      img: 'http://blog.wangriyu.wang/img/yule.jpg',
      services: {
        facebook: false,
        wechat: true,
        twitter: true,
        weibo: true,
        qq: true,
        qzone: true,
        douban: true,
        youdao: true,
        google: false,
        linkedin: true,
        copy: true,
        mail: true
      }
    }
    // var shareConfig = {
    //   title: '<%= post.title %>',
    //   url: window.location.href,
    //   author: '<%= config.author %>',
    //   img: 'https:<%=theme.avatar%>'
    // }
  </script>
  <script src='src/js/qrcode.min.js'></script>
  <script src='src/js/spongebob.min.js'></script>
</div>
```
