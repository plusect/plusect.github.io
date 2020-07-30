# Linux

## 常用命令
### Systemctl目录
`/usr/lib/systemd/system`
### Systemctl命令
`Systemctl start xxx.service`
### zip命令
压缩 `zip [参数] [打包后的文件名] [打包的目录路径]`  
解压 `unzip xxx`
### gunzip命令
解压gz后缀文件 `gunzip xxx`
### tar命令
压缩 `tar -czvf xxx.tar.gz target`  
解压 `tar -xzvf xxx.tar.gz`
### scp命令
`scp (-r) xxx user@ip:/path`
### mv命令
`mv (-r) xxx path`
### 查看目录大小
```
du -h(s) | sort -n
du -h --max-depth=1
```
### 查看cpu信息
`cat /proc/cpuinfo`
### 查看内存
`free -m`
### 查看IO
`iostat (-[k/m][x]) 时间间隔second`
### 创建用户
1. `useradd xxx (-g xxx)`
2. `passwd xxx`
### 创建用户组
`groupadd xxx`
### 查看用户组	
```
groups 查看当前登录用户的组内成员
groups gliethttp 查看gliethttp用户所在的组,以及组内成员
cat /etc/group文件包含所有组
/etc/shadow和/etc/passwd系统存在的所有用户名
```
### 查看用户
`whoami 查看当前登录用户名`
### 查看最近登录
`last`
### 查找文件
`find / -name 'xxx.xxx'`
### 临时修改hosts
`hostname xxx`
### 修改组
`groupmod –n user group`
### 删除用户
`userdel (-r) xxx`
### 删除用户组
`groupdel xxx`
### 用户加入用户组
`gpasswd –a user group`
### 用户退出用户组
`gpasswd -d user group`
### 连接数
`ulimit -n`
### 查看历史命令
`history`
### 执行第几条命令
`!number`
### 执行上一条命令
`!`
### 生成临时目录
`mktemp -d`
### 指定位置生成临时目录
`mktemp -d --tmpdir=/home abc.XXX`
### md5
`md5sum xxx`
### grep显示前后5行
`grep -C 5`
### 查看网卡
```
ip addr 
ifconfig
```
