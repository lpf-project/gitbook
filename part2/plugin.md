## 自带的插件

- highlight： 代码高亮
- search： 导航栏查询功能（不支持中文）
- sharing：右上角分享功能
- font-settings：字体设置（最上方的"A"符号）
- livereload：为GitBook实时重新加载

## 去除自带插件

```json
{
    "title": "gitbook",
    "plugins": [
        "-search"
    ]
}
```


## 第三方插件

具体的插件使用说明：gitbook-plugin-accordion

|模块名称 |	功能描述| 备注|
|---|---|---|
|accordion |	手风琴折叠模块||
|insert-logo|配置logo|
|ace	|代码 ACE 显示||
|copy-code-button|代码复制按钮|
|disqus|评论系统|
|anchor-navigation-ex|页面导航和回到顶部|
|back-to-top-button|回到顶部||
|page-toc-button||安装失败|
|anchors|添加 Github 风格的锚点样式|
|Anchor-navigation-ex|添加Toc到侧边悬浮导航以及回到顶部按钮|本插件只会提取 h[1-3] 标签作为悬浮导航，直接从h2开始，无效
|Edit Link|添加“编辑此页面”链接。|
|Emphasize|为文字加上底色|https://www.mapull.com/gitbook/comscore/custom/plugin/other/emphasize.html
|Expandable-chapters-small|对可扩展章节插件进行微小的更改，以使用较小的箭头。||
|Favicon|为您的网站添加了一个图标和 Apple Touch 图标||
|Github|显示一个跳转到你的 github 地址的链接。||
|Local Video|使用Video.js 播放本地视频|https://dunwu.gitbooks.io/gitbook-notes/content/advanced/plugins.html|
|Prism||
|Search Plus|支持中文搜索, 需要将默认的 search 和 lunr 插件去掉。|
|Sectionx|将页面分块显示，标签的 tag 最好是使用 b 标签，如果使用 h1-h6 可能会和其他插件冲突。
|Simple-page-toc||
|Sitemap-general|||
|Splitter||
|Sharing||
|Tbfed-pagefooter|为页面添加页脚||
|Todo|||
|donate|||
|reward|||
|Google 统计|||
|Baidu 统计||https://www.zhaowenyu.com/gitbook-doc/plugins/cat-count.html|

## 插件配置

```json
{
    "title": "gitbook",
    "plugins": [
        "remove-published-with-link"
    ]
}
```

## [Favicon](https://github.com/menduo/gitbook-plugin-favicon)

```json
{
    "plugins": [
        "favicon"
    ],
    "pluginsConfig": {
        "favicon": {
            "shortcut": "images/favicon32.ico",
            "bookmark": "images/favicon32.ico",
            "appleTouch": "assets/images/apple-touch-icon.png",
            "appleTouchMore": {
                "120x120": "assets/images/apple-touch-icon-120x120.png",
                "180x180": "assets/images/apple-touch-icon-180x180.png"
            }
        }
    }
}
```
- 图标的分辨率要是32*32的
- 可直接生成图标：https://www.logosc.cn/favicon-generator

## insert-logo


## tbfed-pagefooter

在 book.json 中配置 tbfed-pagefooter 插件,详细说明请参考 tbfed-pagefooter 插件.

{
    "plugins": ["tbfed-pagefooter"],
    "pluginsConfig": {
        "tbfed-pagefooter": {
          "copyright":"&copy snowdreams1006",
          "modify_label": "文件修订时间：",
          "modify_format": "YYYY-MM-DD HH:mm:ss"
        }
    }
}

## disqus

https://snowdreams1006.gitbook.io/www/ru-men-jiao-cheng/mygitbook/advance/plugin/plugin-practical

## gitalk

## mygitalk

## search-plus


## 插件安装

执行下面命令，将会自动安装`plugins`字段下配置的插件
```
gitbook install .
```

## 去除gitbook的链接

```json
{
    "title": "gitbook",
    "plugins": [
        "remove-published-with-link"
    ]
}
```