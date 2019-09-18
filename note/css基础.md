# css基础

## css样式

- 1. 内联式css样式   直接写在现有的html标签中。

- 并且css样式代码要写在style=""双引号中，如果有多条css样式代码设置可以写在一起，中间用分号隔开。如下代码：

- 1. 嵌入式css样式，写在当前的文件中。

- 写在head中的<style  type="text/css"></style>内

- 1. 外部式css样式，写在单独一个文件中。

- <link href="base.css"  rel="stylesheet" type="text/css" />

- *rel和type均为固定写法，****不可更改****。*

- 1. 三种方法优先级，一般而言是内联式>嵌入式>外部式 （不考虑权值）

- 实际是根据位置关系，若外部式的link在style后，优先级则会变为外部式优先，其实总结来说，就是--就近原则（**离被设置元素越近优先级别越高**）。

## CSS选择器

- 1. 标签选择器 p{}
  2. 类选择器   .a{}
  3. ID选择器   #a{}

- 1. 子选择器 .food>li{} 用于选择指定元素的第一代子元素
  2. 后代选择器       .first span{} 用于指定元素下的**后辈元素****(****所有子后代元素****)**

- *子选择器仅是指它的****直接后代（第一代后代）****，后代选择器作用于所有子后代元素，后代选择器通过****空格****来进行选择，而子选择器通过**"**>**"*

- 1. 通用选择器 *{}
  2. 伪类选择器 a:hover{}       
  3. 分组选择器 .first,#second       span{}

## 继承

- 1. 标签的权值为1，类选择符的权值为10，ID选择符的权值最高为100。  

- p{color:red;} **/\*权值为1\*/**
     p span{color:green;} **/\*权值为1+1=2\*/**
     .warning{color:white;} **/\*权值为10\*/**
     p span .warning{color:purple;} **/\*权值为1+1+10=12\*/**
     \#footer .note p{color:yellow;} **/\*权值为100+10+1=111\*/**

- 继承权重可理解为0.01，即最低。

- 1. 当多个css样式具有相同权重时，则根据css样式的前后顺序来决定。（后覆盖前）
  2. 重要性 p{color:red       **!important**;}  注意important写在分号";"前

## 文字排版

- 1. 字体 font-family:"微软雅黑","Microsoft YaHei",Helvetica";

- 1. 字号 font-size:20px; 
  2. 颜色       color:#eee;
  3. 粗体 font-weight:700;
  4. 斜体       font-style:**italic**;
  5. 下划线 text-decoration:underline;
  6. 删除线 text-decoration:**line-through**;

## 段落排版

- 1. 缩进 p{text-indent:2em;}  2em是文字的2倍大小
  2. 行间距 p{line-height:1.5em;}         em可省略
  3. 中文字/字母间距 letter-spacing:50px;  单词间距       word-spacing:50px;

- 1. 对齐 text-align:center/right/left;