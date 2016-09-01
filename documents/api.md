### PhpWind 9.0.1移动端接口整理

#### 接口列表

1. [动态帖子列表相关接口](#动态帖子列表相关接口)











##### 动态帖子列表相关接口

###### 1.获取最热帖子列表

请求方法

GET

###### 调用样例
```
/index.php?m=native&c=dynamic&a=hot&page=1&timestamp=1000000&_json=1
```
###### 返回结果
```json
 response: {"err":"","data":""}
```
