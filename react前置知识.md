1、JS,CSS基础
2、Sass（CSS扩展语言）, Compass（基于Sass的二次扩展）
3、Yeoman（脚手架）, Grunt（自动化构建工具）, Webpack（前端模块管理和打包工具）
4、CommonJS, NodeJS（这两个标准库作为js的本地编程语言标准库）
5、Git, GitHub


yeoman bower grunt(build tool, buildy jasy gmake)

1. codekit

2. fis

3. spirit

ruby->gem python->pyopi, setuptools php->pear nodejs->npm


## NodeJS


## ruby
安装sass和compass都得先安装ruby开发环境，ruby通过gems管理包，可以通过https://rubygems.org直接搜索下载安装。国内连不上gems源。
直接安装sass或者compass会遇到ssl问题，可以考虑替换国内镜像源
gem sources -r https://rubygems.org
gem sources -a https://gems.ruby-china.org/



## Sass

### sass、compass和css的关系
compass是在compass基础上的二次开发


screen.scss文件称为宿主文件

申明变量：
$headline-ff: Braggadocio, Arial, Verdana, Helvetica, sans-serif;
$main-sec-ff: Arial, Verdona, Helvetica, sans-serif;

sass和scss的替换：
sass-convert main.scss main.sass

@import 导入
使用css原生@import的既定规则
1. 当@import后边跟的文件名是以.css结尾的时候；
2. 当@import后边跟的是http://开头的字符串的时候；
3. 当@import后边跟的是一个url()函数的时候；
4. 当@import后边带有media queries的时候。

基于sass的既定规则：
1. 没有文件后缀名的时候，sass会添加.scss或者.sass的后缀名；
2. 同一目录下，局部文件(下划线开头）和非局部文件不能重名。

变量操作
1、直接通过操作变量
2、通过函数
- 跟代码块无关的函数，多是自己内置函数，称functions
- 可重用的代码块，称mixin

sass的函数
http://sass-lang.com/documentation/Sass/Script/Functions.html

extend两个知识点
1. extend不可以继承选择器序列；
2. 使用%，用来构建只用来继承的选择器。

HSL颜色：

sass中的@media跟css区别：
sass中的media query可以内嵌在css规则中，在生成css的时候，media query才会被提到样式的最高层级。
好处：避免了重复书写选择器或者打乱样式表的流程。

在嵌套的时候使用sass的at-root指令，使嵌套样式输出到最外层样式表

css文件最后输出样式由output_style控制：expanded（默认），nested，compact，compressed

## Compass

compass核心模块之reset

Reset
@import "compass/reset"

Layout
@import "compass/layout"

CSS3

Helpers

Typography

Utilities


Normalize核心模块
base
html5
links
typography
embeds
groups
forms
tables


Reset核心Mixin
global-reset
nested-reset
reset-box-model
reset-font
reset-body
reset-html5
reset-list-style
reset-table
reset-table-cell
reset-quotation
reset-image-anchor-border
reset-display($selector, $important)
reset-focus

使用gem install compass-normalize
在config.rb中添加 require 'compass-normalize'
在scss中使用 @import "normalize"
或者只引入其中的几个模块 
@import "normalize-version" 必加
@import "normalize/html5"
...

layout模块使用率较低
@import "compass/layout/grid-background";
@import "compass/layout/sticky-footer"
@import "compass/layout/stretching"

CSS3模块及Browser Support模块（重要）

Typography模块（面子）

Helpers模块（里子）

Utilities模块


## React.js

1. JSX里的所有内容必须报在一个react对象里，否则会报错
2. 要获取某个子组件可以通过引用'ref'对应的属性；React.findDOMNode()可以获取实际的DOM元素，但官方并不推荐使用
3. react的事件函数中的event是在原生javascript的event类的基础上实现的react封装，拥有原生event的属性和方法