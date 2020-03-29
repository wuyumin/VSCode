# 常用插件

### 简体中文语言插件

搜索“chinese”

- 扩展标识符：ms-ceintl.vscode-language-pack-zh-hans
- 作用：简体中文语言

### 各个语言插件

<https://marketplace.visualstudio.com/search?target=VSCode&category=Programming%20Languages&sortBy=Downloads>

默认支持语言：HTML(HTML5)、CSS(CSS3)、JavaScript、NodeJS、TypeScript。

### 远程开发插件

#### Remote - SSH

- 扩展标识符：ms-vscode-remote.remote-ssh
- 作用：远程计算机/虚拟机的远程开发

#### Remote - WSL

- 扩展标识符：ms-vscode-remote.remote-wsl
- 作用：windows下的Linux子系统WSL(Windows Subsystem for Linux)的远程开发

#### Remote - Containers

- 扩展标识符：ms-vscode-remote.remote-containers
- 作用：容器的远程开发

### GitLens

- 扩展标识符：eamodio.gitlens
- 作用：git 增强工具

### Git History

- 扩展标识符：donjayamanne.githistory
- 作用：git 日志查看

### Git Graph

- 扩展标识符：mhutchie.git-graph
- 作用：漂亮的 git 提交历史查看

### Code Runner

- 扩展标识符：formulahendry.code-runner
- 作用：直接运行对应语言的代码
- 注：配置项code-runner.executorMap是设置各种语言运行环境(具体配置见插件介绍页)

### Sort lines

- 扩展标识符：tyriar.sort-lines
- 作用：按字母排序代码行

### Go语言插件

- 扩展标识符：ms-vscode.go
- 作用：Go语言插件
- 注：还要安装一些Go第三方包  
  插件参照 <https://github.com/Microsoft/vscode-go/blob/master/src/goInstallTools.ts> allTools变量

### Python语言插件

- 扩展标识符：ms-python.python
- 作用：Python语言插件

### C/C++语言插件

- 扩展标识符：ms-vscode.cpptools
- 作用：C/C++语言插件

### PHP语言插件

- 扩展标识符：felixfbecker.php-intellisense
- 作用：PHP语言插件

### Vetur(Vue 插件)

- 扩展标识符：octref.vetur
- 作用：Vue 插件

### Docker 插件

- 扩展标识符：peterjausovec.vscode-docker
- 作用：Docker 插件

### Todo Tree

- 扩展标识符：Gruntfuggly.todo-tree
- 作用：TODO 插件

### vscode-proto3

- 扩展标识符：zxh404.vscode-proto3
- 作用：Protobuf 3 插件

### Ansible

- 扩展标识符：vscoss.vscode-ansible
- 作用：Ansible 插件

### YAML

- 扩展标识符：redhat.vscode-yaml
- 作用：YAML 插件

### Better TOML

- 扩展标识符：bungcip.better-toml
- 作用：TOML 插件

### XML Tools

- 扩展标识符：dotjoshjohnson.xml
- 作用：XML 插件

### Live Server

- 扩展标识符：ritwickdey.liveserver
- 作用：热更新调试

### Power Mode

- 扩展标识符：hoovercj.vscode-power-mode
- 作用：炫酷特效

设置
```json
    // Power Mode炫酷特效插件设置
    "powermode.enabled": true, // 是否开启
    "powermode.presets": "particles", // 样式效果
    "powermode.enableShake": false, // 是否抖动
```

### Prettier - Code formatter

- 扩展标识符：esbenp.prettier-vscode
- 作用：代码格式化
