# flash-waimai
- 一个完整的外卖系统，包括手机端，后台管理，api
- 基于spring boot和vue的前后端分离的外卖系统
- 包含完整的手机端，后台管理功能
- 本项目主要供交流学习，不建议商用。
## 技术选型
- 核心框架：Spring Boot
- 数据库层：Spring data jpa/Spring data mongodb
- 数据库连接池：Druid
- 缓存：Ehcache
- 前端：Vue.js
- 数据库：mysql5.5以上,Mongodb4.0(不要使用最新版4.2)

## 模块
- flash-waimai-mobile 手机端站点
- flash-waimai-manage后台管理系统
- flash-waimai-api java接口服务
- flash-waimai-core 底层核心模块
- flash-waimai-generate 代码生成模块

## 快速开始
- 数据存储采用了mysql和mongodb，其中基础管理配置功能数据使用mysql，业务数据使用mongodb存储。
- 创建mysql数据库
```sql
    CREATE DATABASE IF NOT EXISTS waimai DEFAULT CHARSET utf8 COLLATE utf8_general_ci; 
    CREATE USER 'waimai'@'%' IDENTIFIED BY 'waimai123';
    GRANT ALL privileges ON waimai.* TO 'waimai'@'%';
    flush privileges;
```
- mysql数据库创建好了之后，启动flash-waimai-api服务，会自动初始化数据，无需开发人员自己手动初始化数据
- 安装mongodb并创建数据库:flash-waimai
使用mongorestore命令  导入mongodb数据,由于测试数据量较大，打包放在了百度云盘：链接：https://pan.baidu.com/s/1mfO7yckFL7lMb_O0BPsviw   提取码：apgd 下载后将文件解压到d:\\elm，如下命令导入数据：
                                              
```
mongorestore.exe -d flash-waimai d:\\elm
```
- 下载项目测试数据的图片（商家和食品图片）：链接：https://pan.baidu.com/s/1rvZDspoapWa6rEq2D_5kzw 提取码：urzw ，将图片存放到t_sys_cfg表中system.file.upload.path配置的目录下

- 启动管理平台:
    - 进入flash-waimai-manage目录：
    - 运行 npm install --registry=https://registry.npm.taobao.org
    - 运行npm run dev
    - 启动成功后访问 http://localhost:9528 ,登录，用户名密码:admin/admin
- 启动手机端:
    - 进入flash-waimai-mobile目录：    
    - 运行 npm install --registry=https://registry.npm.taobao.org
    - 运行npm run local
    - 启动成功后访问 http://localhost:8000

## 运行效果图
- 后台管理
![admin](doc/admin.gif)
- 手机端    
![mobile](doc/mobile.gif)

## 在线演示
- 查看演示系统请不要随意删除数据
- 后台管理：[http://waimai-admin.microapp.store](http://waimai-admin.microapp.store) [服务器资源不足，暂停演示]
- 手机端:[http://waimai-mobile.microapp.store](http://waimai-mobile.microapp.store) [服务器资源不足，暂停演示]

## 文档
[https://microapp.gitee.io/flash-waimai](https://microapp.gitee.io/flash-waimai)
## 开发进度
- flash-waimai-manage [初步完成]
- flash-waimai-mobile[完善中]

## 鸣谢
- 感谢[bailicangdu](https://github.com/bailicangdu),[enilu](https://github.com/enilu),本项目参考参考借鉴了[vue2-elm](https://github.com/bailicangdu/vue2-elm)，[web-flash](https://github.com/enilu/web-flash)，[vue2-manage](https://github.com/bailicangdu/vue2-manage)
- 该项目克隆并扩展自[web-flash](https://github.com/enilu/web-flash),所以开发的时候多看看web-flash的[在线文档](http://enilu.gitee.io/web-flash)
- 该项目不适用与商城系统解决方案，如果有商城系统需求，可以查看另外一个商城的开源系统[https://gitee.com/microapp/linjiashop](https://gitee.com/microapp/linjiashop)(支持H5,微信小程序,APP)

## 交流
- 关注公众号：嗨客帝国，点击flash-waimai菜单进群交流。

![公众号二维码](doc/img/haike.jpg)
