# Git常用命令

## 已经被PUSH的文件加入gitignore使之生效
```bash
# 清除缓存
git rm -r --cached .
# 添加所有
git add .
# 提交
git commit -m 'update .gitignore'
```

## 更改分支名称
```bash
# 本地分支重命名(还没有推送到远程)
git branch -m oldName newName

# 本地和远程仓库同时修改

## 重命名远程分支对应的本地分支
git branch -m oldName newName
## 删除远程分支
git push --delete origin oldName
## 上传新命名的本地分支
git push origin newName
## 把修改后的本地分支与远程分支关联
git branch --set-upstream-to origin/newName
```