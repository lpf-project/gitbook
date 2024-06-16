# 命令

gitbook-cli 是gitbook的管理工具，而gitbook-cli对外暴露执行的指令是gitbook

> gitbook的指令，我们常用的也就2、3个

列出 gitbook 所有的命令

```
gitbook help
```

输出 gitbook-cli 的帮助信息

```
gitbook --help
```

本地编译并启动

```
gitbook serve
```

生成静态网页

```
gitbook build
```

列出本地所有的gitbook版本

```
gitbook ls
```

列出远程可用的gitbook版本

```
gitbook ls-remote
```

安装对应的gitbook版本

```
gitbook fetch 标签/版本号
```

更新到gitbook的最新版本

```
gitbook update
```

卸载对应的gitbook版本

```
gitbook uninstall 2.0.1
```

指定log的级别

```
gitbook build --log=debug
```

输出错误信息

```
gitbook build --debug
```