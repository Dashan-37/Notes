# `SpringCloud`

<br>

### 什么是微服务？

- 微服务是一站式的技术解决方案，微服务之间是可以通过`http` `resetful` 的方式进行请求访问
- 每个微服务都是相互独立的
- 微服务能够解决的技术方案
  * `Eureka`：注册中心
    * `Eureka` `Zookeeper` `Consul` `Nacos`
    * 注册中心，是有`CAP`理论支持的
      * `C`：一致性
      * `A`：高可用
      * `P`：指的分布式系统中的某个节点或者网络分区出现了故障的时候，整个系统仍然能对外提供满足一致性和可用性的服务。也就是说部分故障不影响整体使用。
      * 没有办法全部满足`CAP`特性的，要么偏向于`CP`，要么偏向于`AP`
  * `Ribbon`：客户端负载均衡
    * 概念类似于`Nginx`
  * `Hystrix`：服务熔断和降级
    * 当遇到异常或超时问题时，快速的响应一个结果回来
    * 可以支持服务的限流
  * `Feign`：远程调用`api`
    * 类似的有`RestTemplate`，通过`http`方式进行`reset ful`风格的`api`请求
  * `Zuul`：网关
    * 微服务的第一道屏障
    * 可以在网关中进行权限的校验

<br>

<br>

### 搭建`SpringCloud`版本的步骤

- 导入`pom.xml`中的启动器依赖
- 配置文件，`properties` 或 `yml`
  * 推荐使用`yml`
- 引导器上添加注解
  * `Application`

<br>

<br>

### `Eureka`

`Eureka`的客户端和服务器端

* 客户端
  * 向注册中心注册的微服务
* 服务器端
  * EurekaServer `注册中心`

<br>

<br>

### 搭建服务器端

- `pom.xml`中导入启动器依赖
  - 注意`SpringBood`和`SpringCloud`对应的版本
  - 不要自己随意导入，如果出现启动操作或`jar`包冲突，就是版本问题导致的无法启动