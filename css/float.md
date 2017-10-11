# Chapter 5 Float

- 标准流的概念

inherit 继承父级元素的同一属性值
  
  > 没有 **布局样式** 时，网页呈现的布局

  > 布局样式：`float` `clear` `position` `display` `visibility` 等

- `float` 改变了什么
  1. 浮动的 box 脱离了标准流，原位置被其他 box 占据
  2. 浮动的 box 宽度自适应于内容
  3. 占据浮动 box 的内容在浮动 box 的 `margin` 之外
  
 ```html
 3个盒子浮动  最后一个清除塌缩  浮动
<div id="container">
    <div id="box1">box1...box1...box1...</div>
    <div id="box3">box3...</div>
    <div id="box2">box2...</div>   
    <div class="clear"></div>
</div>
```
```css  
 <style>

        * {  通配符
            margin: 0;
        }

        #container {  这个必须设置
            border: 1px solid red;
            /*padding: 1px;*/
        }

        #box1,
        #box2,
        #box3 {
            padding: 20px;
            border: 10px dashed #3194d0;
            margin: 50px;
            background-color: #ddd;
        }

        #box1 {
            float: left; /* float 浮动\ [fləʊt] */
            background-color: transparent;
            border-color: #2f2f2f;
            margin-bottom: 100px;
        }

        #box3 {
            float: right;  向右浮动 顺序取决于源代码的顺序
        }

        #box2 {
            float: right;
            background-color: #42c02e;
            border-style:solid;
        }

        .clear {
            clear: both;
        }
    </style>
 
```
- 塌缩 `collapse` 的解决
- 清除浮动 `clear`
- 图文混排的实现

    > Source code
    
    ```html
    <div id="container">
        <div id="box1">box1...box1...box1...</div>
        <div id="box3">box3...</div>
        <div id="box2">box2...</div>      
        <div class="clear"></div>
    </div>   
    ```
    
    ```css
    
    /* style.css  全部浮动是，容器无法把盒子全部包起来 */
    .clear {
        clear: both;
    }   
    
    ```
