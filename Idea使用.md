1. Idea 把"Mark Directory As..."的文件夹都加入CLASSPATH。

2. Facets 表示这个module有什么特征，比如 Web，Spring和Hibernate等；

3. Artifact 是maven中的一个概念，表示某个module要如何打包，例如war exploded、war、jar、ear等等这种打包形式；
一个module有了 Artifacts 就可以部署到应用服务器中了！

4. 在给项目配置Artifacts的时候有好多个type的选项，exploed是什么意思：
> 1. explode 在这里你可以理解为展开，不压缩的意思。也就是war、jar等产出物没压缩前的目录结构。建议在开发的时候使用这种模式，便于修改了文件的效果立刻显现出来。  
> 2. 默认情况下，IDEA的 Modules 和 Artifacts 的 output目录 已经设置好了，不需要更改，打成 war包 的时候会自动在 WEB-INF目录 下生产 classes目录，然后把编译后的文件放进去。

5. Java artifact是什么意思，maven一直用，但是不明白中文意思？
> artifact你把它理解成“生成的东西”就差不多了。这个词强调的是这是你软件生产过程中某一步的产生物，不像程序本身，或者是配置文件这些，是你手写出来的。

6. 当点击运行tomcat时，Idea开始做以下事情：
> 1. 运行server前会做一次编译。编译后class文件存放在指定的项目编译输出目录下.
> 2. 根据artifact中的设定对目录结构进行创建.
> 3. 拷贝web资源的根目录下的所有文件到artifact的目录下.
> 4. 拷贝编译输出目录下的classes目录到artifact下的WEB-INF下.
> 5. 拷贝lib目录下所需的jar包到artifact下的WEB_INF下.
> 6. 运行server，运行成功后，如有需要，会自动打开浏览器访问指定url.

7. 文件编码设置（Ctlr+Alt+S): **Editor**->**Code Style**->**File Encodings**,三个地方编码都设为UTF-8.

8. 实时代码模板**Live Templates**：可以补全如 System.Out.Println之类的语句。
> 1. 调用。调用常规的实时代码模板主要是通过两个快捷键：Tab 和 Ctrl + J。如：sys+tab
> 2. 设置。**Editor**->**Code Style**->**Live Templates**。

9. 文件代码模板**File and Code Templates**:可以设置在新建文件时的文件描述、作者等信息。
> 设置。**Editor**->**Code Style**->**File and Code Templates**。

10. 后缀代码模板**Postfix Completion**：比实时代码模板更加便捷一点点的补全，功能本质上也是代码模板。
> 1. 使用。输入`o.notnull`按**Tab**键，代码就会变为`if (o != null)`
> 设置。**Editor**->**General**->**Postfix Completion**。
