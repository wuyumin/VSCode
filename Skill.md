# VSCode 技巧

### 如何使用有私钥密码的ssh协议的git？

1. 打开命令行工具
2. 运行SSH代理
  - windows系统：`start-ssh-agent`并输入私钥密码
  - 类Unix系统：`ssh-agent $SHELL` 和 `ssh-add 私钥路径` (路径默认值是~/.ssh/id_rsa)，输入私钥密码(可能暂不能关掉命令行工具才起效，等git操作一次后就可以关掉命令行了)
3. 运行命令`code`来启动VSCode

另外的思路：先启动VSCode，然后在VSCode命令行中运行SSH代理，接着其它操作。

### 工作区的灵活使用

你一般只能在VSCode打开一个项目，如果要打开多个项目就要启动多个VSCode，其实你可以`将多个项目集中到工作区里`方便统一进行管理。
