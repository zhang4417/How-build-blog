# 如何用hugo搭建个人博客
## install hugo（安装HUGO）
   
    $ hugo version

    若提示出现版本号，则安装成功了

## 创建路径

    $ hugo new site 你的用户名.github.io-creator

## 添加主题

    $ cd 你的用户名.github.io-creator

    $ git init

    $ git submodule add https://github.com/budparr/gohugo-theme-ananke.git themes/ananke

    $ echo 'theme = "ananke"' >> config.toml
## 添加内容

    $ hugo new posts/my-first-post.md

    $ code .
    编辑下面内容，最后将true改为false
    ---
    title: "My First Post"
    date: 2019-03-26T08:47:11+01:00
    draft: true
    ---

## 预览
    $ hugo server -D
    ctrl+单击(http://localhost:1313/)预览

## 修改语言
    打开config.toml
    将en改成zh-Hans
    改title

## 建立静态网页

    $ hugo

    新建一个 .gitignore文件，里面填写public

    $ cd public
    $ git init
    $ git add .
    $ git commit

    复制你新建远程仓库“你的用户名.github.creator.io”里面的两行内容，刷新。
    $ git remote add origin git@github.com:XXXXXXXXXXX
    $ git push -u origin master
