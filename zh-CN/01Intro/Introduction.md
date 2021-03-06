#概述
Lessgo 是一款Go 语言开发的简单、稳定、高效、灵活的 web开发框架。它的项目组织形式经过精心设计，实现前后端分离、系统与业务分离，完美兼容MVC与MVVC等多种开发模式，非常利于企业级应用与API接口的开发。当然，最值得关注的是它突破性地支持了运行时路由重建，开发者可在Admin后台轻松实现启用/禁用模块与操作，添加/移除中间件等功能！同时，它推荐以HandlerFunc与MiddlewareFunc为基础的函数式编程，也令开发变得更加灵活富有趣味性。
此外它也博采众长，核心架构基于[httprouter](https://github.com/julienschmidt/httprouter)并增强优化，数据库引擎内置为[xorm](https://github.com/go-xorm/xorm)和[gorm](https://github.com/jinzhu/gorm)，模板引擎内置为[pongo2](https://github.com/flosch/pongo2)，其他某些功能模块改写自[beego](https://github.com/astaxie/beego)以及其他优秀开源项目。（在此感谢这些优秀的开源项目）

#适用场景
- 网站
- web应用
- Restful API服务应用
- 企业应用

#主要特点:
- 使用简单、运行稳定高效
- 兼容流行系统模式如:MVC、MVVC、Restful...
- 强大的运行时路由重建
- 多异构数据库支持
- 优化的项目目录组织最佳实践，满足复杂企业应用需要
- swagger集成智能API文档
- 集成统一的日志
- SQLMAP方式的动态SQL配置执行API(开发中)
- 开箱即用的权限体系(计划)

#项目架构
![Lessgo Web Framework](https://github.com/henrylee2cn/lessgo/raw/master/doc/LessgoWebFramework.jpg)

#框架构成
- 核心框架：[lessgo](https://github.com/henrylee2cn/lessgo)
- 框架扩展：[lessgoext](https://github.com/henrylee2cn/lessgoext)
- 项目Demo：[demo](https://github.com/henrylee2cn/lessgoext)
- 框架文档  [document](https://github.com/henrylee2cn/lessgo_doc)

#框架下载

```sh
go get -u github.com/henrylee2cn/lessgo
go get -u github.com/henrylee2cn/lessgoext
```

#项目目录组织
─Project 项目开发目录  
├─Config 配置文件目录  
│  ├─app.config 系统应用配置文件  
│  └─db.config 数据库配置文件  
├─Common 后端公共目录  
│  ├─Middleware 中间件目录  
│  └─Model 数据模型  
│  └─... 其他  
├─Static 前端公共目录 (url: /static)  
│  ├─Tpl 公共tpl模板目录  
│  ├─Js 公共js目录 (url: /static/js)  
│  ├─Css 公共css目录 (url: /static/css)  
│  ├─Img 公共img目录 (url: /static/img)  
│  └─Plugin 公共js插件 (url: /static/plugin)  
├─SystemAPI 系统模块后端目录  
│  ├─SysRouter.go 系统模块路由文件  
│  ├─SysCommon 后端公共目录  
│  │  ├─Middleware 中间件目录  
│  │  └─Model 数据模型  
│  │  └─... 其他  
│  ├─Xxx Xxx子模块目录  
│  │  ├─ExampleHandle.go Example操作  
│  │  ├─ExampleModel.go Example数据模型及模板函数  
│  │  └─... Xxx的子模块目录  
│  └─... 其他子模块目录  
├─SystemView 系统模块前端目录 (url: /sys)  
│  ├─Xxx Xxx子模块目录 (url: /sys/xxx)  
│  │  ├─example.tpl ExampleHandle对应的模板文件  
│  │  ├─example2.html 无需绑定操作的静态html文件  
│  │  ├─xxx.css css文件(可有多个)  
│  │  ├─xxx.js js文件(可有多个)  
│  │  └─... Xxx的子模块目录  
├─BusinessAPI 业务模块后端目录  
│  ├─BusRouter.go 业务模块路由文件  
│  ├─BusCommon Business公共目录  
│  │  ├─Middleware 中间件目录  
│  │  └─Model 数据模型  
│  │  └─... 其他  
│  ├─Xxx Xxx子模块目录  
│  │  ├─ExampleHandle.go Example操作  
│  │  ├─ExampleModel.go Example数据模型及模板函数  
│  │  └─... Xxx的子模块目录  
│  └─... 其他子模块目录  
├─BusinessView 业务模块前端目录 (url: /bus)  
│  ├─Xxx Xxx子模块目录 (url: /bus/xxx)  
│  │  ├─example.tpl ExampleHandle对应的模板文件    
│  │  ├─example2.html 无需绑定操作的静态html文件  
│  │  ├─xxx.css css文件(可有多个)  
│  │  ├─xxx.js js文件(可有多个)  
│  │  └─... Xxx的子模块目录  
├─Uploads 默认上传下载目录  
├─Logger 运行日志输出目录  
└─Main.go 应用入口文件 

#贡献者名单
贡献者                          |贡献概要
--------------------------------|--------------------------------------------------
[henrylee2cn](https://github.com/henrylee2cn)|第一作者 (主要代码实现者) 
[changyu72](https://github.com/changyu72)|第二作者 (主要架构设计者) 

#开源协议
Lessgo 项目采用商业应用友好的 [MIT](https://github.com/henrylee2cn/lessgo/raw/master/doc/LICENSE) 协议发布。
 
#项目联系
* 官方QQ群：Go-Web 编程 42730308    [![Go-Web 编程群](http://pub.idqqimg.com/wpa/images/group.png)](http://jq.qq.com/?_wv=1027&k=fzi4p1)
![Lessgo Server](../img/server.jpg)
