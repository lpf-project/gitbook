# 配置

## 目录结构

> 一个比较完整的目录结构如下

```
.
├── README.md
├── SUMMARY.md
├── book.json
├── package.json
├── part1
│   ├── README.md
│   ├── env.md
│   ├── gitbook.md
│   └── markdown.md
├── part2
│   ├── README.md
│   ├── command.md
│   ├── comment.md
│   ├── plugin.md
│   ├── questions.md
│   └── setting.md
├── part3
│   └── github.md
├── part4
│   └── help.md
├── images
└── styles
    └── website.css
```
**详细说明**

|文件|	重要性	|说明
|---|---|---|
|book.json	|可选，非常重要	|保存配置文件数据 详情
|README.md	|必选，重要	|简介，书籍的简单介绍 详情
|SUMMARY.md	|可选，非常重要	|目录，控制左边侧边栏 详情
|images	|可选，图片资源	|本地引用,相对根目录
|styles|可选，自定义样式 |book.json可以配置

> 下面会介绍下，gitbook如何进行一些简单的配置，优化体验，主要解决以下问题

- 默认项目结构或自定义项目结构
- 配置gitbook的基础信息、插件配置

```json
{
    "title": "title",
    "author": "",
    "description": "",
    "direction" : "ltr",
    "language" : "zh-hans",
    "links" : {
        "sidebar" : {
            "Home" : "https://github.com/dunwu/gitbook-notes"
        }
    },
    "root" : ".",
    "structure": {
        "readme": "README.md"
    },
    "styles": {
        "website": "style/common.css"
    },
    "plugins": [
        "remove-published-with-link",
        "anchor-navigation-ex",
        "back-to-top-button",
        "page-toc-button"
    ]
}
```



