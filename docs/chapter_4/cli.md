```javascript
import { parse } from 'https://deno.land/std@/flags/mod.ts';
const { args } = Deno;
const parsedArgs = parse(args);

console.log('parsedArgs', parsedArgs);

function displayHelpMsg(): string {
	return `
   -> crypto-cli v1.0
   run the cli command with the following flags:
   -h, --help: display help message
   -log, --coin: get data for currency with id
   -a, --coins: get data for all currencies within limit
   -l, --limit: maximum results per request
   -i, --id: crypto-currency id
   `;
}

function log() {
	console.log('执行了log命令');
}

if (import.meta.main) {
	(async function () {
		switch (Object.keys(parsedArgs)[1]) {
			case 'help':
			case 'h':
				console.log(displayHelpMsg());
				break;
			case 'log':
				log();
				break;
			default:
				console.log(displayHelpMsg());
		}
	})();
}
```
