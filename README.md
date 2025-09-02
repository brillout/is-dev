Leverage export conditions to know whether the environment is development or production(/staging/...).

```js
import { isDev } from 'is-dev'
// returns true in development
// returns false in production(/staging/...)
console.log(isDev)
```

How it works is dead simple:

```json5
// node_modules/is-dev/package.json
"exports": {
  "development": "./export-true.js",
  "default": "./export-false.js"
}
```

Currently works in:  
✅ Vite  
❌ Node.js  

> Once Vite uses Rolldown (i.e. full-bundle mode), this package will work for Vite-based app.
