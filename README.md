# 学习笔记
## 创建微服务案例
1. 新建maven项目，删除多余的东西；在此基础上，新建两个module，用spring初始化，名为order-service、user-service。
2. 在两个模块内创建实体，配置mybatis，配置端口号，数据库，写一个简单的查询。
3. 启动两个服务，可以各自访问各自的请求。

## 远程调用
1. 在需要调用远程服务的启动类上面注入ResTemplate类，在服务类声明ResTemplate，调用远程接口的url，设置返回对象。

## Eureka
1. 客户端会每个三十秒想服务端发送心跳。
2. 引入服务端依赖，在serve端加入eureka的注解，yml文件中配置eureka的地址服务名。
3. 引入客户端依赖，yml文件中配置。

## 负载均衡
 1. 更改url的主机端口为服务名，在ResTemplate中加入负载均衡的注解。
 2. 当有多个集群时，可以互相分摊访问。

## Ribbon负载均衡
1. 全局配置
2. 服务配置 yml

## nacos
1. 服务的注册和发现，分布式配置。
2. nacos.io 官网，下载，启动。
3. 启动命令
· Windows安装命令
```
startup.cmd -m standalone
```
4. 账号密码都是 nacos

## Feign
1. 比ResTemplate更优雅，声明式
2. 引入依赖，启动类加上注解
3. 创建client类，加注解，写方法。
4. feign 的配置。可以 yml 配置，也可以bean配置；bean配置之后可以加在启动类，这是全局；也可以加在client类上，是局部。
5. feign的性能优化。连接池配置。引入依赖，配置连接池yml。
6. feign的最佳实践。方式一，继承。方式二，抽取，公共模块。

## gateway
1. 网关有两个，zuul较早，gateway比较新。
2. 新建模块，引入依赖，创建启动类。配置yml
3. 断言工厂
4. 过滤器工厂