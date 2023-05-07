# meal_ordering_system
点餐系统
配置：
  one:连接数据库，在本地mysql里面添加apsfc数据库，添加apsfc 20150727 2133.sql文件，然后在代码里跟其进行连接，注意
  在applicationContext.xml文件里面 
   <!--加载数据源连接池-->
    <bean name="druidDataSource" class="com.alibaba.druid.pool.DruidDataSource">
        <property name="driverClassName" value="com.mysql.cj.jdbc.Driver"/>
        <property name="url" value="jdbc:mysql://127.0.0.1/apsfc?autoReconnect=true&amp;useUnicode=true&amp;
        characterEncoding=utf8&amp;useSSL=false&amp;serverTimezone=Asia/Shanghai"/>
        <property name="username" value="root"/>
        <property name="password" value="123456"/>
    </bean>
    这儿把用户跟密码改成自己的进行数据源连接。
    
    
    two:进行tomcat配置，下载tomcat，我这儿下载的是apache-tomcat-9.0.74,然后就是下载idea2023版本，一定要是专业版才可以
    ，学生可以在github进行学生认证之后，转到JetBrains就可以直接免费使用专业版了，注意社区版不能进行web的开发，下载之后把
    本项目导入，然后配置tomcat,连接数据库，tomcat你可以直接用smart tomcat插件配置，然后运行，应该就可以成功了，不过注意
    运行时候不能关闭数据库，然后用tomcat运行。tomcat是服务器嘛，它会传给你web界面，然后对界面操作的时候要一直运行程序，就是
    服务器关闭了的话，那你这个程序就没法继续下去了，所以要一直打开，分为前台和后台，这些应该只要用过手机的人就可以操作。注意
    就是登录的时候要去数据库里面看看管理员以及密码，用户什么的，你也可以添加用户等等。
    
