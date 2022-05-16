## 没事进来逛逛

## layui点击按钮自动刷新页面问题

## 问题

```java
<button class="layui-btn layui-btn-primary" onclick="findData()">查询</button>
```

点击页面上的按钮，执行完button的click事件后，会自动的重新刷新一下当前的页面。

## 原因

button,input type=button按钮在IE和w3c，firefox浏览器区别：

1. 当在IE浏览器下面时，button标签按钮，input标签type属性为button的按钮是一样的功能，不会对表单进行任何操作。
2. 但是在W3C浏览器，如Firefox下就需要注意了，button标签按钮会提交表单，而input标签type属性为button不会对表单进行任何操作。

## 解决方案

将button标签更换为input

```java
<input class="layui-btn layui-btn-primary" value="查询" onclick="findData()"></input>
```

为button按钮增加一个type=”button”属性

```java
<button type="button" class="layui-btn layui-btn-primary" onclick="findData()">查询</button>
```

## SSM常见错误![img](file:///C:\Users\Acer\Documents\Tencent Files\3236888270\Image\C2C\1Q`J0K3O@V$P9K9P5LWJGVH.png)



在检查无误后，仍然出现错误，很有可能是包的版本冲突，更换一下依赖即可

## XXX改为xXX

一、今天在做实习项目的时候，发现了Property 'XXX ' not found on type  com.wjy329.AAA (AAA和XXX都为举例)  的异常信息，首先查看了我的AAA实体类，发现我的XXX是定义了，而且set、get方法也都写好了，在尝试了多次和各种方法后，发现，原来我的XXX是以大写字母开头的，当我改成小写字母开头后（例如：XXX改为xXX），竟然取到值了。。。好吧，今天就记录一下这个异常。

以后大家遇到这样的初级问题，不妨试试。

@JSONField (format="yyyy-MM-dd")
@JsonFormat(pattern = "yyyy-MM-dd", timezone = "GMT+8")
@DateTimeFormat(pattern ="yyyy-MM-dd")
private Date birthday;
5  然后就搜索 JsonFormat 少了一天的关键



springboot项目，在数据库查出数据显示在页面时，时间转化问题





解决方法

1、实体类属性上添加

```java
/**
 * 创建时间
 */
@JsonFormat(pattern = "yyyy-MM-dd", timezone = "GMT+8")
private Date creationDate;
```

2、在配置文件中添加(这里使用的是后缀名为yml的配置文件)

```yml
jackson:
  date-format: yyyy-MM-dd HH:mm:ss
```

解决后的效果

