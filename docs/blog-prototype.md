# 原型设计

`blog-prototype` 项目，有几个作用：

* 需求分析
* 整体界面的原型设计

## 原型界面

* index : 主页，含最新、最热文章，最热标签、最热用户等
	* /blogs
		* order: 排序类型， new/hot ， 默认是 new
		* tag : 博客标签，默认是空
	* ~~/blogs/{id} :具体某篇博客~~
		~~* id ：某篇博客的id~~
* user space : 用户主页空间
	* /u/{username} : 具体某个用户的主页
		* username : 用户账号
	* /u/{username}/blogs ： 查询用户博客，以下三个条件任选一个
		* order: 排序类型， new/hot ， 默认是 new
		* catalog : 博客分类 Id，默认是空
		* keyword : 搜索关键字。博客的标签，即为关键字
	* /u/{username}/blogs/edit : 获取编辑界面
	* /u/{username}/blogs/edit/{id} : 编辑某个博客
		* id : 博客的 id
* search ： 搜索
	* /search
		* q : 搜索关键字
	* /keywords : 最热搜索关键字列表
* login : 登录
	* /login  :GET 获取登录的界面
	* /login  :POST 登录
* register ：注册
	* /register :GET 获取注册的界面
	* /register :POST 注册 ， 注册成功跳转至 登录界面
* users : 用户管理
	* /users : 用户列表
	* /users/{id} :具体某个用户的主页
		* id ：某个用户的id