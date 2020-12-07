jmter读取excel的数据使用的方法是jmter CSV Date Set Config 参数化

但是将excel文件保存成csv格式后，jmter读取后返回的数据总是出现乱码的情况

以下就是解决方法：

1、先做一个excel，如下

​    ![0](https://typora-lxx.oss-cn-beijing.aliyuncs.com/img/20200922124924.png)

在将excel表格另存为csv格式：

​    ![0](https://typora-lxx.oss-cn-beijing.aliyuncs.com/img/20200922124927.png)

**下面是使用CSV Data Set Config参数化将csv里面的数据读取，**

**然后再使用benshell将数据获得**

​    ![0](http://note.youdao.com/yws/public/resource/2392f9e0abec31f775ec916e4b9af900/xmlnote/01AD778AD36F4BBF9A657FC4AF1B209D/731)

下面是添加一个Debug sampler(里面什么也不用，设置保持默认) 和两个http request

​    ![0](https://typora-lxx.oss-cn-beijing.aliyuncs.com/img/20200922124936.png)

​    ![0](http://note.youdao.com/yws/public/resource/2392f9e0abec31f775ec916e4b9af900/xmlnote/49735DA70C5B4BB298CFF4244F98BA78/201)

**下面是查看结果树：**

​    ![0](https://typora-lxx.oss-cn-beijing.aliyuncs.com/img/20200922124940.png)

​    ![0](https://typora-lxx.oss-cn-beijing.aliyuncs.com/img/20200922124943.png)

​    ![0](https://typora-lxx.oss-cn-beijing.aliyuncs.com/img/20200922124946.png)