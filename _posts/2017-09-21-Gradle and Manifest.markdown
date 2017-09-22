


### Gradle是什么
Gradle是用于构建软件的软件，也称为“构建自动化软件”或“构建系统”。
您可能在其他环境中使用其他构建系统，例如make（C / C ++），rake（Ruby），Ant（Java），Maven（Java）

这些工具通过您教授他们的内在功能和规则知道 - 如何确定需要创建的内容（例如，基于文件更改）以及如何创建它们。 构建系统不直接编译，链接，打包等应用程序，而是指示单独的编译器，链接器和打包程序来执行此操作。

Gradle使用构建在Groovy上面的域专用语言（DSL）完成这些任务

### Groovy 是什么

有许多编程语言被设计为在Java VM之上运行,其中一些，如JRuby和Jython，分别是其他常用编程语言（Ruby和Python）的实现，
一种语言只对应一种，而Groovy是其中之一

Groovy脚本看起来有点像Java和Ruby的混搭。与Java一样，Groovy支持

- 使用class关键字定义类 
- 使用extends创建子类 
- 使用导入从外部JAR导入类 
- 使用大括号定义方法体（{和}） 
- 对象是通过新的操作符创建的

和Ruby一样

语句可以是类的一部分，也可以简单地写成一种强制性的风格，如脚本语言 
不输入参数和局部变量

Groovy是一种解释型语言，如Ruby和Java不同。 Groovy脚本通过执行groovy命令运行，将脚本传递给它来运行。
但是，Groovy运行时是一个Java JAR，需要一个JVM才能运行。
Groovy的优势之一是创建一个域专用语言（或DSL）。 例如，Gradle是用于进行软件构建的Groovy DSL。 
特定于Gradle的能力似乎是一流的语言结构，通常与Groovy内在的功能无法区分。 
然而，Groovy DSL主要是声明式的，就像一个XML文件。 
在某种程度上，我们获得了两个世界的最佳效果：XML风格的定义（通常使用较少的标点符号），但具有“到达Groovy”的能力，并根据需要进行自定义脚本编制。

### Android和Gradle关系
Google已经发布了用于Gradle的Android插件，这使得Gradle能够构建Android项目。 Google还在Android Studio中使用Gradle和Gradle作为Android Studio后台的构建系统。

### 为什么使用

最初，当我们构建一个应用程序时，这些构建是使用Eclipse和Ant完成的。 Eclipse是IDE，而Ant是命令行工具。
Eclipse不使用Ant构建Android项目，而是拥有自己的构建系统。 而且我们使用这些工具成功地构建了一百万个应用程序。 这些工具今天仍然可以工作，尽管Ant的支持正在快速消失。

那么为什么要改变？ 有几个因素，包括：
- 维护两个单独的构建系统（Ant和Eclipse的本地方法）变得耗时，随着Android Studio和另一个构建系统的出现，将会变得更加糟糕。 
因此，Google希望基于Gradle，针对IDE和命令行方案的单一构建系统进行标准
- 使用第三方库更方便

### 安装

[Gradle下载页面][1]包含Gradle本身的ZIP存档的链接：二进制文件，源代码或两者。

### 结构

有三部分组成
- 批处理文件(gradlew.bat)和脚本代码(gradlew)
- 用于批处理文件和脚本的jar包(gradle/wrapper)
- 哪里下载gradle (gradle/wrapper/gradle-wrapper.properties)

```
#Wed Apr 10 15:27:10 PDT 2013
distributionBase=GRADLE_USER_HOME
distributionPath=wrapper/dists
zipStoreBase=GRADLE_USER_HOME
zipStorePath=wrapper/dists
distributionUrl=https\://services.gradle.org/distributions/gradle-3.3-all.zip
```

当您创建或导入项目时，或者如果您更改属性文件中引用的Gradle版本，Android Studio将下载distributionUrl属性指向的Gradle，
并将其安装到.gradle/ 在创建的项目目录下.该版本的Gradle将是Android Studio使用的版本。




[1]: https://gradle.org/install/