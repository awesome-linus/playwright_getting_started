# Playwright Getting Started
https://playwright.dev/docs/intro/

## Initial
```
mkdir playwright_getting_started
cd playwright_getting_started
yarn init -y
```

.gitignore
```
node_modules
```

## Installation
```bash
$ npm i -D playwright
```


## First script

index.js
```js
const { webkit } = require('playwright');

(async () => {
  const browser = await webkit.launch();
  const page = await browser.newPage();
  await page.goto('http://whatsmyuseragent.org/');
  await page.screenshot({ path: `example.png` });
  await browser.close();
})();
```


## Run
Output: example.png
```
node index.js
```
