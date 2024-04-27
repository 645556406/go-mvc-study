## go-mvc-study的架构说明

> Go Web开发GoFrame+Vue+ElementUI框架实战教程

### 1. 项目结构  
```
├── app             // 应用目录
│   ├── controller  // 控制器
│   ├── dao         // DAO层
│   ├── model       // 模型层
│   └── service     // 服务层
│   └── utils       // 系统工具
├── boot
├── config          // 系统配置
├── docker
├── document        // 文档目录
├── i18n            // 国际化
├── library         // 类库
├── packed
├── public          // 资源目录
├── router          // 路由
├── template        // 自定义模板
├── Dockerfile
├── go.mod
└── main.go
```

### 2. 项目介绍

```html
项目介绍
一款 Go 语言基于GoFrame、Vue、ElementUI、MySQL等框架精心打造的一款模块化、插件化、高性能的前后端分离架构敏捷开发框架，可快速搭建前后端分离后台管理系统，本着简化开发、提升开发效率的初衷，框架自研了一套个性化的组件，实现了可插拔的组件式开发方式，同时为了敏捷快速开发，框架特地集成了代码生成器，完全自主研发了自定义GO后端服务模板和前端Vue自定义模板，可以根据已建好的表结构，可以快速的一键生成整个模块的所有代码和增删改查等等功能业务，真正实现了低代码开发方式，极大的节省了人力成本的同时提高了开发效率，缩短了研发周期，是一款真正意义上实现组件化、可插拔式的敏捷开发框架。

项目特点
模块化、松耦合
模块丰富、开箱即用
简洁易用、快速接入
文档详尽、易于维护
自顶向下、体系化设计
统一框架、统一组件、降低选择成本
开发规范、设计模式、代码分层模型
强大便捷的开发工具链
完善的本地中文化支持
设计为团队及企业使用
内置模块
用户管理：用于维护管理系统的用户，常规信息的维护与账号设置。
角色管理：角色菜单管理与权限分配、设置角色所拥有的菜单权限。
菜单管理：配置系统菜单，操作权限，按钮权限标识等。
职级管理：主要管理用户担任的职级。
岗位管理：主要管理用户担任的岗位。
部门管理：主要管理系统组织架构，对组织架构进行统一管理维护。
操作日志：系统正常操作日志记录和查询；系统异常信息日志记录和查询。
登录日志：系统登录日志记录查询包含登录异常。
字典管理：对系统中常用的较为固定的数据进行统一维护。
配置管理：对系统的常规配置信息进行维护，网站配置管理功能进行统一维护。
城市管理：统一对全国行政区划进行维护，对其他模块提供行政区划数据支撑。
友链管理：对系统友情链接、合作伙伴等相关外链进行集成维护管理的模块。
个人中心：主要是对当前登录用户的个人信息进行便捷修改的功能。
广告管理：主要对各终端的广告数据进行管理维护。
站点栏目：主要对大型系统网站等栏目进行划分和维护的模块。
会员管理：对各终端注册的会员进行统一的查询与管理的模块。
网站配置：对配置管理模块的数据源动态解析与统一维护管理的模块。
通知公告：系统通知公告信息发布维护。
代码生成：一键生成模块CRUD的功能，包括后端Go和前端Vue等相关代码。
案例演示：常规代码生成器一键生成后的演示案例。
软件信息
软件名称：EasyGoAdmin敏捷开发框架GoFrame+EleVue版本
官网网址：http://www.easygoadmin.vip
文档网址：http://docs.goframe.elevue.easygoadmin.vip
系统演示
演示地址：http://manage.goframe.elevue.easygoadmin.vip

版本说明
版本名称	版本说明	版本地址
GoFrame+Layui混编版	采用GoFrame、Layui等框架研发	https://gitee.com/easygoadmin/EasyGoAdmin_GoFrame_Layui
Beego+Layui混编版	采用Beego、Layui等框架研发	https://gitee.com/easygoadmin/EasyGoAdmin_Beego_Layui
Gin+Layui混编版	采用Gin、Layui等框架研发	https://gitee.com/easygoadmin/EasyGoAdmin_Gin_Layui
Iris+Layui混编版	采用Iris、Layui等框架研发	https://gitee.com/easygoadmin/EasyGoAdmin_Iris_Layui
Revel+Layui混编版	采用Revel、Layui等框架研发	https://gitee.com/easygoadmin/EasyGoAdmin_Revel_Layui
Echo+Layui混编版	采用Echo、Layui等框架研发	https://gitee.com/easygoadmin/EasyGoAdmin_Echo_Layui
GoFrame+EleVue前后端分离版	采用GoFrame、Vue、ElementUI等框架研发前后端分离版本	https://gitee.com/easygoadmin/EasyGoAdmin_GoFrame_EleVue
Beego+EleVue前后端分离版	采用Beego、Vue、ElementUI等框架研发前后端分离版本	https://gitee.com/easygoadmin/EasyGoAdmin_Beego_EleVue
Gin+EleVue前后端分离版	采用Gin、Vue、ElementUI等框架研发前后端分离版本	https://gitee.com/easygoadmin/EasyGoAdmin_Gin_EleVue
Iris+EleVue前后端分离版	采用Iris、Vue、ElementUI等框架研发前后端分离版本	https://gitee.com/easygoadmin/EasyGoAdmin_Iris_EleVue
Revel+EleVue前后端分离版	采用Revel、Vue、ElementUI等框架研发前后端分离版本	https://gitee.com/easygoadmin/EasyGoAdmin_Revel_EleVue
Echo+EleVue前后端分离版	采用Echo、Vue、ElementUI等框架研发前后端分离版本	https://gitee.com/easygoadmin/EasyGoAdmin_Echo_EleVue
GoFrame+AntdVue前后端分离版	采用GoFrame、Vue、AntDesign等框架研发前后端分离版本	https://gitee.com/easygoadmin/EasyGoAdmin_GoFrame_AntdVue
Beego+AntdVue前后端分离版	采用Beego、Vue、AntDesign等框架研发前后端分离版本	https://gitee.com/easygoadmin/EasyGoAdmin_Beego_AntdVue
Gin+AntdVue前后端分离版	采用Gin、Vue、AntDesign等框架研发前后端分离版本	https://gitee.com/easygoadmin/EasyGoAdmin_Gin_AntdVue
Iris+AntdVue前后端分离版	采用Iris、Vue、AntDesign等框架研发前后端分离版本	https://gitee.com/easygoadmin/EasyGoAdmin_Iris_AntdVue
Revel+AntdVue前后端分离版	采用Revel、Vue、AntDesign等框架研发前后端分离版本	https://gitee.com/easygoadmin/EasyGoAdmin_Revel_AntdVue
Echo+AntdVue前后端分离版	采用Echo、Vue、AntDesign等框架研发前后端分离版本	https://gitee.com/easygoadmin/EasyGoAdmin_Echo_AntdVue


```

