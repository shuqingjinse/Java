### Jenkins
****
**注意事项:最新版12.04日的jenkins要使用tomcat8以上包括8**
****
+ **插件安装方式**
> 安装jenkins插件有两种方法,一种是在线安装,一种是离线安装.两种方式介绍如下:

  1. 如果服务器可以上网,那边选择在线安装最好不过了,安装流程为:
  系统管理----插件管理---选择需要的插件直接安装即可
  2. 如果服务器不能上网,那么就只能离线安装,首先去
  http://updates.jenkins-ci.org/download/plugins/
  下载需要的plugin,选择匹配的版本号,下载到本地,然后打开:系统管理---插件管理—高级---找到”上传插件”(浏览,找到扩展名为.hpi的插件，上传之后默认直接就安装了。重启jenkins，安装的插件就可以使用了。
****
Jenkins其实就是一个工具，这个工具的作用就是调用各种其他的工具来达成你的目的。
> Jenkins 是一个开源项目，提供了一种易于使用的持续集成系统，使开发者从繁杂的集成中解脱出来，专注于更为重要的业务逻辑实现上。同时 Jenkins 能实施监控集成中存在的错误，提供详细的日志文件和提醒功能，还能用图表的形式形象地展示项目构建的趋势和稳定性。Jenkins可以做到持续编译和发布软件项目，这使得开发者很容易把他们的改动集成到项目中，还让用户能更加便利的获取编译和测试版本；

一、什么是持续集成（Continuous Integration
持续集成（CI）是一种软件开发实践，它倡导团队开发成员协同工作，有需要的时候就对代码进行集成，不必要等到软件开发后期才开始集成。通常，每次的集成都是通过自动化的构建来验证，包括自动编译、发布和测试，从而尽快地发现集成错误，让团队能够更快的开发内聚的软件。

二、持续集成系统的组成
一个自动构建过程，包括自动编译、分发、部署和测试等。
一个代码存储库，即需要版本控制软件来保障代码的可维护性，同时作为构建过程的素材库。


地址http://mirrors.jenkins-ci.org/下载适合的Jenkins版本。
把得到的war包直接扔到tomcat下，启动tomcat，Jenkins就安装完毕
    ```Java
    Global Tool Configuration配置环境
    配置JDK、配置GIT、配置MAVEN
    创建MAVEN项目
    安装MAVEN插件：Maven Integration plugin
    自动部署插件：
    Deploy to container Plugin
    ```
