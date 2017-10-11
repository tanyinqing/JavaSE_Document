# Chapter 3 常用组件

1. **Grid Basic** `栅格` `.col-*-` [代码](https://github.com/thu/Bootstrap_20170902/blob/master/grid.html)
分块一共分为12块
	- xs (for phones)
	- sm (for tablets)
	- md (for desktops)
	- lg (for larger desktops) 表明不分隔 代表超大屏幕
  
  > [What is the difference among col-lg-*, col-md-* and col-sm-* in twitter bootstrap3?](http://stackoverflow.com/a/28654005/3414180)

2. Typography `排版`    [代码](https://github.com/thu/Bootstrap_20170902/blob/master/typo.html)
	- h1-h6
	- small
	- mark
	- abbr  省略
	- blockquote 标记
	- .blockquote-reverse 样式 反方向
	- dl    dt dd  预定义
	- code   pre code 写代码
	- kbd   键盘快捷键  把它放在背景中
	- pre
	以下文字颜色不同  加点表明是属性
	- `.text-muted`   沉默
	-  `.text-primary` 
	-   `.text-success`  成功
	-   `.text-info`
	-   `.text-warning`
	-   `.text-danger` 警告
	背景色不一样
	- `.bg-primary`
	-  `.bg-success`
	-   `bg-info`
	-   `bg-warning`
	-   `.bg-danger`
	
3. Tables  [代码](https://github.com/thu/Bootstrap_20170902/blob/master/table.html)
	- `.table` + `.table-striped 表格分栏` + `.table-borderd 框` + `.table-hover  鼠标悬停` +  `.table-condensed`
	- **Responsive Tables 响应式表格** 
	- wrapper div  
		- `.table-responsive`
		- 
4. Images [代码](https://github.com/thu/Bootstrap_20170902/blob/master/image.html)
	-`.img-rounded  圆角` `.img-circle 圆形` `.img-thumbnail 缩略图`
	- **Responsive Images 响应式设计** `.img-responsive`
	- **Responsive Embeds 响应式嵌入内容** 
		- div 
	        - `.embed-responsive` + `.embed-responsive-16by9 `宽屏 + `.embed-responsive-4by3 普屏` 
	    - iframe embed video object
	        - `.embed-responsive-item`  
	        
5. Jumbotron `超大屏幕 - 巨幕` [代码](https://github.com/thu/Bootstrap_20170902/blob/master/jumbotron.html)
	- `.jumbotron` 
	- inside container 里面
	- outside container 外面
	
6. Wells `浅容器`  加入一个浅色边框
	- div   [代码](https://github.com/thu/Bootstrap_20170902/blob/master/jumbotron.html)
		- `.well 这个先加` + `.well-sm` + `well-lg`
		
7. Alerts  警告
[代码](https://github.com/thu/Bootstrap_20170902/blob/master/alert.html)
	- div 
	    - `.alert`
	    - \+ `.alert-success` + `.alert-info` + `.alert-warning` + `.alert-danger`
	- link in alert
		- a `.alert-link`
	- **Closing Alerts**
		- div + `alert-dissmissible` + `fade` + `in`
		- a `.close` `data-dismiss="alert"`
	
	  可以点x关闭的提示框
	  
	      ```html
	      <div class="alert alert-success alert-dismissable">
	          <a href="#" class="close" data-dismiss="alert">&times;</a>
	          <strong>Success!</strong> a successful or positive action.
	      </div>
	      ```
    
8. Buttons button / input / a `.btn` [代码](https://github.com/thu/Bootstrap_20170902/blob/master/button.html)
	- styles
		- ``.btn-default`
		- `.btn-primary`
		- `.btn-success`
		- `.btn-info`
		- `.btn-warning`
		- ` .btn-danger`
		- `.btn-link`
   
	- sizes
		- `.btn-lg`
		- `.btn-md`
		- `.btn-sm`
		- `.btn-xs`
		
	- 	status	
		- `.btn-block`  块元素
		- `.active`   活动的
		- `.disabled`  不可点击
        
9. Button Groups 按钮组
	- `.btn-group`
	- \+ `.btn-group-lg`
	- \+ `.btn-group-md`
	- \+ `.btn-group-sm`
	- \+ `.btn-group-xs`
	- \+ `.btn-group-vertical`  按钮垂直排列
	- \+ `.btn-group-justified`
    - **each** `button` / `input` wrap div with `.btn-group` class
	- Dropdown Menus 
    - btn 
	    - `.dropdown-toggle` `data-toggle="dropdown"`
    - span `.caret`
    - ul `.dropdown-menu` `role="menu"`
 按钮组实现下拉菜单
      ```html
      <div class="btn-group">
        <button class="btn btn-primary">Apple</button>
        <button class="btn btn-primary">Samsung</button>
        <div class="btn-group">
          <button class="btn btn-primary dropdown-toggle" data-toggle="dropdown">
            Sony <span class="caret"></span>  小三角
          </button>
          <ul class="dropdown-menu" role="menu">
            <li><a href="#">Tablet</a></li>
            <li><a href="#">Smartphone</a></li>
          </ul>
        </div>
      </div>
      ```
      
10. Glyphicons `[ɡlɪf]` `字体图标` 以及如何引入在线小图标
[代码](https://github.com/thu/Bootstrap_20170902/blob/master/glyphicon.html)
	- span  元素 下面是样式
		- `.glyphicon` 
		- \+ `.glyphicon-*`
		
		- 阿里巴巴图标字体 [alibaba iconfont](http://www.iconfont.cn/)
        		 - 点击购物车按钮加入
        		 - 购物车中添加到项目
        		 - Unicode
        
        	```html
        	<style>
        		@font-face {
        		  font-family: 'iconfont';  /* project id 418173 */
        		  src: url('//at.alicdn.com/t/font_418173_dnpxpzlz0an0cnmi.eot');
        		  src: url('//at.alicdn.com/t/font_418173_dnpxpzlz0an0cnmi.eot?#iefix') format('embedded-opentype'),
        		  url('//at.alicdn.com/t/font_418173_dnpxpzlz0an0cnmi.woff') format('woff'),
        		  url('//at.alicdn.com/t/font_418173_dnpxpzlz0an0cnmi.ttf') format('truetype'),
        		  url('//at.alicdn.com/t/font_418173_dnpxpzlz0an0cnmi.svg#iconfont') format('svg');
        	}
        
        	.icon-font {
        		font-family: iconfont,serif;
        	}
        
        	.icon-heart:before {
        		content: '\e66b';
        	}
        	</style>
        	```
        
        	```html
        	<span class="icon-font">&#xe667;</span>
        	<span class="icon-font icon-heart"></span>
        	```
		
		
11. Badges / Labels `徽章` `标签` 
[代码](https://github.com/thu/Bootstrap_20170902/blob/master/glyphicon.html)
	- badge span 
	    - `.badge`
	- label span
	    - `.label` 
	    - \+ `.label-default, +.label-primary, .label-success, .label-info, .label-warning .label-danger`
	    
12. Progress Bars  进度条 [代码](https://github.com/thu/Bootstrap_20170902/blob/master/progress-bar.html)
	- outer div `.progress` 外层的部分
	- inner div `.progress-bar` `style="width: 12%;进度刻度"`  里面的部分
		- `.progress-bar-success` `.progress-bar-info` `.progress-bar-warning` `.progress-bar-danger` 不同的颜色
	    - `.progress-bar-striped` `.active`
	    
13. Pagination  分页  [代码](https://github.com/thu/Bootstrap_20170902/blob/master/pagination.html)
	- ul
		- `.pagination` + `.pagination-lg` + `.pagination-sm` 
	- li
		- \+ `.active` + `.disabled`
	- ul 
		- `.breadcrumb`
14. Pager  上一页和下一页
  - ul
      - `.pager` 
  - li
      - \+ `.previous` + `.next`
      
15. List Groups  列表组
	- ul / div 
		- `.list-group` 
	- li / a 
		- `.list-group-item` + `.list-group-item-*` + `.active` + `.disabled`
		
16. Panels `面板` 
	- 1st div
		- `.panel-group`  
	- 2nd div
		- `.panel` + `.panel-*`
	- 3rd div
		-  \+ `.panel-headind` + `.panel-body` + `.panel-footer` 
		-
17. Dropdowns `下拉菜单` 
	- div
		- `.dropdown` 
	- button
	    - `.dropdown-toggle`
	    - `data-toggle="dropdown"`
	- span
	    - `.caret`
	- ul
	    - `.dropdown-menu`
	- li
	    - \+ `.divider`
	    - \+ `.dropdown-header`

  ```html
  <div class="dropdown">
    <button class="btn btn-primary dropdown-toggle" data-toggle="dropdown">Dropdown Example
    <span class="caret"></span></button>
    <ul class="dropdown-menu">
      <li><a href="#">HTML</a></li>
      <li><a href="#">CSS</a></li>
      <li><a href="#">JavaScript</a></li>
    </ul>
  </div>
  ```

18. Collapse `折叠板` 
	- button 
		- `data-toggle="collapse"` 
		- `data-target="#demo"` or `<a href="#demo" data-toggle...`
	- div 
		- `id="demo"`
		- `.collapse` 
		 - `.in`
	- Accordion `手风琴` `.panel-group` `data-parent="#demo"` `.panel-collapse`
  
	    ```html
	     <div class="panel-group" id="accordion">
	      <div class="panel panel-default">
	        <div class="panel-heading">
	          <h4 class="panel-title">
	            <a data-toggle="collapse" data-parent="#accordion" href="#collapse1">
	            Collapsible Group 1</a>
	          </h4>
	        </div>
	        <div id="collapse1" class="panel-collapse collapse in">
	          <div class="panel-body">Lorem ipsum dolor sit amet, consectetur adipisicing elit,
	          sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad
	          minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea
	          commodo consequat.</div>
	        </div>
	      </div>
	      <div class="panel panel-default">
	        <div class="panel-heading">
	          <h4 class="panel-title">
	            <a data-toggle="collapse" data-parent="#accordion" href="#collapse2">
	            Collapsible Group 2</a>
	          </h4>
	        </div>
	        <div id="collapse2" class="panel-collapse collapse">
	          <div class="panel-body">Lorem ipsum dolor sit amet, consectetur adipisicing elit,
	          sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad
	          minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea
	          commodo consequat.</div>
	        </div>
	      </div>
	      <div class="panel panel-default">
	        <div class="panel-heading">
	          <h4 class="panel-title">
	            <a data-toggle="collapse" data-parent="#accordion" href="#collapse3">
	            Collapsible Group 3</a>
	          </h4>
	        </div>
	        <div id="collapse3" class="panel-collapse collapse">
	          <div class="panel-body">Lorem ipsum dolor sit amet, consectetur adipisicing elit,
	          sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad
	          minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea
	          commodo consequat.</div>
	        </div>
	      </div>
	    </div>
	    ```
  
19. Tabs `选项卡` / Pills `胶囊` 
	- ul 
		- `.list-inline` 
	    - `.nav` + `.nav-tabs` 
	    - `.nav` + `.nav-pills` + `.nav-stacked` + `.nav-justified` 
	- Dynamic Tabs 
		- `data-toggle="tab"` `.tab-content` `.tab-pane`
    
	    ```html
	    <ul class="nav nav-tabs">
	      <li class="active"><a data-toggle="tab" href="#home">Home</a></li>
	      <li><a data-toggle="tab" href="#menu1">Menu 1</a></li>
	      <li><a data-toggle="tab" href="#menu2">Menu 2</a></li>
	    </ul>
	
	    <div class="tab-content">
	      <div id="home" class="tab-pane fade in active">
	        <h3>HOME</h3>
	        <p>Some content.</p>
	      </div>
	      <div id="menu1" class="tab-pane fade">
	        <h3>Menu 1</h3>
	        <p>Some content in menu 1.</p>
	      </div>
	      <div id="menu2" class="tab-pane fade">
	        <h3>Menu 2</h3>
	        <p>Some content in menu 2.</p>
	      </div>
	    </div>
	    ```
    
  - Dynamic Pills `data-toggle="pill"`
  
	  ```html
	  <ul class="nav nav-pills">
	    <li class="active"><a data-toggle="pill" href="#home">Home</a></li>
	    <li><a data-toggle="pill" href="#menu1">Menu 1</a></li>
	    <li><a data-toggle="pill" href="#menu2">Menu 2</a></li>
	  </ul>
	
	  <div class="tab-content">
	    <div id="home" class="tab-pane fade in active">
	      <h3>HOME</h3>
	      <p>Some content.</p>
	    </div>
	    <div id="menu1" class="tab-pane fade">
	      <h3>Menu 1</h3>
	      <p>Some content in menu 1.</p>
	    </div>
	    <div id="menu2" class="tab-pane fade">
	      <h3>Menu 2</h3>
	      <p>Some content in menu 2.</p>
	    </div>
	  </div>
	  ```
  
20. Navbar nav 导航条 [代码](https://github.com/thu/Bootstrap_20170902/blob/master/nav.html)
	- nav
		- `.navbar` 
		- \+ `.navbar-default` + `.navbar-inverse` + `.navbar-fixed-*` 
	- div
	    - `.container-fluid`
	- div
	    - `.navbar-header` 
	- a
	    - `.navbar-brand` 
	- ul 
	    - `.nav` `.navbar-nav` `navbar-right`
	- navbar with dropdown
		- li `.dropdown`
		- a `.dropdown-toggle` `data-toggle="dropdown"`
		- ul `.dropdown-menu`
	- button `navbar-btn`
	- form
		- `.navbar-form` `.navbar-left`
	- div
		- `.form-group` `.input-group`
	- input
		- `.form-control`
	- button
		-	~~`.navbar-btn`~~
		- `input-group-btn`
	- i
		- `.glyphicon` + `.glyphicon-*`
	- Collapsing Navigation Bar 
		- button 
		    - `.navbar-toggle` `data-toggle="collapse"` `data-target="#navbar"` 
		- span 
			- `.icon-bar` 
		- div 
		    - `.collapse` 
		    - `navbar-collapse`
		    - `id="navbar"`
	    
	    ```html
	    <nav class="navbar navbar-inverse">
	      <div class="container-fluid">
	        <div class="navbar-header">
      适配手机适配三个白条  不出现横向滚动条
	          <button class="navbar-toggle" data-toggle="collapse" data-target="#myNavbar">
	            <span class="icon-bar"></span>
	            <span class="icon-bar"></span>
	            <span class="icon-bar"></span> 
	          </button>
	          <a class="navbar-brand" href="#">WebSiteName</a>
	        </div>
	        <div class="collapse navbar-collapse" id="myNavbar">
	          <ul class="nav navbar-nav">
	            <li class="active"><a href="#">Home</a></li>
	            <li><a href="#">Page 1</a></li>
	            <li><a href="#">Page 2</a></li> 
	            <li><a href="#">Page 3</a></li> 
	          </ul>
	          <ul class="nav navbar-nav navbar-right">
	            <li><a href="#"><span class="glyphicon glyphicon-user"></span> Sign Up</a></li>
	            <li><a href="#"><span class="glyphicon glyphicon-log-in"></span> Login</a></li>
	          </ul>
	        </div>
	      </div>
	    </nav>
	    ```
    
21. Forms  表单 [代码](https://github.com/thu/Bootstrap_20170902/blob/master/form.html)
	 - form
		- `.form-inline` `.form-horizontal` 
	 - div
	   - `.form-group` `.has-success` `.has-warning` `.has-error`
	 - label    
	   - `for=""`
	   - `.control-label` + `.col-*-`
	 - input / textarea / select    
	   - `.form-control` 
	 - div 
	   - `.checkbox` 
	   - `.radio`
	   
22. Inputs `.input-sm` `.input-lg`
	 - label
		- `.checkbox-inline` 
		- `.radio-inline` 
	 - file upload
    
	    ```html
	    <label class="btn btn-warning">
	        Browse <input type="file" style="display:none;">
	    </label>
	    ```
  
	- p
		- `.form-control-static` `help-block`
	- div
		- `.input-group` `.input-group-btn`
	- sapn
		- `.input-group-addon`
	- i
		- `.glphicon`
    
23. Media Object `媒体对象`
	- div
	    - `.media`
	    - `.media-left` `media-right`
	    - `.media-body`
	    - `.media-heading`
	    - `.media-top` `.media-middle` `.media-bottom`

24. Carousel `旋转木马` 走马灯或图片轮播 [代码](https://github.com/thu/Bootstrap_20170902/blob/master/carousel.html)
	- div
		- `id="myCarousel"` `.carousel` `.slide` `data-ride="carousel"` 
	- ol
		- `.carousel-indicators` 
	- li 
		- `data-target="myCarousel"` `data-slide-to="0"` 
	- div
		- `.carousel-inner` 
	- div
		- `.itme` 
	- div 
		- `.carousel-caption` 
	- a
		- `.left` `.carousel-control` `data-slide="prev / next"`
  
  ```html
  <div id="carousel" class="carousel slide" data-ride="carousel">
      <!-- Indicators -->
      <ol class="carousel-indicators">
          <li data-target="#carousel" data-slide-to="0" class="active"></li>
          ...
      </ol>
      <!-- Wrapper for slides -->
      <div class="carousel-inner" role="listbox">
          <div class="item active">
              <img src="img_1.jpg" alt="Chania">
              <div class="carousel-caption">
                  <h3>Chania</h3>
                  <p>The atmosphere in Chania has a touch of Florence and Venice.</p>
              </div>
          </div>
          ...
      </div>
      <!-- Left and right controls -->
      <a class="left carousel-control" href="#carousel" role="button" data-slide="prev">
          <span class="glyphicon glyphicon-chevron-left" aria-hidden="true"></span>
      </a>
      <a class="right carousel-control" href="#carousel" role="button" data-slide="next">
          <span class="glyphicon glyphicon-chevron-right" aria-hidden="true"></span>
      </a>
  </div>
  ```
  
25. Modal `模态框` 弹出框  [代码](https://github.com/thu/Bootstrap_20170902/blob/master/modal.html)
	- button 
		- `data-toggle="modal"` `data-target="#myModal"` 
	- div 
		- `id="myModal"`
		- `.modal` + `.fade` 
	- div  
		- `.modal-dialog` + `.modal-sm` `.modal-lg`
	- div  
		- `.modal-content` 
	- div 
		- `.modal-header` `.modal-body` `.modal-footer` 
	- bottom
		- `data-dismiss="modal"` 
  
26. Tooltip `提示工具` 
	- a
	    - `data-toggle="tooltip"` `title=""` 
	    - `data-placement="top / bottom / left / right"`

	- JavaScript
	    ```javascript
	    <script>
	      $(document).ready(function(){
	          $('[data-toggle=tooltip]').tooltip(); 
	      }); 
	    </script>
	    ```

27. Popover `弹出框` 
[代码](https://github.com/thu/Bootstrap_20170902/blob/master/google-material-lite.html)
	- a
	    - `data-toggle="popover"` 
	    - `title=""` 
	    - `data-content=""` 
	    - `data-placement="top / bottom / left / right"` 
	    - `data-trigger="focus"`
	    - `data-trigger="hover"`
	    
	- JavaScript
    ```javascript
    <script>
      $(document).ready(function(){
          $('[data-toggle=popover]').popover(); 
      });
    </script>
    ```

28. ~~Scrollspy `滚动监听`~~

	> [Bootstrap Scrollspy Plugin (Advanced)](https://www.w3schools.com/bootstrap/bootstrap_scrollspy.asp)

29. ~~Affix `附加导航`~~

	> [Bootstrap Affix Plugin (Advanced)](https://www.w3schools.com/bootstrap/bootstrap_affix.asp)
