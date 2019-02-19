## 安装

### 方式一
[官方的安装方式](https://github.com/denoland/deno_install)

### 方式二（如果方式以因为网络原因无法下载，走这部）

#### Linux/MacOS

截至目前最新的v0.2.11版本安装

第一步：用脚本下载包
```
curl -L http://cnd.yintage.com/install.py | python
```

第二步：配置环境变量，把上一步运行后输出的文字复制到终端运行，例如
```
    echo export PATH="/Users/xxx/.deno/bin":\$PATH >> $HOME/.bash_profile
```

备注：目前如果要使用其他版本把本工程中的，[install.py](./install.py) 的代码进行修改，放到服务器上，curl -L xxx（你存放的路径） | python

#### Windows
##### powerShell安装

```
iwr https://deno.land/x/install/install.ps1 | iex
```

安装可能因为ssl的原因导致失败，如果失败运行下面的命令

```
```
