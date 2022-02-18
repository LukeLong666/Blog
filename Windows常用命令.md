# Windows常用命令

## 刷新DNS
```bash
ipconfig /flushdns
```

## 查找端口
```bash
# 列出所有端口情况
netstat -ano
# 查找某个端口的情况，PID等信息
netstat -aon|findstr "8080"
# 查找某个进程(PID)的情况
tasklist|findstr "39148"
# 强制结束某个进程(PID)及其紫禁城
taskkill /T /F /PID 39148 
```