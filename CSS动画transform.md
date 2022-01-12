# CSS动画transform
## 四个常用功能
* translate 位移
* scale 缩放
* rotate 旋转
* skew 倾斜
> * 一般都需要配合 transition 过渡
> * inline 元素不支持 transform，需先变成 block
## transform 之 translate
### 常用写法
  ``` css
  translateX(<length-percentage>)
  translateY(<length-percentage>)
  translate(<length-percentage>, <length-percentage>?)
  translateZ(<length>)且父容器 perspective
  translate3d(x,y,z)
  ```
  > translate(-50%, -50%) 可做绝对定位的居中

## transform 之 scale
### 常用写法
```css
scaleX(<number>)
scaleY(<number>)
scale(<number>,<number>?)
```
> 用的比较少，因为容易模糊

## transform 之 rotate
### 常用写法
```css
rotate([<angle> | <zero>])
rotateZ([<angle> | <zero>])
rotateX([<angle> | <zero>])
rotateY([<angle> | <zero>])
rotate3d 太复杂
```
> 一般用于360度旋转制作loading

## transition 过渡
### 语法
* transition:属性名 时长 过渡方式 延迟
```css
transition:left 200ms linear
```
* 可以用逗号分隔两个不同属性
```css
 transition:left 200ms,top 400ms
 ```
* 可以用all代表所有属性
```css
 transition:all 200ms
```
* 过渡方式有: linear | ease | ease-in | ease-out | ease-out | cubic-bezier | setp-start | step-end | steps

> ### 并不是所有属性都能过渡
> * display : none => block 没法过渡
> * 一般改成 visibility: hidden => visible
> * display 和 visibility 的区别
> > display和visibility都有讲元素隐藏的意思，但display隐藏的元素不占文档流，而visibility隐藏的元素仍然占文档流
> * background 颜色 和 opacity 透明度可以过渡
> ### 过渡必须要有起始
> 一般只有一次动画或者两次，比如hover和非hover状态的过渡。

### 过渡如果除了起始，还有中间点怎么办
* 办法一：使用两次 transform
* 办法二：使用animation
> * 声明关键帧
> * 添加动画
> ### animation 缩写语法
> * animation：时长 | 过渡方式 | 延迟 | 次数 | 方向 | 填充模式 | 是否暂停 | 动画名
> * 时长: 用秒s或者毫秒ms
> * 过渡方式：跟 transition 取值一样，如linear
> * 次数：3或者2.4或者 infinite
> * 方向：reverse | alternate | alternate-reverse
> * 填充模式：none | fowwards | backwards | both
> * 是否暂停：paused | running
> * 以上的所有属性都有对应的单独属性
> > 如何让动画停在最后一帧：加个forward
> ### @keyframes 完整语法
> #### 标准写法
> * 一种写法是from to
> * 另一种写法是百分数
> ```css
> .div{
>   animation: xxx 1.5s;
> }
> @keyframes xxx {
>   from { transform: translateX(0%) }
>   to { transform: translateX(100%) }
> }
> ```
> ```css
> @keyframes xxx {
>   0% { top: 0; left: 0% }
>   30% { top: 50px; }
>   68%,72% { left: 50px }
>   100% { top: 100px; left: 100px }
> }
> ```

