### gradle版本问题
1. gradle包的版本,在项目的gradle/wrapper目录下面有个gradle-wrapper.properties中有如下内容：
`distributionUrl=https\://services.gradle.org/distributions/gradle-2.2.1-all.zip`
    >团队中人员A,B,C，每个人都有自己的电脑和配置，如何能保证A,B,C使用同一个版本得gradle来编译项目呢，gradle wrapper就用来干这个

2. gradle插件的版本,是android studio为了方便使用gradle进行配置和编译而开发的插件,项目的根目录下的build.gradle中会配置如下代码:
    ```
    buildscript {
    repositories {
        jcenter()
    }
    dependencies {
        classpath 'com.android.tools.build:gradle:2.3.0'

        // NOTE: Do not place your application dependencies here; they belong
        // in the individual module build.gradle files
    }
    }
    ```
3. gradle 与 gradlew: W意思是wrapper，它是一个用bash命令包装过的gradle编译启动脚本，里面会进行环境变量检测和设置。最终进行编译的还是gradle;Gradlew是包装器，自动下载包装里定义好的gradle 版本，保证编译环境统一，gradle 是用本地的gradle

4. [gradle插件与包版本对应相关](https://developer.android.com/studio/releases/gradle-plugin.html)如下：
    > Plugin version 2.0.0 - 2.1.2 ----> Gradle version 2.10 - 2.13
    > Plugin version 2.1.3 - 2.2.3 ----> Gradle version 2.14.1+
    > Plugin version 2.3.0+ ----> Gradle version 3.3+
