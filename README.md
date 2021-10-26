﻿# netlify-functions-api-docs

🚀 Create the documentation of your Netlify functions automatically.

⭐ if you like the project :)

## Quick start

```
yarn add netlify-functions-api-docs
npm install netlify-functions-api-docs
```

### Personalize your docs site

Edit the file `doc_config.js` with the basic information of your site or organization.

```javascript
const netlifydoc = require('netlify-functions-api-docs/index');

const config = {
    basedir: "functions",
    info: {
        sitename: "MY SITE / ORGANIZATION",
        logourl: "MY LOGO URL",
        sitedescription: "MY SITE DESCRIPTION"
    }
}

netlifydoc.createDoc(config);
```

### In the project

Create an `index.doc.json` file inside each function folder.

```
project
│   node_modules
│   functions
|   └───function1
|   │   │   index.js
|   │   │   index.doc.json <-
|   ...
│   package.json
│   doc_config.js    
```

Each file must have the following structure:

```
{
    "name": "ENDPOINT NAME",
    "path": "/endpoint-url",
    "method": "GET",
    "description": "SOME DESCRIPTION"
}
```

### Generate documentation

To generate the documentation we simply execute `yarn run createdoc` or `npm run createdoc`.

