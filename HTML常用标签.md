# HTML常用标签
## a 标签
### 作用：
* 跳转外部页面    
* 跳转内部锚点（通过id实现）
* 跳转到邮箱或者电话（伪协议）
### 属性
* href：指定打开的链接
> #### 网址：
> * http://xxx.com
> * https://xxx.com
> * //xxx.com 最高级的，会自动选择协议
> #### 路径：
> 指的是以html的方式打开文件，跟文件操作的路径不一样。绝对路径前面有 / ，相对路径没有。
> * /a/b/c 以及 a/b/c
> * index.html 以及 ./index.html
> #### 伪协议:
> * javascript: 代码 ;
>> ``` html
>> <a href="javascript:alert(1);">伪协议</a>
>> <a href="javascript:;">不会跳转的 a 标签</a> 
>> <a href="">页面自动刷新</a>
>> <a href="#">页面回到最顶部</a>
>> ```
> * mailto: 邮箱
> * tel: 手机号
> #### 取值为id：
> * href = "#xxx"
> > ```html
> > <a href="#idName">跳转到指定标签</a>
> > ```
* target：设定在哪个窗口打开链接
>#### 内置名字
> * _blank ：新开一个标签打开链接
> * _self ： 默认是在当前页面实现跳转，效果跟留空是一样的
> * _parent ：在当前链接所在的iframe的上一层打开
> * _top ：在当前页面最顶层打开，这里存在一个层级关系
> #### 程序员命名
> 设定一个窗口的名字，点击链接时，浏览器会检测是否存在这个名字的窗口如果没有，就新建一个
> * window 的 name
> * iframe 的 name
> >```html
> > <a href="//baidu.com" target="xxx">go to Baidu</a><br>
> > <a href="//google.com" target="xxx">go to Google</a>
> >```
* download 下载网页，不是所有浏览器都支持，尤其是手机浏览器可能不支持
* rel = noopener 暂时不用，到js后会用到
  
## iframe 标签
内嵌窗口，已经很少使用了，还有些老系统在用。
>```html
><a href="//baidu.com" target="xxx">go to Baidu</a><br>
><a href="//google.com" target="xxx">go to Google</a>
><iframe stle="border:none;width:900px;height:500px" src="" name="xxx"></iframe>
>```

## table标签
展示表格
### 属性
* table
* thead
* tbody
* tfoot
* tr (意思是table-row)
* td (意思是table-data)
* th (意思是table-head)
```html
<table>
  <thead>
    <tr>
      <th>英语</th>
      <th>翻译</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>target</td>
      <td>目标</td>
    </tr>
    <tr>
      <td>reference</td>
      <td>引用</td>
    </tr>
  </tbody>
  <tfoot>
    <td>空</td>
    <td>空</td>
  </tfoot>
</table>
```
#### 代码结果：
![代码结果](https://github.com/Bum-Ble/Notes/blob/main/images/table.png)
### 样式
* table-layout :
  - auto : 根据内容自动设置单元格大小
  - fixed : 根据设置好的单元格大小自动分配单元格的大小
* border-collapse ： 单元格边框合并
* border-spacing ： 单元格边框间隔

## img标签
