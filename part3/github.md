# 通过Github部署Gitbook，提供静态站点

> 这里我么提供一个搭建个人站点的方法，通过部署Github Page来免费搭建自己的博客。

## 了解Github action

Github action可以提供CI/CD部署的自动化流程，而且他集成了很多公用的库，可以帮助你快速的部署自己的服务。

## 如何使用Github action

在根目录的`.github/workflows`下新建文件`jekyll-gh-pages.yml`


```yml
# Sample workflow for building and deploying a Jekyll site to GitHub Pages
name: Deploy Jekyll with GitHub Pages dependencies preinstalled

on:
  # Runs on pushes targeting the default branch
  push:
    branches: ["main"]

  # Allows you to run this workflow manually from the Actions tab
  workflow_dispatch:

# Sets permissions of the GITHUB_TOKEN to allow deployment to GitHub Pages
permissions:
  contents: read
  pages: write
  id-token: write

# Allow only one concurrent deployment, skipping runs queued between the run in-progress and latest queued.
# However, do NOT cancel in-progress runs as we want to allow these production deployments to complete.
concurrency:
  group: "pages"
  cancel-in-progress: false

jobs:
  # Build job
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v4
        
      - name: Setup Node.js
        uses: actions/setup-node@v3
        with:
          node-version: '14' # 或者你需要的其他版本

      - name: Install GitBook CLI
        run: sudo npm install gitbook-cli@2.1.2 --global

      - name: Install GitBook plugins
        run: gitbook install

      - name: Build with GitBook
        run: gitbook build

      - name: Setup Pages
        uses: actions/configure-pages@v5

      - name: Copy _book to _site
        run: cp -r _book ./_site

      - name: Upload artifact
        uses: actions/upload-pages-artifact@v3
        with:
          path: ./_site

  # Deployment job
  deploy:
    environment:
      name: github-pages
      url: ${{ steps.deployment.outputs.page_url }}
    runs-on: ubuntu-latest
    needs: build
    steps:
      - name: Deploy to GitHub Pages
        id: deployment
        uses: actions/deploy-pages@v4

```