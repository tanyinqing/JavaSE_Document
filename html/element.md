# Chapter 4 常用元素

### Document type
- !doctype  `document type`
 
  > [文档类型声明](https://zh.wikipedia.org/wiki/HTML#.E6.A0.87.E8.AE.B0)
 
### Headings  表头
- html
- body
- head
- title
- base
- meta  元标记
    - charset  编码字符集
- **`link`**
- **`style`**  样式
- **`script`**
- h1~h6 `heading` 内容占一行 是 块级元素
- hr `horizontal line` 这个是横线

### Paragraphs  段落
- p `paragraph`  块级元素
- ~~br~~ `break`  强制换行 不推荐使用
- pre   `preformatted`  设置的格式显示时不改变

### Styles  样式
- *style* *`.attr`*

### Text Formatting   文本格式化
- b `bold` 加粗
- em `emphasis`斜体 强调
- i `italic` 斜体
- small  小号
- strong 加粗
- sub `subscript` 下标
- sup `superscript` 上标
```html
3<sub>2</sub><sup>3</sup>
```
- ins `inserted` 下划线
- del `deleted` 中划线
- mark  黄色特殊标记
 
### Quotations  引用
- abbr  `abbreviation`
- address
- bdo   `bi-directional override`引用的反方向
- blockquote    `quotaed section`
- cite
- q `quotation`

### Computer Code  计算机代码
- code
- kbd   `keyboard input`
- samp  `sample output`
- var   `variable`

### Comments  注释
- `<!-- -->`  常规注释
- `<!--[if IE 8]><![endif]-->`  条件注释  因为IE浏览器对样式支持比较差，所以
条件注释

### Links  链接
- a `anchor` 锚点元素
    - href `hyper reference`  超基准
    - target 目标 有这个元素 就在新页面打开
    - image as link  图片作为连接
    - id with href="#" as bookmark 书签
```html
<a href="http://bing.com" target="_blank">必应</a>
<a href="https://zh.wikipedia.org/wiki/%E4%B8%AD%E5%9C%8B#.E8.B4.A7.E5.B8.81">诗</a>
<a href="http://twitter.com/"><img src="img/test.jpg" alt="">推特</a>
```
### Images
- img   `image`
```html
<img src="img/test.jpg" alt="星球图片" height="200" title="title...">
```
### Tables 表格
- table
- tr    `table row` 行
- th    `table heading 表头`
- td    `table data`数据
  - `colspan` 跨列
  - `rowspan` 跨行
- caption  标题

```html

table>th>td*3  按tab键 快捷方式  

样式
 <style>
        table {
            border-collapse: collapse;
        }
        th, td {
            border: 1px solid #f00;
        }
    </style>


<!--表格是分行写的-->
<table cellpadding="5" border="1" cellspacing="0">
    <caption>xxx 表</caption>
    <tr>  <!--table row` 行-->
        <th width="200">table head1</th>  <!--table heading 表头-->
        <th width="100">table head2</th>
        <th width="300">table head3</th>
    </tr>
    <tr>
        <td style="text-align: right">table data1</td>
        <td>table data2</td>
        <td>table data3</td>
    </tr>
    <tr>
        <td colspan="2">column span</td>   <!--跨两列-->
        <td rowspan="2">table data3</td>   <!--跨两行-->
    </tr>
    <tr>
        <td>table data1</td>
        <td>table data2</td>
    </tr>
</table>
```
### Lists 列表
- ul li `unordered list` 无序
- ol li `ordered list` 有序
- dl dt dd `description list / description term 学期/ description data`描述列表 学期 数据

```html
  ul>li*3  快捷写法

<dl>
    <dt>老虎</dt>
    <dd>是一种猫科动物</dd>
    <dt>狮子</dt>
    <dd>是一种猫科动物</dd>
</dl>
```

### Iframes
- iframe
```html
<!--scrolling 表示是否有边框  这个是嵌入一部分页面-->
<iframe src="http://bing.com" frameborder="0" width="500" height="300" scrolling="no"></iframe>
```

### Forms  表单
- **form**
  - action 属性 表单提交的地址
  - method
- **input**
  - name
  - disabled 不可以点击
  - checked 默认选中
  - type `.attr`
      - text  文本
      - password
      - radio  单选框
      - checkbox  多选框
      - button 按钮
      - file  提交文件
      - hidden  存在该按钮 但用户看不到
- **select**
  - **option**
    - selected `.attr`
- **textarea**   用户的输入区域
- **button**

```html
input:file 快捷学法  只有input和冒号后跟type的值才能用

<body>
<form action="http://bing.com/">
    <input type="text" placeholder="username" value="tester" disabled="disabled"><br>
    <input type="password" placeholder="password"><br>
    <input type="radio" name="gender" checked="checked"> Male
    <input type="radio" name="gender"> Female
    <br>
    <input type="checkbox" name="hobbies" checked="checked">Reading
    <input type="checkbox" name="hobbies">TV
    <input type="checkbox" name="hobbies">Movie
    <input type="checkbox" name="hobbies">Game
    <br>
    <input type="week"><br>  h5新增属性 <!--许多不兼容-->
    <select name="city" multiple="multiple">   <!--多选-->
        <option value="Beijing">Beijing</option>
        <option value="Shanghai">Shanghai</option>
        <option value="Shenzhen" selected="selected">Shenzhen</option>
    </select>
    <br>
    <textarea name=""cols="30" rows="5"></textarea>
    <br>
    <input type="button" value="TEST"><br>
    <input type="file" name=""><br>
    <input type="hidden" name="test-key" value="test-value">
    <button>BUTTON</button>
    <input type="submit" value="Sign up">
    <input type="reset" value="RESET">
</form>
</body>
```


### JavaScript
- *`script`*
- *`noscript`*

### HTML Entities 实体也就是特殊符号
- `&copy;` - &copy;
- `&trade;` - &trade;
- `&reg;` - &reg;
- `&yen;` - &yen;
- `&nbsp;` - `none-breaking space`

```html
&lt;img&gt;
&copy;
&trade;
```

## Grouping tags   块级元素
- **div**   `division`
- **span**

## Block Elements and Inline Elements 块级元素和行内元素

- Block-level Element 块级元素
    - A block-level element always starts on a new line and takes up the full width available (stretches out to the left and right as far as it can).
        - `div`
        - `h1 - h6`
        - `p`
        - `form`
- Inline Element 行内元素  根据内容 占位置 
    - An inline element does not start on a new line and only takes up as much width as necessary.
        - `span`
        - `a`
        - `img`
        宽高和内外边距设置不起作用，除非设置成其他属性

## URL

> Uniform Resources Locators  统一资源定位器

```html
scheme://prefix.domain:prot/path/filename
https://www.baidu.com/index.php?tn=site888_3_pg&ssl_s=1&ssl_c=ssl1_1504095ea3d&prec=2
https://tanyinqing.gitbooks.io/java-big-data-engineer-training/content/html/html5.html

https://  超文本传输协议
prefix 前缀 www
baidu 域名
prot  端口号 百度是默认的443
/java-big-data-engineer-training/content/html/  路径名
html5.html  文件名
```