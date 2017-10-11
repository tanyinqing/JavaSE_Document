# Chapter 8 常用样式

- background
    - background-color 背景颜色
    - background-image 背景图片
    - background-repeat 重复
    - background-attachment
    - background-position
```html
 background-attachment: fixed;  /*固定*/
  background-position: center top;
```
- color
- text-aline
    - `text-aline: center;` 内容水平居中
- text-decoration
- *`text-transform`*
- text-indent 设置2em 文本缩进
- *`vertial-aline`*
- line-height
    - `line-height: height;` 内容垂直居中 
- font-family  什么样的字体 楷体或宋体 

[google加载字体的网址](https://fonts.google.com/)
```html
加入这个链接  联网并且能翻墙的情况下就好加载这个字体
<link href="https://fonts.googleapis.com/css?family=Roboto" rel="stylesheet">
样式中加入属性
font-family: 'Roboto', sans-serif; 意思是前面字体不存在的情况下就加载一个等宽字体

```

- font-style   斜体 或 粗体
- font-size  字体的规格
- font-weight 字体的粗细
- list-style
    - list-style-type 无序列表前面的点
    - list-style-position
    - list-style-image 无序列表前面的点换做图片
```css
        ul {
            list-style-type: square;/*前面点的类型  变成方块*/
            }
        ul li {
            float: left; /*导航栏的常规做法*/
        }
```
- border
    - border-color 颜色
    - border-style  样式
    - border-width 宽度
 ```html
 border: 10px #ddd solid ; /*边框*/
```
- **margin**  外边界
    - margin-top
    - margin-right
    - margin-bottom
    - margin-left
     ```html
       margin: 50px 30px 20px 0px ;  /*上右下左 */
    ```
- **padding**
    - padding-top
    - padding-right
    - padding-bottom
    - padding-left
- width
    - min-width
    - max-width
```css
      textarea {
            width: 100px;
            min-width: 100px;
            max-width: 100px;/*宽度就固定了 不能拖动了*/
        }
```
- height
    - min-height
    - max-height
- **display**
- visibility
- **position** 位置
- z-index 相对于屏幕位置的z坐标
- **float**  浮动
- **clear**  清除塔索，就是父元素无法包裹子元素的情形
- *`overflow`*  当子元素的内容超过父元素大小时，决定超出的内容不显示或滚动显示
- cursor  光标的样式
