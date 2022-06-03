# Webflow CMS API Client

## Requirements

- Node.js 12+
- NPM
- Webpack / Browserify (optional)

## Installation

Install the package via NPM

```shell
$ npm i webflow-api-node

```

## Usage

```javascript
const Webflow = require('webflow-api')

// Initialize the API
const api = new Webflow({ token: 'api-token' })

// Fetch a site
api
  .site({ siteId: '580e63e98c9a982ac9b8b741' })
  .then((site) => console.log(site))
```

The `Webflow` constructor takes several options to initialize the API client:

- `token` - the API token **(required)**
- `version` - the version of the API you wish to use (optional)

API Documention and other information:

- [API documentation](https://developers.webflow.com)
- [Generating API Access Token](https://university.webflow.com/lesson/intro-to-the-webflow-api)

## Contributing

Contributions are welcome - feel free to open an issue or pull request.

## License

The MIT license - see `LICENSE`.
