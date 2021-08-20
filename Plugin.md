# 常用插件

插件一般存放在：用户目录的.vscode/extensions/扩展标识符前缀的文件夹里

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

### TODO.md Kanban Board

- 扩展标识符：coddx.coddx-alpha
- 作用：看板式任务管理(通过命令面板搜索kanban使用)

vi TODO.md
```md
# 项目名称

说明: VSCode通过命令面板搜索kanban使用  
项目描述  

### 待办

- [ ] 待办任务1  
  - [ ] 子任务1  
  - [ ] 子任务2  
- [ ] 待办任务2  

### 进行中

- [ ] 进行任务1  
- [ ] 进行任务2  

### 完成 ✓

- [x] 完成任务1  
- [x] 完成任务2  
```

### GitLens

- 扩展标识符：eamodio.gitlens
- 作用：git 增强工具

### Git History

- 扩展标识符：donjayamanne.githistory
- 作用：git 日志查看

### Git Graph

- 扩展标识符：mhutchie.git-graph
- 作用：漂亮的 git 提交历史查看

设置
```js
    // Git Graph设置时间格式，默认是"Date & Time"
    "git-graph.dateFormat": "ISO Date & Time",
```

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

### Rust语言插件

Rust语言插件1
- 扩展标识符：matklad.rust-analyzer
- 作用：Rust语言插件

Rust语言插件2
- 扩展标识符：rust-lang.rust
- 作用：Rust语言插件
- 注：还要安装一些Rust组件
  
注：目前两个插件不能共用。  

### Lua语言插件

lua语法提示
- 扩展标识符：sumneko.lua
- 作用：Lua语言插件

lua格式化工具
- 扩展标识符：koihik.vscode-lua-format
- 作用：Lua语言插件

### Deno语言插件

- 扩展标识符：denoland.vscode-deno
- 作用：Deno语言插件

### Vetur(Vue 插件)

- 扩展标识符：octref.vetur
- 作用：Vue 插件

### Tailwind CSS IntelliSense

- 扩展标识符：bradlc.vscode-tailwindcss
- 作用：tailwind 插件
- 注：需要npm安装tailwindcss及其依赖`npm i tailwindcss@2.2.7 postcss@8.3.6 autoprefixer@10.3.1 -D`和`npx tailwind init`生成tailwind.config.js配置文件插件后才生效

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

### Even Better TOML

- 扩展标识符：tamasfe.even-better-toml
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
```js
    // Power Mode炫酷特效插件设置
    "powermode.enabled": true, // 是否开启
    "powermode.presets": "particles", // 样式效果
    "powermode.enableShake": false, // 是否抖动
```

### Prettier - Code formatter

- 扩展标识符：esbenp.prettier-vscode
- 作用：代码格式化

### Clang-Format

- 扩展标识符：xaver.clang-format
- 作用：代码格式化
