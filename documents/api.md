### PhpWind 9.0.1移动端接口整理

#### 接口列表

1. [动态帖子列表相关接口](#动态帖子列表相关接口)










#### 动态帖子列表相关接口

|  接口|  功能|
|:-------------:|:-------------|
|[/index.php?m=native&c=dynamic&a=hot&_json=1](#1获取最热帖子列表) | 获取最热帖子列表 |
|[/index.php?m=native&c=dynamic&a=new&_json=1](#2获取最新帖子列表) | 获取最新帖子列表 |
|[/index.php?m=native&c=dynamic&a=my&_json=1](#3获取我关注的话题相关帖子列表,帖子数不足时展示话题) | 获取我关注的话题相关帖子列表,帖子数不足时展示话题 |
|[/index.php?m=native&c=dynamic&a=city&_json=1](#4获取同城帖子列表) | 获取同城帖子列表 |
|[/index.php?m=native&c=dynamic&a=sethot&_json=1](#5管理员设置最热帖子) | 管理员设置最热帖子 |
###### 1、获取最热帖子列表

* 请求方法：GET

* 请求参数


 | KEY字段 | 类型 | 必填 | 描述 | 备注 |
 | :------:|:------:|:------:|:------:|:------|
 |  page | int | 是 | 页数 |  第几页，从请求参数获取 |
 |  timestamp | string | 否 | 时间戳 |  作业最近一次执行的时间 |

* 调用样列

```
/index.php?m=native&c=dynamic&a=hot&page=1&timestamp=1000000&_json=1
```
* 测试

  [获取最热帖子列表](http://e.huiin.cn/index.php?m=native&c=dynamic&a=hot&page=1&_json=1)

###### 2、获取最新帖子列表

* 请求方法：GET

* 请求参数


 | KEY字段 | 类型 | 必填 | 描述 | 备注 |
 | :------:|:------:|:------:|:------:|:------|
 |  page | int | 是 | 页数 |  第几页，从请求参数获取 |
 |  maxid | int | 否 | tids |  最大的帖子tids |

* 调用样列

```
/index.php?m=native&c=dynamic&a=new&page=1&maxid=100&_json=1
```
* 测试

  [获取最新帖子列表](http://e.huiin.cn/index.php?m=native&c=dynamic&a=new&page=1&maxid=100&_json=1)

###### 3、获取我关注的话题相关帖子列表,帖子数不足时展示话题

* 请求方法：GET

   请求必须传递 cookie:usersession

* 是否需要登陆： 是

* 请求参数

   | KEY字段 | 类型 | 必填 | 描述 | 备注 |
   | :------:|:------:|:------:|:------:|:------|
   |  page | int | 是 | 页数 |  第几页，从请求参数获取 |

* 调用样列

```
  /index.php?m=native&c=dynamic&a=my&page=1&_json=1
```
* 测试

    [获取我关注的话题相关帖子列表,帖子数不足时展示话题](http://e.huiin.cn//index.php?m=native&c=dynamic&a=my&page=1&_json=1)

###### 4、获取同城帖子列表

* 请求方法：GET

  请求必须传递 cookie:usersession

* 是否需要登陆： 是

* 请求参数

| KEY字段 | 类型 | 必填 | 描述 | 备注 |
| :------:|:------:|:------:|:------:|:------|
|  city | string | 是 | 城市名称 |  城市名称 |
|  page | int | 是 | 页数 |  第几页，从请求参数获取 |

* 调用样列
```
  /index.php?m=native&c=dynamic&a=city&city=aaa&page=1&_json=1
```

* 测试

[获取同城帖子列表](http://e.huiin.cn/index.php?m=native&c=dynamic&a=city&city=aaa&page=1&_json=1)

###### 4、管理员设置最热帖子

* 请求方法：POST

  请求必须传递 cookie:usersession

* 是否需要登陆： 是

* 请求参数


 | KEY字段 | 类型 | 必填 | 描述 | 备注 |
 | :------:|:------:|:------:|:------:|:------|
 |  tid | int | 是 | 版本ID |  版本ID |
 |  starttime | string | 是 | 起始日期 |  如2011-1-1 |
 |  endtime | string | 是 | 结束日期 |  如2016-1-1 |

* 调用样列

```
/index.php?m=native&c=dynamic&a=sethot&_json=1
```

* 测试
    无
