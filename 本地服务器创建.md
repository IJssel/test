## Tomcat下载教程

首先官网下载Tomcat，官网地址-点击进入 <http://tomcat.apache.org/>

![1562291332444](C:\Users\lichen\AppData\Roaming\Typora\typora-user-images\1562291332444.png)

进入Tomcat9下载页面

对应着操作系统位数进行下载，下载后会是一个zip压缩包

![1562291417998](C:\Users\lichen\AppData\Roaming\Typora\typora-user-images\1562291417998.png)

选择64位

![1562291467670](C:\Users\lichen\AppData\Roaming\Typora\typora-user-images\1562291467670.png)

解压，放在某一文件夹下，注意：路径不要包含中文和特殊字符！



## Tomcat配置环境变量教程

我的电脑右键打开属性，点击高级系统设置

![1562292329766](C:\Users\lichen\AppData\Roaming\Typora\typora-user-images\1562292329766.png)

选中高级，点击环境变量

![1562292444596](C:\Users\lichen\AppData\Roaming\Typora\typora-user-images\1562292444596.png)



在变量名中填写： CATALINA_HOME

变量值就是你解压后的路径

然后确定

![1562292725558](C:\Users\lichen\AppData\Roaming\Typora\typora-user-images\1562292725558.png)



系统变量中找到系统变量中的Path

 点击path后编辑

![1562293007133](C:\Users\lichen\AppData\Roaming\Typora\typora-user-images\1562293007133.png)



编辑文本

![1562293185976](C:\Users\lichen\AppData\Roaming\Typora\typora-user-images\1562293185976.png)



在变量值后追加   ;%CATALINA_HOME%\bin;(别忘了前面英文符号；)

然后直接确定

![1562295158914](C:\Users\lichen\AppData\Roaming\Typora\typora-user-images\1562295158914.png)



## Tomcat启动和验证配置环境变量是否成功

![1562310763592](C:\Users\lichen\AppData\Roaming\Typora\typora-user-images\1562310763592.png)

之后出现了Tomcat的启动窗口，若没有报错或者一闪而过，那么说明启动成功了，让黑窗口保持运行，不能关，否则你的服务器也就关闭了，若出现了报错或者一闪而过(启动失败)，可能是你的端口被占用，Tomcat默认的端口是8080，出现这两种情况那么可以试试以下两种：

一、java是否安装

二、修改Tomcat端口号后重启电脑，再用以上步骤启动Tomcat。



当弹出下图中得Dos窗口，表示Tomcat服务器成功的启动了（此窗口关闭，则关闭了服务器）

![1562311081285](C:\Users\lichen\AppData\Roaming\Typora\typora-user-images\1562311081285.png)



注意：出现乱码情况

打开logging.properties文件进行编辑

![1562311326602](C:\Users\lichen\AppData\Roaming\Typora\typora-user-images\1562311326602.png)

找到这行修改java.util.logging.ConsoleHandler.encoding = GBK

![1562311513023](C:\Users\lichen\AppData\Roaming\Typora\typora-user-images\1562311513023.png)





之后验证环境变量是否配置成功，浏览器输入一下 http://localhost:8080 

可以直接点击进入<http://localhost:8080/>

出现如下图，那么就说明配置成功了

![1562310893736](C:\Users\lichen\AppData\Roaming\Typora\typora-user-images\1562310893736.png)



将自己的项目部署到Tomcat服务器上

首先在webapps文件夹下新建一个app文件夹用于保存自己的web项目

![1562311758848](C:\Users\lichen\AppData\Roaming\Typora\typora-user-images\1562311758848.png)



查看自己的ip地址

在命令提示符中输入ipconfig

![1562312731607](C:\Users\lichen\AppData\Roaming\Typora\typora-user-images\1562312731607.png)



查看是否成功

在浏览器中输入自己IP地址+访问路径 如：http://192.168.0.101:8080/APP/images/banner-01.png

![1562312437042](C:\Users\lichen\AppData\Roaming\Typora\typora-user-images\1562312437042.png)注意：Tomcat服务器同一局域网下的其他电脑或手机，才可以访问

​	