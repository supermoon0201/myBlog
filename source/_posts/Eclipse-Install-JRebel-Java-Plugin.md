---
title: Eclipse Install JRebel Java Plugin
---

最近发现公司的小伙伴开发项目，修改完后还要重启tomcat服务，实在是太影响效率，所以想着给大家分享下我一直在使用的Eclipse插件“JRebel”。因为这篇文章重点介绍安装JRebel，所以关于JRebel的介绍请自行搜索。接下来进入正题：
## 1.在线安装Eclipse的JRebel插件

1>我们使用在线安装插件的方式，在Eclipse中选择Help -> Install New Software...

![logo](Eclipse-Install-JRebel-Java-Plugin\1.png)

2>本次JRebel使用的版本是6.4.3，所以我们的“Location”连接添加的是“http://update.zeroturnaround.com/update-site-archive/update-site-6.4.3.RELEASE/”，“Name”内随便命名。

![logo](Eclipse-Install-JRebel-Java-Plugin\2.png)

<!--more-->

3>因为我使用的Eclipse所以选择相应的插件

![logo](Eclipse-Install-JRebel-Java-Plugin\3.png)

剩下的就是一直“Next”，然后耐心等待！安装完成后提示重启Eclipse，同意重启。

## 2.配置JRebel

1>下载JRebel：

​	链接: http://pan.baidu.com/s/1kU5n4tp 密码: 9gki，解压到英文目录下。

```
jrebel6.4.3-cracked
|   jrebel.lic（破解的license）
|   readme.txt
|   setting.png
|
+---jrebel
|       jrebel.jar（破解文件）
|
\---jrebel6
        jrebel.jar（破解文件）
```

2>替换eclipse\plugins\org.zeroturnaround.eclipse.embedder_6.4.3.RELEASE目录下的jrebel.jar

```
.
|   plugin.xml
|
+---jr6
|   \---jrebel
|       |   jrebel.jar（用【jrebel6.4.3-cracked\jrebel6\jrebel.jar】替换）
|       |   jrebel.plugininfo
|       |
|       \---lib
|               jrebel32.dll
|               jrebel64.dll
|               libjrebel32.dylib
|               libjrebel32.so
|               libjrebel64.dylib
|               libjrebel64.so
|
+---jrebel
|       jrebel.jar（用【jrebel6.4.3-cracked\jrebel\jrebel.jar】替换）
|       jrebel.plugininfo
|
+---META-INF
|       JREBEL.RSA
|       JREBEL.SF
|       MANIFEST.MF
|
\---org
    \---zeroturnaround
        \---eclipse
            \---embedder
                    EmbeddedAgentProvider.class
                    EmbeddedJRebel.class
```

3>在Eclipse中选择Help -> JRebel Configuration，打开JRebel 配置视图

 ![logo](Eclipse-Install-JRebel-Java-Plugin\4.png)

4>配置license，点击Activate / Update License，选择解压文件中的“jrebel.lic”

![logo](Eclipse-Install-JRebel-Java-Plugin\5.png)

![logo](Eclipse-Install-JRebel-Java-Plugin\6.png)

最后选择“Change license”，激活成功！

![logo](Eclipse-Install-JRebel-Java-Plugin\7.png)

5> JRebel配置视图中选择“Advanced”标签，选择JRebel 6 Agent 6.4.3...

![logo](Eclipse-Install-JRebel-Java-Plugin\14.png)

## 3.JRebel的使用

配置server

![logo](Eclipse-Install-JRebel-Java-Plugin\8.png)

 ![logo](Eclipse-Install-JRebel-Java-Plugin\9.png)

 点击Alt+P调出project菜单，勾选上Build Automatically

![logo](Eclipse-Install-JRebel-Java-Plugin\10.png)

 配置项目关联JRebel![logo](Eclipse-Install-JRebel-Java-Plugin\11.png)

 出现以下提示，说明已成功。![logo](Eclipse-Install-JRebel-Java-Plugin\13.png)