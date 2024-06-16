# 全文检索

### search-plus

支持中文搜索, 需要将默认的 `search` 和 `lunr` 插件去掉。

```json
{
    "plugins": ["-lunr", "-search", "search-plus"]
}
```

### github

显示一个Github跳转地址

```json
{
    "plugins": [ "github" ],
    "pluginsConfig": {
        "github": {
            "url": "https://github.com/your/repo"
        }
    }
}
```
