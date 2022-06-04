# 宝塔面板第三方云端
这是一个用php开发的宝塔面板第三方云端站点程序。

你可以使用此程序搭建属于自己的宝塔面板第三方云端，实现最新版宝塔面板私有化部署，不与宝塔官方接口通信，满足隐私安全合规需求。同时还可以去除面板强制绑定账号，DIY面板功能等。

网站后台管理可一键同步宝塔官方的插件列表与增量更新插件包，还有云端使用记录、IP黑白名单、操作日志、定时任务等功能。

本项目自带的宝塔安装包和更新包是7.9.2最新版，已修改适配此第三方云端，并且全开源，无so等加密文件。

觉得该项目不错的可以给个Star~

## 声明

1.此项目只能以自用为目的，不得侵犯堡塔公司及其他第三方的知识产权和其他合法权利。

2.搭建使用此项目必须有一定的编程和Linux运维基础，纯小白不建议使用。

## 环境要求

* `PHP` >= 7.3
* `MySQL` >= 5.6
* `fileinfo`扩展
* `ZipArchive`扩展

## 部署方法

- [下载最新版的Release包](https://github.com/flucont/btcloud/releases)
- 设置网站运行目录为`public`
- 设置伪静态为`ThinkPHP`
- 导入`install.sql`到数据库
- 在`.env`里面修改数据库信息，包括数据库地址（HOSTNAME）、数据库名（DATABASE）、用户名（USERNAME）、密码（PASSWORD）
- 访问`/admin`进入网站后台，默认管理员用户名密码：admin/123456

## 使用方法

- 在`系统基本设置`修改宝塔面板接口设置。你需要一个官方最新脚本安装并绑定账号的宝塔面板，用于获取最新插件列表及插件包。并根据界面提示安装好专用插件。
- 在`定时任务设置`执行所显示的命令从宝塔官方获取最新的插件列表并批量下载插件包（增量更新）。当然你也可以去插件列表，一个一个点击下载。
- 在public/install/src和update文件夹里面分别是bt安装包和更新包，解压后源码里面全部的 www.example.com 替换成你自己搭建的云端域名，然后重新打包。可使用VSCode等支持批量替换的软件。
- 将bt安装脚本public/install/install_6.0.sh和更新脚本update6.sh里面的 www.example.com 替换成你自己搭建的云端域名。
- 访问网站`/download`查看使用此第三方云端的一键安装脚本

## 其他

- [bt官方更新包修改记录](./wiki/update.md)

  

