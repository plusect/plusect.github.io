# 绑定远程仓库

1.本地创建仓库 

2.在线平台已经建立好一个空的仓库

3.输入如下命令，将本地仓库与远程仓库关联  

> git remote add **origin** https://github.com/plusect/JavaExercise.git  
**注意**：这里需要注意的是上面命令中的**origin**是远程仓库在本地Git的名称，默认情况下一般命名为origin，如果使用多个平台，为了区分不同平台的远程仓库，也可以改为其他的（例如：Github平台命名为github,Gitee平台命名为gitee）

4.查看本地仓库与远程仓库的关联  
> git remote -v  

# 解除绑定远程仓库
输入如下命令:  

> git remote rm **origin**  
> **注意**: **origin**是远程仓库在本地Git中的名称  



