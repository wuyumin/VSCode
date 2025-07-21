# 常用配置

## 设置项

配置一般分为`用户设置`、`工作区设置`、`项目文件夹设置`。  
`一般可通过菜单上的设置来调整`。 

`用户设置：`配置文件存放在用户目录下。比如windows系统是存放在用户目录下的AppData\Roaming\Code\User\settings.json macOS系统是存放在用户目录下的Library/Application Support/Code/User/settings.json  
```json
{
  // "http.proxy": "http://127.0.0.1:7890", // 设置代理
  // "http.proxyStrictSSL": false, // 验证证书
  // "editor.formatOnSave": true, // 保存时自动格式化

  "files.encoding": "utf8", // 字符集编码 utf8/gbk
  "editor.detectIndentation": false, // 配置tabSize时可能需要这个
  "editor.tabSize": 2, // 一个tab等于多少个空格
  // "editor.insertSpaces": false, // 按tab插入空格
  // "editor.bracketPairColorization.enabled": true, // 括号对着色
  "editor.guides.bracketPairs": "active", // 括号对指南(代码块边缘导轨线着色)
  // 未高亮显示unicode字符
  "editor.unicodeHighlight.allowedLocales": {
    "zh-hans": true
  },

  "update.mode": "none", // 取消自动更新VSCode
  "extensions.autoUpdate": false, // 取消自动更新扩展
  "extensions.autoCheckUpdates": false, // 取消扩展更新检查
  "remote.autoForwardPorts": false, // 取消端口转发
  "security.workspace.trust.enabled": false, // 工作区信任处理
  "workbench.colorTheme": "Visual Studio Dark", // 色彩主题
  "workbench.startupEditor": "none", // 编辑器启动后默认显示
  "workbench.editor.openPositioning": "last", // 新打开页的显示位置
  "editor.renderWhitespace": "all", // 显示隐藏的tab和空格
  "editor.tabCompletion": "on", // tab键补全
  // "editor.minimap.enabled": false, // 是否显示缩略图
  "breadcrumbs.enabled": false, // 禁用导航路径
  "diffEditor.ignoreTrimWhitespace": false, // 显示首尾的空白差异
  "explorer.autoReveal": false, // 资源管理器打开文件时自动显示并选择
  "explorer.compactFolders": false, // 不使用紧凑显示文件夹
  "terminal.integrated.enablePersistentSessions": false, // 是否保持上次的终端对话
  "window.restoreWindows": "none", // 启动后是否自动打开上次使用的窗口
  "window.commandCenter": false, // 隐藏命令中心
  // 显示:排除的文件和文件夹
  "files.exclude": {
    // "**/.git": false, // 临时关闭排除
    "**/.DS_Store": false,
    "**/.idea": true, // JetBrains系列软件配置文件
    "**/__pycache__": true, // python字节码目录
  },
  // 搜索:排除的文件和文件夹
  "search.exclude": {
    // "**/node_modules": true,
    // "**/bower_components": true,
    // "**/*.code-search": true,
    "**/.git": true, // git文件
    "**/.idea": true, // JetBrains系列软件配置文件
    "**/go.sum": true, // go依赖自动文件
    "**/go.work.sum": true, // go工作区自动文件
    "**/Cargo.lock": true, // rust依赖自动文件
    "**/target": true, // rust编译生成
    "**/__pycache__": true, // python字节码目录
  },
  "search.useIgnoreFiles": true,

  // 配置语言的文件关联(自定义文件扩展名映射)
  "files.associations": {
    "*.json": "jsonc",
    "*.rc": "properties",
  },

  // Remote-SSH配置
  "remote.SSH.configFile": "E:\\ConfigPath\\remote_ssh.ini", // 一般是~/.ssh/config

}
```

`工作区设置：`你的工作区配置文件(后缀为.code-workspace文件)的settings项里。
```json
{
	// 单行注释

	/*
	多行注释
	*/

	"folders": [
		{
			"path": "E:\\Projects\\PythonTest"
		}
	],
	"settings": {
	}
}
```

`项目设置`项目文件夹里的.vscode/settings.json文件。  
`项目推荐插件`项目文件夹里的.vscode/extensions.json文件。  
  
管理受信任的域(Manage Trusted Domains): 方便快速打开外部链接。  

### windows系统设置命令终端

终端配置(新版)
```json
  "terminal.integrated.profiles.windows": {
    // Command Prompt
    "Command Prompt": {
      "path": "C:\\WINDOWS\\System32\\cmd.exe",
      "args": []
    },
    // PowerShell
    "PowerShell": {
      "path": "C:\\Windows\\System32\\WindowsPowerShell\\v1.0\\powershell.exe",
      "args": []
    },
    // Git Bash
    "Git-Bash": {
      "path": "D:\\Program Files\\Git\\bin\\bash.exe",
      "args": ["--login", "-i"]
    }
  },
  "terminal.integrated.defaultProfile.windows": "Command Prompt",
```

终端配置(旧版)
```json
  // Command Prompt
  "terminal.integrated.shell.windows": "C:\\WINDOWS\\System32\\cmd.exe",
  // PowerShell
  // "terminal.integrated.shell.windows": "C:\\Windows\\System32\\WindowsPowerShell\\v1.0\\powershell.exe",
  // Git Bash
  // "terminal.integrated.shell.windows": "D:\\Program Files\\Git\\bin\\bash.exe",
```

