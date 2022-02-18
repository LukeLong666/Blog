> 据说从Activiti7开始，官方就开发了相关的Starter，这就使得SpringBoot整合Activiti变得相当简单
## 1. 引入相关依赖
```xml
<!-- Activiti Starter -->
<dependency>
    <groupId>org.activiti</groupId>
    <artifactId>activiti-spring-boot-starter</artifactId>
    <version>7.0.0.Beta2</version>
</dependency>
<!-- Mysql -->
<dependency>
    <groupId>mysql</groupId>
    <artifactId>mysql-connector-java</artifactId>
    <scope>runtime</scope>
</dependency>
```

## 2. 在配置文件中配置所需内容
```yml
spring:

  # 配置数据库信息
  datasource:
    url: jdbc:mysql://127.0.0.1:13306/activiti?characterEncoding=utf-8&amp;serverTimezone=Asia/Shanghai
    driver-class-name: com.mysql.cj.jdbc.Driver
    username: root
    password: root

  # Activiti相关配置
  activiti:
    database-schema-update: true
    db-history-used: true
    history-level: full
    check-process-definitions: false
```

## 3. SpringSecurity权限验证
> 由于Activiti的starter默认集成了SpringSecurity，所以我们需要配置相关内容。
