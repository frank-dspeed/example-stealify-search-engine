# example-stealify-search-engine
A Example that shows how to build a Meta Search Engine like serax for Privacy using @stealify/os-desktop npm package


## Usage
will open a new window with the search result 
```
npx @stealify/example-search-engine "your search"
```


your_code.js
```
require('@stealify/example-search-engine')('your search'); // opens again a new window
```


your_express_app
```
const app = require('express')()
app.use((req)=> {
  req.res.end(require('@stealify/example-search-engine')('your search', { headless: true })) // returns the result as html string
})
app.listen(8080)
```
