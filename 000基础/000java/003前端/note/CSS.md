# CSS

层叠级联样式表

![](..\img\2-1.png)

格式

![](..\img\2-2.png)

## 导入方式

> 连接式
>
> link标签

> 导入式
>
> ![](..\img\2-3.png)

# 选择器

> 标签选择器
>
> ```css
> 标签名{
>     
> }
> ```
>
> 类选择器
>
> ```id选择器
> .类名{
>     
> }
> ```
>
> id选择器
>
> ```css
> #id{
>     
> }
> ```
>
> id	>	类	>	标签

css可去自己网页的广告

## 层次选择器

![](..\img\2-4.png)

> 后代选择器
>
> ```css
> body p{
>     
> }/*body后代的p全选*/
> ```
>
> 子选择器
>
> ```css
> body>p{
>     
> }/*body后一代才选*/
> ```
>
> 相邻兄弟选择器
>
> ```css
> 选择器 + p{
>     /*选中和这个选择器的 下一个p */只有一个!!!
> }
> ```
>
> 通用选择器
>
> ```css
> 选择器 ~ p{
>     /*下面的p全选中*/
> }
> ```
>
> 

## 结构伪类选择器

![](..\img\2-5.png)

```css
ul li:first-child{
    /*ul作为父元素,选择第一个子元素,如果是li则生效*/
}
p:nth-child(n){
    /*找到所有p元素的父元素,如果这个父元素的第n个子元素是p,样式才生效*/
}
p:nth-of-type(n){
    /*找到所有p元素的父元素,这个父元素的第n个p子元素生效*/
}
```

```css
p:hover{
    /*鼠标悬浮时生效*/
}
```

## 属性选择器	!	!

![](..\img\2-6.png)

```css
选择器[过滤条件]{
    /*
    过滤条件可以是标签,标签的绝对值,包含,正则
    */
}
```

## 美化

### 字体

输入font-
快捷

![](..\img\2-7.png)

> font:字体风格	字体粗细	大小	字体(楷体)

### 文本

![](..\img\2-8.png)

![](..\img\2-9.png)

```css
选择器{
    text-decoration:上/中/下划线,none;
}

/*文字相对图片居中对齐*/
img,span{
    vertical-align:middle;/*上中下的中*/
}
center是水平的中
```

![](..\img\2-10.png)

## 超链接伪类

![](..\img\2-11.png)

```css
a:hover{/*悬停*/}
a:active{/*点击时*/}
a:link{/*没点击过*/}
a:visited{/*点击过*/}
```

### 阴影

text-shadow:颜色	X轴	Y轴**(下正)**	模糊半径**(也是px)**

### 表格样式

![](..\img\2-12.png)

```css
/*去点*/
list-style: none;
border:1px(粗细)	solid	red;
```

### 背景

默认repeat

![](..\img\2-13.png)

#### [背景渐变调色](https://www.bilibili.com/video/BV1YJ411a7dy?t=736.1&p=13)

> 网站
>
> [Grabient | Gradient Generator & Palette Finder](https://grabient.com/)

## 盒子模型

![](..\img\2-14.png)

### 边距及居中

总:	margin+border+padding+内容大小

### 边框

> border-radius:	左上开始顺时针
>
> 圆角	=	宽度/2	==>>圆

![](..\img\2-15.png)

### 阴影

box-shadow:	X轴	Y轴**(下正)**	模糊半径**(也是px)	**颜色

#### *居中

> ```css
> div {
>   width: 1000px;
>   height: 1000px;
>   background-color: aqua;
>   /* 启用flex布局 */
>   display: flex;
>   /* 水平居中 */
>   justify-content: center;
>   /* 垂直居中 */
>   align-items: center;
> }
> img {
>   width: 300px;
> }
> ```

### display

> display
>
> block
>
> inline
>
> inline-block
>
> none

<img src="..\img\2-16.png" style="zoom: 67%;" /><img src="..\img\2-17.png" style="zoom:67%;" /><img src="..\img\2-18.png" style="zoom:67%;" />

### 浮动

元素设置浮动后，会从正常的布局流中 “飘” 起来，不再占据原来的位置，**后续元素会向上移动并环绕在它周围**（类似报纸中文字环绕图片的效果）。

- `float: left`
- `float: right`
- `float: none`：默认值，不浮动

## 清除浮动

clear:both;

![](..\img\2-19.png)

父级元素会塌陷,添加

overflow:hidden;

用::after伪类

`::after` 伪元素的核心价值是**在不修改 HTML 结构的前提下，通过 CSS 向元素添加内容或样式**

## 定位

![](..\img\2-20.png)

![](..\img\2-21.png)

## z-index

`z-index` 值越大的元素会显示在越上层，覆盖值较小的元素。