# Chapter 3 DOM

> Document Object Model 文档对象模型

[JavaScript HTML DOM Navigation  英文学习网站](http://www.w3schools.com/js/js_htmldom_navigation.asp)

> Source code 源代码

```html
<html>
  <head>
    <title>DOM Tutorial</title>
  </head>
  <body>
    <h1>DOM Lesson one</h1>
    <p>Hello world!</p>
  </body>
</html>
```

### From the HTML above you can read:

- `<html> is the root node` 根节点
- `<html> has no parents`  父类
- `<html> is the parent of <head> and <body>`
- `<head> is the first child of <html>` 子类
- `<body> is the last child of <html>` 最后的
 
### and:

- `<head> has one child: <title>;`
- `<title> has one child (a text node): "DOM Tutorial"`
- `<body> has two children: <h1> and <p>`
- `<h1> has one child: "DOM Lesson one"`Lesson  课
- `<p> has one child: "Hello world!"`
- `<h1> and <p> are siblings`  兄弟姐妹
 