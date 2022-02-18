# Docker常用命令

## Mysql
```bash
#启动一个Mysql容器
docker run --name <容器名称> -p 13306:3306 -itd -v <本机需要挂在数据地址>:/var/lib/mysql -e MYSQL_ROOT_PASSWORD="root" <镜像ID>
```

## Redis
```bash
#启动一个不映射数据的Redis容器
docker run --name <容器名称> -p 16379:6379 -d <镜像ID> --requirepass ****** redis-server

#查看现有密码
config get requirepass
#设置新的密码
config set requirepass ******
```

## Nacos
```bash
# 启动Nacos
docker run -d --name luke_nacos -p 18848:8848 -e PREFER_HOST_MODE=hostname -e MODE=standalone nacos/nacos-server:v2.0.3

# 修改配置文件
docker exec -it luke_nacos /bin/bash
vi conf/application.properties
```