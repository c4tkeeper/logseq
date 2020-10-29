---
title: OpenFeign
---

## 是什么
        服务调用，声明式Web服务端。只需要一个接口和一个注解
        简单，封装ribbon+restTemplate
        OpenFeign和Feign的区别，在Feign的基础上增强对SpringMVC的支持
    操作步骤
        接口+注解，微服务调用接口+注解FeignClient
        创建模块cloud-consumer-feign-order80
        POM引入spring-cloud-starter-openfeign
        application.yml
        启动类添加注解EnableFeignClients
        业务类
            PaymentFeignService，注解FeignClient(value = "要调用的服务名称")
            OrderFeignController，调用PaymentFeignService的方法
        自带负载均衡功能
    超时控制
