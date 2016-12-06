#display

display默认值是`block`或`inline`

##块级元素block

`div`是一个标准的块级元素,一个块级元素会重新开始一行并且尽可能撑满容器,常用的块级元素包括`p`,`form`和HTML5新元素`header`、`footer`、`section`

##inline

`span`是标准的行内元素,一个行内元素可以在段落中<span>像这样</span>包裹一些文字而不会打乱段落的布局,`a`是最常见的行内元素

##none

`display:none`通常被JavaScript用来在不删除元素的情况下隐藏活显示元素,和`visibility`属性不一样,把display设置成`none`不会保留元素本该显示的空间。

#margin
设置块级元素的width可以阻止它从左到右撑满容器,margin:auto可以使其居中
```css
#main {
    width: 600px;
    margin: 0 auto;
}
```

#max-width

max-width可以使页面更好的处理小窗口情况

#box-sizing

`box-sizing: border-box` 时内边距和边框不在会增加它的宽度

```
.simple {
    width: 500px;
    -webkit-box-sizing: borde-box;
    -moz-box-sizing: border-box;
    box-sizing: border-box;
}
.fancy {
    width: 500px;
    margin: 20px auto;
    padding: 50px;
    -webkit-box-sizing: borde-box;
    -moz-box-sizing: border-box;
    box-sizing: border-box;
}
```

#position
##static

`postion: static`是默认值,表示该元素不会被特殊定位

##relative

`postion: relative`不设置其他值的时候和`static`一样
在元素上设置`top`、`right`、`bottom`、`left`会使其偏离正常的位置,其他的元素不会调整位置来弥补它偏离剩下的空隙

##fixed

一个固定定位相对视窗来定位,意味着元素即便页面滚动它还是会停留在相同的位置。

##absolute

`absolute`和`fixed`的表现类似,它相对它的父元素的定位

#float

`float`可用实现文字环绕图片

##clear

clear被用于控制浮动将段落移动到浮动元素下面

##overflow

当浮动元素比包含它的元素要搞,会溢出容器外,使用`overflow`可以先出浮动
在IE6下还需要增加
```css
.clearfix {
    overflow: auto;
    zoom: 1;
}
```

##百分比宽度

百分比是一种块包含块的计量单位
```css
.image {
    width: 50%;
}
```

#媒体查询

针对不同设备响应不同的显示效果

```css
@media screen and (min-width: 600px) {

}

@media screen and (max-width: 599px) {

}
```
使用`meta viewport`之后可以在移动浏览器上显示的更好

#inline-block

使用`inline-block`创建很多网格来铺满浏览器会很简单
`vertical-align`属性会影响到`inline-block`元素


#column

`column`可以实现文字的多列布局
```css
{
      -moz-column-count: 3;
      -moz-column-gap: 1em;
      -webkit-column-count: 3;
      -webkit-column-gap: 1em;
      column-count: 3;
      column-gap: 1em;
}
```

#flexbox
