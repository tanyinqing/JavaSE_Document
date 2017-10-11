# 数据库设计练习题

1. 仿 [http://dict.cn/](http://dict.cn/) 设计一个简单的在线电子词典数据库表结构，实现从英文查中文，从中文查英文功能

2. 设计一个能够简单实现用户注册、登录、注销的数据库表结构

    ```
    用户注册
        邮箱： |________|
        帐号： |________|
        密码： |________|
        
        |注册|
    ```
    ```
    用户登录
        邮箱： |________|
        密码： |________|
     
        |登录|
     
        |注册|
    ```
    ```
    系统首页
    
        你好：xxx
        
        |注销|
    ```
    
3. 在题 2 的基础上，实现用户留言功能

    ```
    系统首页
        
        你好：xxx
        
        |注销|
        
        留言：+-----------------------------------—+
             |                                    |
             |                                    |
             |                                    |
             +-----------------------------------—+
       
        |提交|         
    ```
    
4. 在题 3 的基础上，添加管理员管理留言功能，管理员无须注册，使用 SQL 初始化

    ```
        管理员：XXX
    
        |注销|
        
        留言列表
        +--------------------------------------------+
        |xxx|留言内容 ...  |2017-01-17 10:57:30| 删除 |
        |xxx|留言内容 ...  |2017-01-17 11:57:30| 删除 |
        |xxx|留言内容 ...  |2017-01-17 12:57:30| 删除 |
        +--------------------------------------------+
    ``` 
    
5. 在题 1 的基础上，实现查英文显示中文释义，及词性、音标、详细解释，例句的功能

6. 实现一个工作日志系统的数据库表设计
    - 注册时选择组别（第一组；第二组；第三组）以及员工或组长身份
    - 员工登录可以发布当天的工作日志，并可以查看自己的所有日志
    - 组长登录可以发布当天的工作日志，并可以查看本组的所有日志
    - 组长可以按姓名和日期进行日志查询
         
    ```
    用户注册
        姓名： |________|
        密码： |________|
        组别：  ________▽
        类型：  ________▽
      
        |注册|
    ```
    ```
    用户登录
        姓名： |________|
        密码： |________|
      
        |登录|
        
        |注册|
    ```
    ```
    系统首页
        你好：aaa
        
        |注销|
        
        日志：+-----------------------------------—+
             |                                    |
             |                                    |
             |                                    |
             +-----------------------------------—+
       
        |提交|
          
        日志列表
        +------------------------+
        |日志内容 ...  |2017-01-17|
        |日志内容 ...  |2017-01-18|
        |日志内容 ...  |2017-01-19|
        +------------------------+
    ```
    ```
    系统首页
        你好：xxx
        
        |注销|
        
        日志：+-----------------------------------—+
             |                                    |
             |                                    |
             |                                    |
             +-----------------------------------—+
       
        |提交|
        
        姓名 __________ 日期 __________ |查询|
        
        日志列表
        +----------------------------+
        |aaa|日志内容 ...  |2017-01-17|
        |bbb|日志内容 ...  |2017-01-17|
        |ccc|日志内容 ...  |2017-01-17|
        |xxx|日志内容 ...  |2017-01-17|
        |aaa|日志内容 ...  |2017-01-18|
        |bbb|日志内容 ...  |2017-01-18|
        |ccc|日志内容 ...  |2017-01-18|
        |xxx|日志内容 ...  |2017-01-18|
        +----------------------------+
        
    ``` 
                              
7. 实现 [简书](http://jianshu.com/) 核心功能的数据库设计                              