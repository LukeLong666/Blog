# Docker常用命令

## Mysql
```bash
#启动一个Mysql容器
docker run --name <容器名称> -p 13306:3306 -itd -v <本机需要挂在数据地址>:/var/lib/mysql -e MYSQL_ROOT_PASSWORD="root" <镜像ID>
```