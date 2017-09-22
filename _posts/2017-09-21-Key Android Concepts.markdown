### Android中的一些重要概念
之前对一些概念还是不清楚,这里重新整理了一下
### Android应用程序
应用程序是用户可以从Play Store安装或以其他方式下载到其设备的东西.该应用程序应该有一些用户界面,并且可能有其他代码设计为在后台工作（多任务）
### 编程语言

绝大多数Android应用程序都是以Java编写的,但是也有其它的编程语言写的,如:
- 您可以使用C / C ++编写应用程序的部分内容,以提升性能,移植现有代码库等
- 您可以使用C / C ++编写整个应用程序,主要用于使用OpenGL for 3D动画的游戏
- 您可以使用HTML,CSS和JavaScript编写应用程序的内容,使用工具将该材料打包到可通过Play商店和类似场所分发的Android应用程序中
- 其它

### 操作系统版本和API级别

大多数Android开发人员的API级别对于

- API Level 19（Android 4.4）
- API Level 21（Android 5.0）
- API Level 22（Android 5.1）
- API Level 23（Android 6.0）
- API Level 24（Android 7.0）
- API Level 25 (Android 7.1)
- API Level 26 (Android 8.0)

### Dalvik和ART

在Android方面,Dalvik和ART是虚拟机（VM）. 虚拟机被许多编程语言所使用,如Java,Perl和Smalltalk. Dalvik和ART的设计非常像Java VM,但是针对嵌入式Linux环境进行了优化
两者之间的差异在于Android 5.0及更高版本上使用了ART,而Dalvik则在旧设备上使用

那么当某人写一个Android应用程序的时候真的会发生什么呢

1. 开发人员编写Java语法源代码,利用Android项目和第三方发布的类库.
2. 开发人员使用Java SDK附带的javac编译器将源代码编译为Java VM字节码.
3. 开发人员将Java VM字节码转换为Dalvik VM字节码,其中包含其他文件到.apk扩展名（APK文件）的ZIP档案中.
4. Android设备或模拟器运行APK文件,导致字节码由Dalvik或ART VM的实例执行.

从您的角度来看,大多数构建工具都被隐藏. 您在第一步输入Java源代码,并在最后输出APK文件.

### 进程和线程
当您的应用程序运行时,它将在自己的进程中执行. 这与其他传统操作系统没有什么不同. Dalvik的一部分魔法使许多进程可以一次运行许多Android应用程序,而不会消耗大量的RAM
Android还将为您的应用程序设置一批线程. 您的代码将被执行的线程大部分时间被不同地称为“主应用程序线程”或“UI线程”

