# HTML全局属性
备注：如果对 HTML 全局属性不熟悉，搜索时在最后加上 MDN
## class
## hidden
## id
## style
## title
## contenteditable
是一个枚举属性，表示元素是否可被用户编辑。 如果可以，浏览器会修改元素的部件以允许编辑。
```html
<div contenteditable="true">
  <p>用户可以在这里可以进行编辑操作</p>
</div>
```
## tabindex
指示其元素是否可以聚焦，以及它是否/在何处参与顺序键盘导航（通常使用Tab键，因此得名）。
* tabindex 为 0 时，元素最后才被tab访问。
* tabindex 为 -1 时，元素不可被tab访问。
```html
<p tabindex="1">单击此窗格中的任意位置，然后尝试在元素之间切换</p>
<div tabindex="2">Tabbable due to tabindex.</div>
<div tabindex="0">Not tabbable: no tabindex.</div>
```
