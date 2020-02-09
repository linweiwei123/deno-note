## Window API
Deno实现了browser的标准，类似browser，Deno环境中只有一个全局对象Window。
可以在Deno环境中可以通过输入console.log(this)或者直接输入window查看window对象中的API

总计18个api，整理后如下：

```
console,
Deno,
queueMicrotask,
atob,
btoa,
clearInterval,
clearTimeout,
fetch,
setInterval,
setTimeout,
performance,
addEventListener,
dispatchEvent,
removeEventListener,
window,
crypto,
onload,
onunload
```
18个方法与window中的相同，详情参考https://developer.mozilla.org/en-US/docs/Web/API/Window