# 遇到的坑

## Android Studio

### 调试安装时手机断开连接？

确认所调试的软件是否在手机上运行，例如输入法则需要启动所开发的输入法；在点击Run之前点击Apply Changes。



### ListView的数据更新要在主线程中

由于notice是post。多线程下，可能由于主线程notice还没执行，导致上次更改还没notice，就已经更新数据。