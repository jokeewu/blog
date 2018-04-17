---
title: parcel尝试打包多页应用
date: 2018-04-17 18:18:28
tags:
- 打包
---

如何安装及如何使用参见[parcel官网](http://www.parceljs.io/)。

新建文件_main.html(任意名称)

```html
<!DOCTYPE html>
<html>
<head>
  <title></title>
</head>
<body>
  <a href="index.html"></a>
  <a href="page1.html"></a>
  <a href="page2.html"></a>
  <!-- more -->
</body>
</html>
```

构建

```shell
parcel build _main.html
```

在实际开发中打包，本地开发环境搭建是比较繁琐复杂的事情。

就目前项目打包有如下需求：

- 针对不同的环境打包，替换对应的API根路径
	
	由于从parcel文档中可以看出还没有类似webpack DefinePlugin功能（创建一个在编译时可以配置的全局常量），目前可用方法，采用字符串替换，可通过gulp-replace。

- 打包成zip压缩包，便于部署
	
	针对此项需求采用gulp/gulp-zip实现




