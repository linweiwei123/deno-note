### 体验Deno

```javascript
import { serve } from "https://deno.land/std@v0.30.0/http/server.ts";
const s = serve({ port: 8000 });
console.log("http://localhost:8000/");
for await (const req of s) {
  req.respond({ body: "Hello World\n" });
}
```

创建server.ts文件，输入以上内存。运行deno server.ts。将启动一个最简的服务器。