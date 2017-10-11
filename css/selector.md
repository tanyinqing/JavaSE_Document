# Chapter 3 选择器

## CSS 的 3 种使用方式

> 优先级： 内联 > 内部 = 外部  
后两种取决于谁后声明，后面的会覆盖前面的

1. 内联样式 `Inline Styles` Markdown中仅支持内联样式

    > Source code
    
    ```html
    <!-- index.html -->
    <h1 style="color: #f00;">headline...</h1>
    ```

2. 内部样式 `Internal Style Sheet` ctrl+shift+回车为快捷键

    > Source code
    
    ```html
    <!-- index.html -->
    <head>
        <style>
            h1 {
                color: #f00;
            }
        </style>
    </head>
    <body>
    <h1>headline...</h1>
    </body>
    ```

3. 外部样式 `External Style Sheet`

    > Source code
    
    ```css
    /* style.css */
    h1 {
        color: #f00;
    }
    ```
    
    ```html
    <!-- index.html -->
    <head>
        <link href="style.css">
     <!--另一种写法  <link rel="stylesheet" href="intro.css">-->
    </head>
    <body>
    <h1>headline...</h1>
    </body>
    ``` 

## CSS 选择器

- 基本选择器  ctrl+shift+回车为快捷键
    - 标记(元素/标签)选择器 以元素名开头
    - `class` 选择器 也叫类别选择器
      - 以 `.` 开头
      - 自定义选择器名
    - `id` 选择器
      - 以 `#` 开头
      - 自定义选择器名
    - `class` 和 `id` 的区别
      - `class` 用 `.` 开头，`id` 用 `#` 开头
      - `class` 值在一个页面中可以使用多次，`id` 只能使用一次
      - `class` 和 `id` 同时存在并发生样式冲突时，`id` 优先级高
      - `class` 可以用空格引用多个值，`id` 不可以
    - 何时用 `class` 何时用 `id`?
```html
        h1 {  标记选择器
            background-color: #ff0;
        }
         .red {  类别选择器  可以多次使用
                    color: #f00;
                }
          #small {  id选择器 一个页面只能应用一次
              font-size: 10px;
          }
          
class 可以用空格引用多个值，id 不可以
<h1 id="blue" class="red bg-yellow">h1...</h1>
```
- 复合选择器
    - 交集选择器
      - 由元素选择器和 `class` 或 `id` 选择器直连构成
      - 选择二者同时满足的标记
    - 并集选择器
      - 由多个基本选择器使用逗号 `,` 连接
      - 选择所有的标记
    - 派生选择器 `descendant selector`
      - 由多个基本选择器使用空格 ` ` 连接
      - 选择含有嵌套关系的标记
      ```html
      h2.red {  交集选择器 必须全符合才可以
                  color: #f00;
              }
        
      h2,
      ul{  /*并集选择器 选择所有的标记 只要满足其中之一就可以应用这个样式*/
          margin: 0; /*外边框*/
          padding: 0; /*or ul dl 的属性*/
          color: blue;
      }

        h1 i {  /*选择只要满足嵌套关系就可以了  派生选择器*/
            color: red;
        }
  
         h1>span {  /*选择满足嵌套关系 必须是子元素才可以 派生选择器*/
            color: red;
        }
      
      ```
- 属性选择器
    - `[attribute]`	用于选取带有指定属性的元素
    - `[attribute=value]`	用于选取带有指定属性和值的元素
    - `[attribute~=value]`	用于选取属性值中包含指定**词汇**的元素
    - `[attribute|=value]`	用于选取带有以指定值开头的属性值的元素，该值必须是整个单词
    - `[attribute^=value]`	匹配属性值以指定值开头的每个元素
    - `[attribute$=value]`	匹配属性值以指定值结尾的每个元素
    - `[attribute*=value]`	匹配属性值中包含指定**值**的每个元素
    
    
    
    ```html
             [href] {
                text-decoration: none;
            } 
           
           [href="http://bing.com"] {
                font-size: 3em;
            }
    
            [title~=tesst] {
                border: 1px solid red;
            }
    
            [title^=tesst] {
                border: 1px solid red;
            }
    
            [class$=r] {
                font-style: italic;
            }
    
            h1[class*=e] {
                font-family: Kartika;
            }
    
            [title|=test] {
                text-decoration: line-through;
            }
    ```
- 伪类 `pseudo-class`

    > A pseudo-class is used to define a special **state** of an element.

    - 锚点的 LoVe - HeAt  有顺序限制
      - `:link`
      - `:visited`
      - `:hover`
      - `:active`
```html
这个是伪类的例子  操作的是某个状态
        a { 
            font-size: 5em;
            text-decoration: none;
        }

        a:link {  链接
            background-color: #ff0;
        }

        a:visited { 访问之后颜色改变
            background-color: cornflowerblue;
        }

        a:hover {  点击时改变颜色
            background-color: lightgreen;
        }

        a:active {
            background-color: red;
        }

        div:hover {
            cursor: crosshair;
        }
```
  
  > All
  
  - `:active`
  - `:checked`
  - `:disabled`
  - `:empty`
  - `:enabled`
  - `:first-child` - Selects every elements that is the first **child** of its parent
  - `:first-of-type` - Selects every elements that is the first **type** of its parent
  - `:focus`
  - `:hover`
  - `:in-range`
  - `:invalid`
  - `:lang(language)`
  - `:last-child`
  - `:last-of-type`
  - `:link`
  - `:not(selector)`
  - `:nth-child(n)`
  - `:nth-last-child(n)`
  - `:nth-last-of-type(n)`
  - `:nth-of-type(n)`
  - `:only-of-type`
  - `:only-child`
  - `:optional`
  - `:out-of-range`
  - `:read-only`
  - `:read-write`
  - `:required`
  - `:root`
  - `:target`
  - `:valid`
  - `:visited`
    
- 伪元素 `pseudo-element` 选中一个元素的特殊的一部分

    > A CSS pseudo-element is used to style specified **parts** of an element.
  
  - `::before`   之前加
  - `::after`
  - `::first-letter`  第一个字母
  - `::first-line`
  - `::selection`  
  
   ```html
      a::before {
               content: 'test';
               color: red;
           }
         
      input::selection {  输入字体，选中部分变颜色
                background-color: yellow;
            }
    ```