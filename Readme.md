
写markdown 语法的工具，可以边写边预览的。
Typora https://www.typora.io/

picasa图片查看器，可以看像素是否一致



TODO:

仿微信发布朋友圈里的图片选择器
https://github.com/malijie/PhotoPicker-master
图片压缩上传
https://github.com/Curzibn/Luban


Android点击EditText文本框之外 整理到demoapp中 http://www.jb51.net/article/104090.htm

1、版本检测和文件下载功能，支持断点续传

2、ffmpeg

4、rxjava、rxandroid



3.开源技术框架选用
目前，android开发社区关于app应用开发的各个层面，都存在一些成熟可靠的实现方面，采用合适的技术方案，有助于提高开发效率，改善代码质量，便于维护等等一系列优点，我们不闭门造车，自己封装的往往也没有开源项目的精良。

3.1.数据库

ormlite，ORM的概念在服务器领域的使用已经是稀松平常，应用到android数据开发，有利于简化数据库访问逻辑，降低开发难度，提高代码的可维护性。在这个基础上，我们在数据库访问增加数据缓存层，提高数据库访问效率，降低耗电（访问硬盘比访问内存耗电）。关于缓存的主要实现策略，一个某个缓存的数据发生了变化，就清楚该缓存数据，下次读取时，重新从硬盘中读取，然后缓存，简化缓存管理逻辑。greendao

3.2.http网络访问

rxjava+retrofit2+okhttp，它们的优点就不解释了，反正就选他们了，当然rxjava不仅仅用于网络访问，还运用于app中的逻辑链式调用，线程切换处理等，强大到你难以想象。

3.3.单元测试

robolectric+powermock+mockito+junit，目前android单元测试，这是已知最靠谱的方案。

3.4.事件处理

eventbus，用于处理应用内之间的消息传递，当然还存在其他的处理方案，我们觉得这种方式比较合适。

3.5.内存泄露检测

leakcanary，作为一个有追求的程序员，怎么能容忍内存泄露的存在，改善应用内存泄露情况，就靠它了。

3.6.布局文件依赖注入

butterknife，摆脱findViewById的厄运。当然，在使用androidstudio时，不要忘记了安装Zelezny这个插件，这样在开发过程中，可以更加的偷懒了。