```go
func init() {
	s := g.Server()
	// 跨域处理
	s.Use(middleware.CORS)
	// 登录验证中间件
	s.Use(middleware.CheckLogin)
	// 操作日志中间件
	s.Use(middleware.OperLog)
	// 登录日志中间件
	s.Use(middleware.LoginLog)

	/* 文件上传 */
	s.Group("/upload", func(group *ghttp.RouterGroup) {
		// 上传图片
		group.POST("/uploadImage", controller.Upload.UploadImage)
	})

	/* 登录注册 */
	s.Group("/", func(group *ghttp.RouterGroup) {
		group.GET("/", controller.Login.Login)
		group.ALL("/login", controller.Login.Login)
		group.GET("/captcha", controller.Login.Captcha)
		group.ALL("/updateUserInfo", controller.Index.UpdateUserInfo)
		group.ALL("/updatePwd", controller.Index.UpdatePwd)
		group.GET("/logout", controller.Index.Logout)
	})

	s.Group("index", func(group *ghttp.RouterGroup) {
		group.GET("/menu", controller.Index.Menu)
		group.GET("/user", controller.Index.User)
	})

	/* 用户管理 */
	s.Group("user", func(group *ghttp.RouterGroup) {
		group.GET("/list", controller.User.List)
		group.GET("/detail", controller.User.Detail)
		group.POST("/add", controller.User.Add)
		group.PUT("/update", controller.User.Update)
		group.DELETE("/delete/:ids", controller.User.Delete)
		group.PUT("/status", controller.User.Status)
		group.PUT("/resetPwd", controller.User.ResetPwd)
		group.GET("/checkUser", controller.User.CheckUser)
	})

	/* 职级管理 */
	s.Group("level", func(group *ghttp.RouterGroup) {
		group.GET("/list", controller.Level.List)
		group.POST("/add", controller.Level.Add)
		group.PUT("/update", controller.Level.Update)
		group.DELETE("/delete/:ids", controller.Level.Delete)
		group.PUT("/status", controller.Level.Status)
		group.GET("/getLevelList", controller.Level.GetLevelList)
	})

	/* 岗位路由 */
	s.Group("position", func(group *ghttp.RouterGroup) {
		group.GET("/list", controller.Position.List)
		group.POST("/add", controller.Position.Add)
		group.PUT("/update", controller.Position.Update)
		group.DELETE("/delete/:ids", controller.Position.Delete)
		group.PUT("/status", controller.Position.Status)
		group.GET("/getPositionList", controller.Position.GetPositionList)
	})

	/* 角色路由 */
	s.Group("role", func(group *ghttp.RouterGroup) {
		group.GET("/list", controller.Role.List)
		group.POST("/add", controller.Role.Add)
		group.PUT("/update", controller.Role.Update)
		group.DELETE("/delete/:ids", controller.Role.Delete)
		group.PUT("/status", controller.Role.Status)
		group.GET("/getRoleList", controller.Role.GetRoleList)
	})

	/* 角色菜单权限 */
	s.Group("rolemenu", func(group *ghttp.RouterGroup) {
		group.GET("/index", controller.RoleMenu.Index)
		group.POST("/save", controller.RoleMenu.Save)
	})

	/* 部门管理 */
	s.Group("dept", func(group *ghttp.RouterGroup) {
		group.GET("/list", controller.Dept.List)
		group.POST("/add", controller.Dept.Add)
		group.PUT("/update", controller.Dept.Update)
		group.DELETE("/delete/:ids", controller.Dept.Delete)
		group.GET("/getDeptList", controller.Dept.GetDeptList)
	})

	/* 菜单管理 */
	s.Group("menu", func(group *ghttp.RouterGroup) {
		group.GET("/list", controller.Menu.List)
		group.GET("/detail", controller.Menu.Detail)
		group.POST("/add", controller.Menu.Add)
		group.PUT("/update", controller.Menu.Update)
		group.DELETE("/delete/:ids", controller.Menu.Delete)
	})

	/* 操作日志 */
	s.Group("operlog", func(group *ghttp.RouterGroup) {
		group.GET("/list", controller.OperLog.List)
	})

	/* 登录日志 */
	s.Group("loginlog", func(group *ghttp.RouterGroup) {
		group.GET("/list", controller.LoginLog.List)
		group.DELETE("/delete/:ids", controller.LoginLog.Delete)
	})

	/* 城市管理 */
	s.Group("city", func(group *ghttp.RouterGroup) {
		group.GET("/list", controller.City.List)
		group.POST("/add", controller.City.Add)
		group.PUT("/update", controller.City.Update)
		group.DELETE("/delete/:ids", controller.City.Delete)
		group.POST("/getChilds", controller.City.GetChilds)
	})

	/* 字典管理 */
	s.Group("dict", func(group *ghttp.RouterGroup) {
		group.GET("/list", controller.Dict.List)
		group.POST("/add", controller.Dict.Add)
		group.PUT("/update", controller.Dict.Update)
		group.DELETE("/delete/:ids", controller.Dict.Delete)
	})

	/* 字典项管理 */
	s.Group("dictdata", func(group *ghttp.RouterGroup) {
		group.GET("/list", controller.DictData.List)
		group.POST("/add", controller.DictData.Add)
		group.PUT("/update", controller.DictData.Update)
		group.DELETE("/delete/:ids", controller.DictData.Delete)
	})

	/* 配置管理 */
	s.Group("config", func(group *ghttp.RouterGroup) {
		group.GET("/list", controller.Config.List)
		group.POST("/add", controller.Config.Add)
		group.PUT("/update", controller.Config.Update)
		group.DELETE("/delete/:ids", controller.Config.Delete)
	})

	/* 配置项管理 */
	s.Group("configdata", func(group *ghttp.RouterGroup) {
		group.GET("/list", controller.ConfigData.List)
		group.POST("/add", controller.ConfigData.Add)
		group.PUT("/update", controller.ConfigData.Update)
		group.DELETE("/delete/:ids", controller.ConfigData.Delete)
		group.PUT("/status", controller.ConfigData.Status)
	})

	/* 友链管理 */
	s.Group("link", func(group *ghttp.RouterGroup) {
		group.GET("/list", controller.Link.List)
		group.POST("/add", controller.Link.Add)
		group.PUT("/update", controller.Link.Update)
		group.DELETE("/delete/:ids", controller.Link.Delete)
		group.PUT("/status", controller.Link.Status)
	})

	/* 站点管理 */
	s.Group("item", func(group *ghttp.RouterGroup) {
		group.GET("/list", controller.Item.List)
		group.POST("/add", controller.Item.Add)
		group.PUT("/update", controller.Item.Update)
		group.DELETE("/delete/:ids", controller.Item.Delete)
		group.PUT("/status", controller.Item.Status)
		group.GET("/getItemList", controller.Item.GetItemList)
	})

	/* 栏目管理 */
	s.Group("itemcate", func(group *ghttp.RouterGroup) {
		group.GET("/list", controller.ItemCate.List)
		group.POST("/add", controller.ItemCate.Add)
		group.PUT("/update", controller.ItemCate.Update)
		group.DELETE("/delete/:ids", controller.ItemCate.Delete)
		//group.GET("/getCateTreeList", controller.ItemCate.GetCateTreeList)
		group.GET("/getCateList", controller.ItemCate.GetCateList)
	})

	/* 广告位管理 */
	s.Group("adsort", func(group *ghttp.RouterGroup) {
		group.GET("/list", controller.AdSort.List)
		group.POST("/add", controller.AdSort.Add)
		group.PUT("/update", controller.AdSort.Update)
		group.DELETE("/delete/:ids", controller.AdSort.Delete)
		group.GET("/getAdSortList", controller.AdSort.GetAdSortList)
	})

	/* 广告管理 */
	s.Group("ad", func(group *ghttp.RouterGroup) {
		group.GET("/list", controller.Ad.List)
		group.POST("/add", controller.Ad.Add)
		group.PUT("/update", controller.Ad.Update)
		group.DELETE("/delete/:ids", controller.Ad.Delete)
		group.PUT("/status", controller.Ad.Status)
	})

	/* 通知管理 */
	s.Group("notice", func(group *ghttp.RouterGroup) {
		group.GET("/list", controller.Notice.List)
		group.POST("/add", controller.Notice.Add)
		group.PUT("/update", controller.Notice.Update)
		group.DELETE("/delete/:ids", controller.Notice.Delete)
		group.PUT("/status", controller.Notice.Status)
	})

	/* 网站设置 */
	s.Group("configweb", func(group *ghttp.RouterGroup) {
		group.GET("/index", controller.ConfigWeb.Index)
		group.PUT("/save", controller.ConfigWeb.Save)
	})

	/* 会员等级 */
	s.Group("memberlevel", func(group *ghttp.RouterGroup) {
		group.GET("/list", controller.MemberLevel.List)
		group.POST("/add", controller.MemberLevel.Add)
		group.PUT("/update", controller.MemberLevel.Update)
		group.DELETE("/delete/:ids", controller.MemberLevel.Delete)
		group.GET("/getMemberLevelList", controller.MemberLevel.GetMemberLevelList)
	})

	/* 会员管理 */
	s.Group("member", func(group *ghttp.RouterGroup) {
		group.GET("/list", controller.Member.List)
		group.POST("/add", controller.Member.Add)
		group.PUT("/update", controller.Member.Update)
		group.DELETE("/delete/:ids", controller.Member.Delete)
		group.PUT("/status", controller.Member.Status)
	})

	/* 统计分析 */
	s.Group("analysis", func(group *ghttp.RouterGroup) {
		group.GET("/index", controller.Analysis.Index)
	})

	/* 代码生成器 */
	s.Group("generate", func(group *ghttp.RouterGroup) {
		group.GET("/list", controller.Generate.List)
		group.POST("/generate", controller.Generate.Generate)
		group.POST("/batchGenerate", controller.Generate.BatchGenerate)
	})
}

```
# go-mvc-study
