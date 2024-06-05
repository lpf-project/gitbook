
- https://dunwu.gitbooks.io/gitbook-notes/content/advanced/plugins.html

## 去除自带的插件

```
npm install gitbook-plugin-remove-published-with-link -D
```
配置
```json
{
    "title": "gitbook",
    "plugins": [
        "remove-published-with-link"
    ]
}
```