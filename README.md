# common-use-configuration
记录一些常用插件或者软件的配置以及资源的网址
========
## Java相关配置
#### myeclipse中配置jetty run
Run Configurations->Maven Build上右键->new:<br>
1.	选择Name，随便填，例如jettyrun <br>
2.	点击Browse Workspace，选择对应要运行的项目<br>
3.	Goals填jetty:run<br>

####	myeclipse安装mybatis generator插件
[下载离线插件](http://pan.baidu.com/s/1i3lk4AT)，解压缩，将解压缩以后的plugins文件夹下的文件放到myeclipse安装目录下的plugins文件夹下。重启myeclipse，在generator.xml上右键，可以看到Generate Mybatis/ibatis artifacts字样，说明安装成功。

####	myeclipse安装jrebel插件
[下载破解插件](http://pan.baidu.com/s/1gd9BjDh)，解压缩，把jrebel.jar和jrebel.lic放到某个文件夹下，然后再myeclipse的vm启动参数中添加：<br>
-noverify -javaagent:D:\Java\jrebel\jrebel.jar     (所放jrebel路径)<br>
-Xbootclasspath/p:D:/Java/jrebel/rebelboot.jar   (设置与jrebel相同路径即可)<br>
-Drebel.generate.show=true<br>
-Drebel.spring_plugin=true<br>
-Drebel.aspectj_plugin=true<br>
-Drebel.cxf_plugin=true<br>
-Drebel.logback_plugin=true<br>
-Drebel.mybatis_plugin=true<br>

## 数据库

####安装Postgresql。
从官网上下载最新[稳定版](http://www.postgresql.org/)，我下载的是Window 下的Version 9.4.5，大小为58.42M，执行exe安装即可。安装好以后，默认用户名是postgres，密码为安装过程中自己设定的。pgAdmin是自带的可视化工具。将#{安装目录}/bin添加到环境变量以后，可以在命令提示符下执行sql命令，[常用命令](http://blog.chinaunix.net/uid-26642180-id-3485465.html)。
