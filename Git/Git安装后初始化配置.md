# Git安装后初始化配置

## 设置Git的用户名和邮箱 

1. 设置用户名    
`git config -global user.name "plusect"`  
2. 设置邮箱  
`git config -global user.email "plusect@gmail.com"`  
3. 验证用户名和邮箱是否正确  
`git config -global user.name`  
`git config -global user.email`  

## 设置SSH互信  

1. 进入用户目录  
`cd ~`  

2. 检查.ssh文件夹是否存在，存在的话是否有内容  
`ls`  

3. 如果有，删除id_rsa id_rsa.pub  
`rm id_rsa id_rsa.pub`  

4. 创建公钥  
`ssh-keygen -t rsa -C "plusect@gmail.com"`  

5. 按三次Enter，直到完成 
    
6. 查看生成的公钥  
`cat id_rsa id_rsa.pub`  

7. 在Github或者Gitee上使用公钥  
