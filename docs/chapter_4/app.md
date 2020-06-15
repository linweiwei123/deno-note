## app.ts

```javascript
import { Application, Router } from 'https://linweiwei123.github.io/aok/mod.ts';
import { init } from './router.ts';
const env = Deno.env.toObject();
const PORT = env.PORT || 4000;
const HOST = env.HOST || '127.0.0.1';

const router = new Router();
init(router);

const app = new Application();

app.use(router.routes());
app.use(router.allowedMethods());

console.log(`Listening on port ${PORT}...`);

await app.listen(`${HOST}:${PORT}`);
```

## router.ts

```javascript
import { Router } from 'https://linweiwei123.github.io/aok/mod.ts';
import data from './dogs.ts';

export function init(router: Router) {
	router.get('/dogs', getDogs);
}

export const getDogs = ({ response }: { response: any }) => {
	response.body = data.dogs;
};
```

## dog.ts

```javascript
interface Dog {
    name: string
    age: number
  }

let dogs: Array<Dog> = [
{
    name: 'Roger',
    age: 8,
},
{
    name: 'Syd',
    age: 7,
},
]


export default {
    dogs
}
```
