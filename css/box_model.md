# Chapter 4 Box model 

1. box **无处不在**

2. box 的并列关系和嵌套关系


> preview  定义的不同字体的样式

<div style="border:1px dashed #333;">
    <div style="color:#666; text-align:center; height:50px; line-height:50px;">margin</div>
    <div style="border:1px solid #ddd; margin:0 50px 50px; background: #ddd;">
        <div style="color:#666; text-align:center; height:20px; line-height:20px;">border</div>
        <div style="margin:0 20px 20px; background:#fff">
            <div style="color:#666; text-align:center; height:30px; line-height:30px;">padding</div>
            <div style="height:50px; color:#333; margin:0 30px 10px; background:#999; color: #fff">
                content
            </div>
<br>

> Source code

```html
<!-- html -->
<div>
    content
</div>    
```

```css
div {
    color: #fff;
    background: #999;
    border: 20px solid #ddd;
    height: 50px;
    margin: 50px;
    pading: 30px;
}
```

- box 之间的边距
  - 并列关系 
    - 块级
      - 垂直外边距取最大值      
    - 行内
      - 水平外边距取和
      - 行内元素的宽度 / 高度 / 上下内外边距均无效
  - 嵌套
   - 块级
   - 行内
   
   ```html
   <!DOCTYPE html>
   <html lang="en">
   <head>
       <meta charset="UTF-8">
       <title>Title</title>
       <style>
           * {
               margin: 0em;
           }
           #box1,
           #box2,
           #box3 {  /*并集选择器*/
               background-color: yellow;
               height: 50px;
               padding: 30px;/*绿色部分 内边界*/
               border: 10px #ddd solid ; /*边框*/
               margin: 50px;   
           }
           #box1 {  /*id选择器*/
               margin: 100px;  垂直外边距取最大值 
               width: 800px;
           }
           span {  行内元素的宽度 / 高度 / 上下内外边距均无效
               padding: 100px;
               margin: 50px;
               background-color: #fcf;
               width: 100px;
               height: 100px;
           }
       </style>
   </head>
   <body>
   <div id="container">
       <div id="box1"></div>
       <div id="box2"></div>
       <div id="box3"></div></div>
   <span>span1...</span>  水平外边距取和
   <span>span1...</span>
   <span>span1...</span>
   </body>
   </html>
   ```