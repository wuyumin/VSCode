# 常用插件

有些插件安装后可能需要重启才生效。  
插件一般存放在: 用户目录的.vscode/extensions/扩展标识符前缀的文件夹里。  
`xxx Extension Pack`一般是工具包组合(多个插件组合)。如`C/C++ Extension Pack`是C/C++的工具包组合。  
查看已安装的插件`code --list-extensions`  
命令行离线安装插件`code --install-extension 扩展id或.vsix本地路径`  

### 简体中文语言插件

搜索“chinese”

- 名称: Chinese (Simplified) (简体中文) Language Pack for Visual Studio Code
- 扩展标识符: ms-ceintl.vscode-language-pack-zh-hans
- 作用: 简体中文语言

### 各个语言插件

<https://marketplace.visualstudio.com/search?target=VSCode&category=Programming%20Languages&sortBy=Downloads>

默认支持语言或运行时: HTML(HTML5)、CSS(CSS3)、JavaScript、NodeJS、TypeScript。  
vue等可能需要配合jsconfig.json文件才能更好定位跳转(如webpack别名)  
jsconfig.json (文件路径是相对于jsconfig.json的位置)
```json
{
  "compilerOptions": {
    "baseUrl": "./",
    "paths": {
      "@/*": ["src/*"]
    }
  },
  "exclude": ["node_modules", "dist"]
}
```

### 远程开发插件

#### Remote - SSH

- 名称: Remote - SSH
- 扩展标识符: ms-vscode-remote.remote-ssh
- 作用: 远程计算机/虚拟机的远程开发

#### Remote - WSL

- 名称: WSL
- 扩展标识符: ms-vscode-remote.remote-wsl
- 作用: windows下的Linux子系统WSL(Windows Subsystem for Linux)的远程开发

#### Remote - Containers

- 名称: Dev Containers
- 扩展标识符: ms-vscode-remote.remote-containers
- 作用: 容器的远程开发

### TODO.md Kanban Board

- 名称: TODO.md Kanban Board
- 扩展标识符: coddx.coddx-alpha
- 作用: 看板式任务管理(通过命令面板搜索kanban使用)

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

### ~~GitLens~~

- 名称: GitLens
- 扩展标识符: eamodio.gitlens
- 作用: git 增强工具

### ~~Git History~~

- 名称: Git History
- 扩展标识符: donjayamanne.githistory
- 作用: git 日志查看

### Git Graph

- 名称: Git Graph
- 扩展标识符: mhutchie.git-graph
- 作用: 漂亮的git提交历史查看

设置
```js
    // Git Graph设置时间格式，默认是"Date & Time"
    "git-graph.dateFormat": "ISO Date & Time",
```

### Markdown Preview Enhanced

注: 原生已支持基本的Markdown预览功能。  
  
- 名称: Markdown Preview Enhanced
- 扩展标识符: shd101wyy.markdown-preview-enhanced
- 作用: Markdown强大支持

### Error Lens

- 名称: Error Lens
- 扩展标识符: usernamehw.errorlens
- 作用: 更好的错误展示

### Code Runner

- 名称: Code Runner
- 扩展标识符: formulahendry.code-runner
- 作用: 直接运行对应语言的代码
- 注: 配置项code-runner.executorMap是设置各种语言运行环境(具体配置见插件介绍页)

### Sort lines

- 名称: Sort lines
- 扩展标识符: tyriar.sort-lines
- 作用: 按字母排序代码行

### Rust语言插件

- 名称: rust-analyzer
- 扩展标识符: rust-lang.rust-analyzer
- 作用: Rust语言插件

- ~~名称: crates~~(升级到了Dependi)
- 扩展标识符: serayuzgur.crates
- 作用: Rust包管理

- 名称: Dependi
- 扩展标识符: fill-labs.dependi
- 作用: Rust包管理(也支持Go/JavaScript/TypeScript/Python包管理)

- 名称: CodeLLDB
- 扩展标识符: vadimcn.vscode-lldb
- 作用: Rust调试
windows系统直接使用Microsoft C++就可以了

### Go语言插件

