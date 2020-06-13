## 安装

### 官方安装方式
[官方的安装方式](https://github.com/denoland/deno_install)

### Linux/MacOS

截至目前最新的v0.32.00版本安装

- 安装最新版本
```
curl -fsSL https://deno.land/x/install/install.sh
```

- 安装制定版本 (例如安装v1.1.0)
```
curl -fsSL https://deno.land/x/install/install.sh | sh -s v1.1.0
```

- 环境变量设置
需要在当前环境变量文件.bash_profile最后加入

```
## 注意: $HOME 是当前系统用户目录
export PATH=$HOME/.local/bin/:$PATH
```

- 验证
在命令窗口中执行 deno --version，就会出现Deno 的版本已经依赖 V8 的版本

```
deno 1.1.0
v8 8.4.300
typescript 3.9.2
```

## 卸载（macOS）
终端输入
```
which deno
```
得到安装所在路径
```
/Users/xxx/.deno/bin/deno

// 通过rm 命令删除
rm /Users/xxx/.deno/bin/deno
```

进入根目录
```
cd ~
```

移除deno
```
rm /Users/xxx/.deno/bin/deno
```