# SEO

**sitemap-general**

```json
{
    "plugins": ["sitemap-general"],
    "pluginsConfig": {
        "sitemap-general": {
            "prefix": "https://github.com/dunwu"
        }
    }
}
```



### sharing <a href="#sharing" id="sharing"></a>

```json
"pluginsConfig": {
    "sharing": {
        "weibo": true,
        "facebook": true,
        "twitter": true,
        "google": false,
        "instapaper": false,
        "vk": false,
        "all": [
            "facebook", "google", "twitter",
                "weibo", "instapaper"
        ]
    }
}
```

Google

```json
"plugins": [
    "ga"
 ],
"pluginsConfig": {
    "ga": {
        "token": "UA-XXXX-Y"
    }
}
```

Baidu

```json
{
    "plugins": ["3-ba"],
    "pluginsConfig": {
        "3-ba": {
            "token": "xxxxxxxx"
        }
    }
}
```

