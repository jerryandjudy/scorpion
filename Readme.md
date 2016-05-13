Readme.md
maven2和maven3都需要把bin目录设置PATH环境变量，命令名都是mvn或mvnDebug，所以这两个版本同时安装是冲突的。


一个简单的共存办法就是，修改maven3的bin下的启动脚本：

把mvn.bat和mvnDebug.bat分别改为mvn3.bat和mvnDebug3.bat
这两个脚本启动时会检查mvn.bat是否存在，所以打开这两个文本文件，找到mvn.bat，修改为mvn3.bat

然后重新打开cmd命令行，输入mvn -version 和 mvn3 -version，即可看到这两个命令对应不同的maven版本：

C:\Users\kk> mvn -version
Apache Maven 2.2.1 (r801777; 2009-08-07 03:16:01+0800)
Java version: 1.6.0_37
Java home: D:\software\Java\jre
Default locale: zh_CN, platform encoding: GBK
OS name: "windows 7" version: "6.1" arch: "amd64" Family: "windows"
C:\Users\kk> mvn3 -version
Apache Maven 3.0.4 (r1232337; 2012-01-17 16:44:56+0800)
Maven home: F:\study\open\apache-maven-3.0.4\bin\..
Java version: 1.6.0_37, vendor: Sun Microsystems Inc.
Java home: D:\software\Java\jre
Default locale: zh_CN, platform encoding: GBK
OS name: "windows 7", version: "6.1", arch: "amd64", family: "windows"
