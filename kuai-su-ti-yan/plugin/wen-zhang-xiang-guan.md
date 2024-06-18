# 文章相关

## anchors

添加 Github 风格的锚点样式

<div align="left">

<figure><img src="../../.gitbook/assets/image (1) (1).png" alt=""><figcaption></figcaption></figure>

</div>

## 导航

anchor-navigation-ex

添加锚点导航和回到顶部按钮

```json
{
    "plugins": [
        "anchor-navigation-ex"
    ],
    "pluginsConfig": {
        "anchor-navigation-ex": {
        "showLevel": false,
        "associatedWithSummary": true,
        "isRewritePageTitle": false,
        "float": {
          "showLevelIcon": false,
          "level1Icon": "fa fa-hand-o-right",
          "level2Icon": "fa fa-hand-o-right",
          "level3Icon": "fa fa-hand-o-right"
        },
        "pageTop": {
          "showLevelIcon": false,
          "level1Icon": "fa fa-hand-o-right",
          "level2Icon": "fa fa-hand-o-right",
          "level3Icon": "fa fa-hand-o-right"
        }
      },
    }
}
```

注意：目录为H1、H2、H3才可以生成目录

### simple-page-toc

> 回到顶部

### &#x20;edit-link <a href="#edit-link" id="edit-link"></a>

```json
{
    "plugins": ["edit-link"],
    "pluginsConfig": {
            "edit-link": {
                "base": "https://github.com/USER/REPO/edit/BRANCH",
                "label": "Edit This Page"
            }
    }
}
```

### &#x20;local-video <a href="#local-video" id="local-video"></a>

### todo

### expandable-chapters-small

> 折叠目录

### alertarea

配置：

```
{
    "plugins": ["alertarea"]
}
```

用法：

```
:::info
this is information
:::
```

展示：

<figure><img src="../../.gitbook/assets/image (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### 文章内目录

```
{
    "plugins": ["page-treeview"]
}
```

