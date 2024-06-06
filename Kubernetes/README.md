# Kubernetes
## kubelet 常用命令
| 查看每个组件               | kubectl get cs                                                   |
|----------------------|------------------------------------------------------------------|
| 查看node状态             | Kubectl get node                                                 |
| 查看pod状态              | Kubectl get pod                                                  |
| 执行容器命令               | kubectl exec -it Pod名称 -c 容器名称 -n 命名空间 -- 命令                     |
| 查看命名空间               | Kubectl get ns                                                   |
| 查看service            | Kubectl get svc                                                  |
| 查看configmap          | Kubectl get cm                                                   |
| 查看crd                | Kubectl get crd                                                  |
| 描述资源                 | Kubectl describe 资源类型 -n 命名空间                                    |
| k8s从指定container中cp文件 | kubectl cp  pod名:/容器目录/文件名  -c 指定的container名 /宿主机目录/文件名 -n 命名空间  |
| cp指定宿主机文件到container  | kubectl cp 宿主机目录/文件名 -n <namespce> <podname>:容器目录 -c <container> |
| 设置污点                 | kubectl taint nodes node名称 key=value:effect                      |
|                      | effect如下三种：                                                      |
|                      | NoSchedule ：表示k8s将不会将Pod调度到具有该污点的Node上                           |
|                      | PreferNoSchedule ：表示k8s将尽量避免将Pod调度到具有该污点的Node上                   |
|                      | NoExecute ：表示k8s将不会将Pod调度到具有该污点的Node上，同时会将Node上已经存在的Pod驱逐出去      |
| 去除污点                 | kubectl taint nodes node名称 key:effect-                           |
| 查看kubelet日志          | journalctl -xu kubelet -f                                        |

## Kustomize

## Helm
