# JS数据类型
## JS 中的7种数据类型
总结：四基两空一对象
*  number 数字
*  string 字符串
* bool 布尔 
* symbol 符号 
* undefined  空 
*  null 空
* object 对象 

## 类型转换
 数字 => 字符串（ number => string ）
```js script
String(num)
num + '' //一般用这个
```
字符串 => 数字（ string => number ）
```js script
Number(str)
parseInt(str) / parseFloat(str)
str - 0 //一般用这个
```
任意 => 布尔（ x => bool ）
```js script
Boolean(x)
!!x //一般用这个
```
任意 => 字符串（ x => string ）
```js script
String(x)
x.toString()
```
注意：JS会有bug，类似的其他bug可以查看[JS秘密花园](http://bonsaiden.github.io/JavaScript-Garden/zh/#object.prototype)
```js script
2.toString() // 报错
(2).toString() // 不报错
2..toString() // 不报错
2 .toString() // 不报错
```

## 五个 falsy 值
falsy 就是相当于 false 但又不是 false 的值
* undefined 
* null
* 0
* NaN
* ''

## base64 转码
一般用来隐藏招聘启事里的简历，注意不能用来加密。
* 正常字符串转为 Base64 编码的字符串
```js 
window.btoa()
```
* Base64 编码的字符串转为原来的字符串
```js
window.atob()
```

## 小知识点
* UTF-8 是 Unicode 一种存储规则，也叫字符编码规则
* JS 的 number 全都是以小数（浮点数）的形式存储的，没有单独的整数
* 字符串 \n\t\r 的长度是 3