- 名称: Go
- 扩展标识符: ms-vscode.go
- 作用: Go语言插件
- 注: 还要安装一些Go第三方包  
  插件参照 <https://github.com/Microsoft/vscode-go/blob/master/src/goInstallTools.ts> allTools变量

- 名称: goctl
- 扩展标识符: xiaoxin-technology.goctl
- 作用: go-zero框架工具

### JavaScript语言插件

- ~~名称: packages~~(使用Dependi替代)
- 扩展标识符: ririd.packages
- 作用: npm包管理

### Python语言插件

- 名称: Python
- 扩展标识符: ms-python.python
- 作用: Python语言插件

- 名称: Ruff
- 扩展标识符: charliermarsh.ruff
- 作用: Ruff代码格式化和代码质量检查插件
如果需要autopep8，请安装autopep8  
如果需要black，请安装Black Formatter  

- 名称: autoDocstring - Python Docstring Generator
- 扩展标识符: njpwerner.autodocstring
- 作用: 自动生成docstring

### C/C++语言插件

- 名称: C/C++
- 扩展标识符: ms-vscode.cpptools
- 作用: C/C++语言插件

- 名称: Clang-Format
- 扩展标识符: xaver.clang-format
- 作用: 代码格式化

### PHP语言插件

- 名称: PHP
- 扩展标识符: DEVSENSE.phptools-vscode
- 作用: PHP语言插件，PHP代码格式化等

注: 下面PHP Intelephense可以不用了(建议替换成上面功能更好的)。
- 名称: PHP Intelephense
- 扩展标识符: bmewburn.vscode-intelephense-client
- 作用: PHP语言插件，PHP代码格式化

### dart语言/flutter插件

- 名称: Dart
- 扩展标识符: Dart-Code.dart-code
- 作用: dart语言插件

- 名称: Flutter
- 扩展标识符: Dart-Code.flutter
- 作用: Flutter插件

### Lua语言插件

- 名称: Lua
- 扩展标识符: sumneko.lua
- 作用: lua语法提示

- 名称: vscode-lua-format
- 扩展标识符: koihik.vscode-lua-format
- 作用: lua格式化工具

### Deno语言插件

- 名称: Deno
- 扩展标识符: denoland.vscode-deno
- 作用: Deno语言插件

### shell脚本插件

- 名称: shell-format
- 扩展标识符: foxundermoon.shell-format
- 作用: shell脚本格式化工具

### Volar(Vue3 插件)

- 名称: Vue - Official(曾用名Vue Language Features (Volar))
- 扩展标识符: Vue.volar
- 作用: Vue3插件

~~TypeScript可能还需要配合`TypeScript Vue Plugin (Volar)`(扩展标识符Vue.vscode-typescript-vue-plugin)~~  

### Vetur(Vue2 插件)

- 名称: Vetur
- 扩展标识符: octref.vetur
- 作用: Vue2插件

### Vue VSCode Snippets

- 名称: Vue VSCode Snippets
- 扩展标识符: sdras.vue-vscode-snippets
- 作用: Vue代码片段

### i18n Ally

- 名称: i18n Ally
- 扩展标识符: Lokalise.i18n-ally
- 作用: 国际化插件

### Tailwind CSS IntelliSense

- 名称: Tailwind CSS IntelliSense
- 扩展标识符: bradlc.vscode-tailwindcss
- 作用: tailwind插件
- 注: 需要npm安装tailwindcss及其依赖`npm i tailwindcss@2.2.7 postcss@8.3.6 autoprefixer@10.3.1 -D`和`npx tailwind init`生成tailwind.config.js配置文件插件后才生效，敲class时可能还需要前面一个`空格`才有提示。

### Docker插件

- 名称: Docker
- 扩展标识符: peterjausovec.vscode-docker
- 作用: Docker插件

### Todo Tree

- 名称: Todo Tree
- 扩展标识符: Gruntfuggly.todo-tree
- 作用: TODO插件

### vscode-proto3

- 名称: vscode-proto3
- 扩展标识符: zxh404.vscode-proto3
- 作用: Protobuf 3插件

### Ansible

- 名称: Ansible
- 扩展标识符: redhat.ansible
- 作用: Ansible插件

