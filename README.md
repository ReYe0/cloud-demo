# 学习笔记
## 创建微服务案例
1. 新建maven项目，删除多余的东西；在此基础上，新建两个module，用spring初始化，名为order-service、user-service。
2. 在两个模块内创建实体，配置mybatis，配置端口号，数据库，写一个简单的查询。
3. 启动两个服务，可以各自访问各自的请求。

## 远程调用
1. 在需要调用远程服务的启动类上面注入ResTemplate类，在服务类声明ResTemplate，调用远程接口的url，设置返回对象。

## Eureka
1. 客户端会每个三十秒想服务端发送心跳。