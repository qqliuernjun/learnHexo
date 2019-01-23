---
title: 知识点..
date: 2019-01-22 17:04:27
updated: 2019-01-23 23:12:11
tags: 零散知识点
categories: js
---

## npm中的qs
- qs.stringify()将对象 序列化成URL的形式，以&进行拼接
- qs.parse()将URL解析成对象的形式

##  深拷贝
1. _.assign({}, obj);
2. JSON.parse(JSON.stringify(obj))

## webpack
>可以使用 require.context() 方法来创建自己的（模块）上下文，这个方法有 3 个参数：要搜索的文件夹目录，是否还应该搜索它的子目录，以及一个匹配文件的正则表达式。

## common.js
>实质是整体加载fs模块（即加载fs的所有方法），生成一个对象（_fs），然后再从这个对象上面读取 3 个方法。这种加载称为“运行时加载”，因为只有运行时才能得到这个对象，导致完全没办法在编译时做“静态优化”。

## es6 Module
>上面代码的实质是从fs模块加载 3 个方法，其他方法不加载。这种加载称为“编译时加载”或者静态加载，即 ES6 可以在编译时就完成模块加载，效率要比 CommonJS 模块的加载方式高。当然，这也导致了没法引用 ES6 模块本身，因为它不是对象。

## proxy reflect
1. proxy修改某些对象的默认行为，进行一些拦截操作
2. reflect是对包含大部分Object prototype的方法，例如:如果使用object.defineProperty无法定义属性会抛异常，而reflect会返回false
3. 然后就是不需要使用try catch 

## webpack gulp
1. Grunt和Gulp的工作方式是：在一个配置文件中，指明对某些文件进行类似编译，组合，压缩等任务的具体步骤，工具之后可以自动替你完成这些任务。
2. Webpack的工作方式是：把你的项目当做一个整体，通过一个给定的主文件（如：index.js），Webpack将从这个文件开始找到你的项目的所有依赖文件，使用loaders处理它们，最后打包为一个（或多个）浏览器可识别的JavaScript文件。
3. Webpack的处理速度更快更直接，能打包更多不同类型的文件。

## 谷歌跨域
>"C:\Program Files (x86)\Google\Chrome\Application\chrome.exe" --args --disable-web-security --user-data-dir

## ! 与 !!
- 在if判断中(value)中的值会被转化为布尔值
- !val 将val转化为布尔值
- !!value 相当于直接判断value不等于 undefined || null || ""

## i++ ++i i-- --i

```                  
	var x = 3;
	y = x++; 
	// y = 3, x = 4

	var a = 2;
	b = ++a; 
	// a = 3, b = 3

	var x = 3; 
	y = x--; // y = 3, x = 2

	var a = 2; 
	b = --a; // a = 1, b = 1
```

>删除对象中的属性 `delete 对象.属性`