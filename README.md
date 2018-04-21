# social-share
一款分享插件

### 字体

来源: icon-fonts: http://www.iconfont.cn

在线:

```
  <link href="//at.alicdn.com/t/font_635087_ef20v4flda62yb9.css" rel="stylesheet">
```
本地(引入 fonts):

```
  <link href="src/css/iconfont.css" rel="stylesheet">
```

### 设置

config: src/js/share.js

```
  /*
  * 分享链接的信息
  */
  var title = 'Wang RiYu\'s Blog' || window.location.href, url = 'http://blog.wangriyu.wang' || window.location.hostname, author = 'yule' || 'yule', img = 'http://blog.wangriyu.wang/img/yule.jpg' || 'http://blog.wangriyu.wang/img/yule.jpg';
  /*
  * 修改 set 为 false 关闭相应按钮
  */
  var config = [{
    name: 'facebook',
    set: true,
    api: `https://www.facebook.com/sharer/sharer.php?u=${encodeURI(url)}`,
    title: 'Share this article on Facebook',
    icon: 'icon-facebook',
  }, {
    name: 'wechat', set: true, api: 'weixin://', icon: 'icon-wechat'
  }, {
    name: 'twitter',
    set: true,
    api: `https://twitter.com/intent/tweet?source=webclient&amp;original_referer=${encodeURI(url)}&amp;text=${encodeURI(title)}&amp;url=${encodeURI(url)}&amp;related=${encodeURI(author)}&amp;via=${encodeURI(author)}`,
    title: 'Share this article on Twitter',
    icon: 'icon-twitter'
  }, {
    name: 'weibo',
    set: true,
    api: `http://v.t.sina.com.cn/share/share.php?url=${encodeURI(url)}&amp;title=${encodeURI(title)}&amp;content=utf8&amp;pic=${encodeURI(img)}`,
    title: 'Share this article on Weibo',
    icon: 'icon-weibo'
  }, {
    name: 'qq',
    set: true,
    api: `http://connect.qq.com/widget/shareqq/index.html?url=${encodeURI(url)}&amp;title=${encodeURI(title)}&amp;pics=${encodeURI(img)}`,
    title: 'Share this article on QQ',
    icon: 'icon-qq'
  }, {
    name: 'qzone',
    set: true,
    api: `http://sns.qzone.qq.com/cgi-bin/qzshare/cgi_qzshare_onekey?url=${encodeURI(url)}&amp;title=${encodeURI(title)}&amp;pics=${encodeURI(img)}`,
    title: 'Share this article on Qzone',
    icon: 'icon-CN_tencentqzone'
  }, {
    name: 'douban',
    set: true,
    api: `http://www.douban.com/recommend/?url=${encodeURI(url)}&amp;title=${encodeURI(title)}&amp;image=${encodeURI(img)}`,
    title: 'Share this article on Douban',
    icon: 'icon-douban'
  }, {
    name: 'youdao',
    set: true,
    api: `http://note.youdao.com/memory/?title=${encodeURI(title)}&amp;pic=${encodeURI(img)}&amp;url=${encodeURI(url)}`,
    title: 'Share this article on YoudaoNote',
    icon: 'icon-youdaoyunbiji'
  }, {
    name: 'google',
    set: true,
    api: `https://plus.google.com/share?url=${encodeURI(url)}`,
    title: 'Share this article on Google+',
    icon: 'icon-googleplus'
  }, {
    name: 'linkedin',
    set: true,
    api: `https://www.linkedin.com/shareArticle?title=${encodeURI(title)}&amp;url=${encodeURI(url)}`,
    title: 'Share this article on LinkedIn',
    icon: 'icon-linkedin'
  }, {
    name: 'copy', set: true, title: 'Copy the link of this article', icon: 'icon-link'
  }, {
    name: 'mail',
    set: true,
    api: `mailto:?subject=${encodeURI(title)}&quot;&amp;body=permalink:${encodeURI(url)}`,
    title: 'Share this article by email',
    icon: 'icon-email'
  }];
```

### 效果

![gif](share.gif)

欢迎提 issue 和 pr，如果觉得好请 star 支持一下!
