## Spring实战第四版 学习笔记

### 学习准备

开发环境:Idea 2018

第四版源代码

第四版电子书

gradle 4.10 包，以及安装

涉及到gradle的配置

idea导入gradle还有些问题，一个是同步时下载失败，一个是导入的时候到底该怎么配置？



### 第一章 Spring之旅

简单介绍了Spring的基本思想，根本使命：简化Java开发：

- 激发POJO
- 依赖注入（DI)
- 面向切面编程
- 使用模板减少样板代码

第一章源码**Knight**分析

程序的分析我们从主函数的入口开始

```java
 public static void main(String[] args) throws Exception {
    ClassPathXmlApplicationContext context = 
        new ClassPathXmlApplicationContext(
            "META-INF/spring/knight.xml");
    Knight knight = context.getBean(Knight.class);
    knight.embarkOnQuest();
    context.close();
```

 程序非常简单，第一行加载配置文件knight.xml；第二行从context中获得knight的实现；第三行然后执行让knight出发去执行任务的方法，最后第四行关闭context。

然后我们可以看一下Knight的代码，它是一个接口：

```java
public interface Knight {
  void embarkOnQuest();
}
```













