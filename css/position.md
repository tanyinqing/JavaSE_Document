# Chapter 6 Position & display & visibility

## `position`这个是属性

- 静态定位
    - 标准流  static
- 相对定位   position: relative;
    - 没有脱离标准流
    - 相对于自己原来的位置发生位置的偏移
- 绝对定位   /*绝对定位脱离了标准流 但内容会重叠*/
    - 脱离了标准流
    - 相对于距离它 **最近的** **已定位** 的 **祖先元素** 进行移动
        - 已定位指 `position` 值不是 `static`，也就是定位不是静态定位
- 固定定位 例如 滚动条 无论屏幕滚动到什么位置 位置都比较固定
    - 脱离了标准流
    - 相对浏览器的最左上角
- 偏移量
    - `top`
    - `left`
    - `right`
    - `bottom`
- `z-index`
    - 对于已定位元素，值越大越靠近上边 z轴上的值 值大的元素会覆盖值小的元素
    
 ```html
   position: static; 这个是默认的 
 相对定位
  #box1 {             
      /*position: fixed;固定定位，起始点不同 始终滚动在屏幕的相对位置  例如
      滚动条*/
             /*相对定位未偏移标准流 但位置相对原来的位置发生改变  */
             position: relative;/*static静态定位*/
             left: 100px; /*向右偏移100px*/
             top:100px; /*向下偏移*/
             width: 100%;/*全部的宽度*/           
             z-index: 1; /*z轴上的索引 值的大小决定谁覆盖谁*/
         }
```
    
## `display`

- `inline` 块级变行内
- `block` 行内变块级
- `inline-block` 对外行内，对内块级
- `none` 不显示且不保留位置
```html
        .box1,
        .box2 {
            display: inline;  块级变行内
        }
        .span1,
        .span2 {
            display: block;  行内变块级
        }

对外行内，对内块级 的使用
 .i-b { 行内元素的宽高和内外边距不起作用
            width: 100px;
            height: 100px;
            display: inline-block;
           /* 加上inline-block 属性 宽度 高度 就起作用了
            但内容仍然在一条线上了*/
        }
        
<span class="i-b">span4..</span>
<span class="i-b">span5..</span>
```

## `visibility`
- `hidden` 不显示但保留位置
```css
        .box3,
        .span3 {
            visibility: hidden;
        }
```