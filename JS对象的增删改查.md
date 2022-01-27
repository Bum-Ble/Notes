# JS对象的增删改查
## 删
删除属性
```js
delete obj.xxx
delete obj['xxx']
```
判断对象不含属性名
```js
'xxx' in obj === false
```
判断对象含有属性名，但是值为 undefined
```js
'xxx' in obj && obj.xxx === undefined
```
注意：
obj.xxx === undefined，不能用作断定 'xxx' 是否为 obj 的属性
## 读
查看自身所有属性
```js
Object.keys(obj)
```
查看自身+共有属性
```js
console.dir(obj)
// 或者自己依次用 Object.keys 打印出 obj.__proto__
```
判断一个属性是自身的还是共有的
```js
obj.hasOwnProperty('toString')
```
两种方法查看属性
* 中括号语法：
```js
obj['key']; 
obj[key] // 变量 key
```
* 点语法：obj.key

## 改
### 修改或增加属性（写属性）
* 直接赋值
* 批量赋值
```js
Object.assign(obj, {age: 18, gender: 'man'})
```
### 修改或增加共有属性
* 无法通过自身修改或增加共有属性
* 我偏要修改或增加原型上的属性
  ```js
  obj.__proto__.toString = 'xxx' // 不推荐用 __proto__
  Object.prototype.toString = 'xxx'
  ```
  一般来说，不要修改原型，会引起很多问题
### 修改隐藏属性(改原型)
* 不推荐使用 __proto__
```js
let obj = {name:'Bumble'}
let obj2 = {name: 'Tom'}
let common = {kind: 'human'}
obj.__proto__ = common
obj2.__proto__ = common
```
* 推荐使用 Object.create
 ```js
 let obj = Object.create(common)
obj.name = 'Bumble'
let obj2 = Object.create(common)
obj2.name = 'Tom'
 ```
 规范大概的意思是，要改就一开始就改，别后来再改

## 增
基本同上(同改)：已有属性则改；没有属性则增。