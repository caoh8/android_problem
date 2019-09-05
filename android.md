# 遇到的坑

## Android Studio

### 调试安装时手机断开连接？

确认所调试的软件是否在手机上运行，例如输入法则需要启动所开发的输入法。

### 解决Android Studio出现File size exceeds configured 
http://www.cocoachina.com/articles/32415

最近在项目中使用到了protobuf，一个相应的类就超过了2.5m，所以在ide中无法找到报红。作为强迫症的我表示想解决这个问题，于是上网搜索了一下解决方案，例如这篇文章：https://blog.csdn.net/qq_35381515/article/details/80111835 。但是我根据指示完成了相应的操作，却发现在我的Android Studio上没有生效。
于是我又进行了一些尝试，终于在我的Android Studio上可以识别比较大的文件了：
点击面板里的Help
点击Edit Custom Properties
这个时候例如在我的电脑上，生成了一个config/idea.properties
在里面加上idea.max.intellisense.filesize=5000,扩大支持打开的文件大小至5M
重启Android Studio
