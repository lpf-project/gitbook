# Gitbook搭建

## 一、说明

示例地址：https://lpf-project.github.io/gitbook/

仓库地址：https://github.com/lpf-project/gitbook

Gitbook是个文档管理的工具，它有两种使用方式：
- 1.在[网站](https://www.gitbook.com/)注册账号使用
- 2.通过CLI工具进行构建，然后和Github进行关联

特点：
- 比较简单，但依赖科学上网，才可以方便使用
- 支持免费部署和独立部署，用markdown书写文档，方便导出电子书
- 支持响应式

## 二、安装使用

### 快速安装

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

### 创建项目

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

### 常用命令

```
// 查看gitbook所有命令
gitbook help
// 启动本地服务器，默认打开localhost:4000，进行开发
gitbook serve
// 打包电子书为静态文件
gitbook build
```

### 注意事项

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

## 三、结构

> 此时，我们的项目就搭建并且启动好了，我们来了解下当前项目的结构，学习下如何进行后续开发

```
.
├── README.md
├── SUMMARY.md
├── part1/
|   ├── README.md
|   └── gitbook.md
└── part2/
    ├── README.md
    └── better_tools.md
```
以下是一个包含文件描述的 Markdown 表格：

```markdown
| 文件         | 描述                           |
|--------------|-------------------------------|
| book.json    | 配置数据 (optional)           |
| README.md    | 电子书的前言或简介 (required) |
| SUMMARY.md   | 电子书目录 (optional)         |
| GLOSSARY.md  | 词汇/注释术语列表 (optional)  |
```

当然，也可以调整目录结构，将文件全部放在docs目录下，此时需要在`book.json`中配置

```json
{
    "root": "./docs"
}
```
调整目录结构为

```
.
├── book.json
└── docs
    ├── README.md
    ├── SUMMARY.md
    ├── part1
    │   ├── README.md
    │   └── gitbook.md
    └── part2
        ├── README.md
        └── better_tools.md
```
`SUMMARY.md`文件介绍

该文件为项目的目录结构和跳转地址