### prettier格式化设置

```json
"prettier.tabWidth": 2,
```

### 自定义格式化[各语言分别设置(多语言一起设置版本1.63+)]

```json
"[html]": {
  "editor.defaultFormatter": "esbenp.prettier-vscode"
},
"[css]": {
  "editor.defaultFormatter": "esbenp.prettier-vscode",
},
"[javascript][typescript]": {
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "editor.formatOnSave": true,
},
"[vue]": {
  "editor.defaultFormatter": "esbenp.prettier-vscode", // vue3: Vue.volar vue2: octref.vetur
  "editor.formatOnSave": true
},
"[json][jsonc]": {
  "editor.defaultFormatter": "esbenp.prettier-vscode"
},

"[yaml]": {
  "editor.defaultFormatter": "redhat.vscode-yaml",
  "editor.formatOnSave": true
},
"yaml.format.singleQuote": true,

"[toml]": {
  "editor.formatOnSave": true
},
"[python]": {
  "editor.defaultFormatter": "charliermarsh.ruff", // 原来是"editor.defaultFormatter": "ms-python.python",
  "editor.formatOnSave": true,
  "editor.codeActionsOnSave": {
    // "source.fixAll": true,
    "source.organizeImports": true,
  },
},
"[rust]": {
  "editor.formatOnSave": true
},
"[c][cpp][h][hpp]": {
  "editor.defaultFormatter": "xaver.clang-format",
  "editor.formatOnSave": true
},
"[shellscript]": {
  "editor.formatOnSave": true
},
```

### rust语言设置

```json
"rust-analyzer.showUnlinkedFileNotification": false,
"rust-analyzer.inlayHints.typeHints.enable": false,
"rust-analyzer.inlayHints.parameterHints.enable": false,
"rust-analyzer.inlayHints.chainingHints.enable": false,
"rust-analyzer.inlayHints.closingBraceHints.enable": false,
"rust-analyzer.cargo.buildScripts.enable": true,
"rust-analyzer.lens.enable": false,
```

### go语言设置

```json
// "go.toolsEnvVars": {
//   "GOPROXY": "https://goproxy.cn,direct"
// },
"go.toolsManagement.checkForUpdates": "off", // 取消gopls更新提示
"go.useLanguageServer": true, // Go语言启用LanguageServer
"go.formatTool": "goimports", // 格式化工具
// staticcheck代码规范配置
"go.lintFlags": [
  "-checks",
  "all,-ST1000,-ST1001,-ST1003,-ST1006,-ST1020,-ST1021,-ST1022,-U1000"
],
// 结构体tag配置(参考https://github.com/fatih/gomodifytags)
"go.addTags": {
  // json,xml,form,validate:required,gorm:column:xxx;type:varchar(255);not null;default:'',bson,redis
  // 可配置多个，英文逗号隔开
  "tags": "json",
  // json=,xml=,form=,validate=,gorm=,bson=,redis=
  // 可配置多个，英文逗号隔开，多个相同最终会合并一起(如json=omitempty,json=options2,yaml=omitempty)
  "options": "json=",
  "template": "{field}",
  // snakecase蛇形 camelcase驼峰
  "transform": "snakecase",
  "promptForTags": false,
},
// 右键显示go常用操作命令配置
"go.editorContextMenuCommands": {
  "removeTags": true,
  "fillStruct": true,
  "playground": false,
  "testCoverage": false,
},
```

### python语言设置

```json
"python.defaultInterpreterPath": "D:\\Python\\miniconda\\envs\\pythonVenv\\bin\\python3.exe", // 加载虚拟环境(填写虚拟环境python二进制文件绝对路径) 旧版本配置项python.pythonPath
//"python.defaultInterpreterPath": "D:\\Python\\venv\\Scripts\\python.exe",
"python.terminal.activateEnvInCurrentTerminal": false,
"python.terminal.activateEnvironment": true,
"ruff.configuration": "C:\\Users\\user\\.config\\pyproject.toml",
// "python.formatting.provider": "yapf", // 需要安装pip3 install yapf(可能需要超级管理员权限)
// "python.formatting.yapfArgs": [
//   "--style={indent_width:2, spaces_before_comment:1, column_limit:120}"
// ],
```

### Zig语言设置

```json
"zig.zls.enabled": "on",
"zig.zls.path": "D:\\bin\\zls.exe",
"zig.zls.inlayHintsShowVariableTypeHints": false,
"zig.zls.inlayHintsShowParameterName": false,
"zig.zls.inlayHintsShowStructLiteralFieldType": false,
"zig.zls.enableArgumentPlaceholders": false,
```

## 键盘快捷方式设置

与设置项菜单同一级的`键盘快捷方式`进行配置 `keybindings.json`文件
```json
// 将键绑定放在此文件中以覆盖默认值
[
  {
    "key": "ctrl+shift+l",
    "command": "editor.action.transformToLowercase"
  },
  {
    "key": "ctrl+shift+u",
    "command": "editor.action.transformToUppercase"
  },
  // ...
]
```
