# DuerOS java sdk

[![DuerOS](http://duer.bdstatic.com/saiya/dueros_static_79c1cb0828ef81e9863d87b7c5a154c2/statics/images//dumi/logo2.png)](http://duer.bdstatic.com)

java 版本sdk
##示例
##2017年11月20日更新添加技能测试功能
1.修改位于com.baidu.duer.dcs.framework.message.DcsRequestBody的类
```
com.baidu.duer.dcs.framework.message.DcsRequestBody
```
2.添加技能,其中参数为技能的id
```
debug.put("bot",new Bot("f0b8d11f-f237-0ec0-7d88-18904b5c0fc0"));
```
##使用
在demo-test/src/main/resources/目录下创建duer.properties,输入，并配置好Oauth回调为
http://127.0.0.1:8080/auth
```
clientId=clientId
clientSecret=clientSecret
```
然后运行demo-test项目下

你可以直接运行控制台程序
```
java xin.yysf.gui.DuerOSGui console
```



======================================================
如果运行gui需要安装相关的gui插件来实现浏览器的展示
======================================================
javafx gui实现
```
java xin.yysf.gui.DuerOSGui
```
使用swt之前，你可能还需要安装它，用来支持浏览器显示
````
sudo apt-get install libwebkitgtk-1.0-0
````
swt gui实现
```
java xin.yysf.gui.DuerOsSwtGui
```
树莓派环境下运行gui,需要配置swt运行环境
````
sudo apt-get install libwebkitgtk-1.0-0
apt-get install libswt-webkit-gtk-4-jni 
sudo apt-get install libswt-gtk-4-jni
sudo apt-get install libswt-gtk-4-java

mvn package
cd demo-test/target
mkdir BOOT-INF
mkdir lib
cp ../../lib/swt-gtk-4.3.2-arm.jar ./BOOT-INF/lib/.
jar -uf0 demo-test-1.0-SNAPSHOT.jar ./BOOT-INF/lib/swt-gtk-4.3.2-arm.jar
java -jar demo-test-1.0-SNAPSHOT.jar
````


![](https://raw.githubusercontent.com/microxdd/dueros/master/duer/STEP1.jpg)

播放音乐示例
![](https://raw.githubusercontent.com/microxdd/dueros/master/duer/STEP2.jpg)

java9 以下的jdk如要启用http2需要在添加vm参数
```
-Xbootclasspath/p:${settings.localRepository}/org/mortbay/jetty/alpn/alpn-boot/${alpn-boot.version}/alpn-boot-${alpn-boot.version}.jar.
```
```
-Xbootclasspath/p:/G:/maven/repository/org/mortbay/jetty/alpn/alpn-boot/8.1.11.v20170118/alpn-boot-8.1.11.v20170118.jar
```
