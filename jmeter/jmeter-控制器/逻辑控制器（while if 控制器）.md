1、如果(if)控制器

1.1：准备数据

1.1.1:如下图，准备两组http取样器数据，并且分布添加Debug取样器

​    ![0](https://typora-lxx.oss-cn-beijing.aliyuncs.com/img/20200922125331.png)

准备数据，两组http请求，其中一组是成功的另一组是人为制造的失败，

1.1.2:执行后可以发现第一组http取样器执行成功后Debug sampler的响应数据中

JMeterThread.last_sample_ok=true

​    ![0](https://typora-lxx.oss-cn-beijing.aliyuncs.com/img/20200922125334.png)

第二组http取样器执行失败Debug sampler的响应数据中

JMeterThread.last_sample_ok=fales

​    ![0](https://typora-lxx.oss-cn-beijing.aliyuncs.com/img/20200922125337.png)

1.2：添加【如果(if)控制器】先禁用 第二个http取样器和其他的Debug Sample

条件：相当于java if （）中的条件，只有是true就会继续执行，如果条件判断fales就不会执行

​    ![0](https://typora-lxx.oss-cn-beijing.aliyuncs.com/img/20200922125340.png)

1.3 ：查看结果树，我们发现【如果(if)控制器】下的Debug samper执行了

​    ![0](https://typora-lxx.oss-cn-beijing.aliyuncs.com/img/20200922125343.png)

1.4：禁用第一个http sampler 并且启用第二个http sampler执行。查看结果树【如果(if)控制器】下的debug取样器没有执行

​    ![0](https://typora-lxx.oss-cn-beijing.aliyuncs.com/img/20200922125346.png)

2：while 控制器

2.1：condition参数的几种写法

2.1.1：什么都不写（会一直循环执行，直到执行到有fail跳出循环）

​    ![0](https://typora-lxx.oss-cn-beijing.aliyuncs.com/img/20200922125349.png)

例1：失败的sampler在前面 成功的sampler在后面 这种情况会一直执行到死循环

​    ![0](https://typora-lxx.oss-cn-beijing.aliyuncs.com/img/20200922125351.png)

例2：成功的sampler在前面 失败的sampler在后面 执行到fail会跳出循环

​    ![0](https://typora-lxx.oss-cn-beijing.aliyuncs.com/img/20200922125354.png)

2.1.2：condition写LAST也会执行跟2.1.1一样的结果

​    ![0](https://typora-lxx.oss-cn-beijing.aliyuncs.com/img/20200922125357.png)

2.1.3：condition的另外几种写法

- ​    ${VAR} -Where VAR is set to fales by some other test elemet

​     判断VAR的值什么时候为fales的时候跳出循环

A.添加CSV文件如下

​    ![0](https://typora-lxx.oss-cn-beijing.aliyuncs.com/img/20200922125400.png)

**！！！注意**

**新建的excel的类型为xlsx，需要将文件另存为转换为cvs文件才可以正常的读取出数据**

​    ![0](https://typora-lxx.oss-cn-beijing.aliyuncs.com/img/20200922125403.png)

B 设置条件

​    ![0](https://typora-lxx.oss-cn-beijing.aliyuncs.com/img/20200922125406.png)

c.查看结果树

​    ![0](https://typora-lxx.oss-cn-beijing.aliyuncs.com/img/20200922125410.png)

- ${__javaScript(${C}==10)}

A.运行函数助手，统计运行次数 记录在myValue这个变量中

​    ![0](https://typora-lxx.oss-cn-beijing.aliyuncs.com/img/20200922125413.png)

B:添加条件为运行参数的次数小于3

​    ![0](https://typora-lxx.oss-cn-beijing.aliyuncs.com/img/20200922125416.png)

c、添加http取样器，在这一步将运行的次数的赋值给myValue 下一步可以直接去myValue的值即可

​    ![0](https://typora-lxx.oss-cn-beijing.aliyuncs.com/img/20200922125419.png)

D：查看结果树发现只循环运行3次就退出了

​    ![0](https://typora-lxx.oss-cn-beijing.aliyuncs.com/img/20200922125422.png)

- ${__javaScript("${VAR2}"=="abcd")}

- ${_P(property)} - where property is set to "false" somewhere else

原文链接：https://blog.csdn.net/hujyhfwfh2/article/details/80634116