# Markdown
## 安装指南
1. 安装VSCode
   1. 配置控制台默认为Git
      1. 左下角Manage-Settings
      2. 搜索Terminal
      3. Terminal > External: Windows Exec
      4. 地址配置为Git地址
      5. 保存重启
   2. 安装VSCode组件
      1. IntelliJ IDEA Keybindings(重新映射快捷键为idea的快捷键)
      2. Markdown All in One(TOC生成目录、导出html、自动补完)
      3. Markdown PDF(导出html、pdf等)
      4. Markdown Preview Github Styling(github风格预览)
      5. PlantUML(代码化的各种类型图生成)
      6. Draw.io Integration(画各种类型图插件)
2. 安装nvm
   1. 下载nvm-setup.zip https://github.com/coreybutler/nvm-windows/releases
   2. 安装nvm
   3. 打开管理员权限的`powershell`
   4. 输入`nvm v`，显示版本则安装成功
   5. 配置node、npm的国内镜像
   ```
   nvm node_mirror https://npm.taobao.org/mirrors/node/
   nvm npm_mirror https://npm.taobao.org/mirrors/npm/
   ```
   1. 查看可用的版本，可选参数available，显示所有可下载的版本  
   `nvm list [available]`
   1. 安装需要的版本，目前稳定版12.18.2  
   `nvm install 12.18.2`
   1. 使用安装的版本  
   `nvm use 12.18.2`
   1. 查看目前使用版本。*的为当前使用的  
   `nvm list`
   1.  卸载版本  
   `nvm uninstall 12.18.2`