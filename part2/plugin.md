---
description: 通过安装第三方插件，帮助文档实现更多的能力
---

# 插件

> 插件比较好配置，主要分为自带插件和三方插件，自带的插件可能不太好用，可以通过配置去除，用第三方插件替代。
>
> 当然，你也可以自行开发插件，适合程序员。

## 自带的插件

* highlight： 代码高亮
* search： 导航栏查询功能（不支持中文）
* sharing：右上角分享功能
* font-settings：字体设置（最上方的"A"符号）
* livereload：为GitBook实时重新加载

### 去除自带插件

{% code fullWidth="false" %}
```json
{
    "title": "gitbook",
    "plugins": [
        "-search"
    ]
}
```
{% endcode %}

## 第三方插件

> 插件的命名一般为：gitbook-plugin-xxx，例如insert-logo插件，实际命名为gitbook-plugin-insert-logo，但因为前缀一致，直接用简写即可。

插件地址直接在npm查询

{% embed url="https://www.npmjs.com/" %}

常用插件列表如下：

| 模块名称                      | 功能描述                                                         | 备注 |
| ------------------------- | ------------------------------------------------------------ | -- |
| accordion                 | 手风琴折叠模块                                                      |    |
| insert-logo               | 配置logo                                                       |    |
| ace                       | 代码 ACE 显示                                                    |    |
| copy-code-button          | 代码复制按钮                                                       |    |
| disqus                    | 评论系统                                                         |    |
| anchor-navigation-ex      | 页面导航和回到顶部                                                    |    |
| back-to-top-button        | 回到顶部                                                         |    |
| page-toc-button           | 安装失败                                                         |    |
| anchors                   | 添加 Github 风格的锚点样式                                            |    |
| Anchor-navigation-ex      | 添加Toc到侧边悬浮导航以及回到顶部按钮                                         |    |
| Edit Link                 | 添加“编辑此页面”链接。                                                 |    |
| Emphasize                 | 为文字加上底色                                                      |    |
| Expandable-chapters-small | 对可扩展章节插件进行微小的更改，以使用较小的箭头。                                    |    |
| Favicon                   | 为您的网站添加了一个图标和 Apple Touch 图标                                 |    |
| Github                    | 显示一个跳转到你的 github 地址的链接。                                      |    |
| Local Video               | 使用Video.js 播放本地视频                                            |    |
| Prism                     |                                                              |    |
| Search Plus               | 支持中文搜索, 需要将默认的 search 和 lunr 插件去掉。                           |    |
| Sectionx                  | 将页面分块显示，标签的 tag 最好是使用 b 标签，如果使用 h1-h6 可能会和其他插件冲突。            |    |
| Simple-page-toc           |                                                              |    |
| Sitemap-general           |                                                              |    |
| Splitter                  |                                                              |    |
| Sharing                   |                                                              |    |
| Tbfed-pagefooter          | 为页面添加页脚                                                      |    |
| Todo                      |                                                              |    |
| donate                    |                                                              |    |
| reward                    |                                                              |    |
| Google 统计                 |                                                              |    |
| Baidu 统计                  | https://www.zhaowenyu.com/gitbook-doc/plugins/cat-count.html |    |

## 插件安装

我们以`accordion`插件为例，两种安装方式

{% tabs %}
{% tab title="批量安装（推荐）" %}
1、在gitbook.json中配置

```
{
    "title": "gitbook",
    "plugins": [
        "accordion"
    ]
}
```

2、执行下面命令，将会自动安装`plugins`字段下配置的插件

```
gitbook install .
```
{% endtab %}

{% tab title="单个插件" %}
npm install gitbook-plugin-accordion
{% endtab %}
{% endtabs %}

## 插件配置

我们以`favicon`插件为例，展示下如何配置

配置文档如下：[https://github.com/menduo/gitbook-plugin-favicon](https://github.com/menduo/gitbook-plugin-favicon)

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
