# example-stealify-search-engine
A Example that shows how to build a Meta Search Engine like serax for Privacy using @stealify/os-desktop npm package


## Usage
with npx
```
// Opens a New Window with the result
npx @stealify/example-search-engine "your search"
// Returns the result as HTML File (string)
npx @stealify/example-search-engine --headless "your search"
```


or programatical

your_code.js that opens a window
```js
require('@stealify/example-search-engine')('your search'); // opens again a new window
```

your_express_app that serves the result
```js
const app = require('express')()
app.use((req)=> {
  req.res.end(require('@stealify/example-search-engine')('your search', { headless: true })) // returns the result as html string
})
app.listen(8080)
```
