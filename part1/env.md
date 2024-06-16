# 环境要求 

gitbook开发时需要在node环境下，执行命令，所以本机要安装node

## 安装node环境

安装地址：https://nodejs.org/en/download/package-manager

这里根据电脑型号和开发者技术水平的不同有不同的安装方式，我们可以选择比较简单的前两种方式安装

- Package Manager: 包安装器
- Prebuilt Installer：dmg、exe，我们常用的软件安装方式
- Prebuilt Binaries：预编译库，需要一些自定义配置，适合有经验的研发
- Source Code：源码安装，适合运维经验丰富的研发安装

```bash
# installs nvm (Node Version Manager)
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash

# download and install Node.js
nvm install 20

```

## 查看安装的node和npm版本

```bash
# verifies the right Node.js version is in the environment
node -v # should print `v20.14.0`

# verifies the right NPM version is in the environment
npm -v # should print `10.7.0`
```

## 参考站点
- [node官网](https://nodejs.org/en)
- [github](https://github.com/)
- [git](https://www.git-scm.com/)
- [gitbook](https://www.gitbook.com/)

