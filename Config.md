# 常用配置

## 设置项

配置一般分为`用户设置`、`工作区设置`、`项目文件夹设置`。  
`一般可通过菜单上的设置来调整`。 

`用户设置：`配置文件存放在用户目录下。比如windows系统是存放在用户目录下的AppData\Roaming\Code\User\settings.json  
```js
{
  // "http.proxy": "http://127.0.0.1:1080", // 设置代理
  // "http.proxyStrictSSL": false, // 验证证书
  // "editor.formatOnSave": true, // 保存时自动格式化

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
  "security.workspace.trust.enabled": false, // 工作区信任处理
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
  // 配置排除的文件和文件夹
  "files.exclude": {
    // "**/.git": false, // 临时关闭排除
    "**/.DS_Store": false,
    "**/.idea": true, // 排除JetBrains系列软件配置文件
  },

  // 配置语言的文件关联
  "files.associations": {
    "*.json": "jsonc",
  },

}
```

`工作区设置：`你的工作区配置文件(后缀为.code-workspace文件)的settings项里。
```js
{
	"folders": [
		{
			"path": "E:\\Projects\\PythonTest"
		}
	],
	"settings": {
	}
}
```

`项目文件夹设置：`项目文件夹里.vscode文件夹下的settings.json文件。

### windows系统设置命令终端

终端配置(新版)
```js
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
```js
  // Command Prompt
  "terminal.integrated.shell.windows": "C:\\WINDOWS\\System32\\cmd.exe",
  // PowerShell
  // "terminal.integrated.shell.windows": "C:\\Windows\\System32\\WindowsPowerShell\\v1.0\\powershell.exe",
  // Git Bash
  // "terminal.integrated.shell.windows": "D:\\Program Files\\Git\\bin\\bash.exe",
```

### prettier格式化设置

```js
"prettier.tabWidth": 2,
```

### 自定义格式化[各语言分别设置(多语言一起设置版本1.63+)]

```js
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
  "editor.defaultFormatter": "octref.vetur",
  "editor.formatOnSave": true
},
"[json][jsonc]": {
  "editor.defaultFormatter": "esbenp.prettier-vscode"
},
"[yaml]": {
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "editor.formatOnSave": true
},
"[toml]": {
  "editor.formatOnSave": true
},
"[python]": {
  "editor.defaultFormatter": "ms-python.python",
  "editor.formatOnSave": true
},
"[rust]": {
  "editor.formatOnSave": true
},
"[c][cpp][h][hpp]": {
  "editor.defaultFormatter": "xaver.clang-format",
  "editor.formatOnSave": true
},
```

### go语言设置

```js
"go.useLanguageServer": true, // Go语言启用LanguageServer
"go.formatTool": "goimports", // 格式化工具
// staticcheck代码规范配置
"go.lintFlags": [
  "-checks",
  "all,-ST1000,-ST1001,-ST1006,-ST1020"
],
// 结构体tag配置(参考https://github.com/fatih/gomodifytags)
"go.addTags": {
  // json,xml,form,validate:required,gorm:column:xxx;type:varchar(255);not null;default:''
  "tags": "json",
  // json=,xml=,form=,validate=,gorm=
  "options": "json=",
  "template": "{field}"
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

```js
"python.defaultInterpreterPath": "D:\\Python\\venv\\Scripts\\python.exe", // 加载虚拟环境(填写虚拟环境python二进制文件绝对路径) 旧版本配置项python.pythonPath
"python.terminal.activateEnvInCurrentTerminal": true,
"python.formatting.provider": "yapf", // 需要安装pip3 install yapf(可能需要sudo)
"python.formatting.yapfArgs": [
  "--style={indent_width: 2}"
],
```

### rust语言设置

```js
"rust-analyzer.inlayHints.parameterHints.enable": false,
"rust-analyzer.inlayHints.chainingHints.enable": false,
"rust-analyzer.inlayHints.typeHints.enable": false,
"rust-analyzer.inlayHints.closingBraceHints.enable": false,
```

## 键盘快捷方式设置

与设置项菜单同一级的`键盘快捷方式`进行配置
```js
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
