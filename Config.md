# 常用配置

配置一般分为`用户设置`、`工作区设置`、`项目文件夹设置`。  
`一般可通过菜单上的设置来调整`。 

`用户设置：`配置文件存放在用户目录下。比如windows系统是存放在用户目录下的AppData\Roaming\Code\User\settings.json  
```json
{
    // "http.proxy": "http://127.0.0.1:1080", // 设置代理
    // "http.proxyStrictSSL": false, // 验证证书
    // "editor.formatOnSave": true, // 保存时自动格式化

    "update.mode": "none", // 取消自动更新VSCode
    "extensions.autoUpdate": false, // 取消自动更新扩展
    "extensions.autoCheckUpdates": false, // 取消扩展更新检查
    "workbench.startupEditor": "none", // 编辑器启动后默认显示
    "editor.renderWhitespace": "all", // 显示隐藏的tab和空格
    "breadcrumbs.enabled": false, // 禁用导航路径
    "diffEditor.ignoreTrimWhitespace": false, // 显示首尾的空白差异
    // 配置排除的文件和文件夹
    "files.exclude": {
        // "**/.git": false, // 临时关闭排除
        "**/.idea": true, // 排除JetBrains系列软件配置文件
    },
}
```

`工作区设置：`你的工作区配置文件(后缀为.code-workspace文件)的settings项里。
```json
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

```json
    // Command Prompt
    "terminal.integrated.shell.windows": "C:\\WINDOWS\\System32\\cmd.exe",
    // PowerShell
    // "terminal.integrated.shell.windows": "C:\\Windows\\System32\\WindowsPowerShell\\v1.0\\powershell.exe",
    // Git Bash
    // "terminal.integrated.shell.windows": "D:\\Program Files\\Git\\bin\\bash.exe",
```

### 自定义格式化(各语言分别设置)

```json
"[javascript]": {
  "editor.defaultFormatter": "vscode.typescript-language-features",
},
"[typescript]": {
  "editor.defaultFormatter": "vscode.typescript-language-features"
},
"[html]": {
  "editor.defaultFormatter": "vscode.html-language-features"
},
"[json]": {
  "editor.defaultFormatter": "vscode.json-language-features"
},
"[yaml]": {
  "editor.defaultFormatter": "esbenp.prettier-vscode"
},
"[toml]": {
  "editor.formatOnSave": true
},
"[rust]": {
  "editor.formatOnSave": true
},
```

### go语言设置

```json
"go.useLanguageServer": true, // Go语言启用LanguageServer
"go.formatTool": "goimports", // 格式化工具
```

### python语言设置

```json
"python.pythonPath": "D:\\Python\\venv\\Scripts\\python.exe", // 加载虚拟环境(填写虚拟环境python二进制文件绝对路径)
"python.terminal.activateEnvInCurrentTerminal": true,
"python.autoComplete.addBrackets": true, // 自动补全函数括号
"python.formatting.provider": "yapf", // 需要安装pip3 install yapf(可能需要sudo)
```
