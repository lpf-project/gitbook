# 快速体验

## 快速安装

安装环境要求
- nodejs > v4.0.0，推荐v10.0.0以上
- Windows，Linux，Unix 或 Mac OS X

通过NPM安装

```
sudo npm i gitbook-cli -g
```

查看安装gitbook的版本

```
gitbook -V
```

## 创建项目

1、初始化

```
mkdir gitbook && cd gitbook
gitbook init
gitbook serve
```
目录结构见SUMMARY.md

2、打包构建
```
// 默认生成_book下
gitbook build
​// 打包到docs目录下
gitbook build ./ ./docs
```

## 常用命令

```
// 查看gitbook所有命令
gitbook help
// 启动本地服务器，默认打开localhost:4000，进行开发
gitbook serve
// 打包电子书为静态文件
gitbook build
```

## 注意事项

1). 执行`gitbook init`时，出现报错信息：

```
TypeError [ERR_INVALID_ARG_TYPE]: The "data" argument must be of type string or an instance of Buffer, TypedArray, or DataView. Received an instance of Promise
```
解决办法有两种：
- 1、node版本不匹配导致的，将node版本切换到`v12.0.0`即可
- 2、手动在根目录下创建`SUMMARY.md`，内容如下，然后再执行`gitbook init`

```md
# Summary

* [Introduction](README.md)
* [Part I](part1/README.md)
    * [GitBook is nice](part1/gitbook.md)
* [Part II](part2/README.md)
    * [Better tools for authors](part2/better_tools.md)
```
此时，我们可以看到当前项目的结构更新了

2). 执行`gitbook serve`时，出现报错信息：

```
/usr/local/lib/node_modules/gitbook-cli/node_modules/npm/node_modules/graceful-fs/polyfills.js:287
      if (cb) cb.apply(this, arguments)
                 ^
TypeError: cb.apply is not a function
```
解决方法：`sudo npm install gitbook-cli@2.1.2 --global`

参考：https://stackoverflow.com/questions/64211386/gitbook-cli-install-error-typeerror-cb-apply-is-not-a-function-inside-graceful
