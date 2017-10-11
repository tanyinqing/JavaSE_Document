# Chapter 7  Layout

- 从外向内 &amp; 从大到小
- `box model` 的观点
- 居中的一种方法 `margin: auto;`
```html
这个是代码部分
<body>
<div id="container">
<div id="header">header</div>
<div id="content">
<div id="left">left</div>
<div id="right">right</div>
    <div class="clear"></div>
</div>
<div id="footer">footer</div>
</div>
</body>
```

```html
这个是样式
  <head>
      <meta charset="UTF-8">
      <title>Title</title>
      <style>
          * {
              margin: 0px;
          }
          #container {
              width: 1000px;
              background-color: #dddddd;
              margin: auto;
          }
          #header {
              height: 200px;
          }
          #left {
              width: 660px; /*减去边框的宽度*/
              background-color: #666;
              float: left;
          }
          #right {
              width: 260px;
              background-color: #999;
          }
          #left,
          #right {
              float: left;
              height: 500px;
              padding: 20px;
              color: inherit;
          }
          #footer {
              height: 300px;
          }
          #header,
          #footer {
              color: #ddd;
              background-color: #333;
          }
          .clear {
              clear: both;
          }
      </style>
  </head>
```