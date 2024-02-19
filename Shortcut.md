# 常用快捷键

注：一些不常用命令可使用命令面板(快捷键`Ctrl + Shift + P`)进行搜索调用  

`Ctrl + P`文件的快速跳转

`空选定并Ctrl + X`剪切行

`空选定并Ctrl + C`复制行

`Ctrl + I`选择当前行

`Ctrl + Shift + K`删除一行

`Alt + ↑/↓`上下移动一行

`Shift + Alt + ↑/↓`复制一行

`Ctrl + Enter`在下面插入行

`Ctrl + Shift + Enter`在上面插入行

`Home`跳转到行首

`End`跳转到行尾

`Ctrl + Home`跳转到页首

`Ctrl + End`跳转到页尾

`Shift + Alt + A`切换块注释

`Ctrl + /`切换行注释

`Ctrl + B`显示/隐藏侧栏

`Ctrl + J`显示/隐藏面板

`Ctrl + G`定位特定的一行

`Ctrl + K + 0(是数字)`折叠所有(所在文件) `Ctrl + K + J`展开所有(所在文件)

`Ctrl + Shift + [`折叠(光标所处) `Ctrl + Shift + ]`展开(光标所处)

`Ctrl + F`查找

`Ctrl + H`替换

`Ctrl + D`匹配当前选中的词汇或者行

`Alt + 单击`插入光标(支持多点编辑)

`Alt + Shift`竖列选择(支持多点编辑)

`Ctrl + Alt + ↑/↓`多游标选择

`Shift + Alt + I`在选定的每一行的末尾插入光标

`Shift + Alt + F`格式化代码

`双击词汇`选中该词汇

`Ctrl + 点击方法名`或`选定方法名任何一处并F12`跳转到方法定义处

`Alt + ←/→`后退/前进

`` Ctrl + ` ``调出终端(命令行工具)

`` Ctrl + Shift + ` ``新终端(命令行工具)

### 自定义快捷键

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

`Ctrl+Shift+L`转换为小写

`Ctrl+Shift+U`转换为大写
