## Deno介绍

### Node存在的问题
- 1、语法老旧，使用callback回调未使用promise API
- 2、应用安全性，例如网络访问、文件读写
- 3、GYP，开发者需要自己写Node与V8之间的绑定逻辑，然而V8可能有些功能已经不再使用。
- 4、NPM模块系统，导致package.json过于关注工程而不是技术代码
- 5、node_modules太重并且增加了算法复杂度
- 6、require语法与browser不同
- 7、没有window对象，影响重构

### Node与Deno的区别
| 特点 |  Node   | Deno  |
| ---- |  ----  | ----  |
| 原生支持的语言 | JavaScript  | Typescript/JavaScript  |
| 模块 | 本地npm模块  | 远端资源 |
| 模块化方式| CommonJS | Typescript标准 | 
| 安全性| 具有很高权限 | 网络权限、写权限需要用户允许 | 
| 与browser的差异| 差异较大 | browser标准，高度相似 |
| 原生能力| 比较丰富，HTTP服务、文件系统都有 | 比较基础，例如HTTP服务、文件系统能力依靠官方库|

### 感悟
- 支持浏览器标准将大大提高同构的便捷性，前端代码或可以直接在deno中运行。