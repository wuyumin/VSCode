# 常用配置

配置一般分为`用户设置`、`工作区设置`、`项目文件夹设置`。  
`一般可通过菜单上的设置来调整`。  
`用户设置：`配置文件存放在用户目录下。比如windows系统是存放在用户目录下的AppData\Roaming\Code\User\settings.json  
`工作区设置：`你的工作区配置文件(后缀为.code-workspace文件)的settings项里。
```json
{
	"folders": [
		{
			"path": "D:\\Projects\\PythonTest"
		}
	],
	"settings": {
		"python.pythonPath": "D:\\Projects\\venv\\Scripts\\python.exe",
		"terminal.integrated.shellArgs.windows": ["/k", "D:\\Projects\\venv\\Scripts\\activate.bat"]
	}
}
```
`项目文件夹设置：`项目文件夹里.vscode文件夹下的settings.json文件。

### win10系统终端 PowerShell 修改为 cmd

```json
"terminal.integrated.shell.windows": "C:\\WINDOWS\\System32\\cmd.exe"
```

### Python 实现终端自动加载 Virtualenv 虚拟环境

```json
"settings": {
		"python.pythonPath": "D:\\Projects\\venv\\Scripts\\python.exe",
		"terminal.integrated.shellArgs.windows": ["/k", "D:\\Projects\\venv\\Scripts\\activate.bat"]
}
```
`python.pythonPath`填写 Virtualenv 虚拟环境 python 二进制文件绝对路径  
Windows系统：`terminal.integrated.shellArgs.windows`填写 Virtualenv 虚拟环境启动文件绝对路径  
Mac系统：`terminal.integrated.shellArgs.osx": ["-c", "source /data/Projects/venv/Scripts/activate"]`  
Linux系统：`terminal.integrated.shellArgs.linux": ["-c", "source /data/Projects/venv/Scripts/activate"]`  
