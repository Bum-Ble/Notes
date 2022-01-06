# CSS基本概念
## 1. 文档流 Normal Flow 与 块、内联、内联块
> 注意：HTML 5 中已经抛弃了「内联元素」的概念，所有元素都可以通过 CSS 变成内联的
### 流动方向
* inline 元素从左到右，到达最右边才会换行
* block 元素从上到下，每一个都另起一行
* inline-block 也是从左到右
### 宽度
* inline 宽度为内部 inline 元素的和，不能用 width 指定
* block 默认自动计算宽度，可用width指定
* inline-block 结合前两者特点，可用width
### 高度
* inline 高度由 line-height 间接确定，跟 height 无关
* block 高度由内部文档流元素决定，可以设 height
* inline-block 跟 block 类似，可以设height
### 脱离文档流
* float
* position : absolute / fixed
* 
## 2. margin 合并
### 哪些情况会合并
* 父子 margin 合并
* 兄弟 margin 合并
### 如何阻止合并
* 父子合并用 padding / border 挡住
* 父子合并用 overflow : hidden 挡住
* 父子合并用 display : flex
* 兄弟合并是符合预期的
* 兄弟合并可以用 inline-block 消除

## 3. 两种盒模型box-sizing（border-box 更符合人类思维）
### 分别是
* content-box 内容盒 ： 内容就是盒子的边界
* border-box 边框盒 ： 框架才是盒子的边界
### 公式
* content-box width = 内容宽度
* border-box width = 内容宽度 + padding + border
