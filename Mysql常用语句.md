# Mysql常用语句

## 查看当前所有事务
> 用于当表被锁时查看进程，并选择杀死某个进程
```sql
#查看任务列表
show processlist;

#查看事务
select * from information_schema.innodb_trx;

#杀死进程
kill 进程ID;
```