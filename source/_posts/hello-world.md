---
title: 建立博客的过程
date: 2018-08-14 00:24:46
description: 通过hexo与码云pages建立自己的博客
keywords: hexo gitee pages
tag: 创建博客
categories: 博客相关
---
> 参考： https://hexo.io/zh-cn/docs/
## 安装hexo
```bash
 npm install -g hexo-cli
```
## 创建hexo项目
```bash
hexo init <folder>
cd <folder>
npm install
```
## 发布到giteePages相关配置

发布到giteePage需要修改根目录下_config.yml配置文件

``` YAML
# URL
## If your site is put in a subdirectory, set url as 'http://yoursite.com/child' and root as '/child/'
url: http://yoursite.com/child
root: /child/
permalink: :year/:month/:day/:title/
permalink_defaults:

# Deployment
## Docs: https://hexo.io/docs/deployment.html
deploy:
  type: git
  repo: https://gitee.com/你的项目/地址Url.git
```

## 打开归档、关于、分类等标签页
> 这些可以查阅even主题的文档 ： [https://github.com/ahonn/hexo-theme-even/wiki](https://github.com/ahonn/hexo-theme-even/wiki)

EG： 新建分类标签页
```bash
hexo new page categories
```
EG：新建文章

```bash
hexo new [layout] <title>
```
默认``layout``是 ``post``；

预计新建文章都是post的布局

## 注意点

- 文章属性 ``description`` 如果是中文，需要用引号，否则这页渲染不到
；后来发现也非必须；也不知当初那个错怎么触发的

给一篇文章配置多个tag
`tags: [vue, js, html]`

## 发布

### clean
清除缓存文件 (db.json) 和已生成的静态文件 (public)。

在某些情况（尤其是更换主题后），如果发现您对站点的更改无论如何也不生效，您可能需要运行该命令。
```bash
hexo clean
```
### deploy
部署网站
```bash
hexo deploy
```

|参数|描述|
|:--:|:--:|
|-g|--generate	部署之前预先生成静态文件|
该命令可以简写为：
```bash
hexo d
```
## 阅读次数添加
参考[https://lfwen.site/2016/05/31/add-count-for-hexo-next/](https://lfwen.site/2016/05/31/add-count-for-hexo-next/)

## 百度统计添加
参考 [https://www.jianshu.com/p/6eb068a68b17](https://www.jianshu.com/p/6eb068a68b17)