### YAML

- 名称: YAML
- 扩展标识符: redhat.vscode-yaml
- 作用: YAML插件

### Even Better TOML

- 名称: Even Better TOML
- 扩展标识符: tamasfe.even-better-toml
- 作用: TOML插件

### XML Tools

- 名称: XML Tools
- 扩展标识符: dotjoshjohnson.xml
- 作用: XML插件

### Rainbow CSV

- 名称: Rainbow CSV
- 扩展标识符: mechatroner.rainbow-csv
- 作用: csv文件插件

### parquet-viewer

- 名称: parquet-viewer
- 扩展标识符: dvirtz.parquet-viewer
- 作用: parquet文件插件

### ~~Live Server~~

- 名称: Live Server
- 扩展标识符: ritwickdey.liveserver
- 作用: 热更新调试

### Power Mode

- 名称: Power Mode
- 扩展标识符: hoovercj.vscode-power-mode
- 作用: 炫酷特效

设置
```js
    // Power Mode炫酷特效插件设置
    "powermode.enabled": true, // 是否开启
    "powermode.presets": "particles", // 样式效果
    "powermode.shake.enabled": false, // 是否抖动
    "powermode.combo.timerEnabled":"hide",
    "powermode.combo.counterEnabled": "hide",
```

### Biome

- 名称: Biome
- 扩展标识符: biomejs.biome
- 作用: 代码格式化

设置
```js
"biome.lspBin": "/Users/user/d/bin/biome",
```

### Prettier - Code formatter

- 名称: Prettier - Code formatter
- 扩展标识符: esbenp.prettier-vscode
- 作用: 代码格式化

### Continue

- 名称: Continue
- 扩展标识符: Continue.continue
- 作用: AI编程工具

设置文件`~/.continue/config.json`
```json
{
  // 注释
  "models": [
    {
      "title": "openai兼容chat",
      "provider": "openai",
      "model": "qwen2.5-instruct:7b", // deepseek-r1:7b
      "apiBase": "http://localhost:11434/v1",
      "apiKey": "empty",
      // "systemMessage": "You are an expert software developer. You give helpful and concise responses."
      "systemMessage": "你叫小智，是吴育民开发的人工智能产品。你是一位专业的软件开发人员，你能提供有用且简洁的回答。"
    }
  ],
  "tabAutocompleteModel": {
    "title": "openai兼容coder",
    "provider": "openai",
    "model": "qwen2.5-coder-instruct:7b",
    "apiBase": "http://localhost:11434/v1",
    "apiKey": "empty"
  }
}
```

### Cline

- 名称: Cline
- 扩展标识符: saoudrizwan.claude-dev
- 作用: AI编程工具

### 通义灵码

- 名称: TONGYI Lingma
- 扩展标识符: Alibaba-Cloud.tongyi-lingma
- 作用: 通义灵码AI编程工具

注: macOS10.15需要安装1.3.x版本(如v1.3.13)  

### typst排版工具

- 名称: Typst LSP
- 扩展标识符: nvarner.typst-lsp
- 作用: typst排版工具

### Thunder Client

- 名称: Thunder Client
- 扩展标识符: rangav.vscode-thunder-client
- 作用: 接口请求(相当于postman)

### REST Client

- 名称: REST Client
- 扩展标识符: humao.rest-client
- 作用: 接口请求(类似于postman、curl)

官网文档<https://github.com/Huachao/vscode-restclient>  
设置
```js
// REST Client扩展设置
// "rest-client.defaultHeaders": {"User-Agent": "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/94.0.4606.54 Safari/537.36"},
```

xxx.http
```ini
#官网及文档https://github.com/Huachao/vscode-restclient

#变量定义
@port = 3000
#变量使用{{port}}

#以三个###分隔多个接口请求

### 请求(RFC2616格式)
GET http://127.0.0.1:3000

### 请求(支持curl格式)
curl -X GET 'http://127.0.0.1:3000' -d 'data'

### POST请求
POST http://127.0.0.1:3000/json
Content-Type: application/json

{
  "username": "zhangsan"
}

### 其它
```
