# 在联网服务器拉取安装 createrepo 所需依赖
1. 拉取需要的所有 rpms 包
```
mkdir createrepo_rpms
cd ./createrepo_rpms
repotrack createrepo
```
# 在联网服务器拉取安装 docker 所需依赖
1. 添加 docker 官方 yum 镜像源  
`yum-config-manager     --add-repo     https://download.docker.com/linux/centos/docker-ce.repo`  
3. 拉取需要的所有 rpms 包
```
mkdir docker_rpms
cd ./docker_rpms
repotrack docker-ce-18.09.9-3.el7 docker-ce-cli-18.09.9-3.el7 containerd.io
```
# 在目标离线服务器创建本地 docker 的 yum 源
## 所有镜像上传到当前服务器
略
## 安装 createrepo
```
cd ./createrepo_rpms
npm -ivh createrepo-0.9.9-28.el7.noarch.rpm
```
## 创建本地 yum 仓库
```
# 使用 rpm 包所在目录创建本地 yum 仓库
createrepo ./docker_rpms/
# 添加到 repo 文件夹
cat <<EOF>> /etc/yum.repos.d/docker.repo
[docker]
name=dokcer-ce
baseurl=file:///opt/local-repos/docker_rpms
gpgcheck=0
enabled= 1
EOF
# 刷新 yum 缓存
yum clean all && yum makecache
# 安装 docker
yum install -y docker-ce-18.09.9-3.el7 docker-ce-cli-18.09.9-3.el7 containerd.io
```
## 启动 Docker  
`systemctl enable docker && systemctl start docker`