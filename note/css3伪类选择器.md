#  伪类选择器

:not 选择除了text元素外的其它元素

``` css
input:nop[type="text"]{}
```

:empty 选择没有内容的元素

``` css
p:empty {}
```

:tatget 选择

?

:first-child 选择第一个子元素

```css
ol lo:first-child {}
```

:last-child

:nth-child(n) 第n个元素

``` css
ol:nth-child(3n){}   //三倍数的子元素,即可以使用表达式,n=1
ol:nth-child(odd){}  // 偶数
ol:nth-child(odd){}  //偶数
```

:nth-last-child(n) 倒数第几个

:first-of-type  选择第一个某类型

``` html
    <div class="wrapper">
      <div>我是一个块元素，我是.wrapper的第一个子元素</div>
      <p>我是一个段落元素，我是不是.wrapper的第一个子元素，但是他的第一个段落元素</p>
      <p>我是一个段落元素</p>
      <div>我是一个块元素</div>
```

``` css
.wrapper > p:first-of-type{}
```

:nth-of-type(n)

``` css
wrapper > p:nth-of-type(2n){}
```

:last-of-type(n) 倒数

:nth-last-of-type(n)倒数第几

:only-child 选择父元素中只有一个的子元素

:only-of-type 选择父元素中只有该一个类型的元素

:enabled 选择表单可用状态的元素

:disabled 选择不可用的

:checked 选中时的样式

::selection 选择鼠标双击选择的样式

:read-only 只读元素的样式

:read-write 非只读状态样式

::before 元素前插入内容 配合content

::after  元素后插入内容 配合content