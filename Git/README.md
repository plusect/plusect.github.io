# Git
## 常用命令
### 解决 filename too long 问题
```
git config --global core.longpaths true
--global是该参数的使用范围，如果只想对本版本库设置该参数，只要在上述命令中去掉--global即可
```
### 拉取远程仓库
`git clone 地址 本地文件夹`
### 查看当前commit
`git reflog`
### stash
`git stash`
### unstash
`git stash pop`