# 利用yoeman react-webpack创建webapp

## 安装

`nmp install -g yo`
`nmp install -g generator-react-webpack`

## 创建项目
创建项目目录：`mkdir my-new-project && cd my-new-project`

运行generator：`yo react-webpack`

编辑`package.json`，例如描述、作者和其他相关信息

## 生成components
`yo react-webpack:component my/namespaced/components/name`
以上命令会生成一个新的component以及它默认的stylesheet和基本测试案例

## 生成一个新的无状态功能插件(stateless functional components)
`yo react-webpack:component my/namespaced/components/name --stateless`

[react官方讲解](https://facebook.github.io/react/blog/2015/10/07/react-v0.14.html)

## 添加一个PostCSS插件

例如添加autoprefixer
```
cd my-new-project
npm install autoprefixer
```

```
//在cfg/base.js中加载
...
postcss: function() {
	return [
		require('autoprefixer')({
			browsers: ['last 2 versions', 'ie >= 8']
		})
	];
}
...
```

## 使用方法
相关命令行：
```
//开启服务器
npm start 或者
npm run serve

//使用发行版开启开发者模式服务
npm run serve:dist

//只创建发行版本并且复制静态文件
npm run dist

//运行单元调试
npm test

//当文件改变的时候，自动运行单元调试
npm run test:watch

//验证所有src目录中的文件
npm run lint

//清除所有生产环境目录
npm run clean

//只复制静态资源
npm run copy
```

react-dev tools会在当前环境注册一个全局变量`__REACT_DEVTOOLS_GLOBAL_HOOK__`

autoprefixed-loader

json-loader

VCD原则：view controller data

CSS Modules, Radium

React Flux

React Animation API

React Canvas

React Native